---
title: Configure the Playbook tab component for your workspace
description: Use the Tabs component in UI Builder to configure the Playbook tab on the contract repository record page for your workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-confg-playbook-comp.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Playbook tab, Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure the Playbook tab component for your workspace

Use the Tabs component in UI Builder to configure the **Playbook** tab on the contract repository record page for your workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **Experiences** tab.

3.  Open your workspace.

4.  Select the page on your workspace where you want to configure the **Playbook** tab.

    \[Omitted image "cmpro-uib-page.png"\] Alt text: Pages in the Legal Counsel Center experience on the UI Builder

5.  Select the **Main Tab** component.

    \[Omitted image "cmpro-main-tab-uib.png"\] Alt text: Main tab component on the record page

6.  Select **Add** under the **Tabs** section.

7.  In the pop-up window, select **Start from an empty container**.

8.  Select **Next**.

9.  On the form, fill in the fields.

    1.  In the **Tab label** field, enter `Playbook`.

        The **Tab ID** field is automatically updated.

    2.  On **Hide tab**, hover over the field and select the option to bind the data broker configured for the playbook.

        For more information, see .

        \[Omitted image "cmpro-connect-data.png"\] Alt text: Tab settings to connect the data broker to the tab component.

    3.  Select **Create**.

    The new tab appears under the **Main tab** component.

    \[Omitted image "cmpro-new-playbook-tab.png"\] Alt text: New playbook tab under the Main Tab component

10. Expand **Playbook** and then select **Add content**.

11. In the Add content window, select **Playbook Focused Vertical** and then select **Add**.

    \[Omitted image "cmpro-playbook-content.png"\] Alt text: Add content for the tab.

12. In the Data resources drawer under the Data and scripts section, select **Playbook Custom Layout**.

    \[Omitted image "cmpro-playbook-custom-layout.png"\] Alt text: Playbook custom layout under the Data resources drawer.

    The Playbook configuration modal appears.

13. In the **Configuration** tab, do the following:

    1.  In the **Parent SysID**, select the record sysid under `props`.

    2.  In the **Parent Table**, select the record table under `props`.

    3.  In the **Playbook Experience**, select `Contract Metadata Extraction Playbook`.

14. Select **Save** on the UI Builder header.


**Parent Topic:**[Configuring the Playbook tab on contract repository records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-config-playbook-tab.md)

