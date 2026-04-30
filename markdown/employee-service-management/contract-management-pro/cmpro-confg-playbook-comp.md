---
title: Configure the Playbook tab component for your workspace
description: Use the Tabs component in UI Builder to configure the Playbook tab on the contract repository record page for your workspace.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-26"
reading_time_minutes: 1
breadcrumb: [Configure the Playbook tab, Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
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

    ![Pages in the Legal Counsel Center experience on the UI Builder](../image/cmpro-uib-page.png "Page and variants for your workspace")

5.  Select the **Main Tab** component.

    ![Main tab component on the record page](../image/cmpro-main-tab-uib.png "Main tab component on the left pane")

6.  Select **Add** under the **Tabs** section.

7.  In the pop-up window, select **Start from an empty container**.

8.  Select **Next**.

9.  On the form, fill in the fields.

    1.  In the **Tab label** field, enter `Playbook`.

        The **Tab ID** field is automatically updated.

    2.  On **Hide tab**, hover over the field and select the option to bind the data broker configured for the playbook.

        For more information, see [Connect data to your components](https://www.servicenow.com/docs/access?context=connect-data&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

        ![Tab settings to connect the data broker to the tab component.](../image/cmpro-connect-data.png "Connect data broker to the tab component")

    3.  Select **Create**.

    The new tab appears under the **Main tab** component.

    ![New playbook tab under the Main Tab component](../image/cmpro-new-playbook-tab.png "Playbook tab")

10. Expand **Playbook** and then select **Add content**.

11. In the Add content window, select **Playbook Focused Vertical** and then select **Add**.

    ![Add content for the tab.](../image/cmpro-playbook-content.png "Add playbook content")

12. In the Data resources drawer under the Data and scripts section, select **Playbook Custom Layout**.

    ![Playbook custom layout under the Data resources drawer.](../image/cmpro-playbook-custom-layout.png "Playbook custom layout")

    The Playbook configuration modal appears.

13. In the **Configuration** tab, do the following:

    1.  In the **Parent SysID**, select the record sysid under `props`.

    2.  In the **Parent Table**, select the record table under `props`.

    3.  In the **Playbook Experience**, select `Contract Metadata Extraction Playbook`.

14. Select **Save** on the UI Builder header.


