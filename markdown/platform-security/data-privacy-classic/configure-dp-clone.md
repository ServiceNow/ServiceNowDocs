---
title: Configure data privacy clone request
description: Data privacy clone integration is configured using a PostClone script to create and execute data privacy jobs for configured policies on the target. After running the script, users will see de-identified data and will not have access to the original data.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data privacy clone, Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Configure data privacy clone request

Data privacy clone integration is configured using a PostClone script to create and execute data privacy jobs for configured policies on the target. After running the script, users will see de-identified data and will not have access to the original data.

## Before you begin

Role required: data\_privacy\_clone\_processor, data\_privacy\_admin, and admin

## Procedure

1.  Activate the data privacy plugin \(sn\_dp\_store\_app\) on the source instance.

    The plugin can only be installed by Customer Service and Support.

    The data privacy PostClone script is installed.

2.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

3.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Privacy Policy Configuration**.

4.  Create a Privacy Policy configuration.

    Select **Apply to All in Data Class** and **Apply when Cloning**. See [Create a data privacy policy](config-dp-policy.md) for more information.

5.  Back up data privacy configurations.

6.  As the data privacy admin, submit a clone request.


## Result

The data privacy PostClone script executes on the target Instance and The PostClone script creates a data privacy federated job record on the target instance. The federated job creates and executes a data privacy job for each post-clone policy, in Application Order, on the target instance.​The backup source is cloned to the target Instance. Data privacy PostClone script creates and executes data privacy jobs for configured policies on the target instance.

The elevated data privacy clone processor can log on to the target instance and monitor the post-clone federated job state on the dp\_federated\_job.list and dp\_job.list​.

