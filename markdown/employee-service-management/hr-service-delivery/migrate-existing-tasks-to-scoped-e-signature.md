---
title: Migrate existing HR task templates and open HR tasks to e-signature
description: Migrate existing HR task templates and open HR tasks to the new HR task type for e-signature with the Migrate HR e-signature tasks scheduled job. The scheduled job automatically updates the HR task type and e-signature template based on your existing configurations. It also disables the old HR task types for credential, e-signature, and sign document.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR e-signature, HR Documents, HR Service Delivery, Employee Service Management]
---

# Migrate existing HR task templates and open HR tasks to e-signature

Migrate existing HR task templates and open HR tasks to the new HR task type for e-signature with the **Migrate HR e-signature tasks** scheduled job. The scheduled job automatically updates the HR task type and e-signature template based on your existing configurations. It also disables the old HR task types for credential, e-signature, and sign document.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

**Important:**

Starting with the Zurich release, HR task types: Credential, E-signature \(e\_signature\), and Sign Document are now deprecated and no longer supported or available for new activation. E-signature provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

The **Migrate HR e-signature tasks** scheduled job migrates existing HR task templates and open HR tasks from the **Credential**, **E-Signature**, and **Sign Document** HR task types to the new **E-signature** HR task type.

|Pre-migration|Post-migration|
|-------------|--------------|
|![Before migrating to new HR task type for e-signature](../image/e-signature-migrate-existing-task-types.png)|![After migrating to new HR task type for e-signature](../image/e-signature-migrate-new-task-type.png)|

The associated document and signature configurations are also migrated to new or existing e-signature templates. If an e-signature template for the applicable document and signature configuration already exists, then the existing e-signature template is used. Otherwise, a new e-signature template is created.

<table id="table_ljh_1rw_5hb"><thead><tr><th>

Pre-migration HR task type

</th><th>

Post-migration e-signature template

</th></tr></thead><tbody><tr><td>

Credential

</td><td>

-   Document type: Managed document
-   Signature type: Credential

</td></tr><tr><td>

E-Signature

</td><td>

-   Document type: Managed document
-   Signature type: Signature

</td></tr><tr><td>

Sign Document

</td><td>

-   Document type: HR document template
-   Signature type: Signature

</td></tr></tbody>
</table>Finally, the HR task types for **Credential**, **E-Signature**, and **Sign Document** are disabled. Only the new HR task type for **E-signature** remains.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the **Migrate HR E-signature Tasks** scheduled job.

3.  Click **Execute Now**.

    Depending on the data you have, the migration may take some time.

    -   Existing HR task templates are updated to the e-signature task type and an e-signature template.
    -   Open HR tasks are updated to the e-signature task type and an e-signature template.
    -   HR task types for **Credential**, **E-Signature**, and **Sign Document** are disabled.

