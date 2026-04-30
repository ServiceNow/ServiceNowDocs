---
title: Add a workflow with Workflow Studio
description: Use Workflow Studio to build a workflow to standardize the way that the department processes requests. Configure the workflow to execute whenever a department request is submitted. This workflow will request an approval from a group of users designated as Department Request Approvers.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Tutorial part 1: Begin with an MVP, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Add a workflow with Workflow Studio

Use Workflow Studio to build a workflow to standardize the way that the department processes requests. Configure the workflow to execute whenever a department request is submitted. This workflow will request an approval from a group of users designated as Department Request Approvers.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the Navigator panel, expand the Table category and select the **Marketing Design Request** table.

3.  Select **Flows**.

4.  Select **Add new flow**.

5.  In the **Name** field, enter `Marketing design request created`.

6.  Select **Show advanced options**.

7.  In the **Run as** field, select **System user**.

8.  Select **Continue**.

9.  Select **When the record is created** for how to trigger your flow.

10. Select **Continue**.

11. Beneath the trigger, select **Add a node**.

12. Select **Action**.

13. Select **Update Record**.

    ![Add an update record action to your flow.](../image/sns-z-tut-wf-node.png)

14. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) under **Inputs** for the **Record** field.

15. Select **Trigger – Record Created**.

16. Select **Record**.

    ![Use the data pill picker to select Trigger-Record Created > Record.](../image/sns-z-tut-wf-inputs-record.png)

17. In the **Table** field, search for and select the **Marketing Design Request** table.

18. Select **Add field value** under **Fields**.

19. Set Fields to **Assigned to**.

20. Set Value to **David Loo**.

    ![Select Assigned to as the field and David Loo as the assignee.](../image/sns-z-tut-wf-assigned-to.png)

21. Select **Done**.

22. Select **Add a node**.

23. Select **Action**.

24. Select **AES Catalog Builder**.

25. Select **Wait for Condition**.

26. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) on the Action Properties modal, under **Record**.

27. Select **Trigger – Record Created**.

28. Select **Record**.

    ![Use the data pill picker to select the Trigger-Record Created > Record.](../image/sns-z-tut-wf-record-trigger.png)

29. Select the **Marketing Design Request** table in the **Table** field.

30. Select **Edit** under the **Table** field.

31. Set the condition to **\[State\] \[is\] \[Design complete\]**.

32. Select **Done**.

    ![Set the condition to State is Design complete.](../image/sns-z-tut-wf-table-cond.png)

33. Select **Add a node**.

34. Select **Flow Logic**.

35. Select **If**.

    ![Add an If Flow Logic into a new node.](../image/sns-z-tut-wf-flow-logic.png)

36. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) next to **Condition 1**.

37. Select **Trigger – RecordCreated**.

38. Select **Record**.

39. Select **External**.

40. Select **Done**.

    ![Select the Trigger-Record Created>Record>External.](../image/sns-z-tut-wf-flow-logic-prop.png)

41. Select the \(+\) on the true branch.

42. Select **Action**.

43. Select **Ask For Approval**.

    ![Add the Ask for Approval action to your flow.](../image/sns-z-tut-wf-ask-approval.png)

44. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) next to the **Record** field.

45. Select **Trigger – Record Created**.

46. Select **Record**.

    ![Add Trigger-Record Created > Record to the Record field.](../image/sns-z-tut-wf-ask-approval-record.png)

47. Select the **Approve Approval Action**.

48. Change to **Approve or Reject**.

    ![Add an Approve or Reject action to the approval action](../image/sns-z-tut-wf-approval-action.png)

49. Select **Choose approval rule**.

50. Change to **Anyone approves or rejects**.

51. Select **Add Group**.

52. Select **Pick a group**.

53. Search for `brand`.

54. Select **Branding Dept**.

55. Select **Done**.

    ![Add the Branding department group to the approval rule.](../image/sns-z-tut-wf-approval-group.png)

56. Select \(+\) to add FlowLogic after the approval.

57. Select **Flow Logic**.

58. Select **If**.

    ![Add If flow logic to your approval action.](../image/sns-z-tut-wf-approval-flow-if.png)

59. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) next to Condition 1.

60. Select **4 – Ask For Approval**.

61. Select **Approval State**.

    ![Select 4-Ask for approval > approval state for the Condition.](../image/sns-z-tut-wf-approval-cond.png)

62. Select **Select a choice**.

63. Select **Approved**.

64. Select **Done**.

65. Select the \(+\) on the false branch.

66. Select **Action**.

67. Select **Update Record**.

    ![Add the action to update a record under the False option.](../image/sns-z-tut-wf-false-action.png)

68. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) under the **Inputs** section, next to **Record**.

69. Select **Trigger – Record Created**.

70. Select **Record**.

    ![Add a trigger-record created input.](../image/sns-z-tut-wf-trigger-record.png)

71. Select **Add field value** under **Fields**.

72. Select **Select a field**.

73. Search for `state`.

74. Select **State**.

75. Select **Select a choice**.

76. Select **Closed Incomplete**.

    ![Add an option for the Closed Incomplete state.](../image/sns-z-tut-wf-add-field-state.png)

77. Select **Done**.

78. Select \(+\) below the Action you just created.

79. Select **Flow Logic**.

80. Select **End Flow**.

    ![Add the End Flow flow logic.](../image/sns-z-tut-wf-end-flow.png)

81. Select **Done**.

82. Select **Add a node** under the If Action.

    ![Add a node under the If action.](../image/sns-z-tut-wf-add-node.png)

83. Select **Action**.

84. Select **Update Record**.

85. Select the data pill picker \(![](../image/sns-z-tut-data-pill-picker.png)\) in the **Inputs** section, next to **Record**.

86. Select **Trigger – Record Created**.

87. Select **Record**.

88. Select the **Marketing Design Request** table in the **Table** field.

89. Select **Add field value**.

90. Select **Select a field**.

91. Search for `state`.

92. Select **State**.

93. Select **Select a choice**.

94. Select **Closed Complete**.

    ![Select the Closed Complete option.](../image/sns-z-tut-wf-field-closed.png)

95. Select **Done**.

96. Select **Save**.

97. Select **Activate**.


**Parent Topic:**[ServiceNow Studio tutorial part 1: Begin with an MVP](../concept/sns-z-tutorial-begin-with-mvp.md)

