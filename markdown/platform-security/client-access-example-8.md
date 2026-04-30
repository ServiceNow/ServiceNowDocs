---
title: Test a Windows Management Instrumentation credential encrypted with Secrets Management
description: Verify that your Windows Management Instrumentation \(WMI\) credential is encrypted with Secrets Management and use an Integration Hub workflow to complete end-to-end testing.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Test a Windows Management Instrumentation credential encrypted with Secrets Management

Verify that your Windows Management Instrumentation \(WMI\) credential is encrypted with Secrets Management and use an Integration Hub workflow to complete end-to-end testing.

## Before you begin

Role required: admin, KMF\_admin, sn\_secrets.secret\_manager, and sn\_kmf.cryptographic\_manager

-   Integration Hub Enterprise must be active on your instance. For details, see [Request an Integration Hub plugin](https://www.servicenow.com/docs/access?context=request-integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   You must have a configured secrets group on your instance. See steps 1 through 3 listed in [Configuring client accessible secrets](../concept/client-access-secret-landing.md).
-   You must have a configured credential encrypted with Secrets Management. See steps 1 through 9 listed in [Create credentials and test credential encryption](client-access-example-4.md).

## Procedure

1.  Confirm that the desired MID Server is associated with the Secret Group.

    Open the Secret Group with Criteria \[sn\_sm\_criteria\_secret\_group\] record, and look for your MID Server in the **Secret Group – Identity Group Members** list. If your MID Server isn’t associated with a group see [Create a secret group with criteria](client-access-example-3.md).

2.  Confirm that the credential is encrypted with Secrets Management.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Open your credential record.

        Verify that you have a credential alias listed in the **Credential alias** field. If you have not created one already, see [Create a Connection &amp; Credential alias](../../../product/credentials/task/connection-alias.md).

    3.  Select and hold \(or right-click\) the header of your credentials record, and select **Show XML** from the list.

    4.  In the XML view of the record, find the password and confirm that the value starts with `□□□A□□`.

        ![XML view of a credential alias record](../images/XML-view.png)

3.  Create a testing workflow in Workflow Studio.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Select **New**, then select **Action** from the list.

    3.  Enter a name in the **Action name** field.

        Leave the **Application** field set to Global.

    4.  Select the **Build action** button.

4.  Configure a record lookup step in Workflow Studio.

    1.  In the **Action Outline**, select the plus button to add a new step.

        Find and select the **Look Up Record** step type.

    2.  In the **Table** field, select **MID Server \[ecc\_agent\]**.

    3.  For the condition, select **Name is**, followed by the name of your MID Server.

    ![Look up Record step configuration](../images/test_flow_example.png)

    **Important:** Make sure that the selected MID Server is the same as the one associated with the secret group.

5.  Configure a record lookup step in Workflow Studio.

    1.  In the **Action Outline**, select the plus button to add a new step below your Look Up Record step.

        Find and select the **PowerShell** step type.

    2.  In the **PowerShell Step** form, fill in the fields as needed.

<table id="table_qsc_q4g_2bc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection

</td><td>

Select **Define Connection Inline**

</td></tr><tr><td>

Credential Alias

</td><td>

Select your credential alias

</td></tr><tr><td>

Host

</td><td>

Enter the IP address of the target Windows server

</td></tr><tr><td>

Port

</td><td>

Enter `22` if it isn’t already the default.

</td></tr><tr><td>

MID Selection

</td><td>

Select **Specific MID Server**

</td></tr><tr><td>

MID Server

</td><td>

Drag in the **MID Server Record** pill from the **Data** panel

 This data pill is visible in the **Data** panel on the right edge of the screen, under **Look Up Record step**.

</td></tr><tr><td>

Remoting Type

</td><td>

Select **Run on a MID Server or have your script establish a remote session**

</td></tr></tbody>
</table>    ![PowerShell step configuration](../images/test_flow_example_2.png)

6.  Create a script for your test action.

    1.  In the **Script Type** field, select **Inline Script**.

    2.  Use the following script, replacing the example path with the path from your test host.

        ```
        Get-Date | Out-File -FilePath C:\Users\<path>\sm_ig_text_file.txt
        ```

        **Note:** You may also run your own script that suits your remote host configuration. It’s important to confirm that a connection was established using the SM-encrypted value.

    3.  Select the **Save** button to save your action.

    ![Script configuration for the PowerShell step](../images/test_flow_example_3.png)

7.  Select the **Test** button to test your action.

8.  Review the output logs for any error messages.

9.  Verify that a test file has been created on the host server in the file path you provided in the script.

    ![Test file within a host server's file system](../images/test_flow_example_4.png)


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

