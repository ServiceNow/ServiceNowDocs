---
title: Working on a case through contact tracing visualization
description: The contact tracing visualization in a case is a graphical representation of the affected user and potentially exposed contacts.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Managing cases to follow up with potentially exposed contacts, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Working on a case through contact tracing visualization

The contact tracing visualization in a case is a graphical representation of the affected user and potentially exposed contacts.

## About Contact Tracing Visualization

The contact tracing visualization available on the case form provides multiple options based on the status of the potentially exposed contacts. While working on a case, the case manager can use this visualization to view all potentially exposed contacts added to the case, their status, drill down to the next two levels of potential exposures , and take action as needed.

![Contact tracing visualization area of the Case form.](../image/contact-tracing-visualization-5.png "Contact tracing visualization")

Each card represents a potentially exposed contact who might have been potentially impacted by the affected user.You can view how many potentially exposed and infected contacts users have for their current case \(where they are the reported person\) and the totals for other active cases they are in.

**Note:** The totals for other active cases do not include numbers from a user's current case.

For example, consider a sample employee's case, Employee A. The employee has five potentially exposed contacts and one of them is infected. One of Employee A's potentially exposed contacts, Employee B, has three potentially exposed contacts from the current case. None of Employee B's contacts are infected. Employee B is also a potentially exposed contact in two other cases. Employee B's card provides the total number of potentially exposed contacts in those cases and how many are infected.

To review details about a potentially exposed contact's current case, click **Show Details**. To navigate to cases in which the contact is a potentially exposed contact, click **other active cases**.

**Tip:** Use the **Filter** option to view a filtered list of cards, such as by status or the source of exposure.

## Visualization options

Select a card to view various options on the card based on the status of the exposed contact.

You can change the health status or create case tasks for multiple potentially exposed contacts in one step. Select all cards by clicking **Select All**, or select a few cards by pointing to a card and selecting the check box. Updating the health status of an exposed contact updates their health status and outcome in all open case tasks in which they are included as an exposed contact.

<table id="table_xpt_vwp_z4b"><thead><tr><th>

Status of the exposed contact

</th><th>

Options available on the card

</th></tr></thead><tbody><tr><td>

**Under investigation** The user is being contacted about the health status.

</td><td>

-   View basic details of the user such as email ID and location.
-   View how many potentially exposed and infected contacts users have for their current case and any other active cases the user is in.
-   Navigate to a user's other active cases.
-   Create a task for follow-up.
-   Create a case.
-   View potentially exposed contacts who might have been in contact with the selected user.

</td></tr><tr><td>

**Infected** The user has been classified as positive for a condition, such as COVID-19.

</td><td>

-   View basic details of the user such as email ID and location.
-   View how many potentially exposed and infected contacts users have for their current case and any other active cases the user is in.
-   Navigate to a user's other active cases.
-   Create a task for follow-up.
-   Create a case if no case has been created yet.
-   View the case if a case has been already created.
-   View potentially exposed contacts who might have been in contact with the selected user.
-   Change the status.

</td></tr><tr><td>

**Cleared** The user has been reported safe.

</td><td>

-   View basic details of the user such as email ID and location.
-   View how many potentially exposed and infected contacts users have for their current case and any other active cases the user is in.
-   Navigate to a user's other active cases.
-   Create a task for follow-up.
-   Create a case if no case has been created yet.
-   Change the status.

</td></tr></tbody>
</table>## Vaccination statuses in contact tracing visualization

Organizations with Contact Tracing and the Vaccination Status application can view vaccination statuses on the **Exposed Contacts** list and contact tracing visualization. The **Vaccinated** label on a card indicates that the user is vaccinated.

For more information, see [Configure contact tracing visualization to show vaccination status](../task/add-vaccination-status-to-case-visualization.md).

![Contact tracing visualization area with examples of vaccinated contacts.](../image/contact-tracing-visualization-vaccine-status.png "Potentially exposed contacts with Vaccinated status")

<table id="table_cqt_vwp_z4b"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vaccinated status

</td><td>

Case managers with the Vaccination Status sn\_imt\_vaccine.vaccine\_profile\_reader role can see the following:

-   The **Vaccinated** status that displays for vaccinated contacts.
-   The **Vaccinated** column appears in the **Exposed Contacts** list with values of **True** or **False**.

</td></tr><tr><td>

Vaccination filter

</td><td>

Case managers with the sn\_imt\_vaccine.vaccine\_profile\_reader role can filter exposed contacts based on their vaccination status. In the contact tracing visualization, click **Filter**. Select the **Vaccinated** check box to hide contacts who are not vaccinated. Clear the check box to remove the filter and show all contacts.**Note:** The **Vaccinated** filter is visible to case managers without the sn\_imt\_vaccine.vaccine\_profile\_reader role but it does not reveal any vaccination data. Selecting the check box \(without the role\) hides all contacts as if none of them were vaccinated because the user does not have the necessary permissions to see vaccination statuses.

</td></tr></tbody>
</table>**Parent Topic:**[Managing cases to follow up with potentially exposed contacts](../concept/exposure-case-management.md)

