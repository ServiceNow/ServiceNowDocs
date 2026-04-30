---
title: Create opportunities in Opportunity Marketplace
description: Opportunity owners create gigs, projects, and volunteer opportunities. Opportunity details for Project type opportunities can be imported from projects in the ServiceNow Project Workspace. These opportunities are different from internal jobs. OPM enables you to manage any opportunities you create and track applications. The ability to create opportunities is based on user criteria.
locale: en-US
release: yokohama
product: Opportunity Marketplace
classification: opportunity-marketplace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use Opportunity Marketplace, Opportunity Marketplace, Talent Development, Employee Service Management]
---

# Create opportunities in Opportunity Marketplace

Opportunity owners create gigs, projects, and volunteer opportunities. Opportunity details for Project type opportunities can be imported from projects in the ServiceNow Project Workspace. These opportunities are different from internal jobs. OPM enables you to manage any opportunities you create and track applications. The ability to create opportunities is based on user criteria.

## Before you begin

Role required: No role required, but you must be a licensed user for the Talent Development features.

**Note:** Access is based on user criteria.

## Procedure

1.  From the Employee Center, go to **Opportunity Marketplace** &gt; **Opportunities you own**.

    Any existing opportunities that you own are listed. For the first opportunity you create, you see the message **No opportunities yet**.

2.  Select **Create an opportunity**.

    The **Create an opportunity** widget is started. There are 3 opportunity templates provided with the base system. If you need a different opportunity type, you can create your own custom opportunity types.

    **Note:**

    Access to create custom opportunities is controlled by user criteria maintained in the Opportunity Type table \[sn\_opp\_market\_opportunity\_type\].

    Creating and editing of opportunity, position, or application table records from lists and forms can result in unwanted behavior. Lists and forms should be updated from the Employee Center portal.

    -   Gig: For details on gigs, see [Gig opportunities](../concept/egd-oppt-mrktplc-gig.md).
    -   Project: For details about what a project is, see [Project opportunity](../concept/egd-oppt-mrktplc-project.md)
    -   Volunteer: For details about what a volunteer opportunity is, see [Volunteer opportunities](../concept/egd-oppt-mrktplc-volunteer.md)
    **Tip:** If you need a different opportunity type, you can create custom opportunity types. For more details, read [Creating custom opportunity types in Opportunity Marketplace](../concept/egd-oppt-mrktplc-custom-oppt-type.md).

3.  Select a template, then select **Next**.

4.  Fill in the form with the details for the opportunity that you selected.

    1.  From the **Opportunity owner** list, select co-owners to an opportunity to enable management of the opportunity.

        The user who creates the opportunity is by default the owner of the opportunity. You can add additional owners by selecting users from the list.

    2.  From the **Who can view this opportunity?** list, select one or more groups to enable members of the group to view the opportunity.

        User criteria control who can view opportunities. Leaving this field empty, enables everyone in your organization to see the opportunity. Select user groups to restrict access to the members of the selected groups.

        For information about creating user groups, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    To read details about the opportunity forms and fields, see [Form fields for creating opportunities in Opportunity Marketplace](../reference/egd-oppt-mrktplc-oppty-form-fields.md).

5.  Select **Next**.

6.  Select **Add a role**.

    **Note:** Because a gig can contain only one role, adding additional roles isn't available for Gig opportunities.

7.  Fill in the form with the role details.

    To read more details about the role form and fields, see [Form fields for creating opportunities in Opportunity Marketplace](../reference/egd-oppt-mrktplc-oppty-form-fields.md).

8.  Review the details of your opportunity.

    Select the **Edit** icon if you must change any of the details.

9.  When you’re satisfied with your opportunity, select **Publish**.

    You may be prompted to **Submit for approval** instead. This occurs when the opportunity meets specific conditions, requiring approval prior to publishing. For more information, see [Opportunity publishing approval](../concept/egd-oppt-pubs-approval.md).


**Parent Topic:**[Use Opportunity Marketplace](../concept/egd-oppt-mrktplc-using.md)

