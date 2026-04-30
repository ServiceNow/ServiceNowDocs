---
title: Configure Flow Designer to manage the integration
description: On your instance, use Workflow Studio to manage an integration between your local network and your instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Configure Flow Designer to manage the integration

On your instance, use Workflow Studio to manage an integration between your local network and your instance.

## Before you begin

Role required: admin, KMF\_admin, sn\_secrets.secret\_manager, and sn\_kmf.cryptographic\_manager

In these steps, you create a Workflow Studio workflow to create a text file on your local system.

## Procedure

1.  On your instance, navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Create an action in ServiceNow by selecting **New** and selecting **Action**.

    ![Creating a new action in flow designer](../images/client-side-8.png)

3.  Enter a name in the **Action name** field, and select **Submit**.

4.  Create a step by selecting the plus sign between **Inputs** and **Error Evaluation** in the **Action Outline**.

    ![Creating a new action step](../images/client-side-9.png)

5.  In the **Choose a step to add to your action** window, select **Look Up Record**.

    ![Selecting an action step](../images/client-side-10.png)

6.  In the **Look Up Record step** section, select **MID Server \[ecc\_agent\]** in the **Table** field.

7.  Create another step by selecting the plus sign under your **Look Up Record step**.

8.  In the **Choose a step to add to your action** window, select **SSH**.

    **Note:** If you don't see the **SSH** option, you must activate the required plugin.

9.  In the **SSH Step** section, enter the following information:

    |Field|Value|
    |-----|-----|
    |Connection|Select **Define Connection Inline**|
    |Credential Alias|Select the credential alias for the SSH credential that was created in earlier steps.|
    |Host|Enter the IP address for the host that you're connecting to via SSH.|
    |Port|Enter `22.`|
    |MID Selection|Select **Specific MID Server**.|

10. To fill the **MID Server** field, drag the **MID Server Record** pill from the **Data** section into the field.

    ![Dragging MID server data pill](../images/client-side-12.png)

    **Warning:** When dragging the pill into the field, select the pill and not the black arrow next to the pill.

11. In the **SSH Configuration** section, enter the following value into the **Command** field.

    ```
    /bin/date > sm_ig_text_file.txt
    ```

    This command creates a text file in your local system using the decrypted secrets from the MID Server. The MID Server grants access to the ServiceNow instance \(through Workflow Studio\) without ever giving the ServiceNow instance access to the decrypted secret.

    **Tip:** The `/bin/date` command is inserting the current date/time into the created text file. This command demonstrates that the integration is happening in real time based on the current date/time versus when the text file was created.

12. Select the **Save** button to save the workflow.


**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

