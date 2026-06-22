---
title: Display the priorities and goals on the project form
description: If you are an existing user, configure the project form to upgrade to the Goal Framework. The benefit of the Goal Framework is that it enables you to set targets for goals. You can also define strategic priorities and associated goals as part of the organization's strategic plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/environmental-social-governance/operational-sustainability-management/configure-project-form.html
release: zurich
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an Operational Sustainability Management \(formerly ESG Management\) goal, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Display the priorities and goals on the project form

If you are an existing user, configure the project form to upgrade to the Goal Framework. The benefit of the Goal Framework is that it enables you to set targets for goals. You can also define strategic priorities and associated goals as part of the organization's strategic plans.

## Before you begin

Role required: sys\_admin

## About this task

If you have preconfigured forms, you must do this configuration to make the new framework features and fields available. The following images show the form fields before and after configurations.

\[Omitted image "before-config.png"\] Alt text: Before configuration of new fields, the framework has the Strategies field and the Goals field.

\[Omitted image "after-configuration.png"\] Alt text: After configuration of new fields, the framework has the Strategic priority field and the Primary goal field.

The same procedure can be performed on the Demand and Program forms as well. For more information, see [Goal framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/goal-framework/goal-framework.md).

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Open a project.

3.  Click the additional actions icon \(\[Omitted image "additional-information.png"\] Alt text: Additional actions icon.\) and do the following:

    1.  Click **Configure**.

    2.  Click **Form Layout**.

    3.  Under the Form view and section, set the **View name** field to the view that has the goal and strategy Glide list.

    4.  Under the Form view and section, set the **Section** field to **Business Case**.

    5.  In the Available list, select **Primary goal \[+\]** and click the tree workflow icon \(\[Omitted image "tree-workflow.png"\] Alt text: Tree workflow icon.\).

    6.  In the Available list, double-click **Strategic priority \[+\]**.

        The Selected list shows **Primary goal.Strategic priority**.

    7.  Click **Save**.

    Repeat this step for all the views that have the goal and strategy Glide list, such as Score and Financial.


## Result

The Project form shows the **Strategic priority** field and the **Primary goal** field.

**Parent Topic:**[Create an Operational Sustainability Management \(formerly ESG Management\) goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/environmental-social-governance/operational-sustainability-management/create-esg-goal.md)

