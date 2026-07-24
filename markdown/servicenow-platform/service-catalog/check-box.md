---
title: Check box
description: The check box variable lets you enable and disable options by selecting and clearing it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/check-box.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Check box

The check box variable lets you enable and disable options by selecting and clearing it.

To make a check box mandatory, select the **Selection Required** option when you create the variable. For example, use this option to require users to select the **I agree** check box for an agreement form. If users try to submit the agreement form without selecting the check box, an alert message is displayed to tell users that they must select the check box.

A group of check box variables is created when you create consecutive check box variables. These check box variables are sorted by their order within the group. If you want to define a custom label for the group of check boxes, create a label variable at the start of the consecutive check box variables. The label is then considered a part of this group and acts a label of the group. If there is no custom label, check boxes are grouped under an **Options** label by the application.

In a group of check box variables:

-   If any check box variable in the group is mandatory, the entire group becomes mandatory irrespective of the visibility of the mandatory check box variable. An asterisk \(\*\) is then displayed next to the group label and you must select at least one of these check boxes.
-   Hiding the label hides the entire group.
-   If all other check box variables of a mandatory check box group are hidden and not selected, the following scenarios are applicable:
    -   The group remains mandatory as long as there is one check box in the group that is visible and not selected.
    -   The last check box of this group cannot be hidden if it is not selected.

In Service Portal, to make a group of check box variables mandatory, set at least one of the check box variables as mandatory. While defining the label for a group of check boxes, setting a label mandatory does not make the group of check box variables mandatory.

In catalog builder, the following scenarios are applicable:

-   If there are two consecutive check boxes, then a virtual container is created for a group of check boxes. Only check box variable types can be added inside the group
-   Even if a check box variable is added immediately after a group of check boxes, it is automatically added to the group.

Under the **Type Specifications** tab, you can specify the price in different currency types. Also, you can configure the price in the following pricing models:

-   Calculated
-   Fixed
-   Multiple

For information on the pricing models, see [Price fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/price-fields.md) .

\[Omitted image "VariableCheckBoxG.png"\] Alt text: A check box variable

**Parent Topic:**[Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/r_VariableTypes.md)

**Related topics**  


[Attachment]()

[Break]()

[Container start, container split, and container end]()

[Date, Date and time, and Duration]()

[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/email.md)

[HTML]()

[IP Address]()

[Label]()

[List collector]()

[Lookup multiple choice]()

[Lookup select box]()

[Custom and Custom with label]()

[Masked]()

[Multi-line text]()

[Multiple choice]()

[Numeric scale]()

[Reference]()

[Requested for]()

[Rich Text Label]()

[Select box]()

[Single-line text]()

[UI page]()

[URL]()

[Wide single-line text]()

[Yes/No]()

[Variable support in various channels]()

