---
title: Record Producer form
description: Description of the fields on the Record Producer form.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Record Producer form

Description of the fields on the Record Producer form.

<table id="table_d3f_4nd_2p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The descriptive name for the record producer.**Note:** The list shows only tables and database views that meet the scope protections for field styles.

</td></tr><tr><td>

Table name

</td><td>

The table in which the record producer creates records.

</td></tr><tr><td>

Active

</td><td>

A check box for making the record producer active. Only active record producers are available to users if they meet the role criteria.

</td></tr><tr><td>

Preview Link

</td><td>

A link that opens a preview of the item.

</td></tr><tr><td>

Post insert script

</td><td>

Script that operates on the submitted record, after the record is inserted in the associated table.**Note:** Post insert script overrides the target record values and record producer template values.

</td></tr><tr><td colspan="2">

Accessibility

</td></tr><tr><td>

Catalogs

</td><td>

The service catalog this record producer belongs to.

</td></tr><tr><td>

Category

</td><td>

The service catalog category this record producer belongs to. When users perform catalog searches, only items that are assigned to a category appear in search results.

</td></tr><tr><td>

View

</td><td>

The CMS view in which the item is visible.

</td></tr><tr><td>

Roles

</td><td>

The roles required to use the record producer.

</td></tr><tr><td>

Availability

</td><td>

The interface the record producer is available from: **Desktop and Classic Mobile**, **Desktop Only**, or **Classic Mobile Only**.

</td></tr><tr><td>

Can cancel

</td><td>

A check box for displaying a **Cancel** button on the record producer. Users can click **Cancel** to cancel the record producer and return to the last-viewed screen

</td></tr><tr><td colspan="2">

What it will contain

</td></tr><tr><td>

Short description

</td><td>

A short summary of the record producer.

</td></tr><tr><td>

Description

</td><td>

The full description of the record producer. You can embed videos, images, links to internal knowledge base \(KB\) articles, and links to external sources of information and instruction documentation.

 The description appears under a **More information** link on the record producer to give users any additional information they need.

</td></tr><tr><td>

Meta

</td><td>

Comma-separated list of tags used to search for the record producer. See [Configure keyword search for catalog items](../task/search-catalog-item.md).

</td></tr><tr><td>

Hide on Service Portal

</td><td>

If selected, the record producer is not available on Service Portal.

</td></tr><tr><td>

Redirect To

</td><td>

Specifies the redirect behavior of the record producer after its generation.Possible values are:

 -   **Generated Task record**: Redirects to the task record created using the record producer.
-   **Catalog Homepage**: Redirects to the service catalog where the order for the record producer is placed.

 The default value is based on the **Specifies the default behavior of record producer after record generation** property in the **Service Catalog** &gt; **Catalog Administration** &gt; **Properties** page.

</td></tr><tr><td>

Script

</td><td>

Scripts that are run to dynamically assign values to specific fields on the created record.

</td></tr><tr><td>

Icon

</td><td>

The small icon that appears on the list of service catalog items. Click the **Click to add** link and upload the photo.

</td></tr><tr><td>

Picture

</td><td>

The picture that appears at the top of the record producer form on the desktop view. Click the **Click to add** link and upload the photo.

</td></tr><tr><td>

Classic Mobile picture

</td><td>

The small picture that appears on the list of service catalog items. Click the **Click to add** link and upload the photo.This field is available when you select the **Classic Mobile** for the **Classic Mobile picture type**.

</td></tr><tr><td>

Classic Mobile picture type

</td><td>

The picture that the mobile interface uses on the list of service catalog items. Select one of the following:-   Desktop: Uses the icon specified in the **Icon** field. Selecting this option hides the **Classic Mobile picture** field.
-   Classic Mobile: Uses the icon specified in the **Classic Mobile picture** field.
-   None: Does not use any picture on the mobile view. Selecting this option hides the **Classic Mobile picture** field.

</td></tr><tr><td colspan="2">

Generated Record Data

</td></tr><tr><td>

Template

</td><td>

Static assignments for fields on the created record.

</td></tr><tr><td colspan="2">

Portal Settings

</td></tr><tr><td>

Hide Attachment

</td><td>

If selected, the **Add attachments** button is not displayed for the record producer.**Note:**

-   Applicable for a catalog item and record producer.
-   An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Hide 'Save as Draft'

</td><td>

If selected, the **Save as Draft** button isn't displayed for the record producer on the portals.

 You can let requesters save a draft of a record producer while requesting it on the portals such as Employee Center and Service Portal, and Now Mobile app. The requesters can access the saved drafts from the My Request widget in the **Drafts** tab on the portals and edit the drafts.

</td></tr><tr><td>

Mandatory Attachment

</td><td>

If selected, adding an attachment is mandatory for the record producer.**Note:** Applicable for a catalog item and record producer.

</td></tr><tr><td class="sub-head" colspan="2">

Universal Request Config

</td></tr><tr><td colspan="2">

This section is available only when the Universal Request plugin \(com.snc.universal\_request\) is activated. For information about this configuration, see [Service Catalog configuration for Universal Request](../concept/ur-catalog-config.md).

</td></tr><tr><td>

UR certified/enabled item

</td><td>

Option to specify that a universal request should also be created along with a task-based record. In the universal request, a reference is created to the associated task-based record, which becomes the primary task of the universal request.

</td></tr><tr><td>

Requires Additional Review

</td><td>

Option to automatically select the **Needs resolution review** check box on the corresponding universal request. For information about the universal request fields, see [Universal Request form](https://www.servicenow.com/docs/access?context=new-ur-record-form&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).The **Requires Additional Review** field appears only when the **UR certified/enabled item** check box is selected.

</td></tr></tbody>
</table>For information about creating record producers, see [Create a record producer](../task/t_DefRecProdInSCat.md).

**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

