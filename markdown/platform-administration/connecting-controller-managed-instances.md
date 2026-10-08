---
title: Connecting controller and managed instances
description: Connecting a production instance to the non-production instances it manages involves three steps: setting the controller, adding the instances to manage, and approving requests to manage instances.Set a production instance as a controller that manages non-production instances.Add non-production instances to a controller and request approval for the controller to manage them.Review a request to allow a controller to manage an instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/connecting-controller-managed-instances.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 4
keywords: [controller instance, managed instances, Multi-Instance Setup, controller instance, Multi-Instance Setup, production instance, add instance, automatic scan, managed instances, action needed, approve request, resend request]
breadcrumb: [Multi-Instance Setup, Multi-Instance Management, Get started, Administer the ServiceNow AI Platform]
---

# Connecting controller and managed instances

Connecting a production instance to the non-production instances it manages involves three steps: setting the controller, adding the instances to manage, and approving requests to manage instances.

Before a production instance can manage non-production instances, you must set it as the controller. Then, you connect it to one or more non-production instances by adding them as managed instances. Adding a managed instance automatically sends an access request to that instance's administrator, and after the admin approves the request, the connection is active.

## Set a production instance as a controller

Set a production instance as a controller that manages non-production instances.

### Before you begin

[Install Multi-Instance Setup and AMF Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/install-multi-instance-setup.md).

Role required: sn\_amf.amf\_core\_admin or admin

### About this task

The controller, or manager, is a production instance used to manage connected non-production instances. A production instance must be set as a controller before you can discover or add non-production instances.

### Procedure

1.  From a production instance, navigate to **All** &gt; **Multi-Instance Setup** &gt; **Multi-Instance Setup**.

2.  From the pop-up window, select **Set as controller**.


### What to do next

From the controller instance, you can discover or add any non-production instances that you want to manage.

## Add managed instances to the controller

Add non-production instances to a controller and request approval for the controller to manage them.

### Before you begin

A production instance must be set as a controller, or manager, that can manage non-production instances.

To detect non-production instances to manage, you must install the AMF Core plugin \(com.glide.amf\) on any non-production instance that you want a controller to manage. For more information, see [Install Multi-Instance Setup and AMF Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/install-multi-instance-setup.md).

Role required: sn\_amf.amf\_core\_admin or admin

### About this task

To add managed instances, you can run a scan to automatically discover related non-production instances or add them manually. Each instance has an assigned environment type, which identifies a managed instance's role in your application life cycle. Multi-Instance Setup uses three default environment types \(Development, Test, and Production\) but you can create custom environment types if needed.

The environment type can be used by other ServiceNow applications that use Multi-Instance Management for cross-instance communication, such as Developer Sandboxes. Otherwise, custom environment types are primarily a label for your own use.

**Note:** Multi-Instance Setup adds environment types on top of the Multi-Instance Management framework, which only distinguishes non-production instances from production instances.

### Procedure

1.  From the controller instance, navigate to **All** &gt; **Multi-Instance Setup** &gt; **Multi-Instance Setup**.

2.  Select **Add instance**.

3.  From the pop-up window, select one of the following options for adding instances.

<table><thead><tr><th align="left" id="d320863e305">

Option

</th><th align="left" id="d320863e308">

Description

</th></tr></thead><tbody><tr><td id="d320863e314">

**Run scan**

</td><td>

Run a scan to automatically discover related non-production instances. The scan reads the instance's defined update set sources, such as a source connecting a test instance to a production instance, to identify instances and their environment types.

1.  Review the discovered instances and their environments.
2.  Select **Save and request access**.
If no instances are discovered, select **Add another instance** to add instances manually instead.

</td></tr><tr><td id="d320863e341">

**Skip and set up manually**

</td><td>

Manually add an instance if you already know the instance name and environment.

 1.  From the Instance drop-down list, select an instance.
2.  From the Environment drop-down list, complete one of the following steps:
    -   Select an existing environment type.
    -   Enter a name for the environment and select **Create environment**.
3.  To add more instances, select **Add another instance** and repeat the previous steps.
4.  Select **Save and request access**.


</td></tr></tbody>
</table>
### Result

Multi-Instance Setup automatically sends a request to each instance's admin to grant management control to the controller instance. In the Status column of the Managed Instances list, an instance appears with a status of Approval pending until the admin responds to the request. In the Action needed column, you can select a link to open the request in the non-production instance.

If you need to change an environment assignment after adding an instance, select **Edit** to change the environment for one or more instances.

### What to do next

The admins for each non-production instance must review and approve requests to manage instances and make connections active.

## Review a request to manage an instance

Review a request to allow a controller to manage an instance.

### Before you begin

Role required: sn\_amf.amf\_core\_admin or admin

### Procedure

1.  Navigate to a request in one of the following ways depending on the instance type.

<table id="choicetable_rjs_qcs_lkc"><thead><tr><th align="left" id="d320863e480">

Option

</th><th align="left" id="d320863e483">

Description

</th></tr></thead><tbody><tr><td id="d320863e489">

**From the non-production instance**

</td><td>

Navigate to **All** &gt; **Multi-Instance Management** &gt; **Instance Configuration** &gt; **Manager Instances**.

</td></tr><tr><td id="d320863e513">

**From the controller instance**

</td><td>

1.  Navigate to **All** &gt; **Multi-Instance Setup** &gt; **Multi-Instance Setup**.
2.  From the Managed Instances list, identify an instance that has a status of Approval pending.
3.  From the Action needed column, select the link to open the pending request.
4.  Select **Go to requests**.

On the non-production instance, the Manager Instances list that contains all requests from controllers opens.

</td></tr></tbody>
</table>2.  From the Approval column of the Manager Instances list, select one of the following options:

    -   **Approve** to grant the controller access to manage the instance.
    -   **Reject** to deny the controller access to manage the instance.

### Result

If a request is approved, the connection between the controller and managed instance is active. This connection supports cross-instance communication and data sharing with other ServiceNow applications, such as Developer Sandboxes, Automated Test Framework, and more.

To resend a request that was previously rejected, you must add the non-production instance to the controller as a managed instance again. For more information, see [Add managed instances to the controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/connecting-controller-managed-instances.md).

