---
title: Configure Sentiment Analysis
description: Activate the required plugin, enable the sentiment analysis property, and assign roles to use the sentiment analysis feature.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure Sentiment Analysis

Activate the required plugin, enable the sentiment analysis property, and assign roles to use the sentiment analysis feature.

Follow the steps in the table below to configure the sentiment analysis property for cases.

<table id="table_ih2_hfc_5rb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ensure that your instance is set up for Predictive Intelligence \(PI\).

</td><td>

Predictive Intelligence is a ServiceNow platform feature that provides a layer of artificial intelligence, which serves as a framework for machine learning models. For more information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Activate the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\).

</td><td>

The Task Intelligence for Customer Service application enables customers to leverage machine learning algorithms in Customer Service Management. The sentiment analysis feature is included with this application.

 This application automatically activates the following plugins:

-   Predictive Intelligence for Customer Service Management \(com.snc.csm\_ml\)
-   Customer Service \(com.sn\_customerservice\)
-   Skills Management \(com.snc.skills\_management\)
-   Dynamic Translation \(com.glide.dynamic\_translation\)
-   ServiceNow Language Detection Service Spoke \(com.glide.language\_detection\_spoke\)
-   Predictive Intelligence - Task Intelligence \(com.glide.platform\_ml\_task\)
-   Admin Center for Task Intelligence \(com.sn\_ti\_admin\)

</td></tr><tr><td>

Configure the Case list and Case form to display the sentiment analysis fields.

</td><td>

The sentiment analysis feature adds the following fields:

-   **Original sentiment**
-   **Current sentiment**
-   **Sentiment over time**

 Configure these fields for each of the following interfaces as needed:

-   CSM Configurable Workspace
-   CSM Agent Workspace
-   Core UI Platform interface

</td></tr><tr><td>

Use the [Task Intelligence Admin Console](csm-task-intel-admin-center.md) to create and deploy a sentiment model.

</td><td>

See [Create a model to predict case sentiment](csm-task-intel-create-sentiment-solution.md).

</td></tr></tbody>
</table>## Configure sentiment analysis fields

The sentiment analysis feature uses the following fields to display sentiment prediction information on Cases list and Case form:

-   Original sentiment
-   Current sentiment
-   Sentiment over time

Add the sentiment fields to Case list views and to the Case form for CSM Configurable Workspace, CSM Agent Workspace, and Core UI.

-   In CSM Configurable Workspace, these fields appear as secondary values in the configurable form header. You can configure secondary values to display either below the primary value at the top of the form or in the Record Information tab in the contextual side panel. \(For more information, see [Display the form ribbon and form header secondary values in the Contextual side panel](../task/config-csm-display-header-in-sidebar.md).\)
-   In CSM Agent Workspace, these fields appear in the Case form header.
-   In Core UI, these fields appear on the Case form.

<table id="table_odd_3dc_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Original sentiment

</td><td>

The sentiment that is predicted when a case is created. The values for this field include:-   Positive
-   Neutral
-   Negative

</td></tr><tr><td>

Current sentiment

</td><td>

The most recent sentiment prediction for the case. This prediction is assessed when a case is created and updated. The values for this field include:-   Positive
-   Neutral
-   Negative

 When a case is created, the **Original sentiment** and **Current sentiment** are assigned the same value.

 When a case is updated, the **Original sentiment** remains the same and the **Current sentiment** is updated with the most recent prediction.

</td></tr><tr><td>

Sentiment over time

</td><td>

A trend indicator that reflects the change in sentiment as a case is updated. The values for this field include:

-   Improving
-   Neutral
-   Declining

 This field requires a minimum of two sentiment predictions in order to calculate a value.

</td></tr></tbody>
</table>## Configure sentiment fields for CSM Agent Workspace

To add the sentiment fields to the Case list:

1.  Enter **sys\_aw\_list.list** in the application navigator and press **Enter**.
2.  Click **All** from the Case \[sn\_customerservice\_case\] table.
3.  Click the lock icon next to the **Columns** field.
4.  Select and move the sentiment fields from the **Available** column to the **Selected** column.
5.  Click the lock icon again.
6.  Click **Update**.

To add the sentiment fields to the Case form header:

1.  Select **CSM Workspace** as the application scope.
2.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.
3.  In the Table column of the Form Headers list, select **sn\_customerservice\_case**.

    If adding sentiment fields for a case type, select the case type table that extends the Case table.

4.  Click **New** in the Secondary Values related list.
5.  Select the desired sentiment field in **Field** field and click **Submit**.
6.  Repeat step 5 for the remaining sentiment fields.
7.  Click **Update** on the Form Header form.

## Configure sentiment fields for CSM Configurable Workspace

To add the sentiment fields to the Case list:

1.  Enter **sys\_ux\_list.list** in the application navigator and press **Enter**.
2.  Click **All** from the Case \[sn\_customerservice\_case\] table.
3.  Click the lock icon next to the **Columns** field.

    If adding sentiment fields for a case type, select the case type table that extends the Case table.

4.  Select and move the sentiment fields from the **Available** column to the **Selected** column.
5.  Click the lock icon again.
6.  Click **Update**.

To add the sentiment fields to the Case form header:

1.  Select **CSM Workspace** as the application scope.
2.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.
3.  In the Table column of the Form Headers list, select **sn\_customerservice\_case**.
4.  Click **New** in the Secondary Values related list.
5.  Select the desired sentiment field in **Field** field and click **Submit**.
6.  Repeat step 5 for the remaining sentiment fields.
7.  In the UX header Configurations list, click **Edit**.
8.  In the **Collection** field, add **CSM/FSM Configurable Workspace Header Config**.
9.  Click **Update** on the Form Header form.

## Configure sentiment fields for Core UI

To add the sentiment fields to the Case list:

1.  Navigate to **Customer Service** &gt; **Cases** &gt; **All**.
2.  Right-click the list header and select the desired list view.
3.  Right-click any column heading and select **Configure** &gt; **List Layout**.
4.  Select and move the fields from the **Available** column to the **Selected** column.
5.  Click **Save**.

To add the sentiment fields to the Case form:

1.  Navigate to **Customer Service** &gt; **Cases** &gt; **All**.
2.  Open a case.
3.  Right-click the form header and select **Configure** &gt; **Form Layout**.
4.  Select and move the fields from the **Available** column to the **Selected** column.
5.  Click **Save**.

**Related topics**  


[Sentiment Analysis](case-sentiment-analysis.md)

