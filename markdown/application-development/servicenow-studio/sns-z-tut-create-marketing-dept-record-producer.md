---
title: Create the Marketing department record producer
description: Create a record producer for the Marketing department using ServiceNow Studio.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Tutorial part 1: Begin with an MVP, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Create the Marketing department record producer

Create a record producer for the Marketing department using ServiceNow Studio.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select **Create** &gt; **File** &gt; **User Interface** &gt; **Record Producer**.

3.  Select **Continue**.

4.  Select **AES Record Producer**.

5.  In the **Item Name** field, enter `Marketing Design Request`.

6.  Select **Continue to Destination**.

7.  In the **Record submission table** field, search for an select the **Marketing Design Request** table.

8.  Select **Continue to Location**.

9.  Select **Browse** to view the catalogs.

10. Move **Service Catalog** from **Available options** to **Selected catalogs**.

11. Select **Save selections**.

    ![For Location, browse and move Service Catalog to the selected catalogs box.](../image/sns-z-tut-rp-location.png)

12. In the **Categories** section, select **Browse**.

13. Move **Departmental Services** from **Available options** to **Selected categories**.

14. Select **Save selections**.

    ![Move departmental services from the available options to selected categories.](../image/sns-z-tut-rp-departmental-svcs.png)

15. Select **Continue to Questions**.

16. Select **Insert new question**.

17. Set the **Question type** to **Text**.

18. Set the **Question subtype** to **Single-line**.

19. Select **Map to a specific field on the table**.

20. Choose **Project name** for the Table field.

21. In the **Question label** field, enter `Project name`.

22. Select **Mandatory**.

    ![Add details to the questions form and make it mandatory.](../image/sns-z-tut-rp-questions.png)

23. Select **Insert question** at the bottom of the screen.

24. Repeat the same steps to insert the following additional questions.

    |Question type|Question subtype|Map to specified field on table|Table field|Question label|Name|Mandatory|
    |-------------|----------------|-------------------------------|-----------|--------------|----|---------|
    |Text|Multi-line|X|Description|Description|`description`|Yes|
    |Text|Multi-line|X|Design copy|Design copy|`design_copy`|No|
    |Text|Multi-line|X|Special instructions|Special instructions|`special_instructions`|No|
    |Toggle|Check box|X|External|External|`external`|No|

25. Select **Insert new question** and fill in the form with the following specifications.

    |Field|Selection|
    |-----|---------|
    |Question type|Choice|
    |Question subtype|Dropdown \(fixed values\)|
    |Map to a specific field on the table|Select this option|
    |Table field|Media type|
    |Question label|Media type|
    |Mandatory|Select this option|

    ![Configure settings for the Media Type question.](../image/sns-z-tut-rp-media-type.png)

26. Select **Continue to Choices**.

27. Select **Include none** choice.

28. Select the \(+\) to add to the **Available Choices**.

29. In the **Display name** field, enter `Print`.

30. In the **Value** field, enter `print`.

31. Select the \(+\).

32. In the **Display name** field, enter `Digital`.

33. In the **Value** field, enter `digital`.

    ![Add print and digital options for the media type.](../image/sns-z-tut-rp-media-options.png)

34. Select **Insert question** at the bottom of the screen.

35. Select **Review and submit**.

36. Select **Submit**.


**Parent Topic:**[ServiceNow Studio tutorial part 1: Begin with an MVP](../concept/sns-z-tutorial-begin-with-mvp.md)

