---
title: HR PIWB template: Auto-categorize email cases
description: Use a guided template that walks you through setting up a machine learning model to categorize the email cases automatically for improved productivity and cost savings.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [HR Predictive Intelligence Workbench implementation, HR Predictive Intelligence Workbench, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR PIWB template: Auto-categorize email cases

Use a guided template that walks you through setting up a machine learning model to categorize the email cases automatically for improved productivity and cost savings.

## Before you begin

Role required: sn\_piwb\_hr\_content.admin

## About this task

This template walks you through customizing a use case model to categorize the email cases. When the use case template shows the label **Guided**, you can use several implementation steps and are automatically taken to evaluate and tune your models when you click **Start**. Otherwise, you begin by creating a machine learning model.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Create New from Templates**.

2.  Select the **Email case categorization for HR** guided template.

    ![PIWB Email case categorization use case model](../image/piwb-hr-email-categorization.png "Email case categorization use case")

3.  Provide a unique name for your use case in the **Use case name** field.

    **Note:** The use case contains multiple models that you create. You can use the same name as the template, if required.

4.  Provide a name for the model in the **Model name** field.

    **Note:** Models are trained based on default parameters. The name of the model should reflect its purpose, for example, `Email case categorization for HR`.

5.  Click **Start**.

    **Note:** To start implementation, you must provide a use case name and short description.

    The use case setup page opens displaying the name and description of the use case you created. On this page, you can see all the implementation phases to create and implement your use case model.

6.  In the **Create and train models** section of the setup, click **Start** to create a model associated with your use case.

7.  Fill in the required fields with a **Model name** and **Short description**.

    **Note:** Other data related to the model is pre-filled by default, such as the **Data table**, **Predicted field**, and **Processing Language**.

8.  Expand the **Review the filters used to train this model** section to view the default filters.

    Review the base system parameters set to help train the model in the **Input fields** and **Number of records** fields. To modify this data, click **Advanced Setup** and then **Save** any changes you make. You can customize the filters to best represent your business data or add new criteria by clicking **New Criteria**.

    **Note:** By clicking **Advanced Setup** you can change the processing language, review, and modify the filters used to train the model. You can customize the filters to best represent your business data or add new criteria by clicking **New Criteria**. Review and modify the input fields used to generate predictions. Customize the fields to best represent your business data by moving fields between the **Available** and **Selected** lists. Ensure that you have sufficient number of records for the model. Save any changes you make.

9.  Click **Save**.

    The use case **ML Model** setup page opens.

10. Click **Continue** in the **Create and train models** section.

    The **Create a model** page opens.

11. Click **Train this model**.

    The process may take a while. The **Train this model** window appears letting you know that the process takes a while.

12. Click **Start** to initiate training.

    The ML Model setup page opens.

13. Click **View Progress** below the header on the ML Model setup page to monitor the training process and click close.

14. Click **View Progress** below the header on the use case setup page to monitor the training process.

15. Click **Start** to initiate training.

    The use case setup page opens with the trained model.

16. On the available trained model, click the **Tune values**.

    The use case model record opens. You can view the **Precision\(%\)**, **Coverage\(%\)**, and **Net Automation\(%\)** scores.

    **Note:** Refine your use case model by defining the right combination of coverage and precision values.

17. When you are ready to test your use case model, click **Test your models** .

    ![PIWB model guided steps for training, testing, and integration](../image/piwb-steps.png "Guided Steps")

    The use case **Testing your models** page opens.

18. In the **Select models to test** section, refine the models for testing and comparison.

    Move the options from **Available** to the **Selected**. Remember, selecting more models takes more processing time for a batch test.

19. In the **Define testing parameters** section, decide if you want to test one use case model.

    Select the **Single test** test type. **Single test** is the default.

    **Note:** Select **Batch test** when you want to test more than one use case model.

    Determine the number of top results you want to display.

20. In the **Input fields** section, provide a short description of your use case model test.

21. Click **Run Test**.

    View the test results data in the View test results section with details such as predicted values and confidence.

22. Click **Mark as complete** to complete testing.

23. When you are ready to integrate your use case model into your business processes, click **Start** in the **Integrate a model** section.

24. In the **Select a model to integrate** section, select the model from the available list.

25. In the **Retraining Schedule** field you can change the definition, if desired.

    The default value is **Run Once**, but you can retrain as often as every 30 days to every 180 days.

26. Click **Integrate**.

    On the confirmation pop-up, click **Integrate** again to complete this action. You have integrated a use case model into your business process.


## Result

When the configuration is complete, the solution auto-categorizes the HR service for email cases. For more information, see [Auto-case creation from an email](../concept/hr-agent-intelligence-1.md)

## What to do next

You can verify the integration status from **HR Administration** &gt; **HR AI Configurations** &gt; **Solution definition**. The use case is now mapped to the selected solution definition.

**Parent Topic:**[HR Predictive Intelligence Workbench implementation](../concept/hr-piwb-implementation-guidance.md)

**Related topics**  


[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Get started with Predictive Intelligence](https://www.servicenow.com/docs/access?context=install-predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&section=get-started-predictive-intelligence&ft:locale=en-US)

[Predictive Intelligence Workbench integration and customization](https://www.servicenow.com/docs/access?context=itsm-piwb-integ-implem-custom&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

