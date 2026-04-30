---
title: DevOps value stream metrics in Digital Portfolio Management
description: View key metrics related to the performance of your solutions in Digital Portfolio Management \(DPM\). If you manage your solutions in a DevOps model, then you can view DevOps data for your business applications as well as link to the DevOps Change Workspace directly from DPM.
locale: en-US
release: zurich
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Digital Portfolio Management, IT Service Management]
---

# DevOps value stream metrics in Digital Portfolio Management

View key metrics related to the performance of your solutions in Digital Portfolio Management \(DPM\). If you manage your solutions in a DevOps model, then you can view DevOps data for your business applications as well as link to the DevOps Change Workspace directly from DPM.

Key metrics help you evaluate the impact on the performance of work being done on your solutions. View DevOps value stream metrics in the context of your business applications in DPM, for example, mean time to restore from changes, change failure rates, and lead time. You can also access the DevOps Change Workspace directly from your business applications in DPM to make data-driven decisions. Accelerate metrics are displayed on both the **Build** tab and the **Run** tab so that you can view the data in the context of your business applications for each phase. You can see flow metrics data on the **Build** tab of your business applications.

**Note:** To view DevOps accelerate metrics and flow metrics in DPM, admins must enable the DevOps system property. See [Configure the Digital Portfolio Management experience](../task/dpm-configure-experience.md) for more information.

On the **Build** tab of your business applications, view the following data in numeric forms and in charts:

-   Accelerate metrics
    -   Average lead time to deploy over the last 30 days
    -   Commit to deploy lead time
    -   Average deployment frequency over the last 30 days
    -   Production deployments frequency
-   Flow metrics
    -   Average flow time for epics
    -   Average flow time for epics and features
    -   Average number of bugs and stories
    -   Distribution of bugs and stories
    -   Work in progress cycle time for epics, stories, and bugs \(each has their own widget\)
    -   Work in progress items

On the **Run** tab of your business applications, view the following accelerate metrics data in numeric form and in charts:

-   Average mean time to restore from incident caused by changes \(over the last 30 days\)
-   Mean time to restore from incidents caused by changes, broken out by DevOps changes and non- DevOps changes

    **Note:** Non- DevOps changes are other changes listed on the Change table.

-   Average change failure rates over the last 30 days
-   Change failure rate over time, broken out by DevOps changes and non- DevOps changes
-   Mean time to restore

