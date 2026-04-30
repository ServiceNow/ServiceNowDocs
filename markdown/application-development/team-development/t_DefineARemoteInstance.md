---
title: Define a remote instance
description: For each instance, define other instances in the hierarchy as remote instances.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Building an instance hierarchy, Configure, Team Development, Planning your application, Building applications]
---

# Define a remote instance

For each instance, define other instances in the hierarchy as remote instances.

## Before you begin

Role required:

-   admin role on the instance you’re registering.
-   teamdev\_user role on the instance you’re registering.

## About this task

This example demonstrates how to set up a remote instance for subdevelopment instances.

## Procedure

1.  If IP address access control is enabled, log in to the remote instance and add the subdevelopment instance as an exception.

2.  On the subdevelopment instance, navigate to **Team Development** &gt; **Remote Instances**.

3.  Select **New**.

4.  Define the remote instance, such as the parent development instance, by completing the form.

5.  Fill in the form.

<table id="table_mbs_gx1_bq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name describing the instance.

</td></tr><tr><td>

Type

</td><td>

Specify whether the remote instance is a development, test, or UAT instance.

</td></tr><tr><td>

Active

</td><td>

Specify whether the local instance communicates with the remote instance as a member of Team Development. **Note:** Team Development operations such as comparing changes between instances or selecting a parent instance are only available for active remote instances.

</td></tr><tr><td>

URL

</td><td>

Specify the URL of the remote instance using the appropriate transfer protocol. Each remote instance record should have a unique URL. **Note:** Creating duplicate records with the same URL can cause errors.

</td></tr><tr><td>

User name

</td><td>

Enter the user on the remote instance who authorizes Team Development operations on the instance. **Note:** This user account must have an appropriate role on the remote instance.

</td></tr><tr><td>

Password

</td><td>

Enter the password of the authorizing user.

</td></tr><tr><td>

Short description

</td><td>

Enter any other relevant information about the remote instance.

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  Repeat step 1 through step 5 for each instance in the hierarchy that this instance interacts with.


**Parent Topic:**[Building an instance hierarchy](../concept/c_InstanceHierarchies.md)

