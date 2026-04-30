---
title: HR e-signature
description: Sign electronic documents from any desktop or mobile device with e-signature. E-signature is a scoped application that enables users to sign managed documents, knowledge articles, or HR document templates with their typed or drawn e-signature, their credentials, or as an acknowledgment.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# HR e-signature

Sign electronic documents from any desktop or mobile device with e-signature. E-signature is a scoped application that enables users to sign managed documents, knowledge articles, or HR document templates with their typed or drawn e-signature, their credentials, or as an acknowledgment.

The e-signature \[com.snc.esign\] plugin activates the sn\_esign.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only e-signature admin user by requiring a minimum number \(default is two\) of active users with this role.

HR e-signature is a **non-embedded signature** capability for managed documents, and knowledge articles, attached to an HR task for fulfilment. It supports three signing types \(Acknowledgement, Credential, and Signature\) and two document types \(Managed Documents and Knowledge Articles\).

## HR and e-signature roles

By default, the following HR roles contain the following e-signature roles.

<table id="table_syn_r3w_5hb"><thead><tr><th>

HR role

</th><th>

E-signature role

</th></tr></thead><tbody><tr><td>

HR administrator\[sn\_hr\_core.admin\]

</td><td>

E-signature administrator\[sn\_esign.admin\]

</td></tr><tr><td>

HR basic\[sn\_hr\_core.basic\]

</td><td>

E-signature manager\[sn\_esign.config\_manager\]

</td></tr></tbody>
</table>You can use the assignments as-is or change them. To change the default assignments, see [Components installed with e-signature](https://www.servicenow.com/docs/access?context=components-installed-with-e-signature&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for information on how to assign a role to another role, group, or user.

## How to use e-signature templates with HR tasks

Users with the HR administrator \[sn\_hr\_core.admin\] or basic \[sn\_hr\_core.basic\] role can create e-signature templates. Each e-signature template pairs a document type to sign \(managed document, knowledge article, or HR document template\) with a signature type \(signature, credential, or acknowledgment\). For example, you could create an e-signature template for a non-disclosure agreement that requires a typed or drawn signature.

For more information, see [Configure an e-signature template](https://www.servicenow.com/docs/access?context=configure-e-signature-configuration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

You can then use the e-signature templates in HR tasks or HR task templates to request signatures from users.

**Note:** On the HR task form, make sure that the HR task type sets to **E-signature**.

-   [Adding an HR task to an HR case](../task/t_ViewAnHRTask.md)
-   [Configure an HR task template](../task/configure-hr-task-template.md)

## Migrating existing HR task templates and open HR tasks to e-signature

Migrate existing HR task templates and open HR tasks to the new HR task type for e-signature with the **Migrate HR e-signature tasks** scheduled job. The scheduled job automatically updates the HR task type and e-signature template based on your existing configurations. It also disables the old HR task types for credential, e-signature, and sign document.

For more information, see [Migrate existing HR task templates and open HR tasks to e-signature](../task/migrate-existing-tasks-to-scoped-e-signature.md).

## Activation information

E-signature automatically activates when you activate Case and Knowledge Management. If it does not activate, you can manually [activate e-signature](https://www.servicenow.com/docs/access?context=activate-e-signature&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). For information on what components install with the feature, see [Components installed with e-signature](https://www.servicenow.com/docs/access?context=components-installed-with-e-signature&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Related topics**  


[E-signature](https://www.servicenow.com/docs/access?context=e-signature&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

