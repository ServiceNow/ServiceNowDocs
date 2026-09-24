---
title: Request a TRM product in Enterprise Architecture Workspace
description: Submit a request to add a software or hardware product to the TRM library and optionally include one or more lifecycle records with the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-request-a-trm-products.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Working with Technology Reference Model \(TRM\) in EA Workspace, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Request a TRM product in Enterprise Architecture Workspace

Submit a request to add a software or hardware product to the TRM library and optionally include one or more lifecycle records with the request.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Technology Portfolio page by selecting the Technology Portfolio icon \[Omitted image "technology-portfolio-icon.png"\] Alt text:.

3.  In the **TRM catalog** tab, select **Request TRM product**.

4.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Request TRM product form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-product-request-form.md).

5.  Include lifecycle records with the request by selecting the **TRM product lifecycles** tab, then select **Create lifecycle**.

    **Note:**

    -   For software products: You can add up to 5 version and edition combinations, with a maximum of 10 phases per combination.
    -   For hardware products: You can add up to 5 hardware models, with a maximum of 10 phases per hardware model.
    1.  For a software product, enter the **Version**, **Edition**, **TRM phase**, **Phase start date**, and **Phase end date**.

    2.  For a hardware product, select the **Hardware model**, then fill in the **TRM phase**, **Phase start date**, and **Phase end date**.

        The **Model number** and **Barcode** fields are populated automatically when you select a hardware model.

    3.  To add more phases to the same version or hardware model, select the add TRM lifecycle phase icon \[Omitted image "bubble-chart-zoom-in.png"\] Alt text:.

    4.  To add another version and edition group or hardware model group, select **Add version and edition** for software product or select **Add model** for hardware model.

6.  Select **Submit**.


## Result

A confirmation message appears with the request number, for example: `Request for TRM product is created successfully: TRMPREQ0000000`. Select the request number to track the status of the request. The request is routed to an Enterprise Architect for approval.

**Parent Topic:**[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-work-with-trm.md)

**Related topics**  


[View Technology Reference Model technical debts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/view-trm-tech-debt.md)

[View all TRM phases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-view-all-trm-phases.md)

[Create a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle.md)

[View all TRM categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/view-all-trm-categories.md)

[View all TRM products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-view-all-trm-products.md)

[Update TRM technical debt data using scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-run-job-trm-tech-debts.md)

[View all TRM products grouped by product category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-view-all-trm-products-grouped-by-product-category.md)

[Request a TRM product lifecycle in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-request-a-trm-product-lifecycle.md)

[Associate an Architectural Artifact to a TRM product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-assoicate-artifact-trm-prod.md)

[Create TRM product lifecycles in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle-req.md)

[Run a job to sync TRM product names in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-schedule-job-sync-trm-product-names.md)

[Approve or reject TRM requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-approve-trm-req.md)

