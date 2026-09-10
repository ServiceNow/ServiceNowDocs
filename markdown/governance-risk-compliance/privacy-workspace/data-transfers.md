---
title: Manage data transfers
description: Organizations often transfer personal data between applications, vendors, business units, and regions, which might be subject to privacy regulations. The Privacy Management application captures each movement of personal data as a data transfer record on the processing activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/data-transfers.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 4
keywords: [data transfer, hierarchy, transfer mechanism, custom relationship]
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Manage data transfers

Organizations often transfer personal data between applications, vendors, business units, and regions, which might be subject to privacy regulations. The Privacy Management application captures each movement of personal data as a data transfer record on the processing activity.

## Overview of data transfer

When personal data moves between nodes in a processing activity, including entities, business applications, business processes, companies, vendors, and locations, privacy teams must track where the data goes, whose data is involved, and which legal safeguards permit each movement. Data transfer records capture this information on the processing activity. Each record represents a specific movement of personal data from one node to another, across regions.

## How data transfer records are generated

Data transfer records are generated from hierarchy relationships on a processing activity. When you create a relationship that involves sending or receiving personal data from one node to another, the system generates a transfer record for that movement.

By default, only the following relationship types generate data transfer records:

-   **Send data to**
-   **Received data from**

For information on the different relationship types, see [New hierarchy relationship forms in Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/new-relationship-forms.md).

-   **Data transfer example**

    Consider a Recruitment processing activity that depends on an HR platform in Australia and a recruiting application in Germany. The recruiting application sends personal data to the HR platform. To capture this data flow, you define a relationship with the following details:

    -   Primary record: Recruitment processing activity
    -   Primary node: Recruiting application
    -   Primary node location: Germany
    -   Relationship type: Sends data to
    -   Related node: HR platform
    -   Related node location: Australia
    This relationship generates one data transfer record: Germany \(Recruiting application\) to Australia \(HR platform\).


The **Send data to** and **Received data from** relationship types have data subject selection enabled, which captures whose personal data is involved in the transfer, their locations, and the impacted data elements. When you add this information, the system generates additional data transfer records from each data subject location to each node involved in the movement.

**Note:** A privacy admin can enable data subject selection in custom relationship types by modifying the sn\_privacy.relationship\_involving\_data\_subjects system property. For steps, see [Configure data subject selection in hierarchy relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-ds-sys-property-hierarchy.md).

-   **Data transfer example with data subject selection**

    In the same example, consider that the recruiting application sends personal data of employees located in California to the HR platform. So, you add the following data subject information to the above relationship:

    -   Data subject type: Employees
    -   Data subject location: California
    This generates two additional transfer records for the same relationship, capturing employee personal data movement from California \(Employees\) to Germany \(Recruiting application\), and from California \(Employees\) to Australia \(HR platform\).


You can remove transfers that don't apply during the assessment review. For steps, see [Review a privacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/review-a-privacy-assessment.md).

## Adding data transfers to a processing activity

Data transfer records are added to a processing activity in one of the following ways:

-   A business user defines hierarchy relationships in a privacy impact assessment \(PIA\) and submits it. The system generates data transfer records for each movement of personal data between the nodes involved. When an analyst marks the assessment as complete, these records are mapped to the processing activity.
-   An analyst creates a **Sends data to** or **Received data from** hierarchy relationship directly on the **Processing data inventory** &gt; **Hierarchy** tab of the processing activity. Data transfer records are automatically generated in the **Regulatory details** &gt; **Data transfers** tab.
-   An analyst manually records data transfers on the **Regulatory details** &gt; **Data transfers** tab of the processing activity.

## Transfer mechanisms

An analyst reviews the data transfer records generated for a processing activity and assigns each one a transfer mechanism. A transfer mechanism identifies the legal safeguard that permits data transfers, such as Binding Corporate Rules \(BCRs\) or Standard Contractual Clauses \(SCCs\). To learn about different transfer mechanisms in Privacy Management, see [Transfer mechanisms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/transfer-mechanisms.md).

-   To add a transfer mechanism to a data transfer record, see [Add a transfer mechanism to a data transfer record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/add-transfer-mechanism-dt.md).
-   To add new transfer mechanisms in your Privacy Workspace, see [Manage transfer mechanisms in the Privacy Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/update-transfer-mechanism.md).

## Roles requirements

|User|Required role|Task|
|----|-------------|----|
|Business user|sn\_privacy.business\_user and sn\_privacy.assessment\_responder|Defines data flows through hierarchy relationships in a privacy assessment.|
|Privacy analyst|sn\_privacy.analyst|Reviews data transfers and adds corresponding transfer mechanisms.|
|Privacy manager|sn\_privacy.manager|Adds new transfer mechanisms in the application or updates existing ones.|
|Privacy admin|sn\_privacy.admin|Configures the sn\_privacy.relationship\_involving\_data\_subjects system property to support data subject selection in custom relationships.|

-   **[Create a data transfer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/create-a-data-transfer.md)**  
Record a data transfer directly on a processing activity if it wasn't captured as part of a hierarchy relationship.
-   **[Delete a data transfer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/delete-a-data-transfer.md)**  
Delete a data transfer record from a processing activity.
-   **[Transfer mechanisms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/transfer-mechanisms.md)**  
Transfer mechanisms identify the legal safeguard that permits a specific data transfer between locations.

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

