---
title: Train the clustering solution for standard change proposal
description: Train the Standard change proposal solution definition to use clustering capabilities to identify and suggest Standard Change templates to create a change.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence for Change Management, Configure, Change Management, IT Service Management]
---

# Train the clustering solution for standard change proposal

Train the Standard change proposal solution definition to use clustering capabilities to identify and suggest Standard Change templates to create a change.

## Before you begin

Ensure that Change Management - Standard Change Template Intelligence \(com.snc.change\_management.ml.sctp\) plugin is activated.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Intelligent Solution Configuration** &gt; **Standard Change Proposal**.

2.  Customize the default solution definition to train the solution.

    By default, the **Std Change Template Candidates** is the solution definition provided. To generate records in the **std\_change\_template\_candidate** list, execute the scheduled job Update Standard Change Cluster Candidates. You can also configure the scheduled job to run at specific periods by selecting the required option in the Run field in the **Scheduled Script Execution** page. You can then create standard change templates from the clusters generated.

    For more information on creating and training the solutions, see Create and train a clustering solution.

3.  Click **Update**.


**Parent Topic:**[Predictive Intelligence for Change Management](../concept/change-mgmt-intelligent-solutions.md)

