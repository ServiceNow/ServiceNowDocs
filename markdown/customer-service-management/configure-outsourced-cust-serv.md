---
title: Configure Outsourced Customer Service
description: Configure various components of Outsourced Customer Service based on the specific requirements of your organization.Configure various aspects of Outsourced Customer Service based on the specific requirements of your organization.OSP managers and agents view cases based on the defined outsourced criteria. Defining outsourcing criteria can be based on account, asset, consumer, or sold product. For example, consumer-based criteria could be defined for all Spanish speaking consumers and all consumers based out of Australia.An administrator creates groups and associates it to an OSP. This group is the default group to which the case is assigned to when an OSP agent transfers the unresolved case back to an enterprise.An administrator creates Outsourced Service Providers \(OSPs\) after which OSP managers and agents must be onboarded to manage and fulfill cases. As an administrator you can onboard both the OSP managers and agents.An enterprise creates Outsourced Service Providers \(OSPs\) to provide customer service to external customers.Run diagnostics, review and customize components, and start collecting data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Outsourced Customer Service, Extend capabilities, Configure, Customer Service Management]
---

# Configure Outsourced Customer Service

Configure various components of Outsourced Customer Service based on the specific requirements of your organization.

## Set up Outsourced Customer Service

Configure various aspects of Outsourced Customer Service based on the specific requirements of your organization.

### Before you begin

Role required: sn\_csm\_ocs.csm\_ocs\_admin

### About this task

There’s a sequence of tasks that enable you to configure Outsourced Customer Service. You can perform these tasks based on the plugin you activated. Certain setup tasks apply only if you activated the Outsourced Customer Service plugin and this point is noted at the top of each task.

To configure Outsourced Customer Service, use the Customer Service guided setup. The guided setup takes you through the entire setup and configuration process.

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Outsourced Customer Service** &gt; **Guided Setup**.

    The Outsourced Customer Service Guided Setup page is displayed.

2.  On the Onboarding Outsourced Service Provider \(OSP\) window, select **Get Started**.

3.  View the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Setup Outsourced Service Provider

</td><td>

Creates an OSP by specifying the internal manager and setting up transfer group.**Note:** Whenever an OSP is set up and mapped, it automatically creates a company record.

</td></tr><tr><td>

Setup Outsourcing Criteria

</td><td>

Defines outsourcing criteria based on account, consumer, asset, and sold product. OSP agents can view all the cases matching the outsourcing criteria. For example, consumer-based criteria can be defined for all Spanish speaking consumers and all consumers based out of Australia.

</td></tr><tr><td>

Onboard Manager

</td><td>

Onboard OSP manager for managing cases and agents. Once onboarding is complete, a password reset email is sent to the manager's email id.

</td></tr><tr><td>

Setup Assignment Groups

</td><td>

Creates a group and associates it to an OSP manager. OSP manager assigns cases to the agents assigned to the group.

</td></tr><tr><td>

Onboard Agent

</td><td>

Onboard agents for an OSP for fulfilling cases. Once onboarding is complete, a password reset email is sent to the agents email id.

</td></tr></tbody>
</table>4.  Go back to the Outsourced Customer Service Guided Setup page.

5.  On the Case Routing and Assignment window, click **Get Started**.

6.  View the list of tasks to configure the feature.

    |Task|Description|
    |----|-----------|
    |Create Matching Rules|Rules to identify customer service cases that meet certain conditions.|
    |Create Assignment Rules|Cases that meet certain conditions based on the rules created are routed to customer service agents.|

7.  To perform a task, select **Configure**.

    This button opens the page in your instance where the configuration is completed.


## Define outsourcing criteria

OSP managers and agents view cases based on the defined outsourced criteria. Defining outsourcing criteria can be based on account, asset, consumer, or sold product. For example, consumer-based criteria could be defined for all Spanish speaking consumers and all consumers based out of Australia.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Outsourced Service Providers**.

2.  Select the OSP name.

3.  Select **Outsourcing Criteria** related list.

4.  Select **New**.

5.  Fill in the fields on the new record form, as appropriate.

<table id="choicetable_nmd_nql_mlb"><thead><tr><th align="left" id="d116418e388">

Option

</th><th align="left" id="d116418e391">

Description

</th></tr></thead><tbody><tr><td id="d116418e397">

**Description**

</td><td>

Description for the outsourcing criteria.

</td></tr><tr><td id="d116418e406">

**Table**

</td><td>

The table that stores the task for which the outsourcing criteria is created. Select either **Account**, **Asset**, **Consumer**, or **Sold Product** tables.

</td></tr><tr><td id="d116418e427">

**Condition**

</td><td>

The conditions in which the outsourcing criteria apply.Use the buttons in this field to build one or more conditions on the selected table. A condition is made up of a selected field, an operator, and a value. Add conditions using the **AND** and **OR** buttons. Delete conditions by selecting the **X** to the right of a condition.

</td></tr></tbody>
</table>6.  Select **Submit**.

    OSP managers and agents can now view assigned cases which meet the condition under **All Cases**, **Unassigned Cases**, **My Cases**, and **Open Cases**. For example, if an OSP organization has been created with outsourcing criteria with the consumer table selected, an agent belonging to this OSP can view cases created by a consumer.


### What to do next

Create groups and set assignment rules for the OSPs.

## Create groups and assignment rules

An administrator creates groups and associates it to an OSP. This group is the default group to which the case is assigned to when an OSP agent transfers the unresolved case back to an enterprise.

### Before you begin

Role required: admin

### Procedure

1.  Select an OSP you have created.

2.  Go to **Groups** related list.

3.  Click **New**.

4.  Fill in the fields on the Outsourced Service Provider form, as appropriate.

    |Option|Description|
    |------|-----------|
    |**Name**|The OSP group name.|
    |**Group email**|Group email distribution list or the email address of the group's point of contact, such as the group manager.|
    |**Manager**|The OSP manager's name.|
    |**Type**|Category for this group. For example, a group designated as type **catalog** is a service catalog group and can also be accessed under the **Service Catalog** &gt; **Catalog Policy** &gt; **Fulfillment Groups** module.|
    |**Description**|Helpful information about the group.|

5.  Click **Submit**.

6.  Click **Group Staff** related list to view the list of members for the selected group.

7.  Click **Assignment Rules** related list to define assignment rules.

8.  Click **Submit**.


## Onboard Outsourced Service Provider staff

An administrator creates Outsourced Service Providers \(OSPs\) after which OSP managers and agents must be onboarded to manage and fulfill cases. As an administrator you can onboard both the OSP managers and agents.

### Before you begin

Role required: user\_admin

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Outsourced Service Providers**.

2.  Select an existing OSP.

3.  Select the **Onboard Staff** related link.

4.  Fill in the fields on the Outsourced Service Provider form, as appropriate.

    |Option|Description|
    |------|-----------|
    |**First Name**|The first name of the OSP manager or agent.|
    |**Last Name**|The family name of the OSP manager or agent.|
    |**User ID**|A unique ID for the OSP manager or agent.|
    |**Role**|The role to onboard, such as an agent or a manager.|
    |**Email**|The OSP manager or agent's email address.|
    |**Outsourced Service Provider**|The OSP that you have selected.|
    |**Mobile Phone**|The OSP manager or agent's mobile phone number.|
    |**Business Phone**|The OSP manager or agent's business phone number.|
    |**Assignment Group**|Select the group that was created while creating an OSP.|

    **Note:** A new OSP staff member record is created and the OSP is created in the **Organization** field of the service organization external staff \[sn\_csm\_service\_organization\_external\_staff\] table. Additionally, the same change applies to other related lists, including Onboard Agent, ​Onboard Manager, ​Create Group​, Transfer Case, ​Register Staff​, and Register Member.

5.  Select **Submit**.

    The onboarded staff records are visible under the **Service Organization Staff** related list.

    **Note:** Once onboarding is complete, a password reset email is sent to the manager's or agent's email address.


## Create an Outsourced Service Provider

An enterprise creates Outsourced Service Providers \(OSPs\) to provide customer service to external customers.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Outsourced Service Providers**.

2.  Select **New**.

3.  Fill in the fields on the Outsourced Service Provider form, as appropriate.

<table id="choicetable_ckq_svb_hlb"><thead><tr><th align="left" id="d116418e970">

Option

</th><th align="left" id="d116418e973">

Description

</th></tr></thead><tbody><tr><td id="d116418e979">

**Name**

</td><td>

The OSP's name.

</td></tr><tr><td id="d116418e988">

**Service Provider Type**

</td><td>

Customer or Field service provider.

</td></tr><tr><td id="d116418e997">

**Manager**

</td><td>

The OSP's manager name.

</td></tr><tr><td id="d116418e1006">

**Website**

</td><td>

The web address for the internal business location.

</td></tr><tr><td id="d116418e1016">

**Notes**

</td><td>

Any note regarding the OSP.

</td></tr><tr><td id="d116418e1025">

**Company**

</td><td>

The company or organization to which the OSP belongs.**Note:** The **Company** field is a read-only field. Additionally, there’s a 1:1 relationship between an OSP and a company. It means that only one company record can be mapped to an OSP record at any given time.

</td></tr><tr><td id="d116418e1039">

**Active**

</td><td>

Enables the OSP. The default value is set to **True**.

</td></tr><tr><td id="d116418e1051">

**Contact**

</td><td>

Enter **Phone** or **Fax phone** number.

</td></tr><tr><td id="d116418e1066">

**Address**

</td><td>

The OSP's postal address. The following address fields are available by default:

-   Street
-   City
-   State/Province
-   ZIP/Postal Code
-   Country


</td></tr><tr><td id="d116418e1094">

**Case Transfer**

</td><td>

Search and select the **Case transfer group**, which is the default group to which the case is assigned when an OSP agent transfers the case.

</td></tr></tbody>
</table>    The following fields on the company record are automatically updated whenever you update them on the OSP record:

    -   **Name**
    -   **Street**
    -   **City**
    -   **State**
    -   **Zip/Postal Code**
    -   **Country**
    -   **Latitude**
    -   **Longitude**
    -   **Fax phone**
    -   **Phone**
    -   **Website**
    -   **Active**
4.  Select **Submit**.


### What to do next

Define outsourcing criteria so that cases matching the criteria are visible to the OSP managers and agents.

**Related topics**  


[Outsourced Service Provider agent tasks](osp-agent-tasks.md)

[Outsourced Service Provider manager tasks](osp-manager-tasks.md)

## Configure the Performance Analytics for the Outsourced Customer Service

Run diagnostics, review and customize components, and start collecting data.

### Before you begin

A ServiceNow AI Platform administrator must have installed the content pack plugins or ServiceNow Store application for this Platform Analytics Solution.

Role required: pa\_admin

### Procedure

1.  Run all diagnostics on all records, as described in Performance Analytics diagnostics.

    These diagnostics can catch many mismatches between the configuration of your Platform Analytics Solutions and your tables.

2.  Navigate to **Performance Analytics** &gt; **Administration Console**.

3.  Click the **Dashboards** link in the **Explore and Manage** tile.

4.  Verify the names of the dashboards that have been installed with this Platform Analytics Solution

5.  Open the **Indicator Sources** tab.

6.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the indicator sources on the dashboard name.

        This screenshot shows the indicator sources filtered on the Outsourced Service Provider dashboard from the Self-Service Analytics for CSM Platform Analytics Solution.![The Indicator source for Outsourced Service Provider dashboard.](../image/osp-indicator-dashboard.jpg)

    2.  Review the facts table, conditions, and frequency of the indicator sources compared to the data structure on your own instance.

    3.  If necessary, open an indicator source and make corrections.

    4.  If you are editing an indicator source record, go to the Indicators related list and review the **Conditions** field for each indicator.

        Changing the indicator source can also affect the additional conditions on the individual indicators.

7.  If you changed the time field stamps in any indicator sources, also change any related Performance Analytics scripts.

8.  Open the Breakdown Sources tab.

9.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the breakdown sources on the dashboard name.

10. Navigate to **Performance Analytics** &gt; **Jobs**.

11. Set up and run the historical job for this Platform Analytics Solution, &lt;name of historical job&gt;.

12. Edit and activate the scheduled data collection job for this Platform Analytics Solution, &lt;name of scheduled job&gt;


