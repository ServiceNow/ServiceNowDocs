---
title: Create the data model
description: Define the data for the Marketing Services application in ServiceNow Studio.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Tutorial part 1: Begin with an MVP, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Create the data model

Define the data for the Marketing Services application in ServiceNow Studio.

## Before you begin

Role required: admin

## About this task

The first step in creating an application is defining the data. This lab will use the table inheritance feature of the ServiceNow AI Platform and extend the system Task table for all requests. This will allow the Marketing Services application to access base fields and capabilities of the platform, such as assigning requests to users and asking for approvals.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select **Create** &gt; **File**.

3.  In the **Application** field, select the Marketing Services application.

4.  Select the **Data** category, and select **Table**.

5.  Select **Continue**.

6.  Select **Create a blank table**.

7.  Select **Continue**.

8.  Select **Create from an extensible table**.

9.  Select **Continue**.

10. Select the **Table** field, then select the **Task** table from the list.

11. Select **Continue**.

12. In the **Table label** field, enter `Marketing Design Request`.

13. Select the check box for **Auto number**.

14. In the **Prefix** field, enter `MDREQ`.

    ![Fill in the form for your new table.](../image/sns-z-tut-data-1.png)

15. Select **Continue**.

16. Set permissions for the Marketing Design Request table.

    1.  For the default admin role, select the check box for **All** permissions.

    2.  For the default user role, select the check boxes for the following permissions.

        -   **Create**
        -   **Read**
        -   **Write**
17. Select **Continue**.

18. Select **Edit table** once the table is ready.

19. Close the Welcome to Table Builder dialog by either selecting the Close dialog icon \(![](../../../reuse/icons/product-icons/close-outline-24.svg)\) or selecting **Next** to complete the tour of Table Builder features.

20. Select **+ Add a new field** to add a field to the Marketing Design Request table.

21. In the **Column label** field, enter `Project name`, then press the Enter key.

22. Hover over the field and select the open side panel icon \(![](../image/sns-z-tut-open-side-panel-icon.png)\).

23. In the Properties side panel, select the check box for **Mandatory**.

24. In the **Max. length** field, enter `160`.

25. Select **Save**.

    ![Fill in the properties for the Project name field.](../image/sns-z-tut-project-name.png)

26. Select **+ Add a new field** to add another field to the table.

27. In the **Column label** field, enter `Special instructions` and press the Enter key.

28. Hover over the field and select the open side panel icon \(![](../image/sns-z-tut-open-side-panel-icon.png)\).

29. In the Properties side panel, enter `400` in the **Max. length** field.

30. Select **Save**.

    ![Fill in the properties for the Special instructions field.](../image/sns-z-tut-special-instr.png)

31. Select **+ Add a new field** to add another field to the table.

32. In the **Column label** field, enter `Design copy` and press the Enter key.

33. Hover over the field and select the open side panel icon \(![](../image/sns-z-tut-open-side-panel-icon.png)\).

34. In the Properties side panel, enter `160` in the **Max. length** field.

35. Select **Save**.

    ![Fill in the properties for the Design copy field.](../image/sns-z-tut-design-copy.png)

36. Select **+ Add a new field** to add another field to the table.

37. In the **Column label** field, enter `Media type` and press the Enter key.

38. Set the field type to **Choice**.

    1.  Select the value in the **Type** column to open the field type list.

    2.  Enter `Choice` in the **Type** field or select **Choice** from the list of field types.

        ![Set the field type to Choice by selecting Choice from the list.](../image/sns-z-tut-field-type-choice.png)

    3.  Select the **Choice type** field, then select **Dropdown with --None--** from the list.

    4.  Select in the **Choices** field.

    5.  Enter `Digital`, then press the Enter key or select **Add** to add the choice.

    6.  Add another choice by selecting in the **Choices** field.

    7.  Enter `Print`, then press the Enter key or select **Add** to add the choice.

    8.  Select **Done**.

    ![Add a choice field with Digital and Print as the choice options.](../image/sns-z-tut-dropdown-choices.png)

39. Select **+ Add a new field** to add another field to the table.

40. In the **Column label** field, enter `External` and press the Enter key.

41. Set the field type to **True/False**.

    1.  Select the value in the **Type** column to open the field type menu.

    2.  Enter `True/False` in the **Type** field or select **True/False** from the list of field type options.

        ![Set the field type to True/False by selecting True/False from the list.](../image/sns-z-tut-field-type-true-false.png)

42. Search for the existing State field by entering `State` in the Filter fields search bar.

    ![Search for the existing State field by entering State in the Filter fields search bar](../image/sns-z-tut-filter-fields-state.png)

43. Hover over the State field and select the open side panel icon \(![](../image/sns-z-tut-open-side-panel-icon.png)\).

44. In the Properties side panel, expand the **Choices** section by selecting the expand icon \(![Expand console](../../../script/debugging/image/console_expand.png)\).

45. Select **Edit**.

    ![Select Edit to edit the choices for the field.](../image/sns-tut-z-edit-choices.png)

    **Note:** If you see **View** instead of **Edit**, check to make sure that you're in the Global scope so you can edit the table.

46. In the **Edit choices** dialog, change the label for the **Work in Progress** field to **Assigned** by using the Backspace key \(or keyboard shortcut\) and entering `Assigned`.

    ![Change the Work in Progress label to read Assigned.](../image/sns-z-tut-edit-choices-state.png)

47. Scroll down in the choices list, then select **+ Add a choice**.

48. In the **Label** field, enter `Design complete`.

49. In the **Value** field, enter `8`.

50. Select the move choice icon \(![Move element.](../../../administer/form-builder/image/fb-move-icon.png)\) for the Design complete field and drag the field between the **Assigned** and **Closed complete** fields.

    ![Rearrange the choices in the table.](../image/sns-z-tut-edit-choices-state-2.png)

51. Select **Apply**.

52. In the Changing this will create an override dialog, select **Confirm**.

53. Select **Save** to save your changes.


**Parent Topic:**[ServiceNow Studio tutorial part 1: Begin with an MVP](../concept/sns-z-tutorial-begin-with-mvp.md)

