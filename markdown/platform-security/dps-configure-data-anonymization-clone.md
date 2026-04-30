---
title: Configure data anonymization clone request
description: Data privacy clone integration is configured using a PostClone script to create and execute data privacy jobs for configured policies on the target. After running the script, users will see de-identified data and will not have access to the original data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create anonymization policies, Data anonymization, Platform Privacy]
---

# Configure data anonymization clone request

Data privacy clone integration is configured using a PostClone script to create and execute data privacy jobs for configured policies on the target. After running the script, users will see de-identified data and will not have access to the original data.

## Before you begin

The data privacy PostClone script is installed with the activation of the data privacy plugin \(sn\_dp\_store\_app\). See [Activate data privacy](dps-activate-data-privacy.md) for details.

Role required: data\_privacy\_clone\_processor, data\_privacy\_admin, and admin

## Procedure

1.  Activate the data privacy plugin \(sn\_dp\_store\_app\) on the source instance.

    The data privacy PostClone script is installed.

2.  Elevate to the **data\_privacy\_admin** role.

    For details on role elevation, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

3.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

4.  Select **Create new policy**.

    See [Create anonymization policies](dps-create-anonymization-policies.md) for details.

5.  Select **Data tables or columns**.

6.  Select **Create**.

7.  Enter a name and select a data class.

8.  Select to **Activate the policy during cloning**.

9.  Select the policy order to run if there are multiple clone policies.

    A data privacy job for Postclone configuration with a higher Application Order might start before another job of lower order, if the job with the higher order does not involve any table related to other lower order job.

10. Select **Continue**.

11. Complete the policy configuration and publish the policy.

12. Back up data privacy configurations.

13. Schedule the anonymization job.

    See [Create anonymization job](dps-create-anonymization-job.md)for details.

14. As the data privacy admin, submit a clone request.


## Result

The data privacy PostClone script executes on the target Instance and The PostClone script creates a data privacy federated job record on the target instance. The federated job creates and executes a data privacy job for each post-clone policy, in Application Order, on the target instance.​The backup source is cloned to the target Instance. Data privacy PostClone script creates and executes data privacy jobs for configured policies on the target instance.

The elevated data privacy clone processor can log on to the target instance and monitor the post-clone federated job state on the dp\_federated\_job.list and dp\_job.list​.

