---
title: Create a Credential record for the Automation Anywhere spoke
description: Create a credential record for the Automation Anywhere instance. The Automation Anywhere spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Create a Credential record for the Automation Anywhere spoke

Create a credential record for the Automation Anywhere instance. The Automation Anywhere spoke connection and credential alias uses these credentials to authorize actions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automation Anywhere** &gt; **Authentications**.

2.  Open the record, **Automation Anywhere Credential**.

3.  On the form, fill these values.

<table id="table_ysd_lwd_pmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Default name of the credential record.**Note:** Users are cautioned against modifying the default credential name.

</td></tr><tr><td>

User Name

</td><td rowspan="2">

Credentials to log in to your Automation Anywhere instance.

</td></tr><tr><td>

Password

</td></tr><tr><td>

Credential alias

</td><td>

Default credential alias available along with the Automation Anywhere spoke. For example, select **sn\_autoanywher\_spk.Automation\_Anywhere**.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Automation Anywhere**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to your Automation Anywhere instance.

</td></tr><tr><td>

Dedicated Integration User

</td><td>

Option to specify if you are using a dedicated user for the purpose of integrating Automation Anywhere and ServiceNow instances.**Note:**

-   The dedicated user mentioned here, should be used only for the purpose of integrating Automation Anywhere with ServiceNow.
-   If you aren't using a dedicate user, the ServiceNow instance makes 2 or 3 API calls to execute an action.
-   If you are using a dedicated user, the ServiceNow instance makes only one API call to execute an action.


</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  Click **Get Token**.

    **Note:** This step is applicable when you select the **Dedicated Integration User** check box.

    The confirmation message, `Token retrieval successful` is displayed.


