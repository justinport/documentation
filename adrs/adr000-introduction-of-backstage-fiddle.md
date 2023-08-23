---
id: adrs-adr000
title: 'ADR000: Introduction of Backstage.io Fiddle'
description: Architecture Decision Record (ADR) for the introduction and setup of a new application - Backstage.io Fiddle for experimenting with features in the AWS training environment.
---

## Context

With the growth of our development community, there's an increasing need to provide a stable environment for our main instance of Backstage.io. Simultaneously, the demand for an isolated space for developers to experiment without affecting the primary environment is rising. The forces driving this decision include:

1. **Technological**: The need for separate environments to test and introduce new software features and modules without affecting the main instance.
2. **Social**: With the growth of our developer community, there's a heightened demand for an environment where they can innovate without restrictions.
3. **Project Local**: Understanding that experiments in the main environment can cause unintended disruptions, impacting other developers' work and potentially causing downtimes.

## Decision

We will introduce a new application named "Backstage.io Fiddle" in our AWS training environment. This application will:

1. Serve as a sandbox for experimentation where new features, plugins, and integrations can be trialed.
2. Be completely isolated from Backstage.io's main instance, guaranteeing zero interference with the primary production setup.
3. (If deemed necessary) Periodically sync data and configurations from the main environment, ensuring up-to-date and realistic testing scenarios.

## Consequences

1. **Positive**:
   - Developers can test and innovate freely without risking the main instance's stability.
   - Quicker innovation as developers can rapidly test and refine new ideas.
   - A decrease in potential conflicts and downtimes in the primary environment due to inadvertent breakages from experimental changes.
   - Will serve as a means to learn the platform and minimize dependencies.
   
2. **Negative**:
   - There may be some initial overhead in terms of setting up, maintaining, and possibly syncing the "Fiddle" environment.
   - If not clearly communicated, there's potential for confusion among developers about the new environment's purpose and utilization.

3. **Neutral**:
   - With this separate environment in place, developers will need to ensure that successful experiments get integrated back into the main environment, adding an additional step to the deployment process.

In introducing Backstage.io Fiddle, our objective is to encourage innovation while assuring that our main instance remains consistent and dependable for the entire development community.