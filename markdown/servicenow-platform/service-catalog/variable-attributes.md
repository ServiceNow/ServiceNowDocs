---
title: Service Catalog variable attributes
description: There are a few Service Catalog variables support specific attributes to define the behavior and restrictions for variables.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a service catalog variable, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog variable attributes

There are a few Service Catalog variables support specific attributes to define the behavior and restrictions for variables.

In the Catalog variable form, under the **Type Specifications** tab, you can specify the variable attributes in the **Variable attributes** field.

**Note:**

-   You can enter multiple attributes for a variable type by separating each with a comma.
-   You can enter multiple values for an attribute by separating each with a semicolon.
-   If you don't see the **Variable attributes** field, enable the **Show attributes when Type is One of Certain Values** UI policy.
-   Pre-selected values are not cleared automatically when the dependent variable value changes when using an attribute or reference qualifier. Create a client script to clear the values based on your needs and the needs of your customer.

## Variable attributes

-   **allowed\_extensions**

    Specifies a list of allowed file types. For example, `allowed_extensions=txt;pdf`.

    Applicable variables: Attachment

-   **barcode**

    Specifies if the barcode can be scanned using the mobile camera for identifying a variable value of a catalog item. For example, `barcode=true`.

    Applicable variables: Single Line Text

-   **max\_file\_size**

    Specifies the maximum file size in MB. For example, `max_file_size=2`.

    Applicable variables: Attachment

-   **glide\_list**

    Changes the list collector interface from slushbucket to glide list.

    Applicable variables: List collector

-   **is\_searchable\_choice**

    If set to **true**, enables you to search for and select the required value for the variable. For example, `is_searchable_choice=true`.

    **Note:**

    -   For Lookup select box, a default value is available at the page load itself.
    -   This attribute is not applicable in Service Portal.
    Applicable variables: Lookup select box, Select box

-   **max\_length**

    Sets the maximum number of characters allowed in the field. By default, the field accepts long strings of text, several thousand characters. Set the **max\_length** attribute as appropriate for the information that the variable is collecting. For example, to allow for entry of an address, set `max_length=200`, or other appropriate length.

    Applicable variables: Single-line text, Wide single-line text

-   **max\_unit**

    Sets the maximum unit of time for the duration. Possible values are `max_unit=days`,`max_unit=hours`,`max_unit=minutes`, and `max_unit=seconds`.

    For example, if `max_unit=minutes`, the duration is displayed in minutes and seconds. In this case, a duration of 2 days 3 hours 5 minutes 15 seconds is displayed as 3065 minutes 15 seconds.

    Applicable variables: Duration

-   **no\_filter**

    Hides the filter fields that appear above a list collector.

    Applicable variables: List collector

-   **ref\_ac\_columns**

    Specifies the columns with display values that appear in an auto-completion list in addition to the name. Separate column names with a semicolon. For example, `ref_ac_columns=user_name;email;sys_created_on` allows auto-complete to match text from the user\_name, email, and sys\_created\_on columns.

    Applicable variables: Reference, Requested For.

-   **ref\_ac\_order\_by**

    Specifies the column that is used to sort the auto-completion list. For example, `ref_ac_order_by=name` sorts the auto-completion choices alphabetically by name.

    Applicable variables: Reference

-   **ref\_auto\_completer**

    Specifies the name of a JavaScript class \(client-side\) that creates the list for auto-completion choices. Valid class values include:

    -   **AJAXReferenceCompleter**: Displays matching auto-complete choices as a drop-down list. The list only displays the display value column of the reference table. If there is no other auto-completion class specified, reference fields automatically use this class.
    -   **AJAXTableCompleter**: Displays matching auto-complete choices as rows in a table. The table displays the display value column of the reference table and any columns listed in the ref\_ac\_columns attribute.
    -   **AJAXReferenceChoice**: Displays matching auto-complete choices as a drop-down list. The list only displays the display value column of the reference table. The list only displays up to 25 matching choices. If there are more than 25 auto-complete choices, the reference field instead displays the choices with the AJAXTableCompleter class.
    Applicable variables: Reference

-   **ref\_qual\_elements**

    A list of fields to be sent back to the server to get an updated reference.

    Applicable variables: Lookup multiple choice, Lookup select box, List Collector.


**Important:** Attribute behavior is specific to the service catalog desktop.

**Parent Topic:**[Create a service catalog variable](../task/t_CreateAVariableForACatalogItem.md)

**Related topics**  


[Define help information for a service catalog variable](../task/t_DefineHelpInformation.md)

[Define a question choice for a variable](../task/define-question-choice-var.md)

