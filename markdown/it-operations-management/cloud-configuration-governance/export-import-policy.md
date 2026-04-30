---
title: Export or import a cloud policy
description: To back up, move, or restore a policy, you can export and import the policy as an update set. The update set includes rules, conditions, actions, scripts, and script categories.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Export or import a cloud policy

To back up, move, or restore a policy, you can export and import the policy as an update set. The update set includes rules, conditions, actions, scripts, and script categories.

## Before you begin

Role required: sn\_cmp.cloud\_admin or admin.

## Procedure

1.  On the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Perform the following action to export a policy:

    1.  Click the export icon for the policy.

        ![Export icon for a policy](../image/export-cloud-policy.png)

        The instance generates an update set.

3.  To import a policy, install the update set as follows:

    1.  On the instance to import to, navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Click the **Import Update Set from XML** related link.

    3.  In the Import XML popup, click **Choose File**, select the file, and then click **Upload**.

    If a policy that you exported from the source environment exists in the target environment and both policies have the same sys\_id, then the policy in the target environment is updated.

    **Note:** If the policy that you exported from the source environment exists in the target environment, and the policies have different sys\_ids, then an error occurs during the import process. You must export a different policy from the source environment or delete the policy with the same name in the target environment.


**Parent Topic:**[Policies for Cloud Provisioning](../concept/cloud-policy.md)

**Related topics**  


[System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

