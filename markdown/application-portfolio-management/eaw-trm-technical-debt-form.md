---
title: TRM technical debt form
description: Technology Reference Model \(TRM\) technical debts are created for products that aren't aligned with TRM phases and standards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-trm-technical-debt-form.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [TRM technical debt, technical debt form, technology reference model]
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# TRM technical debt form

Technology Reference Model \(TRM\) technical debts are created for products that aren't aligned with TRM phases and standards.

<table id="table_ak2_5fg_tyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reason

</td><td>

Reason why the technical debt was created. Select this value to open the technical debt record.

</td></tr><tr><td>

Business Application

</td><td>

Business application associated with the TRM product.

</td></tr><tr><td>

State

</td><td>

State of the technical debt record: Active, Resolved, or Archived. For details on how the record moves between states, see [TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md).

</td></tr><tr><td>

TRM product

</td><td>

TRM product. A software product that has version-specific life cycles.

</td></tr><tr><td>

TRM phase

</td><td>

Phase of the TRM product. The following TRM phases are available: -   Approved: The technology is approved for use.
-   Approved with Constraints: The technology can be used within the constraints specified in the comments.
-   Divest: A decision was taken to divest from the use of the technology.
-   Evaluation: This technology is being evaluated and cannot be used for production purposes.
-   Unapproved: The technology is not permitted to be used.

 **Note:** You can modify these phases by navigating to **EA Workspace** &gt; **Setup** &gt; **TRM Phases**.

</td></tr><tr><td>

Software product

</td><td>

Software product related to the TRM product.

</td></tr><tr><td>

Version

</td><td>

Version of the software product. The software product model name usually contains this version.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software product. Populated only when the technical debt is created from a TRM product lifecycle that matches on version and edition.

</td></tr><tr><td>

Software product model

</td><td>

Software product model related to the TRM product.

</td></tr><tr><td>

Operating system

</td><td>

Operating system on which the TRM product can be deployed. This field appears only when **Software** is selected in the **Type** field.

</td></tr><tr><td>

Last run

</td><td>

Timestamp when the **Populate TRM technical debts in the EA Workspace** scheduled job last ran to update the table with technical debt.

</td></tr><tr><td>

Server

</td><td>

Server related to the TRM product. **Note:** This field is available starting with Technology Lifecycle Management \(TLM\) plugin version 1.7.1.

</td></tr><tr><td>

TRM level

</td><td>

Level \(Product or Product Lifecycle\) at which the technical debt is created.

</td></tr></tbody>
</table>## Related lists

The **Discovered Technology** related list shows the TLM discovered technology records that this technical debt was created from.

Use this related list as your starting point to investigate and remediate the technical debt. Open a discovered technology record from the list. Use its **Number** field to open the full TPM Discovered Technology record, or its **TLM technology lifecycle** field to open the associated technology lifecycle record. From there, you can identify and update the underlying TRM product or TRM product lifecycle that's causing the debt.

**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[View Technology Reference Model technical debts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/view-trm-tech-debt.md)

[TRM technical debt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-manage-trm-technical-debt.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

[Governing TRM product fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-trm-governing-fields.md)

