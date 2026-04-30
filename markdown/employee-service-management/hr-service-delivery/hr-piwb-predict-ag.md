---
title: HR PIWB template: Predict the assignment group for incoming cases
description: Use a guided template that walks you through setting up a machine learning model to predict the correct assignment group for cases.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [HR Predictive Intelligence Workbench implementation, HR Predictive Intelligence Workbench, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR PIWB template: Predict the assignment group for incoming cases

Use a guided template that walks you through setting up a machine learning model to predict the correct assignment group for cases.

## Before you begin

Role required: sn\_piwb\_hr\_content.admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Create New from Templates**.

2.  Select the **Predict Assignment Group for HR Cases** guided template and click **Start**.

3.  Provide a unique name for your use case in the **Use case name** field.

4.  Provide a unique name for the model in the **Model name** field.

5.  Click **Advanced Setup**.

    The use case set up page opens displaying the name and description of the use case you created. On this page, you can see all the implementation phases you will work through to create and implement your use case model.

6.  In the **Create a model** section of the setup, fill in the required fields with a **Model name** and **Short description**

    **Note:** Other data related to the model is pre-filled by default, such as the **Data table**, **Predicted field**, and **Processing Language**.

7.  Expand the **Review the filters used to train this model** section to view the default filters.

    You can customize the filters to best represent your business data or add new criteria by clicking **New Criteria**.

8.  Expand the **Review the input fields for this model** section to view the pre-populated fields.

    You can customize the fields to best represent your business data by moving fields between the **Available** and **Selected** slush buckets.

9.  Click **Save**.

    The use case **ML Model** setup page opens.

10. Click **Continue** in the **Create and train models** section.

    The **Create a model** page opens.

11. Click **Train this model**.

    The **Train this model** window appears letting you know that the process will take a while.

12. Click **Start** to initiate training.

    You are returned to the ML Model setup page.

13. Click **View Progress** below the header on the ML Model setup page to monitor the training process.

14. Click **Start** to initiate training.

    You are returned to the use case setup page.

15. Click **View Progress** below the header on the use case setup page to monitor the training process.

16. On the use case setup page, click **Start** in the **Evaluate and tune your models** section.

    The use case **Evaluate and tune your models** page opens. Here you can refine your use case model, defining the right combination of coverage and precision to use.

17. Click the box next to the use case model that you want to evaluate and tune.

    You can view the evaluation data for the use case model by clicking the chevron icon next to the model name to expand details.

18. In the **Select an Action** list menu, select **Open model record**.

    The use case model record opens. You can view the **Precision\(%\)**, **Coverage\(%\)**, and **Net Automation\(%\)** scores.

19. In the **Retraining Schedule** field you can change the definition, if desired.

    The default value is **Run Once**, but you can retrain as often as every 30 days to every 180 days.

20. If you made evaluation or tuning changes to the use case model, click either **Update** or **Update and retrain**, to run retraining again one time.

    The use case **Evaluate and tune your models** page opens.

21. If you are ready to test your use case model, click the box next to the model that you want to test.

22. In the **Select an Action** list, select **Test this model**.

    The use case **Testing your models** page opens with the use case model you selected to test is in the **Selected** slush bucket.

23. In the **Select models to test** section, decide if there are other use case models available that you want to test.

    If so, move them to the **Selected** slush bucket.

24. In the **Define testing parameters** section, decide if you want to test one use case model.

    If so, select the **Single test** test type. **Single test** is the default.

    **Note:** Select **Batch test** when you want to test more than one use case model.

25. Determine the number of top results you want to display.

26. In the **Input fields** section, provide a short description of your use case model test.

27. Click **Run Test**.

28. View the test results data for the use case model in the **View test results** section.

29. If you are ready to integrate your use case model into your business processes, return to the use case **Evaluate and tune your models** page and select the box next to the model that you want to integrate.**Start** in the **Integrate the best model** section.

30. In the **Select an Action** list menu, select **Integrate this model**.

    The **Select a model to integrate** page opens.

31. Click **Integrate**.

32. Click **Integrate** again when the pop-up asks you if you are sure you want to perform this action.

    You have integrated a use case model into your business process.

    **Note:** For details regarding trained use case integration implementation, refer to [Predictive Intelligence Workbench integration and customization](https://www.servicenow.com/docs/access?context=itsm-piwb-integ-implem-custom&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).


**Parent Topic:**[HR Predictive Intelligence Workbench implementation](../concept/hr-piwb-implementation-guidance.md)

