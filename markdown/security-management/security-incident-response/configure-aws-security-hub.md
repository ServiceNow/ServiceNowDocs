---
title: Register and configure the AWS Security Hub portal
description: Register your application in the AWS Security Hub portal and grant your users with read and write access to the application.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Register and configure the AWS Security Hub portal

Register your application in the AWS Security Hub portal and grant your users with read and write access to the application.

## Registering a ServiceNow® user profile on AWS portal

## Before you begin

Role required: AWSSecurityHubFullAccess

## Procedure

1.  Log in to the AWS portal.

2.  Navigate to **Identity and Access Management \(IAM\)** &gt; **Users** &gt; **Create New User**.

3.  The following table describes the fields that you must configure to create a user profile:

<table id="table_hbz_vdx_2dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Specify user details** &gt; **User name**

</td><td>

Name for the user profile.

</td></tr><tr><td>

**Set permissions** &gt; ******Add user to group**

</td><td>

Add the user profile to a group with predefined permission policies.You can create a group according to your preference and assign permission policies to the group. Later, you can add user profiles to the group and the permission policies assigned to the group is automatically assigned to the user profiles.

</td></tr><tr><td>

**Copy permissions**

</td><td>

Copy permissions from a user profile and assign the same to the new user profile.

</td></tr><tr><td>

**Attach policies directly**

</td><td>

Add AWSSecurityHubFullAccess as the permission policy for your user profile.Assign a new permission policy to the user profile according to your preference.

</td></tr><tr><td>

Review and create

</td><td>

Review all the details that you added in the user profile.

</td></tr></tbody>
</table>4.  Select **Create user**.

5.  Select **View user** from the displayed pop-up window.

6.  Create an access key and a secret access key for the user profile.

    You require these keys to access the AWS Security Hub integration from your ServiceNow® instance.

7.  Navigate to **AWS Services** &gt; **Search** &gt; **AWS Security Hub** &gt; **.**

8.  Select **Go to Security Hub**.

9.  In the Enable AWS Security Hub page, select **Download** to enable AWS Config.

    Download the files and run them in your account. This grants you permission to gather all the information from various AWS reporting services and aggregate into AWS Security Hub.

10. Select **Enable AWS Security Hub**at the bottom of the page.

    It takes a few moments for the AWS Security Hub Dashboard to display all the details.

11. Change Region from **Global** to **US East \(Ohio\)**.

    The code for **US East \(Ohio\)** is **us-east-2**. All ServiceNow® resources are assigned to this region code.


