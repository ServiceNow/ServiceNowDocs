---
title: Manually run a supplier document configuration
description: Run a supplier document configuration to enable supplier managers, supplier owners, and supplier contacts to immediately upload the required documents.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Supplier Document Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Manually run a supplier document configuration

Run a supplier document configuration to enable supplier managers, supplier owners, and supplier contacts to immediately upload the required documents.

## Before you begin

Role required: sn\_slm.manager, sn\_slm.owner, sn\_slm.contact or sn\_slm.admin

## About this task

The supplier document configuration is configured to run based on the run conditions that you set. However, you can run them manually when needed. Running the document configuration creates either or both of the following in the Supplier Collaboration Portal, based on the run conditions:

-   A tile in the Documents widget on the My Company page. The supplier contact can upload a document using this tile in the Documents widget.

    **Note:** The Documents widget is created if you select **Anyone** from the **Required from** field in the Upload preferences form. The tile in the Documents widget is named after the supplier document type name that you provided when creating the supplier document configuration.

-   The Upload Document task on the My To-dos page. The supplier contact can upload a document using this task. The Upload Document task is created if you select **Everyone** from the **Required from** field and also set the **Generate task for** field to **Yes** in the Upload preferences form.

## Procedure

1.  Do one of the following.

<table><thead><tr><th align="left" id="d110203e98">

To

</th><th align="left" id="d110203e101">

Do This

</th></tr></thead><tbody><tr><td id="d110203e107">

**Run a document configuration from the Platform UI**

</td><td>

Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Administration** &gt; **Document Configuration**

</td></tr><tr><td id="d110203e131">

**Run a document configuration from the Source-to-Pay Workspace**

</td><td>

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.
2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\) and navigate to **Lists** &gt; **Administration** &gt; **Document Configuration**.


</td></tr></tbody>
</table>2.  Select the document configuration that you want to run.

3.  Select **Execute Now**.![Selected button for running the document configuration manually.](../image/run-doc-config-manually.png)


**Parent Topic:**[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

**Related topics**  


[Create a supplier document configuration](create-doc-config.md)

[Uploading supplier documents](../concept/upload-doc-about.md)

[Configure document expiration monitoring attributes](configure-document-expiration-monitoring-attributes.md)

[Create a supplier document configuration](create-doc-config.md)

[Uploading supplier documents](../concept/upload-doc-about.md)

