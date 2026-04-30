---
title: Attachment
description: When submitting a catalog item request, this variable lets you upload an attachment for a question of the item.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-20"
reading_time_minutes: 5
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Attachment

When submitting a catalog item request, this variable lets you upload an attachment for a question of the item.

After you upload the attachment, you can also download, update, and delete it. Even when fulfilling the request, you can download, update, and delete the attachment in a requested item or catalog task. You can specify restrictions for file size and extensions using the **max\_file\_size** and **allowed\_extensions** variable attributes. For information on these variable attributes, see [Service Catalog variable attributes](variable-attributes.md).

**Important:**

-   You should specify only an integer value for the following:
    -   The `max_file_size` variable attribute
    -   The **glide.sc.variable.attachment.default\_max\_size** system property \(catalog-level\). The default value is 20.
-   If the `max_file_size` variable attribute is not specified, the **glide.sc.variable.attachment.default\_max\_size** system property value is considered as the upper limit for the attachment file size.
-   Irrespective of the file size allowed in the variable, the attachment file size cannot exceed the size specified in **com.glide.attachment.max\_size** system property, which is applicable for attachments across ServiceNow AI Platform.
-   The g\_form.setValue\(\) API is supported in catalog client scripts.

**Note:** When you edit an attachment, the existing attachment is removed and a new attachment is uploaded.

When you upload an attachment to this variable, an entry is created in the Attachment \[sys\_attachment\] table. The variable is not updated until you submit the item request, add it to the cart, or save the record while editing it \(in fulfiller flows\). If you delete or update the attachment before submitting the corresponding catalog item, the entry in the Attachment \[sys\_attachment\] table is cleared.

The attachment uploaded for this variable is copied in the following scenarios:

-   In an order guide, when the variable is cascaded to a catalog item in the rule base

    **Important:** The individual variable attributes are not honored for the catalog items in the rule base. For example, let us consider that a variable in the **Describe Needs** section allows a .pdf attachment and the variable of a catalog item in the rule base allows a .txt attachment. When you upload an attachment of .pdf type for a variable in the **Describe Needs** section, it is initially cascaded to the variable in the catalog item as well and the variable attributes specified in the catalog item are not honored. However, if you delete this initially cascaded attachment from an individual item and try to upload a new attachment, then the individual variable attributes of the catalog item are honored.

-   In a record producer, when the variable is mapped to a task table field. This variable can be mapped only to the File Attachment field type of a task table.

**Important:** After an attachment is copied, the changes to the individual attachments are independent. For example, any change to an attachment in the order guide does not impact the same attachment cascaded to the catalog item in the rule base.

**Warning:** Since the attachments are copied, a larger size can lead to performance issues.

If the system-wide anti-virus check is enabled, the anti-virus check is performed on the attachment when you:

-   Submit a request for the corresponding catalog item
-   Add the catalog item to the cart or wish list

**Note:**

-   This variable is not supported in a multi-row variable set.
-   This variable is supported in flows and workflows.
-   This variable is available in condition builder
-   For this variable, item variable assignment is not supported in order guide.

![The Attachment variable](../image/AttachmentVariable.png "Attachment variable")

**Parent Topic:**[Types of service catalog variables](r_VariableTypes.md)

**Related topics**  


[Break](break.md)

[Check box](check-box.md)

[Container start, container split, and container end](contain-start-split-end.md)

[Date, Date and time, and Duration](date.md)

[Email](email.md)

[HTML](html.md)

[IP Address](ip-address.md)

[Label](label.md)

[List collector](list-collector.md)

[Lookup multiple choice](lookup-multiple-choice.md)

[Lookup select box](lookup-select-box.md)

[Custom and Custom with label](custom.md)

[Masked](masked.md)

[Multi-line text](multi-line.md)

[Multiple choice](multiple-choice.md)

[Numeric scale](numeric-scale.md)

[Reference](reference.md)

[Requested for](requested-for.md)

[Rich Text Label](rich-text-label.md)

[Select box](select-box.md)

[Single-line text](single-line-text.md)

[UI page](ui-page.md)

[URL](url.md)

[Wide single-line text](wide-single-line-text.md)

[Yes/No](yes-no.md)

[Variable support in various channels](variables-availability.md)

