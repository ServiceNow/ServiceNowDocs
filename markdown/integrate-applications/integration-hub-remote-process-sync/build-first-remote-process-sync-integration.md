---
title: Build your first Remote Process Sync integration
description: Step through an example of how to build a Remote Process Sync integration in order to link the automated processes of two ServiceNow instances together.
locale: en-US
release: zurich
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 21
breadcrumb: [Getting started, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Build your first Remote Process Sync integration

Step through an example of how to build a Remote Process Sync integration in order to link the automated processes of two ServiceNow® instances together.

## Before you begin

-   Activate Remote Process Sync on each instance in your integration by purchasing the Integration Hub Enterprise package. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md).
-   Activate the explicit roles security feature on each instance in your integration. For more information, see Explicit Role plugin.
-   Learn about how to build and manage an Integration Hub Remote Process Sync integration by checking out [Getting started with Remote Process Sync](../reference/getting-started-with-remote-process-sync.md).
-   Confirm the instances that you will link together in the following example are not production instances. It is recommended to test this example on sub-production instances only in order to avoid overwriting any important data on either instance. You might also want to use a [Personal Developer Instance](https://developer.servicenow.com/dev.do#!/guides/sandiego/now-platform/pdi-guide/personal-developer-instance-guide-introduction) for testing this example integration.
-   Confirm that you do not have any existing business rules, workflows, or Workflow Studio flows whose logic will conflict with the flows we will create in the following example.
-   Role required: admin

## About this task

In the following example, you will step through how to link two ServiceNow instances' automated processes together. The use case for this example is that a customer creates requests for hardware that are fulfilled by a vendor. We will refer to the customer's instance as Instance A, and the vendor's instance as Instance B. We will start by setting up credentials in each instance that can access the remote instance. We will also create a user in each instance that can run the outbound and inbound flows.

## Procedure

1.  In Instance A, ensure that your domain is set to `global`, and then navigate to **System Security** &gt; **Users and Groups** &gt; **Users**.

2.  Select **New** to open a new User form view, and then fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |User ID|Enter `rps.api.instance.a`|
    |First name|Enter `RPS API User for Instance A`|

    Select **Save**.

3.  While still on the User form, select **Set Password** to set a password.

    For details, see steps four and five in [Configure password for a user](https://www.servicenow.com/docs/access?context=reset-your-password&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

4.  [Reset the password](https://www.servicenow.com/docs/access?context=c_EnrollInPasswordReset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for RPS API User for Instance A.

5.  Navigate back to **System Security** &gt; **Users and Groups** &gt; **Users** and select the User record that you just created.

    1.  Navigate to and select the Roles related list.

    2.  Select **Edit...** to configure the user's roles.

    3.  In the search window above Collection, enter `ih_process_sync_api`.

    4.  Select **ih\_process\_sync\_api** and **snc\_external** from the Collection list, and then select the add button \(![Add button](../../flow-designer/images/slushbucket-add.png)\) to add these roles to the Roles List.

        **Note:** The snc\_external role restricts the access of external users to only the resources they have been explicitly granted access to.

    5.  Select **Save**.

6.  Select **New** to open a new User form view, and then fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |User ID|Enter `rps.run.as`|
    |First name|Enter `RPS Run as User A`|

    Select **Save**.

7.  While still on the User form, select **Set Password** to set a password.

    For details, see steps four and five in [Configure password for a user](https://www.servicenow.com/docs/access?context=reset-your-password&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

8.  [Reset the password](https://www.servicenow.com/docs/access?context=c_EnrollInPasswordReset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for RPS Run as User A.

9.  Navigate back to **System Security** &gt; **Users and Groups** &gt; **Users** and select the User record that you just created.

    1.  Navigate to and select the Roles related list.

    2.  Select **Edit...** to configure the user's roles.

    3.  In the search window above Collection, enter `ih_process_sync_run_as`.

    4.  Select **ih\_process\_sync\_run\_as** from the Collection list, and then select the add button \(![Add button](../../flow-designer/images/slushbucket-add.png)\) to add that role to the Roles List.

    5.  In the search window above Collection, enter `incident_manager`.

    6.  Select **incident\_manager** from the Collection list, and then select the add button \(![Add button](../../flow-designer/images/slushbucket-add.png)\) to add that role to the Roles List.

    7.  Select **Save**.

10. In Instance B, ensure that your domain is set to `global`, and then navigate to **System Security** &gt; **Users and Groups** &gt; **Users**.

11. Select **New** to open a new User form view, and then fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |User ID|Enter `rps.api.instance.b`|
    |First name|Enter `RPS API User for Instance B`|

    Select **Save**.

12. While still on the User form, select **Set Password** to set a password.

    For details, see steps four and five in [Configure password for a user](https://www.servicenow.com/docs/access?context=reset-your-password&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

13. [Reset the password](https://www.servicenow.com/docs/access?context=c_EnrollInPasswordReset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for RPS API User for Instance B.

14. Navigate back to **System Security** &gt; **Users and Groups** &gt; **Users** and select the User record that you just created.

    1.  Navigate to and select the Roles related list.

    2.  Select **Edit...** to configure the user's roles.

    3.  In the search window above Collection, enter `ih_process_sync_api`.

    4.  Select **ih\_process\_sync\_api** and **snc\_external** from the Collection list, and then select the add button \(![Add button](../../flow-designer/images/slushbucket-add.png)\) to add these roles to the Roles List.

        **Note:** The snc\_external role restricts the access of external users to only the resources they have been explicitly granted access to.

    5.  Select **Save**.

15. Select **New** to open a new User form view, and then fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |User ID|Enter `rps.run.as`|
    |First name|Enter `RPS Run as User B`|

    Select **Save**.

16. While still on the User form, select **Set Password** to set a password.

    For details, see steps four and five in [Configure password for a user](https://www.servicenow.com/docs/access?context=reset-your-password&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

17. [Reset the password](https://www.servicenow.com/docs/access?context=c_EnrollInPasswordReset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for RPS Run as User B from Instance B.

18. Navigate back to **System Security** &gt; **Users and Groups** &gt; **Users** and select the User record that you just created.

    1.  Navigate to and select the Roles related list.

    2.  Select **Edit...** to configure the user's roles.

    3.  In the search window above Collection, enter `ih_process_sync_run_as`.

    4.  Select **ih\_process\_sync\_run\_as** from the Collection list, and then select the add button \(![Add button](../../flow-designer/images/slushbucket-add.png)\) to add that role to the Roles List.

    5.  In the search window above Collection, enter `incident_manager`.

    6.  Select **incident\_manager** from the Collection list, and then select the add button \(![Add button](../../flow-designer/images/slushbucket-add.png)\) to add that role to the Roles List.

    7.  Select **Save**.

19. In Instance A, navigate to **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**, and then select **New**.

    1.  From the list of connection options, select **Basic Auth Credentials**.

    2.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `RPS Vendor Credentials`|
        |User name|Enter `rps.api.instance.b`|
        |Password|Enter the password for RPS API User for Instance B.|

        **Note:** The credentials you enter must match the credentials for the RPS API User that you created in Instance B.

    3.  Select **Submit**.

20. While still in Instance A, navigate to **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**, and then select **New**.

    1.  In the Name field, enter `RPS Vendor Demo`.

        Leave all other fields as they are, and then select **Submit**.

    2.  From the list, select the `RPS Vendor Demo` record that you just created.

    3.  In the Connections related list, select **New**.

    4.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `RPS Vendor`.|
        |Credential|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS Vendor Credentials` record from the list.|
        |Connection URL|Enter the base URL of Instance B. The URL should begin with `https://` and end with `.service-now.com/`|

    5.  Leave all other fields as they are, and then select **Submit**.

21. In Instance B, navigate to **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**, and then select **New**.

    1.  From the list of connection options, select **Basic Auth Credentials**.

    2.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `RPS Customer Credentials`|
        |User name|Enter `rps.api.instance.a`|
        |Password|Enter the password for RPS API User for Instance A.|

        **Note:** The credentials you enter must match the credentials for the RPS API User that you created in Instance A.

    3.  Select **Submit**.

22. While still in Instance B, navigate to **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**, and then select **New**.

    1.  In the Name field, enter `RPS Customer Demo`.

        Leave all other fields as they are, and then select **Submit**.

    2.  From the list, select the `RPS Customer Demo` record that you just created.

    3.  In the Connections related list, select **New**.

    4.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `RPS Customer`.|
        |Credential|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS Customer Credentials` record from the list.|
        |Connection URL|Enter the base URL of Instance A. The URL should begin with `https://` and end with `.service-now.com/`|

    5.  Leave all other fields as they are, and then select **Submit**.

    We've successfully created credentials that can be used to access each remote instance. Now, let's ensure that we can send and receive data between instances by configuring the Remote System record for a Process Sync Definition in each instance.

23. In Instance A, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then select **New**.

    1.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `Hardware Request Process`|
        |Description|Enter `Process for requesting hardware and handling fulfilled hardware requests`|

    2.  Leave all other fields as they are, and then select **Submit**.

    3.  From the list, select the `Hardware Request Process` record that you just created.

24. In the Remote Systems related list, select **New**.

    1.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `Vendor Instance - Instance B`|
        |Description|Enter `Vendor instance that fulfills hardware requests`|
        |Connection Alias|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS_Vendor_Demo` record from the list.|
        |Inbound API User|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS API User for Instance A` record from the list.|
        |Run as|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS Run as User` record from the list.|

    2.  In the context header, select the additional actions icon \(![Additional actions icon](../images/additional-actions-context-header.png)\) and then select **Copy sys\_id**.

        You will need this Sys ID as the value for the External ID field of the Remote System record in Instance B.

    3.  Leave all other fields as they are, and then select **Submit**.

25. In Instance B, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then select **New**.

    1.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `Hardware Fulfillment Process`|
        |Description|Enter `Process for fulfilling hardware requests`|

    2.  Leave all other fields as they are, and then select **Submit**.

    3.  From the list, select the `Hardware Fulfillment Process` record that you just created.

26. In the Remote Systems related list, select **New**.

    1.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Enter `Customer Instance - Instance A`|
        |Description|Enter `Customer instance that requests hardware`|
        |External ID|Paste the value of the Sys ID that you copied from the Remote System record in Instance A.|
        |Connection Alias|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS_Customer_Demo` record from the list.|
        |Inbound API User|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS API User for Instance B` record from the list.|
        |Run as|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `RPS Run as User` record from the list.|

    2.  Leave all other fields as they are, and then select **Submit**.

    3.  From the Remote Systems related list, select the `Customer Instance - Instance A` record.

    4.  In the context header, select the additional actions icon \(![Additional actions icon](../images/additional-actions-context-header.png)\) and then select **Copy sys\_id**.

        You will need this Sys ID as the value for the External ID field of the Remote System record in Instance A.

27. In Instance B, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Remote Systems - All**, and then select the `Customer Instance - Instance A` record from the list.

    1.  In the External ID field, paste the value of the Sys ID that you copied from the Remote System record in Instance A.

    2.  Select Update to save your changes to the record.

    3.  From the list, select the `Customer Instance - Instance A` record.

    4.  In the Related links section, select **Validate and Activate Remote System**.

        You should see a message that displays `Remote system validated and activated successfully`. If you see an error message instead, go back and check the configuration for the Remote System record.

    We have successfully connected Instance A and Instance B together so that they can share data across their process workflows. Now, we will define how our integration will trigger and run automatically, as well as which fields we want to capture and sync between instances.

28. In Instance A, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then select the `Hardware Request Process` record from the list.

29. In the Process Events related list, select **New**.

    1.  In the Name field, enter `Request Hardware`.

        **Note:** This field is case-sensitive. It functions similarly to an API endpoint method name.

    2.  Leave all other fields as they are, and then select **Submit**.

30. In the Process Events related list, select **New**.

    1.  In the Name field, enter `Hardware Request Fulfilled`.

    2.  Leave all other fields as they are, and then select **Submit**.

31. In the Capture Definitions related list, select **New**.

    1.  In the form, fill in the following fields:

<table id="table_phs_5qv_rnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process Event

</td><td>

select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `Request Hardware` record from the list.

</td></tr><tr><td>

State

</td><td>

Select **Active**

</td></tr><tr><td>

Source Table Name

</td><td>

Select **Incident \[incident\]**

</td></tr><tr><td>

Filter

</td><td>

In the condition builder, select **Assignment Group** &gt; **is** and then select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\). Choose the `Hardware` record from the list.

</td></tr><tr><td>

Include fields

</td><td>

Select the following fields and then select the add item button \(![Add item button](../images/slushbucket-add-item-icon.png)\) to add them to the Selected list:-   Number
-   Short description
-   Assignment group
-   Severity
-   State
 **Note:** Sys ID is already included in the Selected list. Leave this field in the Selected list as well.

</td></tr></tbody>
</table>    2.  Leave all other fields as they are, and then select **Submit**.

32. In the Outbound Flows related list, select **New**.

    1.  In the form, fill in the following fields:

<table id="table_ezn_htc_snb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process Event

</td><td>

From the list, select **Request Hardware**.

</td></tr><tr><td>

Outbound Subflow

</td><td>

Select `Copy of Remote Process Sync Outbound Flow Template - Basic` record.

To make a copy, follow these steps.

1.  Use the **Configure Subflow** button next to the **Outbound Subflow** field to navigate to Workflow Studio.
2.  In Workflow Studio, select the Subflows tab.
3.  Filter the **Name** column to locate the `Remote Process Sync Outbound Flow Template - Basic` record and select it.
4.  In the subflow, select the More Actions menu, then select **Copy subflow**.
5.  **Publish** the subflow copy.
This template subflow handles the correlation of local and remote records and sends the captured payload to the remote instance.**Note:** When building your own integration, you can add [Remote Process Sync actions](../reference/remote-process-sync-actions.md) to personalize this template subflow to your needs. To edit this template subflow in Workflow Studio, select the Configure Subflow icon \(![Configure Subflow icon](../images/configure-subflow-icon.png)\).

</td></tr><tr><td>

Remote System

</td><td>

Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `Vendor Instance - Instance B` record from the list.

</td></tr></tbody>
</table>    2.  Leave all other fields as they are, and then select **Submit**.

33. In Instance B, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then select the `Hardware Fulfillment Process` record from the list.

34. In the Process Events related list, select **New**.

    1.  In the Name field, enter `Request Hardware`.

    2.  Leave all other fields as they are, and then select **Submit**.

35. In the Process Events related list, select **New**.

    1.  In the Name field, enter `Hardware Request Fulfilled`.

    2.  Leave all other fields as they are, and then select **Submit**.

        **Note:** Create Process Event records in both instances with names that match. This will help you keep track of the linked process workflows between instances.

36. In the Capture Definitions related list, select **New**.

    1.  In the form, fill in the following fields:

<table id="table_sqp_4xd_snb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process Event

</td><td>

select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `Hardware Request Fulfilled` record from the list.

</td></tr><tr><td>

State

</td><td>

Select **Active**

</td></tr><tr><td>

Source Table Name

</td><td>

Select **Incident \[incident\]**

</td></tr><tr><td>

Filter

</td><td>

In the condition builder, select **Assignment Group** &gt; **is** and then select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\). Choose the `Hardware` record from the list. Then, select **AND** to add another condition and select **Incident state** &gt; **is** &gt; **Resolved**.

</td></tr><tr><td>

Include fields

</td><td>

Select the following fields and then select the add item button \(![Add item button](../images/slushbucket-add-item-icon.png)\) to add them to the Selected list:-   Number
-   State
-   Resolved by
-   Resolution notes
-   Resolution code
 **Note:** Sys ID is already included in the Selected list. Leave this field in the Selected list as well.

</td></tr></tbody>
</table>    2.  Leave all other fields as they are, and then select **Submit**.

37. In the Outbound Flows related list, select **New**.

    1.  In the form, fill in the following fields:

<table id="table_sc4_pyd_snb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process Event

</td><td>

From the list, select **Hardware Request Fulfilled**.

</td></tr><tr><td>

Outbound Subflow

</td><td>

Select `Copy of Remote Process Sync Outbound Flow Template - Basic` record.

To make a copy, follow these steps.

1.  Use the **Configure Subflow** button next to the **Outbound Subflow** field to navigate to Workflow Studio.
2.  In Workflow Studio, select the Subflows tab.
3.  Filter the **Name** column to locate the `Remote Process Sync Outbound Flow Template - Basic` record and select it.
4.  In the subflow, select the More Actions menu, then select **Copy subflow**.
5.  **Publish** the subflow copy.
This template subflow handles the correlation of local and remote records and sends the captured payload to the remote instance.**Note:** When building your own integration, you can add [Remote Process Sync actions](../reference/remote-process-sync-actions.md) to personalize this template subflow to your needs. To edit this template subflow in Workflow Studio, select the Configure Subflow icon \(![Configure Subflow icon](../images/configure-subflow-icon.png)\).

</td></tr><tr><td>

Remote System

</td><td>

Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `Customer Instance - Instance A` record from the list.

</td></tr></tbody>
</table>    2.  Leave all other fields as they are, and then select **Submit**.

    We have successfully set up how our Remote Process Sync integration will trigger, and which fields will be captured and sent to either remote instance. In this final section, we will customize the inbound flows in Workflow Studio so that they properly transform inbound data.

38. In Instance B, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then select the `Hardware Fulfillment Process` record from the list.

39. Make a copy of the `Remote Process Sync Inbound Flow Template - Basic` record.

    1.  Navigate to Workflow Studio and select the Subflows tab.

    2.  Filter the **Name** column to locate the `Remote Process Sync Inbound Flow Template - Basic` record and select it.

    3.  In the subflow, select the More Actions menu, then select **Copy subflow**.

40. In the subflow, update the Payload.

    1.  Expand the `Transform Payload from Inbound Sample` action.

    2.  In the Sample Payload field, enter the following sample payload:

        ```
        {"capture_metadata":{"changed_by":"admin","timestamp":"2020-09-24 19:26:59"},
        "changed_fields":[
          {"display_value":"","value":"incident","key":"sys_class_name"},
          {"display_value":"","value":"552c48888c033300964f4932b03eb092","key":"sys_id"},
          {"display_value":"","value":"INC0040015","key":"number"},
          {"display_value":"","value":"","key":"short_description"},
          {"display_value":"Hardware","value":"9f5b572d9cd82010f877a5cfd1fdce30","key":"assignment_group"},
          {"display_value":"","value":"1","key":"severity"},
          {"display_value":"","value":"2","key":"state"}]}
        ```

        **Note:** This payload is a complex object that represents the captured metadata and fields that are sent from Instance A to Instance B.

    3.  Select **Done**.

41. In the subflow, under the `Else` flow logic, select **Create Incident Record**.

    1.  Add the following fields and associated values:

        |Field|Value|
        |-----|-----|
        |Short description|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **short\_description**.|
        |Description|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **short\_description**.|
        |Assignment group|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **assignment\_group**.|
        |Urgency|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **severity**.|
        |State|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **state**.|

    2.  Select **Done**.

42. Under the `If` flow logic next to `then`, select **Update Incident Record**.

    1.  In the Fields input, add the following fields and associated values:

        |Field|Value|
        |-----|-----|
        |Short description|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **short\_description**.|
        |Description|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **short\_description**.|
        |Assignment group|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **assignment\_group**.|
        |Urgency|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **severity**.|
        |State|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **state**.|

    2.  Select **Done**.

43. **Publish** the subflow.

44. Back in the Hardware Fulfillment Process record, in the Inbound Flows related list, select **New**.

    1.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Process Event|From the list, select **Request Hardware**.|
        |Inbound Subflow|Select `Copy of Remote Process Sync Inbound Flow Template - Basic`.|
        |Remote System|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `Customer Instance - Instance A` record from the list.|

    2.  Leave all other fields as they are, and then select **Submit**.

45. In Instance A, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then select the `Hardware Request Process` record from the list.

46. Make a copy of the `Remote Process Sync Inbound Flow Template - Basic` record.

    1.  Navigate to Workflow Studio and select the Subflows tab.

    2.  Filter the **Name** column to locate the `Remote Process Sync Inbound Flow Template - Basic` record and select it.

    3.  In the subflow, select the More Actions menu, then select **Copy subflow**.

47. In the subflow, update the Payload.

    1.  Expand the `Transform Payload from Inbound Sample` action.

    2.  In the Sample Payload field, enter the following sample payload:

        ```
        {"capture_metadata":{"changed_by":"admin","timestamp":"2020-10-26 14:18:45"},
        "changed_fields":[
          {"display_value":"","value":"incident","key":"sys_class_name"},
          {"display_value":"","value":"d4cdfce8db4c2410cfe4d9595e96197b","key":"sys_id"},
          {"display_value":"","value":"INC0040014","key":"number"},
          {"display_value":"","value":"101","key":"state"},
          {"display_value":"","value":"Resolved by caller","key":"close_code"},
          {"display_value":"System Administrator","value":"6816f79cc0a8016401c5a33be04be441","key":"resolved_by"},
          {"display_value":"","value":"","key":"close_notes"}]}
        ```

        **Note:** This payload is a complex object that represents the captured metadata and fields that are sent from Instance B to Instance A.

    3.  Select **Done**.

48. Under the `If` flow logic next to `then`, select **Update Incident Record**.

    1.  In the Fields input, add the following fields and associated values:

        |Field|Value|
        |-----|-----|
        |State|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **state**.|
        |Resolved by|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **resolved\_by**.|
        |Resolution notes|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **close\_notes**.|
        |Resolution code|Select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker.png)\). Dot-walk to and then select **1 - Transform Payload from Inbound Sample** &gt; **Changed Fields** &gt; **close\_code**.|

    2.  Select **Done**.

49. In the subflow, delete the `Else` statement.

50. **Publish** the subflow.

51. Back in the Hardware Fulfillment Process record, in the Inbound Flows related list, select **New**.

    1.  In the form, fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Process Event|From the list, select **Hardware Request Fulfilled**.|
        |Inbound Subflow|Select `Copy of Remote Process Sync Inbound Flow Template - Basic`.|
        |Remote System|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\), and then select the `Vendor Instance - Instance B` record from the list.|

    2.  Leave all other fields as they are, and then select **Submit**.


## Result

We've finished building our Remote Process Sync integration. The integration will now trigger whenever a user creates an Incident record with the Hardware assignment group in Incident A. When this happens:

-   The fields specified in Instance A's Capture Definition are captured and stored in a local record.
-   The local record is correlated with a remote record in Instance B.
-   The captured fields are mapped to the fields we specified in Instance B's Inbound Flow.

Then, when a user resolves the correlated Incident record in Instance B:

-   The fields specified in Instance B's Capture Definition are captured and stored in a local record.
-   The local record is correlated with the remote record in Instance A.
-   The captured fields are mapped to the fields we specified in Instance A's Inbound Flow.

## What to do next

Test out your Remote Process Sync integration by creating an Incident record in Instance A with the Hardware assignment group. Then, resolve the correlated Incident record in Instance B. If your correlated records don't sync as expected, check your Inbound API User's credentials and Process Sync Definition configuration in each Instance. If you continue to experience issues with your example integration, refer to [Monitoring and troubleshooting your integration](../reference/getting-started-with-remote-process-sync.md#monitoring-troubleshooting-rps).

