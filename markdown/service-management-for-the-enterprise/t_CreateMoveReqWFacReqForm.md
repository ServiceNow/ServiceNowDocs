---
title: Create a move request with the move request form
description: Facilities staff members can create move requests using the move request form.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Facilities move requests, Facilities move management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Create a move request with the move request form

Facilities staff members can create move requests using the move request form.

## Before you begin

Role required: facilities\_read

## About this task

Associating a CI to a move request helps your facilities team understand which services or assets are affected in a move. You can also use this form to include extra comments and work notes for the move request.

## Procedure

1.  Navigate to **All** &gt; **Facilities Move** &gt; **Requests** &gt; **Create New**.

2.  Fill in the fields on the form, as appropriate.

<table id="table_rbb_2xm_xq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An auto-generated number that identifies the move request record.

</td></tr><tr><td>

Priority

</td><td>

The priority that describes the importance of this request. By default, all requests are set to **4-Low**.

</td></tr><tr><td>

Move date

</td><td>

Select a date for the move request to be performed.

</td></tr><tr><td>

State

</td><td>

The state that describes what work stage this request is in. By default, all requests are set to **Open**.

</td></tr><tr><td>

Opened

</td><td>

Auto-filled with the date and time the request was opened.

</td></tr><tr><td>

Assignment group

</td><td>

Select the group from which an agent is assigned to the request. You can select only assignment groups associated with the service management application you are using.

**Note:** If you selected the **Use the dispatch queue** option on the Facilities Management Configuration screen, only users with the Dispatcher role can edit this field. If you did not select the **Use the dispatch queue** option, all users except those users with the Basic and Initiator roles can edit this field.

</td></tr><tr><td>

Requested by

</td><td>

The name of the requester.

</td></tr><tr><td>

Assigned to

</td><td>

Select the agent to assign the request to. If you already selected an assignment group, you can only select agents who belong to that group. If email notifications are enabled on your instance, a built-in email notification automatically sends an email to this user when you save the request record.

**Note:**

-   If you selected the **Use the dispatch queue** option on the Facilities Management Configuration screen, only users with the Dispatcher and Agent roles can edit this field. If you did not select the **Use the dispatch queue** option, all users except those users with the Basic and Initiator roles can edit this field.
-   If you selected an assignment group and want to assign the work to a new user, click the reference lookup icon next to **Assigned to**, click **New**, and create a user. Be aware, however, that you must navigate to **User Administration &gt; Groups** and add the user to the assignment group before the request can be assigned.


</td></tr><tr><td>

Template

</td><td>

\[Required\] The workflow template to be used for the fulfillment of this request.

</td></tr><tr><td>

Short description

</td><td>

\[Required\] A brief summary of the request. Optionally, you can click the search knowledge icon to view articles in the knowledge base relating to this product model, plan, or CI. Doing so could provide a solution related to the reason you are submitting this request.

</td></tr><tr><td class="sub-head" colspan="2">

Move Details

</td></tr><tr><td>

User to be moved

</td><td>

Select a name if you are opening this request on behalf of another user.

</td></tr><tr><td>

From location

</td><td>

The location from which the user is moved.

</td></tr><tr><td>

To location

</td><td>

The location to which the user is moved.

</td></tr><tr><td>

Requested move date

</td><td>

Select a date for the move request to be performed.

</td></tr><tr><td>

Boxes

</td><td>

Select this check box if the user requires that boxes be delivered before their move.

</td></tr><tr><td>

Security badge update

</td><td>

Select this check box if the user being moved requires changes in location access.

</td></tr><tr><td>

Move assets

</td><td>

Select this check box if the user being moved requires assets to be moved along with them.

</td></tr><tr><td class="sub-head" colspan="2">

Work Notes

</td></tr><tr><td>

Description

</td><td>

A detailed description of the request. The description is always visible to the submitter. Therefore, if you add or modify the description for a request that another user submitted, the user is able to see the changes.

</td></tr><tr><td>

Work notes

</td><td>

Extra notes that you want to share between users who can access the request form. A user who submits the request through the service catalog cannot see the work notes.

</td></tr></tbody>
</table>    **Note:** To specify an **Assignment group**, and assign the work to a user not in your user table, click the magnifying glass icon in the **Assigned to** field. Then click **New**, and create the user record. Be aware, however, that the new user is not recognized.

3.  Continue with one of the following options.

    |Option|Action|
    |------|------|
    |**To assign the move request to yourself**|Click **Assign to me**.|
    |**To initiate the workflow**|Click **Ready for Work**.|
    |**To save the form without initiating workflow**|Click **Save**.|


**Parent Topic:**[Facilities move requests](../concept/c_FacMoveRequests.md)

