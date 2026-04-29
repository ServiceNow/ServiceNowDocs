---
title: Add a playbook to your workflow
description: Add visibility and consistency to your workflow by adding a playbook to your app in ServiceNow Studio. The goal of this section is that when new Marketing Design Requests are submitted, the playbook opens in a new tab, providing clear context for the marketing team and ensuring they understand the purpose and importance of each step in the workflow.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Tutorial part 2: Automate and improve, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Add a playbook to your workflow

Add visibility and consistency to your workflow by adding a playbook to your app in ServiceNow Studio. The goal of this section is that when new Marketing Design Requests are submitted, the playbook opens in a new tab, providing clear context for the marketing team and ensuring they understand the purpose and importance of each step in the workflow.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select **File** &gt; **Automation** &gt; **Playbook**.

3.  Select **Continue**.

4.  Enter `Marketing Design Request` in the **Playbook name** field.

5.  Select **Build Playbook**.

6.  Select **Start**.

    ![Select the Start button on your new playbook.](../image/sns-z-tut-pb-start.png)

7.  Select **Define your own conditions for when your process runs**.

8.  Choose **Record create** for Trigger type.

9.  Choose **Marketing Design Request** for Table.

    ![Add information about when your playbook should run.](../image/sns-z-tut-pb-add-properties.png)

10. Select **Done**.

11. Select the \(+\) to add a new stage.

    ![Add a new stage.](../image/sns-z-tut-pb-create-stage.png)

12. Select **Create a stage**.

13. Enter `Create Design` in the **Label** field.

14. Select **Save and close**.

15. Hover over the Create Design stage until the \(+\) buttons appear on either side.

16. Select the \(+\) to the right of the Create Design stage to add a second stage.

    ![Add a second stage.](../image/sns-z-tut-pb-create-design.png)

17. Select **Create a stage**.

18. Enter `Review Design` in the **Label** field.

19. Select **Save and close**.

20. Select the \(+\) button in the Create Design stage.

21. Select the **Add an activity** button in the popup.

    ![Add an activity to the Create Design stage.](../image/sns-z-tut-pb-add-activity.png)

22. Select **Autocompleting User Form** under **Common Activities**.

23. Enter `Complete Marketing Design` in the **Label** field.

24. Select the **Automation** tab.

25. Select the **Record** data pill picker icon ![](../image/sns-z-tut-data-pill-picker.png).

26. Select the **Trigger**.

27. Select the trigger record.

    ![Complete the information needed for the autocompleting user form.](../image/sns-z-tut-pb-automation.png)

    **Note:** Your labels may appear slightly differently.

28. Select **Add Condition**.

    **Note:** You may need to save the changes on the panel and reopen if **Add Condition** does not appear.

29. Set the condition to **\[State\] \[is\] \[Design complete\]**.

    ![Complete the Add Condition form.](../image/sns-z-tut-pb-design-complete.png)

30. Select **Save**.

31. Select the **UI Layout** tab.

32. Remove the **This activity &gt; Label** data pill from the **Title** field.

33. Select the **Title** data pill picker icon ![](../image/sns-z-tut-data-pill-picker.png).

34. Select the **Trigger**.

35. Select the trigger record.

36. Select **Project name**.

    ![Remove the label in the title field and select the project name as the trigger.](../image/sns-z-tut-pb-remove-label.png)

    **Note:** Your labels may appear slightly differently.

37. Enter `description,special_instructions,design_copy,media_type,external` in the **Record fields** field.

38. Enter `assigned_to,state` in the **Form fields** field.

39. Select **Associated Record** in the **Attachment source** field.

    ![Complete the form with the listed information.](../image/sns-z-tut-pb-record-fields.png)

40. Select **Save and close**.

41. Switch to the **Review Design** stage.

42. Select \(+\).

43. Select **Add a decision**.

    ![Add a decision in the Review Design stage.](../image/sns-z-tut-pb-add-decision.png)

44. Select the **Branches** tab.

45. Enter `Is external` in the **Branch label** field.

46. Select **Add Condition**.

47. Select **Trigger – Marketing Design Request** in the **Field** field.

48. Select **External**.

    ![Add a condition.](../image/sns-z-tut-pb-add-condition.png)

49. Complete the condition statement with **\[Trigger-Marketing Design Request\] \[is\] \[true\]**.

    ![Complete the fields for the condition.](../image/sns-z-tut-pb-add-cond-final.png)

50. Select **Save and close**.

51. Select **\(+\)** on the Is external branch.

52. Select **Add an activity**.

    ![Add an activity on the Is external branch.](../image/sns-z-tut-pb-add-activity-2.png)

53. Select **View Approval Requests** under the **Global** category.

54. Select **Add Condition** on the **Automation** tab.

55. Set the field and operator to **\[Approval for\] \[is\]**.

56. Select the **Value** data pill picker icon ![](../image/sns-z-tut-data-pill-picker.png).

57. Select **Trigger**.

58. Select the trigger record.

    ![Add an activity trigger to your condition.](../image/sns-z-tut-pb-add-activity-trigger.png)

    **Note:** Your labels may appear slightly differently.

59. Select **Save and close**.

60. Select **Activate** for the playbook.

61. Open the **Marketing Services** workspace from the Navigator panel.

62. Select **Record Pages**.

63. Select **Marketing Design Request Record Page**.

64. Select **Record details**.

65. Select **+ Add a playbook**.

66. Enter `Playbook` in the **Tab name** field.

67. Select **Global Playbook Experience** in the **Playbook experience** field.

68. Select **Add**.

    ![Add the playbook to your workspace.](../image/sns-z-tut-pb-add-pb.png)


## Result

When new Marketing Design Requests are submitted, the Playbook opens in a new tab, providing clear context for the marketing team and ensuring they understand the purpose and importance of each step in the workflow.

![The completed playbook is added to your workspace and opens when new requests are submitted.](../image/sns-z-tut-pb-complete-pb.png)

**Parent Topic:**[ServiceNow Studio tutorial part 2: Automate and improve](../concept/sns-z-tutorial-automate-improve.md)

