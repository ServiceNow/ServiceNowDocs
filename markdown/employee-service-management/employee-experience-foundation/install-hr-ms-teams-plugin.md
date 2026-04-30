---
title: Install HR Service Delivery integration with Microsoft Teams application
description: Install the HR Service Delivery integration with Microsoft Teams application to integrate with ServiceNow instance for the collaboration between the agents and employees.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Plan your installation, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Install HR Service Delivery integration with Microsoft Teams application

Install the HR Service Delivery integration with Microsoft Teams application to integrate with ServiceNow instance for the collaboration between the agents and employees.

## Before you begin

Role required: admin

**Note:** If you install HR Service Delivery integration with Microsoft Teams app, you don’t need to download Conversational Integration with Microsoft Teams separately.

## Procedure

1.  Navigate to **System Application** &gt; **All Available Applications** &gt; **All**.

2.  In the search field, enter `HR Service Delivery for Microsoft 365`.

    You can search for the application by its name or ID. If you cannot find an application, visit the ServiceNow app store to view [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2). For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

    **Note:** All the dependent plug-ins are automatically installed in this process.


## What to do next

You must also install the following update sets from the app store for [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2):

-   human\_resources\_integrations\_rca\_records
-   human\_resources\_service\_portal\_rca\_records
-   human\_resources\_lifecycle\_events\_rca\_records
-   human\_resources\_core\_rca\_records
-   content\_automation\_rca\_records
-   document\_templates\_rca\_records.xml
-   fix\_script\_start\_chat\_field\_decorator\_HR

All the Restricted Caller Access\(RCA\) privileges are displayed in **Application Restricted Caller Access Privileges** list.

Download and execute the **fix\_script\_start\_chat\_field\_decorator\_HR** to display the field decorator in the ticket to initiate a chat with the requester.

-   **[Verify Application Restricted Caller Access \(RCA\) Privileges](verify-rca-privileges-hr.md)**  
Verify that there are no duplicate entries in the Restricted Caller Access \(RCA\) records before uploading an RCA data set to fix the configuration issues.
-   **[Import Update set from XML and install fix script](upload-rca-hr.md#)**  
Import update set from XML to provide cross-scope access to HR Service Delivery applications and run fix script to display field decorator in the ticket.

**Parent Topic:**[Plan your installation](../concept/plan-installation-ms-teams.md)

