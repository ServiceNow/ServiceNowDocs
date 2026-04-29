---
title: Preview and remediate tag audit failures
description: Preview audit reports for resources that tag policies identify as non-compliant. Remediate failures by adding or updating tags.
locale: en-US
release: australia
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Preview and remediate tag audit failures

Preview audit reports for resources that tag policies identify as non-compliant. Remediate failures by adding or updating tags.

## Before you begin

Configure tag policies and remediation policies. See [Configure a tag policy for Tag Governance](configure-tag-governance-policy.md) and [Configure remediation policies on tag audit findings](configure-remediation-tag-governance-.md).

**Note:** The update to cloud works only for AWS and Microsoft Azure Cloud resources for CMDB classes listed in the Tag Remediation form.

Role required: sn\_itom\_tag.tag\_admin, admin

## About this task

Based on the tag policies that you create, you can preview remediation flows and auto-generate missing tags for non-compliant CIs. The Tag Remediation Preview related list displays this information. See [Flows](https://www.servicenow.com/docs/access?context=flows&version=australia&pubname=australia-build-workflows&ft:locale=en-US) and [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Note:**

-   If you select the **Update Tags in Cloud** check box while configuring remediation, the Preview audit filters failures belonging to the listed CI classes.
-   If you selected both the **Auto-Remediate** and **Update Tags in Cloud** settings while configuring remediation, then tags are updated both in the CMDB and in cloud resources \(only for supported CMDB CI classes\).
-   If you select only **Auto-Remediate**, the remediation runs and updates tags in the CMDB alone.

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Remediation**.

2.  From the Tag Remediations list, select the record that you want to view.

3.  Select the **Preview Remediation** related link.

    The Tag Remediation Previews related list displays the non-compliant CIs.

4.  Select the Tag Remediation Previews related list to identify the missing tags and their values.

5.  On the Tag Remediation Keys related list, select **New** to create a tag remediation key.

    The fields on the Tag Remediation Key form are described in [Tag Remediation Key form](../reference/tag-gov-tag-remediation-key-form.md).

6.  Select **Submit**.

    You have created the Tag Remediation keys associated with the policy.

7.  Select the **Generate Keys** related link, if you have run the **Tag Key Policy**.

    The **Generate Keys** related link appears only for the **Tag Key Policy** policy type. Because the policy specifies the expected tags, you can select the **Generate Keys** related link to generate the keys that you need for remediation instead of manually adding them in the Tag Remediation Keys related list.

8.  Select the **Generate Key Values** related link, if you have run the **Tag Key &amp; Value Policy**.

    The **Generate Key Values** related link appears only for the **Tag Key and Value Policy** policy type. Because you have already specified the values you are looking for in the tag policy, you can select the **Generate Key Values** related link to add the expected key values.

9.  Select the **Remediate Tags** related link.

    The remediation flow to add missing tags initiates. A relevant information message displays on the form when the Remediation is active. Select the **More Info** link on the message to navigate to the default flow context.


## Result

Based on the tag audit result findings and the Tag Remediations Keys that you create, the remediation flow adds missing tags to the non-compliant CIs to achieve policy compliance.

