---
title: Use Predictive Intelligence in Workflow Studio with ML actions
description: Use Predictive Intelligence actions in Workflow Studio to create flows that incorporate your model predictions.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-01-16"
reading_time_minutes: 8
breadcrumb: [Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Use Predictive Intelligence in Workflow Studio with ML actions

Use Predictive Intelligence actions in Workflow Studio to create flows that incorporate your model predictions.

## Before you begin

-   Make sure the following plugins are activated in your instance: Predictive Intelligence \(com.glide.platform\_ml\) and Predictive Intelligence for Workflow Studio \(com.snc.ml\_flowdesigner\).
-   Create or use an existing trained Predictive Intelligence solution.
-   Roles required: ml\_admin or admin, and flow\_designer or delegated\_developer.

## About this task

Workflow Studio enables you to automate complex processes. The first thing to identify is what process you want to automate. In this example scenario, you're automating the assignment of a Category to an incident record. When you complete the flow, the next incident record created in your instance updates the Category field in the record based on the text entered in the **Short description** field.

You can deploy any active and trained classification, similarity, or regression ML solution in your flow, as appropriate for your use case.

**Note:** The regression framework is deprecated in the Yokohama release. You can continue to use existing regression solutions but you can't create new ones.

In this example procedure, you create a flow that implements the ml\_incident\_categorization solution in a Workflow Studio action. You can find this solution by searching on the ML Solutions \[ml\_solution\] table, as shown in the image below. Confirm that the solution you use has been trained and its **Active** value is set to **true**.

![An image showing the ML Solution that will be used as input to the Flow Designer flow](../images/use-predict-intel-flow-designer-ml-actions1.png)

For more information on how to use Flow Designer in Workflow Studio, see [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US). For information about the Actions included in Predictive Intelligence for Workflow Studio, see the Spoke actions table in [Machine Learning solutions for Flow Designer](https://www.servicenow.com/docs/access?context=predictive-intelligence-spoke&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **New** &gt; **Flow**.

    ![In Workflow Studio, on the Flows tab, the selection for a new flow is highlighted.](../images/use-predictive-intelligence-flow-designer-ml-actions2Y.png)

3.  On the **Let's get the details for your flow** screen, configure the following fields.

    Expand **Show additional properties** to view all fields.

    |Field|Description|
    |-----|-----------|
    |Flow Name|Provide a name for the flow. In this scenario, you enter `Auto-assign Category to Incident`.|
    |Description|Enter a brief summary description of what the flow delivers. For example, you enter the following: `When an incident is created, it automatically triggers this flow, which uses ML Solutions to predict the correct Category for the incident.`|
    |Application|Select **Global**.|
    |Protection|Select **--None--** or **Read-only**. In this scenario, you select **--None--**.|
    |Run As|Select **User who initiates session**.|
    |Run with role\(s\)|Leave blank.|
    |Flow priority default|Medium \(default\).|

4.  Select **Build flow**.

    ![The screen for Let's get the details for your flow, with fields filled according to the example.](../images/use-predictive-intelligence-flow-designer-ml-actions3Y.png)

    The Flow screen appears, showing the Auto-assign Category to Incident name you assigned to the flow. If a Getting started screen appears, select **Skip tour**.

5.  In the TRIGGER section of the Flow screen, configure the following fields to create a trigger for the flow.

    1.  **Select a Trigger**: Select **Record**, then from the list of possible options for Record, select **Created**.

        ![On the tab for the example flow, in the Trigger section, the Record-Created selection is highlighted.](../images/use-predictive-intelligence-flow-designer-ml-actions4Y.png) ![]()

    2.  **Table**: Select **Incident \[incident\]**.

        **Note:** After you configure both the **Trigger** and **Table** fields, record data pills appear in the **Data** section of the screen so you can use them in your flow.

        ![On the tab for the example flow, in the Trigger section, the Table field is filled with the value Incident.](../images/use-predictive-intelligence-flow-designer-ml-actions5Y.png)

    3.  **Condition**: Select **Add filters** if you want to add any conditions to the flow.

    4.  Open the **Advanced Options** panel to view additional conditions you can apply to the flow.

    5.  To close the panel, select **Advanced Options**.

    6.  Select **Done**.

6.  In the ACTIONS section of the screen, configure the following fields to create a Classification Prediction action.

    1.  **Action** tab: Select **Action** &gt; **Predictive Intelligence** &gt; **Classification Prediction**.

        ![In Actions section of the example, the search result for Predictive Intelligence is highlighted. Under that installed spoke is a list of ML model types with Classification Prediction highlighted.](../images/use-predictive-intelligence-flow-designer-ml-actions7Y.png)

        Select the information icon \(![](../../now-assist-admin/image/info-icon.png)\) to see the description of a Classification Prediction.

    2.  **Solution \[ML Solution\]**: Select **ml\_incident\_categorization**.

    3.  **Top N**: Enter `3` for the example scenario.

        When you enter a number, such as 3, the system uses the top three ML predictions that have the highest prediction confidence score. If you don't enter anything, the system sets the default value to 1.

    4.  **Input Record**: Drag and drop your **Trigger → Incident Record** data pill into the Input Record field.

        ![An image showing how to drag and drop the trigger record pill into the Input Record field.](../images/use-predict-intel-flow-designer-ml-actions8.png)

        The Action, Solution Name, Top N, and Input Record values provide a base for the Category prediction.

        **Note:** The data pill you drop into this record must also be a record. For example, don't try to drop a table pill or a date/time pill into the Input Record field.

    5.  Select **Done**.

        **Result**: The Classification Prediction action is completed in the flow and its data pills appear in the Data section of the screen.

        ![An image showing the completed Classification Prediction action](../images/use-predict-intel-flow-designer-ml-actions9.png)

7.  In the ACTIONS section of the screen, use the following steps to create actions and flow logic for the incident's Prediction Results.

    **Note:** Although you can use a loop to iterate through every prediction result, the scenario shown in this documentation uses a relatively small number of actions. For more advanced flow configurations, see the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

    1.  **For each item in** **list of items**: Drag and drop the **Prediction Results** data pill into the **Items** field.

        ![An image showing how to drag and drop the Prediction Results data pill into the Classification Prediction action](../images/use-predict-intel-flow-designer-ml-actions10.png)

        **Note:**

        In order to access the list of items in the Regression Prediction action, you don't need the **For Each Item in** flow logic.

        \(The regression framework is deprecated in the Yokohama release. You can continue to use existing regression solutions but you can't create new ones.\)

    2.  Select **Done**.

        **Result**: The Prediction Results action is started in the flow and its data pills appear in the Data section of the screen.

8.  In the ACTIONS section of the screen, select **Action** &gt; **Predictive Intelligence** &gt; **PI Confidence Check**.

    The PI Confidence Check is a tool you can use to compare values in a flow. In this use case, it compares prediction result values, and the output from the check is either True or False.

    ![An image showing how to use PI Confidence Check in the flow](../images/use-predict-intel-flow-designer-ml-actions11.png)

9.  Drag and drop the **confidence** data pill into the **Predicted Number from Predictive Intelligence** field.

10. Enter `50` in the **Comparison Threshold** field.

    In this example scenario, you enter the number 50, which tells the system to use predictions that have a confidence score above 50%.

11. Select **Done**.

    ![This image shows users how to drag the Confidence data pill into the Predicted Number from Predictive Intelligence field](../images/use-predict-intel-flow-designer-ml-actions12.png)

12. Select **Flow Logic** &gt; **If** to add a condition to the flow.

    ![This image shows users how to evoke flow logic for the PI Confidence Check action](../images/use-predict-intel-flow-designer-ml-actions14.png)

13. Configure the following fields to define the first part of the condition flow logic.

    -   **Condition**: Enter a name for the condition that defines what it does. In this example scenario, you enter `Confidence greater than 50`.
    -   **Condition 1**: Drag and drop the **Confidence To Predict** data pill into the field. Select **is**, and enter the value `True`. This step completes the first part \(the antecedent\) of the condition flow logic.
    -   Select **Done**.
    ![This image shows users how to use flow logic to create and define a condition](../images/use-predict-intel-flow-designer-ml-actions15.png)

14. Select **Action** and enter `worknote` into the search field.

15. Select **ITSM** &gt; **Add Worknote** to add a work note as the second part \(the conclusion\) of the condition.

    ![This image shows users how to locate the Add Worknote action in the flow](../images/use-predict-intel-flow-designer-ml-actions16.png)

16. Configure the following fields to define the second and final part of the condition flow logic.

    -   **Action**: As a result of Step 14 above, **Add Worknote** appears automatically in this field.
    -   **task \[task\]**: Drag and drop the **Incident Record** data pill into the field.
    -   **work note**: Drag and drop the **predicted\_value** data pill into the field. This step completes the condition flow logic conclusion.
    -   Select **Done**.
    ![This image shows users how to configure and save the Add Worknote action in the flow](../images/use-predict-intel-flow-designer-ml-actions17.png)

17. Select **Action** and enter `update record` into the search field.

18. Select **Update Record**.

    ![This image shows users how to locate the Update Record action](../images/use-predict-intel-flow-designer-ml-actions18.png)

19. Configure the following fields to update the Incident Record.

    -   **Action**: As a result of Step 16 above, **Update Record** appears automatically in this field.
    -   **Record**: Drag and drop the **Incident Record** data pill into this field.
    -   **Table**: Select **Incident \[incident\]**.
    -   **Fields**: Select **Category**. Then drag and drop the **predicted\_value** data pill into this field, next to the **Category** value.
    -   Select **Done**.

        ![This image shows users how to configure and save the Update Record action](../images/use-predict-intel-flow-designer-ml-actions19.png)

20. Select **Save**.

21. Select **Activate**.

    **Result**

    -   Your Auto-assign Category to Incident flow is activated and complete.

        ![This image shows users what their completed flow looks like](../images/use-predict-intel-flow-designer-ml-actions20.png)

    -   It also appears as published in the Flows column on the Workflow Studio home screen.

        ![This image shows users that their completed flow appears as published on the Flow Designer screen](../images/use-predict-intel-flow-designer-ml-actions21.png)

22. Navigate to **Incidents**.

23. Select **New** to create a test incident record in the Incidents table.

    In this example scenario, you create record INC0010011.

    ![This image shows users how to create a new incident record](../images/use-predict-intel-flow-designer-ml-actions22.png)

24. In the record you created, note in the following image that the Category value is set to **Inquiry / Help**.

25. In the **Short description** field, enter `Email not working`.

26. Select **Submit**.

    ![This image shows users the Number and Category values for the new record they created, and instructs them to enter the 'Email not working' value into the Short Description field](../images/use-predict-intel-flow-designer-ml-actions23.png)

    **Result**

    The system updates the incident record to show that its Category value has changed from **Inquiry / Help** to **Email**.

    -   ![This image shows users that the Category record value has changed from Inquiry to Email](../images/use-predict-intel-flow-designer-ml-actions24.png)

    -   ![This image shows users the bottom of the record, where the Work Note they created states that the Category for the record has been updated from Inquiry to Email](../images/use-predict-intel-flow-designer-ml-actions25.png)


**Related topics**  


[Machine Learning solutions for Flow Designer](https://www.servicenow.com/docs/access?context=predictive-intelligence-spoke&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

