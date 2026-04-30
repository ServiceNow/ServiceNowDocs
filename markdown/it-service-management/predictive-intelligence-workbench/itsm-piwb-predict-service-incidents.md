---
title: Predict Service for incoming incidents
description: Use this guided template to auto-assign incoming incidents to the correct service to reduce your incident resolution times.
locale: en-US
release: xanadu
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [ITSM Predictive Intelligence Workbench implementation, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Predict Service for incoming incidents

Use this guided template to auto-assign incoming incidents to the correct service to reduce your incident resolution times.

## Before you begin

Role required: piwb\_manager or piwb\_viewer

## About this task

This template walks you through customizing a use case model to predict the service for your incoming incidents. When the use case template shows the label **Pretrained**,you will bypass several implementation steps and are automatically taken to evaluate and tune your models when you click **Start**. Otherwise, you will begin by creating a machine learning model.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Templates**.

2.  Select the **Predict Service for incoming incidents** guided template.

    ![Predict Service for incoming incidents template.](../image/piwb-use-case-predict-service-int.png)

3.  In the **Use case - Predict Service for incoming incidents** pop-up form, provide a unique name for your use case in the **Use case name** field.

    ![Use case pop-up form.](../image/ITSMPIWBUseCaseSetupPopup.png)

    **Note:** The use case will contain multiple models that you create. You can use the same name as the template, if desired.

4.  Although not mandatory, it's beneficial to provide unique details about the use case in the **Short description** field.

    **Note:** Typically the short description provides details about what the goal of the use case is or your purposes for creating the use case.

5.  Provide a name for the model in the **Model name** field.

    **Note:** Models are trained based on default parameters. The name of the model should reflect its purpose, for example, "Model for past years data".

6.  Review the base system parameters set to help train the model in the **Input fields** and **Number of records** fields.

    To modify this data, click **Advanced Setup**.

    **Note:** By clicking **Advanced Setup** you can change the processing language, review and modify filters used to train the model. You can customize the filters to best represent your business data or add new criteria by clicking **New Criteria**. Review and modify input fields used to generate predictions. Customize the fields to best represent your business data by moving fields between the **Available** and **Selected** lists. Save any changes that you make.

7.  Click **Start**.

    A pop-up message lets you know your model is created and that training is underway.

    **Note:** To start implementation, you must provide at least a use case name and model name.

    ![ITSM PWIB Model creation Great Job pop-up.](../image/ITSMPIWBGreatJobPopup.png)

8.  Click **Done**.

    The use case page displays the name and description of the use case you created. On this page, you can see all the guided implementation phases you will work through to create and implement your use case model.

    ![ITSM PIWB Use Case Guided Steps.](../image/ITSMPIWBGuidedSteps.png)

9.  Click **View Progress** below the header on the use case setup page to monitor a current training process.

    ![ITSM PIWB training progress.](../image/ITSMPIWBModelTrainingProcess.png)

    **Note:** When training is complete, you will receive an email notification letting you know your use case model training was successful. For more information about use case model notifications, refer to [ITSM Predictive Intelligence Workbench notifications](../reference/itsm-piwb-notifications.md).

10. Click the model name under **Trained Models** on the use case setup page to view associated data about the trained model.

    The **Model details** page opens.

11. In the **Retraining Schedule** field of the **Models detail** page you can change the definition, if desired.

    The default value is **Every 30 days**, but you can retrain as often as once to every 180 days.

12. If you made schedule retraining changes to the use case model, click either **Update** or **Update and retrain**, to retrain again.

13. To tune a model, click **Tune Values** on the use case setup page under **Trained Models**.

    The tuning page for the use case opens displaying the associated model name with the following data: **Distribution \(%\)**, **Net Automation**, **Precision \(%\)**, **Coverage \(%\)**, and any comments. View the evaluation data used for the use case and associated model

    **Note:** You can only tune values when the model is trained.

14. If desired, tune and refine the model by defining the right combination of coverage and precision to use.

15. Double-click in the **Precision \(%\)** and **Coverage \(%\)** fields to change values.

    Changes are automatically saved.

16. If desired, click **Create Another** to create another model associated with your use case in the **Create and train models** section of the setup page.

    Repeat the process to create and train the model.

17. In the **Test your models** section of the use case page, click **Start** to begin the testing process.

    The **Testing your models** page opens.

    ![Testing models](../image/PIWBTestingModels.png)

18. Under **Select models to test**, decide if there are other use case models available that you want to test.

    If so, move them to the **Selected** list.

19. Under **Define testing parameters**, decide if you want to test one use case model.

    If so, select the **Single test** test type. **Single test** is the default.

    **Note:** Select **Batch test** when you want to test more than one use case model.

20. Determine the number of top results you want to display.

21. Under **Input fields**, provide a short description of your use case model test.

22. Click **Run Test**.

23. View the test results data for the use case model under **View test results**.

    ![ITSM PIWB single testing](../image/piwb-single_testing.png)

    ![ITSM PIWB batch testing.](../image/piwb-batch_testing.png)

24. If you are ready to integrate your use case model into your business processes, return to the use case set up page and click **Start** in the **Integrate a model** section.

    The **Select a model to integrate** page opens.

25. In the **Select a Model** drop-down menu, select the model you want to integrate.

    The **Select a model to integrate** page opens.

    ![Integrate model.](../image/PIWBIntegrateModel.png)

    **Note:** You can change the retraining schedule via this page if you desire. Use the **Retraining Schedule** drop down selection field to change from the default 30 day value.

26. Click **Integrate**.

27. Click **Integrate** again when the pop-up asks you if you are sure you want to perform this action.

    You have integrated a use case model into your business process.

    **Note:** For details regarding trained use case integration implementation, refer to [Predictive Intelligence Workbench integration and customization](../concept/itsm-piwb-integ-implem-custom.md).


