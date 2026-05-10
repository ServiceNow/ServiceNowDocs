---
title: Personalized Answers on Employee Center
description: Get personalized Answers about your leave balance within the ServiceNow system or with an integrated third-party application.Set up a third-party-integrated instance to provide employees with Personalized Answers for leave balances on Employee Center.Configure the leave balance-related actions or any other information like payroll, medical benefits. Configure the related actions depending on the data type.Configure the data fetch type according to your organizational requirement for Personalized Answers- time off on Employee Center.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setup search experience, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Personalized Answers on Employee Center

Get personalized Answers about your leave balance within the ServiceNow® system or with an integrated third-party application.

With this feature, the employees can search for personal, relevant data, using AI- Search to get the Personalized Answers. The search works whether the data resides with ServiceNow® or any other integrated third-party application.

There are two third-party integrations supported for the Personalized Answers- time off, Kronos and Workday.

Kronos is supported in India, China, and North America. Workday is supported in Australia.

The Personalized Answers- time-off integration enables employees to find information about their leave balances.

In addition to searching for leave balances specifically, employees can also search for information such as 'how much sick leave do I have left'.

## Set up Personalized Answers for PTO

Set up a third-party-integrated instance to provide employees with Personalized Answers for leave balances on Employee Center.

### Before you begin

Role required: esc\_admin

### About this task

Set up the Personalized Answers, an AI-search enabled feature, for information like leave balance or more on the Employee Center search page.

The default third-party integration for the PTO balance search is Kronos and Workday but you can add your desired integration app for any other information.

**Note:** Employee Center does not provide Workday-integration by default.

A live query is answered based on an OAuth authentication on the Kronos-integrated instance.

The following plugins are required for the set-up of this feature with Kronos:

-   sn\_kronos\_spoke
-   app\_ex\_integrated\_answers
-   com.glide.hub.action\_step.payload

For more information on ServiceNow® plugins, see [List of plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

**Note:** app\_ex\_integrated\_answers plugin runs with Employee Center version 26.0.1 and Employee Experience Foundation version 25.0.1. When you install the plugin, it prompts that the appropriate versions of the said applications are going to be installed.

After the plugins are installed, [Set up the UKG spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-kronos.md) to register Kronos as an OAuth provider and authenticate requests from ServiceNow®.

After the UKG setup, ensure that the following prerequisites are established, before training and publishing the NLU model:

**Note:**

1.  The application registry, connections, and credentials must be within the Kronos application scope.
2.  The **sys\_user.list** must have the **Employee number** field in its **Personalized List Columns**. The employee number on the Employee Center portal is synced with the Kronos employee numbers.

If both the prerequisites are in order, move on to the following procedure:

### Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models** &gt; **Personalized Answers Leave Model**.

    The **Personalized Answers Leave Model** link should be in Draft state.

2.  Select **English**.

3.  Select **Intents** on the **Personalized Answers Leave Model** page.

4.  Select **Train model** on the top right-hand corner of the page.

5.  To view the **Publish your model** widget, after the training is over, go back to the **Personalized Answers Leave Model** page.

6.  Select **view phase**.

7.  Select **Publish**.

    ![This is a system diagram displaying the API calls made to use the Personalized Answers on Employee Center](../images/pa-api-calls-sys-diagram.jpg "Personalized Answers- Kronos integrated")

8.  To test the published model, navigate to **All** &gt; **NLU Workbench** &gt; **Models** &gt; **Personalized Answers Leave Model** &gt; **Intents** &gt; **Try model**.


### Result

The new genius result card is available on the search result page integrated with the Kronos data.

Use the Personalized Answers on your Kronos-integrated Employee Center portal to seek information on your remaining leave balance.

**Note:** Admins can review employee search logs in the **sys\_search\_event** table.

### Configure related actions for Personalized Answers

Configure the leave balance-related actions or any other information like payroll, medical benefits. Configure the related actions depending on the data type.

#### Before you begin

Role required: esc\_admin

#### About this task

Use the **Personalized Answers** related actions to act on the information found using the Personalized Answers on Employee Center. Set up different third-party integration, different types of information, and configure the action URLs as required.

#### Procedure

1.  Navigate to **All** &gt; **Personalized Answers** &gt; **API Mapping Configuration** &gt; **Get Leave balance**.

2.  Make the **View Policy** and **Request for Leaves** functional on the personalized answer page, by configuring **Primary action URL** and **Secondary action URL**.

    **Note:** The action names **View Policy** and **Request for Leaves** are default features. You can configure the action URLs, as suitable.

3.  Enable multi-location support for the third-party integration by selecting the **Multi-location** check box.

    **Note:** If you want to get the leave balance data for multiple locations, you must select the check box. Otherwise, the data for any one location is considered as default.


## Configure the data fetch type

Configure the data fetch type according to your organizational requirement for Personalized Answers- time off on Employee Center.

### Before you begin

Role required: esc\_admin

### About this task

Use any data fetch type, Live Call, AI Search, and Glide Query as required for the Personalized Answers- time off feature on Employee Center.

### Procedure

1.  Navigate to **All** &gt; **Personalized Answers** &gt; **Third Party Integration**.

2.  Select the third-party integration, Kronos or Workday.

3.  Choose **Live Call**, **AI Search**, or **Glide Query** according to your organizational need.

    **Note:** Workday supports **Live Call** if the Workday-integration is already available to you. Employee Center does not provide Workday-integration by default.

4.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **Employee Time off balance** to view the source of the **AI Search** and **Glide Query** data.


