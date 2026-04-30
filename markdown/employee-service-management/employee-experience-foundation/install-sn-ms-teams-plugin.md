---
title: Install IT Service Management integration with Microsoft Teams application
description: Install the IT Service Management integration with Microsoft Teams application for the collaboration between the agents and employees.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Plan your installation, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Install IT Service Management integration with Microsoft Teams application

Install the IT Service Management integration with Microsoft Teams application for the collaboration between the agents and employees.

## Before you begin

Role required: admin

**Note:** If you install IT Service Management integration with Microsoft Teams app, you don’t need to download Conversational Integration with Microsoft Teams separately.

## Procedure

1.  Navigate to **System Application** &gt; **All Available Applications** &gt; **All**.

2.  In the search field, enter `IT Service Management for Microsoft 365`.

    You can search for the application by its name or ID. If you cannot find an application, visit the ServiceNow app store to view [IT Service Management for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/14eb9da8c3f310102986a81c8640dd08). For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install** button.

    **Note:** All the dependent plug-ins are automatically installed in this process.

    You must also install the **fix\_script\_start\_chat\_field\_decorator\_IT** update set to have a field decorator in a ticket to initiate a chat with the requester.

4.  Download the **fix\_script\_start\_chat\_field\_decorator\_IT** update set from the app store.

    If you can't find the fix script, click **Show more** to view the list of supporting links and docs.

    Click **fix\_script\_start\_chat\_field\_decorator\_IT** to download the XML file.

    ![Fix Script XML file from IT Service Management for Microsoft 365 store](../images/fix-script-itsm-new.png)

5.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets** &gt; **Related Links** &gt; **Import Update Set from XML**.

    ![Import update set from XML](../images/import-xml01.png)

6.  In the XML file field, click **Choose file** button and select **fix\_script\_start\_chat\_field\_decorator\_IT** XML file and upload the XML file.

7.  Click **Fix script to add start Microsoft Teams chat field decorator**.

8.  Click **Preview Update Set**.

    ![Preview Update Set](../images/preview-update-set.png)

9.  Click **Commit Update Set**.

    ![Commit update set](../images/commit-update-set.png)

    The Fix script to add start Microsoft Teams chat field decorator will be in Committed state.

    ![Committed state](../images/committed-state.png)

10. Navigate to **System Definition** &gt; **Fix Scripts**.

11. In the **Name** search field, enter `Add Teams chat Field Decorator`.

12. Click **Add Teams chat Field Decorator** fix script.

13. Click **Run Fix Script** button.

    The ![Microsoft Teams](../images/teams-decorator.png) icon is displayed as a field decorator in a record.


**Parent Topic:**[Plan your installation](../concept/plan-installation-ms-teams.md)

