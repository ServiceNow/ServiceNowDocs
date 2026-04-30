---
title: Configure a record producer
description: Configure the record producer so that it contains the necessary questions for employee travel requests.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Creating user experiences, App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure a record producer

Configure the record producer so that it contains the necessary questions for employee travel requests.

## Before you begin

Role required: admin or catalog\_admin

## About this task

The second phase in building the user experience for the employee travel request application is to configure the record producer. We configure the record producer so that it contains the necessary questions for employee travel requests, such as travel dates, location, and estimated airfare.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Add a record producer](app-tutorial-add-record-producer.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Configure a record producer](app-tutorial-configure-record-producer.md)

</td></tr></tbody>
</table>This procedure covers the second part of the task demonstrated in the tutorial video. The first part of the procedure is outlined in the previous topic [Add a record producer](app-tutorial-add-record-producer.md).

Follow along to configure the record producer for the employee travel request application.

Create a record producer 

|Timestamp|Section|
|---------|-------|
|0:21|Specify a destination table.|
|0:32|Choose the location.|
|0:42|Create question containers.|
|1:01|Insert questions.|
|3:49|Preview the record producer.|
|3:58|Configure settings.|
|4:05|Select user access.|
|4:10|Review and submit the record producer.|

## Procedure

1.  Ensure that the travel request record producer is open.

    -   To open a record producer from your instance home page, navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**. Then select your application and select the record producer that you want to configure.
    -   To open a record producer that you have created, select **Edit record producer**.
    When your record producer is open, it appears in the canvas space.

    ![Your record producer is open in the canvas space.](../image/app-tutorial-record-producer-open.png)

2.  Edit or add details about the record producer in the **Item name** or **Short description** fields.

3.  Select **Continue to Destination** to specify the table in which the record producer creates records.

4.  Enter `Travel request` in the **Record submission table** field, then select the employee travel request table from the list.

    By setting the travel request table as the destination table, travel requests submitted through the record producer become records in the employee travel request table.

5.  Select **Continue to location** to specify the location of your record producer.

    **Note:** Location determines where users can find the record producer. You can locate your record producer in a catalog, such as the Service Catalog, which is a set of business and technical products, services, and offerings that users can order. You can also locate your record producer with a topic, such as a knowledge base article. For more information about locations for record producers, see [Creating or editing catalog item template](https://www.servicenow.com/docs/access?context=create-cat-item-template-cat-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    In our tutorial, we locate our record producer in the Service Catalog, so that employees can access the employee travel request form easily.

6.  In the **Catalogs** card, select **Browse**.

7.  From the **Available options** list, select **Service Catalog** and use the move icon \(![Move icon](../image/app-tutorial-move-right-icon.png)\) to add it to the **Selected catalogs** list.

8.  Select **Save selections**.

9.  Select **Continue to questions** to start building the form questions.

10. Create containers, or sections, for the form questions.

    1.  Select the arrow icon \(![Arrow icon](../image/app-tutorial-dropdown-arrow-icon.png)\) in the **Insert new question** button to expand the menu of available question types.

    2.  Select **Single column container** from the list.

    3.  In the **Title** field, enter `General Information`.

    4.  Select **Submit**.

    5.  Repeat the procedure in steps a-d to create as many containers as needed.

    In our tutorial, we create another container for our form questions with the following specifications:

    |Container type|Title|
    |--------------|-----|
    |Two column container|`Travel Details`|

11. Add a question to the form.

    **Note:** You can build different types of questions for your record producer. To see the full list of available question types in Catalog Builder, see [Create a question for a catalog item in Catalog Builder](https://www.servicenow.com/docs/access?context=create-question-cat-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    In our tutorial, we create several questions to collect details about employees' travel requests.

    1.  In the correct question container, hover over the plus icon \(![Add icon](../image/plus-icon.png)\), then select **+ Insert**.

        In our tutorial, we insert this question in the General Information container.

    2.  Select **New question**.

    3.  Select and enter the following values for the new question.

        |Question type|Question subtype|Map to specific field on table|Table field|Question label|Name|Mandatory|
        |-------------|----------------|------------------------------|-----------|--------------|----|---------|
        |**Choice**|**Dropdown \(fixed values\)**|Yes|**Reason for travel**|`What is the reason for travel?`|`reason_for_travel`|Yes|

    4.  Select **Continue to Choices** to complete additional configurations for the question.

    5.  In the **Available choices** section, hover over the plus icon \(![Add icon](../image/plus-icon.png)\), then select **+ Insert**.

    6.  In the **Display name** field, enter `Customer meeting`.

    7.  Repeat the process in steps e and f to add additional choices.

        In our tutorial, we add two additional choices. The following list includes the names for each additional choice that we add:

        -   `Internal meeting`
        -   `Training`
    8.  Select **Insert question**.

12. Repeat the procedure outlined in step 11 to create as many questions as needed.

    In our tutorial, we add the following additional questions to our form in the Travel Details container:

    1.  We add a question to determine the employee's departure date.

        |Question type|Question subtype|Map to specific field on table|Table field|Question label|Name|Mandatory|Additional configurations|
        |-------------|----------------|------------------------------|-----------|--------------|----|---------|-------------------------|
        |**Date / Time**|**Date**|Yes|**Departure date**|`When are you leaving?`|`departure_date`|Yes|None, select **Insert question**.|

    2.  We add a question to determine the employee's return date.

        |Question type|Question subtype|Map to specific field on table|Table field|Question label|Name|Mandatory|Additional configurations|
        |-------------|----------------|------------------------------|-----------|--------------|----|---------|-------------------------|
        |**Date / Time**|**Date**|Yes|**Return date**|`When are you returning?`|`return_date`|Yes|None, select **Insert question**.|

    3.  We add a question to determine where the employee is traveling from.

        |Question type|Question subtype|Map to specific field on table|Table field|Question label|Name|Mandatory|Additional configurations|
        |-------------|----------------|------------------------------|-----------|--------------|----|---------|-------------------------|
        |**Choice**|**Record reference**|Yes|**Travel from**|`Where are you traveling from?`|`travel_from`|Yes|Select **Source table** &gt; **Airport**.|

    4.  We add a question to determine where the employee is traveling to.

        |Question type|Question subtype|Map to specific field on table|Table field|Question label|Name|Mandatory|Additional configurations|
        |-------------|----------------|------------------------------|-----------|--------------|----|---------|-------------------------|
        |**Choice**|**Record reference**|Yes|**Travel to**|`Where are you traveling to?`|`travel_to`|Yes|Select **Source table** &gt; **Airport**.|

    5.  We add a question to determine the estimated cost of the travel.

        |Question type|Question subtype|Map to specific field on table|Table field|Question label|Name|Mandatory|Additional configurations|
        |-------------|----------------|------------------------------|-----------|--------------|----|---------|-------------------------|
        |**Text**|**Single line**|Yes|**Estimated airfare**|`What is your estimated airfare?`|`estimated_airfare`|Yes|Select **Text validation** &gt; **Number**.|

13. Preview your form by selecting **Preview**.

14. When you’re ready to finalize your form, select either **Continue to settings** or the **Settings** tab in the side panel.

15. Select the check box next to any of the following portal settings.

    In our tutorial, we select the check box next to **Hide 'Add to wishlist' button** and **Hide attachment button**. You can select or deselect these settings in your record producer.

    -   To prevent users from saving your record producer item to their wish list, select the check box next to **Hide 'Add to wishlist' button**.
    -   To hide the component that enables users to provide attachments in the record producer form, select the check box next to **Hide attachment button**.
    -   To require users to provide attachments, such as receipts or screenshots for service requests, select the check box next to **Make attachment mandatory**.
16. Select **Continue to access**.

17. Choose from the following options to define which users or groups have access to the form.

    **Important:** If you don’t select any users or groups to grant or deny access, your form is available to everyone.

    In our tutorial, we don’t grant or deny access to any users or groups.

    -   To make the form available to specific users or groups, select **Browse** in the **Available for** card, then search for the users or groups that you want to grant access to. Move the users or groups from the **Available options** list to the **User criteria granted access** list using the move icon \(![Move icon](../image/app-tutorial-move-right-icon.png)\).
    -   To make the form unavailable for certain users or groups, select **Browse** in the **Unavailable for** card, then search for the users or groups that you want to deny access to. Move the users or groups from the **Available options** list to the **User criteria denied access** list using the move icon \(![Move icon](../image/app-tutorial-move-right-icon.png)\).
18. Select **Continue to review and submit** to review and finalize your form.

19. Select **Submit**.


## Result

Your record producer is configured and ready for testing.

## What to do next

Continue building the employee travel request application by proceeding to the next step: [Adding logic and automation](../concept/app-tutorial-logic-automation-layer.md).

