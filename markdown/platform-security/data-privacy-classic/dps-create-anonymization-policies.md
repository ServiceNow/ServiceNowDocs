---
title: Create anonymization policies
description: Configure an anonymization policy to specify which techniques are used when anonymizing your data.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Create anonymization policies

Configure an anonymization policy to specify which techniques are used when anonymizing your data.

## Before you begin

The data privacy configuration defines tables, `sys_user` and other, and columns to the de-identified, depending on the use case and specifies parameterized types of the techniques to be used while de-identifying data.

**Note:** To complete a privacy configuration, you must first configure a data privacy technique configuration. See [Create anonymization techniques](dps-create-anonymization-techniques.md) for more information.

Role required: data\_privacy\_admin and admin

## Procedure

1.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

    All anonymization policies display. Published policies are available to schedule the anonymization job.

3.  Select **Create new policy**.

4.  Select to either anonymize **Data tables or columns**, **User specific data**, **Catalog variable**, or **Real time data**.

    |Data Type|Description|
    |---------|-----------|
    |Data tables or columns|Records that match the data policy will be anonymized.|
    |User specific data|Select a set of users or user groups to be anonymized.|
    |Catalog variable|Anonymize sensitive data stored in catalog item variables and form fields.|
    |Real time data|Anonymize real time entries for a set of columns.|

    Data privacy policies can only apply to classified data, for more information on data classification, see [Data classification](../concept/dps-data-classification.md).

5.  Select **Create**.

    There are sequential steps required to complete the policy. You must **Define details** and **Assign techniques**. **Select user reference** is also required when defining the policy for user specific data.

    For catalog variables, you will **Define details** and select the scope \(either **Service catalog request** or **Record producer**\), then review the **Data pattern anonymization**.

    **Note:** Data pattern anonymization uses the information currently in the active data pattern table.

6.  Define the details for the new anonymization policy.

    -   Enter the policy name in the **Name** field, and the policy description in the **Description** field.
    -   Define what channels automatically activate the policy and the channel priority in **Activation Channels**
    -   In the **Data Class** field, select the data class to use with this policy.
    -   Turn on or off real time data anonymization.
    **Note:** If you are not anonymizing an entry, select the **DoNothing** technique rather than leaving the entry empty. Policies with empty values in the Privacy Technique Configuration field cannot execute when used in data privacy jobs.

7.  Select **Continue** to move to the next configuration step.


