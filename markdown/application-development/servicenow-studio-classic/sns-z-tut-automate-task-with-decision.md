---
title: Automate a manual task with Decision Builder
description: Decouple business decisions from application logic by adding a decision table to your application in ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-z-tut-automate-task-with-decision.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Tutorial part 2: Automate and improve, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Automate a manual task with Decision Builder

Decouple business decisions from application logic by adding a decision table to your application in ServiceNow Studio.

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select **Create** &gt; **File**.

3.  Select **Automation** &gt; **Decision table**.

4.  Select **Continue**.

5.  In the **Name** field, enter `Choose graphic designer`.

6.  Select **Build decision table**.

7.  Next to **Inputs**, select **\(+\) Add**.

8.  On the form, fill in the fields.

    |Field|Entry|
    |-----|-----|
    |Label|Request|
    |Type|Reference|
    |Table|Marketing Design Request|
    |Mandatory|Toggle off|

    \[Omitted image "sns-z-tut-dec-table.png"\] Alt text: Create a new input.

9.  Select **Add condition column**.

10. Select **\(+\) Add condition column**.

11. Enter `Is external` for the Condition column label.

12. On the form, fill in the fields.

    |Field|Entry|
    |-----|-----|
    |Data to evaluate|Field|
    |Field|External field on the Marketing Design Request table|

    \[Omitted image "sns-z-tut-condition-col.png"\] Alt text: Fill in the form for a new condition column.

13. Select **Done**.

14. Select **\(+\) Add result column**.

15. On the form, fill in the fields.

    |Field|Entry|
    |-----|-----|
    |Result column label|Graphic designer|
    |Result type|Reference|
    |Result table|User \[sys\_user\]|

16. Select **Done**.

17. Select in the line of the empty **Is external** condition.

    \[Omitted image "sns-z-tut-condition-col-2.png"\] Alt text: Select in the empty line of the condition column.

18. Select **true**.

19. Select **OK**.

20. Set the true result to **Bud Richman**.

21. Set the Default result to **Howard Johnson**.

    \[Omitted image "sns-z-tut-condition-col-3.png"\] Alt text: Set true and default results for the condition column.

22. Select **Save**.

23. Select **Publish**.

24. Confirm and select **Publish**.

25. In the Navigator panel, return to the Marketing Design Request table.

26. Select **Flows**.

27. Select the **Marketing design request created** flow.

    \[Omitted image "sns-z-tut-table-flow.png"\] Alt text: On the Flows tab, select the marketing design request created flow.

28. Select the **\(+\)** directly below the Trigger.

29. Select **Flow Logic**.

30. Select **Make a decision**.

    \[Omitted image "sns-z-tut-flow-dec.png"\] Alt text: Create flow logic with the Make a decision action.

31. Set **Decision Table** to **Choose graphic designer**.

32. Toggle **Use Branches** off.

33. Select the **Request** data pill picker icon \(\[Omitted image "sns-z-tut-data-pill-picker.png"\] Alt text:\).

34. Select **Trigger – Record Created**.

35. Select **Record**.

    \[Omitted image "sns-z-tut-flow-pick.png"\] Alt text: Select the data pill picker and select trigger-record created.

36. Select **Done**.

37. Select the ellipsis on the **Update** action immediately following the Make a decision action.

38. Select **View**.

    \[Omitted image "sns-z-tut-flow-ellipses.png"\] Alt text: Select View on the Update action.

39. Select the **Fields** data pill picker.

    \[Omitted image "sns-z-tut-fields-picker.png"\] Alt text: Select the Fields data pill picker.

40. Select **1 – Make a Decision** &gt; **Decision Table Multiple Result Record** &gt; **Result elements** &gt; **Graphic designer**.

    \[Omitted image "sns-z-tut-dec-table-path.png"\] Alt text: Select each option in the Make a decision action, ending with the Graphic designer selection.

41. Select **Done**.

42. Select **Save**.

43. Select **Activate**.

44. Confirm your selection by selecting **Activate** again.


**Parent Topic:**[ServiceNow Studio tutorial part 2: Automate and improve](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-z-tutorial-automate-improve.md)

