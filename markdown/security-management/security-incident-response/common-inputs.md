---
title: Example 2: Common Inputs: Sighting Search
description: The example below demonstrates the common inputs capability action.Add common run time inputs that apply for all the selected implementations as applicable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/common-inputs.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Examples, Unified experience framework, SIR Workspace Orchestration, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Example 2: Common Inputs: Sighting Search

The example below demonstrates the common inputs capability action.

You can perform **Run Sighting Search** related integration capabilities action using the **Investigation** tab from the SIR Workspace.

1.  On the **Investigation** tab, navigate to the **Entry Points Lists** section displayed on the left side of the page.
2.  Select the respective entry point and run the integration capability action.

    **Note:** You can also navigate to the **Related Records** tab on the workspace to perform the integrations capabilities action.


**Parent Topic:**[Unified Experience examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/unified-expereince-example.md)

**Related topics**  


[Example 1: Select implementations: Threat Lookup]()

[Example 3: Add specific runtime details inputs to an implementation: Run Additional Actions]()

## Add common inputs to an implementation

Add common run time inputs that apply for all the selected implementations as applicable.

### Before you begin

Role required: sn\_si.analyst

The available implementations are listed. Select the implementation\(s\), after you select them only the supported records will be submitted against each selected implementation\(s\).

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open any security incident.

3.  Go to **Investigation** tab of the workspace.

    The investigation tab with the entry points lists is displayed.

    \[Omitted image "example1.png"\] Alt text: Investigation tab of workspace

4.  Select the associated observable from the entry point lists.

    For example, select **Associated Observables** related list. The corresponding observables records are displayed.

    **Note:** You can select an implementation to perform a sighting search for the selected observables, or by selecting multiple implementations.

    \[Omitted image "example1-run-threat-lookup.png"\] Alt text: Run Threat Lookup

5.  Select any observable check box that you wish to perform the threat lookup.

6.  Select **Run Sighting Search** to perform email search.

    The Run Sighting Search Implementations modal dialogue box is displayed.

    \[Omitted image "example2-run-sighting-search.png"\] Alt text: An example that shows on how to add common runtime inputs by selecting Sightings Search capability

7.  Select one or more implementations from the list.

8.  Click **Next**.

    After the selected records are submitted, a message is displayed that the Sighting search is being requested. Once the implementation is processed in the backend, the results are displayed in the **Sighting Search** related list section. Also, the respective implementation activity is displayed in the Activity section. Two activities are displayed, one is when the implementation execution is started and the second one is when the execution is completed.

9.  Select the common run time input value.

10. Click **Submit**.

    \[Omitted image "sighting-search-request.png"\] Alt text: Sighting search execution is under process

    After the selected records are submitted, a message is displayed that the Sighting search is being requested. Once the implementation is processed in the backend, the results are displayed in the **Sightings Search Results** related list section. Also, the respective implementation activity processing status is displayed in the **Activity** section.


