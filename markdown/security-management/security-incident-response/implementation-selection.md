---
title: Select implementations
description: Select one or more implementations as applicable.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Example 1: Run Threat Lookup, Unified Experience example, Unified experience framework for integrations powered by Capability Framework, SIR Workspace Orchestration, Working with Security Incident Records, Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Select implementations

Select one or more implementations as applicable.

## Before you begin

Role required: sn\_si.analyst

The available implementations are listed. Select the implementation\(s\), after you select them only the supported records will be submitted against each selected implementation\(s\).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any security incident.

3.  Go to **Investigation** tab of the workspace.

    The investigation tab with the entry points lists is displayed.

    ![Investigation tab of the workspace](../image/example1.png)

4.  Select the associated observable from the entry point lists.

    For example, select **Associated Observables** related list. The corresponding observables records are displayed.

    **Note:** You can select an implementation to perform a lookup on the selected observables, or you can perform the lookup by selecting all implementations.

    ![Run Threat Lookup](../image/example1-run-threat-lookup.png "Run Threat Lookup")

5.  Select any observable check box that you wish to perform the threat lookup.

6.  Navigate to the related lists actions drop down that is displayed on top of the related lists page.

7.  Select **Run Threat Lookup** to perform threat intel related integration capabilities action.

    **Note:** The Run Threat Lookups capability performs threat intelligence lookups to determine whether one or more observables are associated with any known security threats.

    The **Run Threat Lookup Implementations** modal screen is displayed.

    ![Run Threat Lookup Implementations](../image/example1-run-threat-lookup-select.png "Run Threat Lookup Implementations")

8.  Select one or more implementations from the list.

9.  Click **Submit**.

    After the selected records are submitted, a message is displayed that the lookup is being executed. Once the implementation is processed in the backend, the results are displayed in the **Threat Lookup Results** related list section. Also, the respective implementation activity is displayed in the **Activity** section. Two activities are displayed, one is when the implementation execution is started and the second one is when the execution is completed.

    ![User Reported Phishing view: Associated Observables section.](../image/example1-execution.png)

    **Note:** The **Threat intel** related lists such as the associated observables related lists are displayed in the **Threat Lookup Results** section, and the **Sightings Search** related lists are displayed in the **Sightings Search Results** section under the Related Records.


**Parent Topic:**[Example 1: Select implementations: Threat Lookup](example-1-select-implementations-threat-lookup.md)

