---
title: Universal Request properties
description: Administrators can use Universal Request properties to determine and configure the application behavior.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Universal Request reference, Universal Request, Employee Service Management]
---

# Universal Request properties

Administrators can use Universal Request properties to determine and configure the application behavior.

Navigate to **Universal Request** &gt; **Administration** &gt; **Properties** to view and edit the properties.

<table id="table_tdj_glz_mlb"><thead><tr><th>

Property

</th><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Copy Universal Request

</td></tr><tr><td>

Enable copy universal request feature

</td><td>

sn\_uni\_req.com.snc.universal\_request.copy.enable

</td><td>

Copies the details of an existing Universal Request to a new record.

</td></tr><tr><td>

Copy attachments from originating universal request

</td><td>

sn\_uni\_req.com.snc.universal\_request.copy.attach

</td><td>

Copies an attachment of an UR record to a target record.

</td></tr><tr><td>

List of attributes \(comma-separated\) that will be copied from the originating universal request

</td><td>

sn\_uni\_req.com.snc.universal\_request.copy.attributes

</td><td>

List of attributes that will be copied from the originating Universal Request record.

</td></tr><tr><td class="sub-head" colspan="3">

Transfer type

</td></tr><tr><td>

Select the transfer type to determine how the primary ticket is handled

</td><td>

sn\_uni\_req.transfer\_type

</td><td>

Determines how the primary ticket is handled based on the selection.-   **Universal\_request:** If this transfer type is selected, then the primary ticket is transferred back to UR and UR assignment group is changed based on the **Service** selected during transfer. The primary ticket is handled based on the transfer reason and no new primary ticket is created.
-   **Department only:** If your organization has a department level routing agent group to handle requests, then select this transfer type. When this transfer type is selected, UR is directly transferred to the department level routing group, and a general inquiry primary ticket is created.
-   **Department:** If this transfer type is selected, then based on the **Transfer Action** and **Service** selected, the UR is transferred back to the service level or department assignment group. The primary ticket is handled based on the transfer reason.

**Note:** If the **Service** is disabled, then a general primary task is created for the selected department.

-   **Service:** If this transfer type is selected, then based on the **Action** and **Service** selected, the UR is transferred back to the service level or department assignment group. The primary ticket is handled based on the transfer reason. For `Transfer to department` transfer action:
    -   If no service is selected, a general inquiry primary ticket is created for the selected department.
    -   If a specific service is selected, a primary ticket is created for the selected service.

</td></tr><tr><td class="sub-head" colspan="3">

Associated Ticket

</td></tr><tr><td>

Select the type to determine how the associated ticket creation is handled

</td><td>

sn\_uni\_req.associated\_ticket

</td><td>

Determines how the associated ticket is handled based on the selection.-   **Department only:** If your organization has department level service set configurations of Universal Request, then select this type. When this mode of associated ticket creation is selected, primary ticket agents are able to create associated tickets for the departments configured with UR.
-   **Service:** When this mode of associated ticket creation is selected, primary ticket agents are able to create associated tickets for the services or departments configured with UR.
-   **False**: This disables the associated ticket creation functionality.

</td></tr><tr><td class="sub-head" colspan="3">

Portal

</td></tr><tr><td>

Portal suffix to which the UR link is redirected.

</td><td>

sn\_uni\_req.universal\_request\_portal

</td><td>

The default portal to which all the UR links are redirected.

</td></tr><tr><td class="sub-head" colspan="3">

Predictive Intelligence

</td></tr><tr><td>

Enable universal request auto categorization

</td><td>

sn\_uni\_req.auto\_categorization

</td><td>

Enables the application to use the Universal Request Categorization solution for UR to predict the assignment group and create service level tickets.

</td></tr><tr><td>

The minimum confidence level required for the Universal Request auto categorization predictive intelligence suggestions to be considered

</td><td>

sn\_uni\_req\_ml.auto\_categorization.min\_confidence

</td><td>

Determines the minimum confidence level required for the Universal Request application to provide auto categorization suggestions using the predictive intelligence solution.

</td></tr><tr><td>

Enable to auto-restrict requests with sensitive information

</td><td>

sn\_uni\_req\_ml.sensitive\_detection

</td><td>

Identifies and automatically marks the UR as sensitive if the request has sensitive information in the short description or description.

</td></tr><tr><td>

The minimum confidence level required to automatically mark Universal Requests containing sensitive information as restricted

</td><td>

sn\_uni\_req\_ml.sensitive\_detection.min\_confidence

</td><td>

Determines the minimum confidence level required for the Universal Request application to mark Universal Requests containing sensitive information as restricted.

</td></tr><tr><td>

Enable to view similar closed Universal Request recommendations

</td><td>

sn\_uni\_req.similar\_closed\_universal\_request

</td><td>

Enables the application to use the Universal Request Similarity solution for UR to search and display closed Universal Requests that are similar to the UR created.

</td></tr><tr><td class="sub-head" colspan="3">

Other Properties

</td></tr><tr><td>

Enable service transition comments while creating department requests from Universal Request

</td><td>

sn\_uni\_req.universal\_request\_show\_service\_transition

</td><td>

Enables or disables the visibility of additional comments to the requester that mentions the details of the department transition.

</td></tr><tr><td>

Define the fields to automatically map for UR mapping configuration

</td><td>

sn\_uni\_req.com.snc.universal\_request.transfer.auto.map

</td><td>

The list of fields that must be automatically mapped with UR fields for direct transfer between departments.

</td></tr><tr><td>

Define parent tables that should not create a UR for record producers

</td><td>

sn\_uni\_req.com.snc.ur.record\_producer.parent.exclude

</td><td>

Excludes the specified parent tables when a UR is created from a record producer.

</td></tr><tr><td>

General email address for Universal Requests

</td><td>

sn\_uni\_req.ur\_email

</td><td>

Creates a universal request when an email is received in the general email address mailbox.**Note:** You can add multiple email addresses with comma-separated .

</td></tr><tr><td>

Enable Request \(RITM\) integration with Universal Request

</td><td>

sn\_uni\_req.com.snc.ur.request\_integration

</td><td>

Creates a universal request when a request is submitted from a catalog item or record producer.

</td></tr></tbody>
</table>**Parent Topic:**[Universal Request reference](ur-reference-topic.md)

