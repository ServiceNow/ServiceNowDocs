---
title: Tutorial part 3: Create a table by uploading a PDF into ServiceNow Studio
description: Create a table in your application by adding a PDF into ServiceNow Studio.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 3: Create a table by uploading a PDF into ServiceNow Studio

Create a table in your application by adding a PDF into ServiceNow Studio.

## Before you begin

Download the PDF for this part of the tutorial: [We Volunteer Survey](https://drive.google.com/file/d/1BwvG8zFzlQdwYMBpGpxP_RS2Rz5ycp5G/view?usp=sharing)

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to your application dashboard tab for the We Volunteer app.

2.  Select **Create**.

3.  In the Create file modal, select **Table \(sys\_db\_object\)**.

4.  Select **Continue**.

5.  Select **Upload a PDF**.

6.  Select **Continue**.

7.  Drag a PDF onto your browser screen or browse for the PDF to upload, and upload the We Volunteer survey template PDF.

8.  Select **Continue**.

    **Note:** It may take a couple minutes to extract the content from the PDF.

9.  Enter the following table details:

    -   Table label: Volunteer Survey Response
    -   Auto number: True
    -   Prefix: VSR
10. Select **Continue**.

11. Set the following permissions for each default role.

    -   Admin role: Select **All**
    -   User role: Select **Read**
12. Select **Continue**.

13. Select **Go to PDF extractor**.

    **Note:** The PDF extractor opens with the PDF contents on the left side and the tables and fields list on the right. You must select each element from the PDF that you want to bring into the table.

    ![The PDF extractor opens with the PDF on one side of the screen and the table on the other.](../image/sn-studio-tutorial-pdf-extract.png)

14. Extract the first question by selecting it in the PDF.

    A modal opens with the label populated with the question. You can edit the details of the question here.

15. Select **Field Type** and select **Choice** from the dropdown list.

16. Select **Choice Type**, and select **Dropdown --without-- None**.

17. Select each check box on the PDF and select **Add** after each one.

    ![Add each question and answer set to the table by selecting them from the PDF.](../image/sn-studio-tutorial-pdf-questions.png)

18. Select **Add field**.

19. Select the next question on the form to add it to your table.

20. Repeat steps 15-17 for the second question.

21. For the third question, select it to bring up the editing modal and select **True/False** as the field type.

22. Select **Add field**.

23. Select **Add new field**.

24. Repeat steps 21-22 for questions 4 and 5.

25. Select the last two questions one at a time and select **Add field**.

26. Select **Save**.

27. In the File Navigator, expand the **Data** category, and select **Table**.

28. Select **Open list**.

    A list of all the tables in your instance opens in a new integrated tab.

29. Under the Label column, select **Search**.

30. Enter `Location`, and press **Enter**.

31. Select the Location \[cmn\_location\] table from the search results.

32. Select **Add new field** and use the following specifications:

    -   Column Label: Type
    -   Type: Choice
    -   Choice Type: Dropdown with --None--
    -   Choices: Event, Others
33. Select **Done**.

34. Select **Save**.


**Parent Topic:**[ServiceNow Studio tutorial](../concept/lab-sns-lab-guide.md)

