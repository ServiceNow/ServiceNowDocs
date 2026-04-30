---
title: Import Update set from XML and install fix script
description: Import update set from XML to provide cross-scope access to HR Service Delivery applications and run fix script to display field decorator in the ticket.Run the fix\_script\_start\_chat\_field\_decorator\_HR in the ServiceNow instance to display Start Microsoft Teams chat field decorator in the ticket to initiate a chat with the requester.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install HR Service Delivery, Plan your installation, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Import Update set from XML and install fix script

Import update set from XML to provide cross-scope access to HR Service Delivery applications and run fix script to display field decorator in the ticket.

## Before you begin

Role required: admin

## About this task

Following table depicts the RCA record mapping to its feature.

|RCA Record|Plugin|Plugin Name|
|----------|------|-----------|
|content\_automation\_rca\_records.xml|\{Content Automation\}|\[com.sn\_content\_automation\]|
|document\_templates\_rca\_records.xml|\{Document Templates\}|\[com.snc.document\_templates\]|
|human\_resources\_core\_rca\_records.xml|\{Human Resources Scoped App: Core\}|\[com.sn\_hr\_core\]|
|human\_resources\_integrations\_rca\_records.xml|\{Human Resources Scoped App: Integrations\}|\[com.sn\_hr\_integrations\]|
|human\_resources\_lifecycle\_events\_rca\_records.xml|\{Human Resources Scoped App: Lifecycle Events\}|\[com.sn\_hr\_lifecycle\_events\]|
|human\_resources\_service\_portal\_rca\_records.xml|\{ Employee Center \}|\[com.sn\_hr\_service\_portal\]|
|human\_resources\_workspace\_rca.xml|\{Human Resources Scoped App: Workspace\}|\[com.sn\_hr\_agent\_workspace\]|

For more information about the Update sets, see [Update set transfers](https://www.servicenow.com/docs/access?context=update-set-transfers&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Procedure

1.  Download the update sets from the app store for [HR Service Delivery integration with Microsoft Teams](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2).

    If you can't find the XML files, click **Show more** to view the list of supporting links and docs.

2.  Click each of the XML files to download on to your computer.

    -   human\_resources\_integrations\_rca\_records
    -   human\_resources\_service\_portal\_rca\_records
    -   human\_resources\_lifecycle\_events\_rca\_records
    -   human\_resources\_core\_rca\_records
    -   content\_automation\_rca\_records
    -   document\_templates\_rca\_records.xml
    -   fix\_script\_start\_chat\_field\_decorator\_HR
    -   human\_resources\_workspace\_rca.xml
3.  Navigate to upload XML files.

    -   Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets** for the RCA script XML uploads.
    -   Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets** for the fix script XML upload.
4.  Right-click on the **Name** column header and select **Import XML** menu.

5.  Select **Browse** on the Import XML form and select the update set XML file.

6.  Select **Upload**.

7.  Select the XML file by its name on the Retrieved Update Sets form for RCA script type and Local Update Sets form for fix script type.

8.  Select **Preview Update Set**.

9.  Select **Commit Update Set**.

    The XML scripts will be in Committed state.


## Result

The RCA and fix script XMLs are uploaded.

**Parent Topic:**[Install HR Service Delivery integration with Microsoft Teams application](install-hr-ms-teams-plugin.md)

## Install Fix Script for HR Service Delivery integration with Microsoft Teams

Run the **fix\_script\_start\_chat\_field\_decorator\_HR** in the ServiceNow instance to display **Start Microsoft Teams chat** field decorator in the ticket to initiate a chat with the requester.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System Definition** &gt; **Fix Scripts**.

2.  Enter `Add Teams chat Field Decorator` in the **Name** column search.

3.  Select **Add Teams chat Field Decorator** fix script.

4.  Select **Active** check box.

5.  Select **Run Fix Script**.

    The ![Microsoft Teams decorator](../images/teams-decorator.png) icon is displayed as a field decorator in a record.


