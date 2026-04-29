---
title: Associate tool objects to applications – Classic
description: After creating an application, you can associate plans, repositories, pipelines, and artifacts with it.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Applications, DevOps Change Velocity, IT Service Management]
---

# Associate tool objects to applications – Classic

After creating an application, you can associate plans, repositories, pipelines, and artifacts with it.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.app\_owner

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Apps &amp; Pipelines** &gt; **Apps**.

2.  Select the application.

3.  From the application record page, select the related list for the object type that you want to associate.

<table id="choicetable_ewm_tlh_wwb"><thead><tr><th align="left" id="d275118e77">

Object type

</th><th align="left" id="d275118e80">

Steps

</th></tr></thead><tbody><tr><td id="d275118e86">

**Plans**

</td><td>

1.  Select the **Plans** related list.
2.  Select **Edit**.
3.  From the list of plans available in DevOps, select the plans to track and associate with the application.
4.  Select **Save**.


</td></tr><tr><td id="d275118e122">

**Repositories**

</td><td>

1.  Select the **Repositories** related list.
2.  Select **Edit**.
3.  From the list of repositories available in DevOps, select the repositories to track and associate with the application.
4.  Select **Save**.
 **Note:** When the property **Enable automatic association of repos to apps on pipeline execution** is enabled, repositories are automatically assigned to applications when a pipeline associated with an app identifies commits of a repository that is not yet associated.

</td></tr><tr><td id="d275118e165">

**Pipelines**

</td><td>

1.  Select the **Pipelines** related list.
2.  Select **Edit**.
3.  From the list of pipelines available in DevOps, select the pipelines to track and associate with the application.
4.  Select **Save**.
 **Note:** While associating a pipeline with an app, the pipeline steps are also fetched during import.

 **Note:** When the property **Enable automatic association of repos to apps on pipeline execution** is enabled, if a repository is already associated to an application, then the corresponding unassigned pipelines are automatically assigned to the same app.

</td></tr></tbody>
</table>
