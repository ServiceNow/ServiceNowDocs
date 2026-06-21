---
title: Configure the Public Sector landing page with UI Builder
description: Use the UI Builder to change certain fields in the Public Sector landing page of the CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/government-industry/public-sector-digital-services/public-sector-configure-landing-page.html
release: xanadu
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up the CSM Configurable Workspace for Public Sector Digital Services, Optional configuration steps for Public Sector Digital Services Core, Public Sector Digital Services Core, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure the Public Sector landing page with UI Builder

Use the UI Builder to change certain fields in the Public Sector landing page of the CSM Configurable Workspace.

## Before you begin

Role required: admin

## About this task

The CSM Landing Page gives agents an overview of their new, assigned, and high-priority cases, plus the cases assigned to their groups. Replace certain fields in the landing page with fields relevant to public sector. You can also add or change other fields as needed. For more information on using UI Builder to modify pages, see Work with pages.

## Procedure

1.  Navigate to **All** and in the filter, enter and select **UI Builder**.

2.  Navigate to the CSM Landing Page:

    1.  In the list of **My experiences**, select the **CSM/FSM Configurable Workspace**.

    2.  In **UI Builder**, navigate to **Page** &gt; **Landing Page** and select **CSM Landing Page**.

        \[Omitted image "ps-csm-landing-page.png"\] Alt text: View of CSM landing page with fully customizable content.

    3.  In the message displayed at the top of the page, select **Edit in original scope**.

        \[Omitted image "ps-edit-original-scope-msg.png"\] Alt text: Top view of CSM landing page containing a button to edit in original scope.

3.  In the CSM Landing Page, select the **My active cases** component and in the **Config** tab of the Configuration pane, delete the **account** field from the **Columns**.

    \[Omitted image "ps-csm-landing-page-active-cases.png"\] Alt text: Admin view of the configuration pane showing the account field being removed from the columns of the landing page.

4.  Add the **Constituent** field:

    1.  In the Configuration pane, select **+Add** in the **Columns** list to open the field chooser.

        \[Omitted image "ps-constituent-field.png"\] Alt text: Admin view of the configuration pane, where you can customize the fields, columns, and sections displayed.

    2.  In the Choose a field list, select **Consumer** &gt; **Constituent** and then select **OK**.

        \[Omitted image "ps-field-list.png"\] Alt text: Admin view of the field list, displaying a list of all fields that can be added or removed from the CSM landing page.

    3.  In the Configuration pane, rearrange the columns by moving **consumer.constituent** below **short.description**.

        \[Omitted image "ps-configuration-pane-rearrange.png"\] Alt text: Admin view of the configuration pane that shows columns being rearranged.

5.  Repeat Steps 3 and 4 to change the **My Team’s cases** component.

6.  Make other page changes as needed.

7.  Select **Save** in the top right corner to save the landing page changes.


**Parent Topic:**[Set up the CSM Configurable Workspace for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/government-industry/public-sector-digital-services/setting-up-csm-fsm.md)

