---
title: Set up a webhook for the Jenkins spoke
description: Set up a webhook application to receive the required updates from Jenkins at your ServiceNow instance.Create a authorization key to authorise requests from Jenkins.Authorise requests from Jenkins by providing authorization key for webhook in your ServiceNow instance.Receive updates from Jenkins by providing the authorization key in Jenkins.Provide user friendly descriptions to the subflows in the Jenkins v2 spoke.Provide subflows as answers to the conditions mentioned in the decision table. When the specified conditions are met, the associated subflow is triggered.Create a webhook routing policy and customize subflow as per your requirement.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Jenkins v2 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a webhook for the Jenkins spoke

Set up a webhook application to receive the required updates from Jenkins at your ServiceNow instance.

## Before you begin

Role required: admin

## Create authorization key for the Jenkins v2 spoke

Create a authorization key to authorise requests from Jenkins.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Enter this command in the **Run script \(JavaScript executed on server\)** text field:

    `gs.info(GlideSecureRandomUtil.getSecureRandomString(32));`

3.  Click **Run Script**.

4.  Copy and record the generated value for later use.

    ![Client Secret or Authorization Key](../image/auth-token.png)


## Provide authorization key for webhook

Authorise requests from Jenkins by providing authorization key for webhook in your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Jenkins v2** &gt; **Webhook Client Details**.

2.  Click **New**.

3.  On the form, fill these values:

    |Field|Description|
    |-----|-----------|
    |Authorization Key|Authorization key you had generated. See [Create authorization key for the Jenkins v2 spoke](receive-jenkins-upd.md#) for more information.|
    |Name|Name to identify the webhook client record.|

4.  Click **Submit**.


## Provide authorization key in Jenkins

Receive updates from Jenkins by providing the authorization key in Jenkins.

### Before you begin

Role required: admin.

### Procedure

1.  Log in to your Jenkins account.

2.  Click and open the job for which you want to configure your webhook.

3.  Click **Configure**.

4.  In the **Bindings** tab, click **Add** and select **Jenkins**.

    For more information about the using the plugin, see [Credentials Binding](https://plugins.jenkins.io/credentials-binding/).

    ![Jenkins Credentials Provider](../image/jenkins-bindings.png)

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Kind|Select **Secret text**.|
    |Secret|Enter authorization key. See [Create authorization key for the Jenkins v2 spoke](receive-jenkins-upd.md#) for more information.|
    |ID|Provide unique identifier to identify the record.|

6.  Click **Add**.

7.  In the **Post-build Actions** tab, configure task and specify script to receive updates at your ServiceNow instance.

    -   Sample Windows **Script**: `curl "https://<instance-name>.service-now.com/api/sn_jenkinsv2_spoke/jenkins_v2_webhook/build_status" -X POST -H "content-type:application/json" -H "jenkinsKey: %<ID>%" -d "{\"Job_Name\":\"%JOB_NAME%\",\"Job_Path\":\"%JOB_URL%\",\"Build_Number\":\"%BUILD_NUMBER%\"}"`
    -   Sample Shell **Script**: `curl "https://<instance-name>.service-now.com/api/sn_jenkinsv2_spoke/jenkins_v2_webhook/build_status" -X POST -H "content-type:application/json" -H "jenkinsKey: ${<ID>}" -d "{\"Job_Name\":\"${JOB_NAME}\",\"Job_Path\":\"${JOB_URL}\",\"Build_Number\":\"${BUILD_NUMBER}\"}"`
    **Note:** ID in the script is the ID you had provided in the Jenkins Credential Provider form.

    For more information about the using the plugin, see [Post build task](https://plugins.jenkins.io/postbuild-task/).

8.  Click **Apply**.


## Provide description to subflow

Provide user friendly descriptions to the subflows in the Jenkins v2 spoke.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Jenkins v2** &gt; **Webhook Answer Subflows**.

2.  Click **New**.

3.  On the form, fill these values:

    |Field|Description|
    |-----|-----------|
    |Description|Description about the subflow.|
    |Subflow|Required subflow in the Jenkins v2 spoke.|

4.  Click **Submit**.


## Provide answers to the decision table

Provide subflows as answers to the conditions mentioned in the decision table. When the specified conditions are met, the associated subflow is triggered.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Open the record for the **Jenkins v2 spoke**.

3.  In the **Decisions** tab, click **New**.

4.  On the form, fill these values:

<table id="table_awj_xgv_z3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Default answer

</td><td>

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Jenkins. See [Jenkins v2 Spoke](../concept/jenkins-spoke.md) for information about the supported fields.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.1.  Click the Lookup icon \(![Lookup icon](../image/lookup-icon.png)\).
2.  Select the required subflow from the Document list.

**Note:** Ensure that the **Table name** is `Jenkins v2 Webhook Answer Subflow [sn_jenkinsv2_spoke_webhook_answer_subflow]`.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Customize a webhook

Create a webhook routing policy and customize subflow as per your requirement.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of the required default subflow.

4.  Customize the Jenkins Webhook Answer Subflow: Process build information subflow as per your requirement and publish it.

    See [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information about creating and using subflows and [Jenkins v2 Spoke](../concept/jenkins-spoke.md) for information about the fields that the routing policies and subflows support.

5.  Navigate to **Jenkins v2** &gt; **WebHook Answer Subflows**.

6.  Click **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Description|Description about the subflow.|
    |Subflow|Required subflow in the Jenkins v2 spoke.|

8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.

9.  Navigate to **System Definition** &gt; **Decision Tables**.

10. Open the record for the **Jenkins v2** spoke.

11. In the **Decisions** tab, click **New**.

12. On the form, fill these fields:

<table id="table_zhp_k2d_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Default answer

</td><td>

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Jenkins. See [Jenkins v2 Spoke](../concept/jenkins-spoke.md) for information about the supported fields.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.1.  Click the Lookup icon \(![Lookup icon](../image/lookup-icon.png)\).
2.  Select the required subflow from the Document list.

**Note:** Ensure that the **Table name** is `Jenkins v2 Webhook Answer Subflow [sn_jenkinsv2_spoke_webhook_answer_subflow]`.

</td></tr></tbody>
</table>13. Click **Submit**.


