---
title: Configure Playbook
description: Set up an end-to-end playbook, from intake on portal all the way to decision stage.Set up an end-to-end playbook, from intake on portal all the way to decision stage, using the default Social Benefits Playbook playbook as a template.Configure the record generator for a benefit program.Create a playbook content item so that users can navigate to the Nutrition Assistance application from the service catalog on the Government Service Portal.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-29"
reading_time_minutes: 4
breadcrumb: [Social Benefits Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Playbook

Set up an end-to-end playbook, from intake on portal all the way to decision stage.

Social benefit applications are characterized by significant complexity due to intricate eligibility criteria and extensive documentation requirements. Playbooks and Playbooks on Portal capabilities can be leveraged by agencies to provide guided application processes from end to end.

## Configure the Playbook Process for a social benefit program in Social Benefits Playbook

Set up an end-to-end playbook, from intake on portal all the way to decision stage, using the default Social Benefits Playbook playbook as a template.

### About this task

Create variant\(s\) of the default Social Benefits Playbook process, tailoring the default playbook flow to meet customer needs. Duplicate the default playbook flow to create a new instance of the playbook.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    Workflow Studio opens in a new window.

2.  In the Processes list, select **Social Benefits Playbook**.

3.  Select the **More actions** icon \(\) and select **Duplicate**.

4.  Update the Label field to the name of the Social Benefit program you are duplicating the playbook for.

    For example, for a Nutrition Assistance benefit program, enter **Nutrition Assistance**.

5.  Enter a brief description of the benefit program to a brief description of the benefit program.

    For example, for a Nutrition Assistance benefit program, you may enter `Manage applications for the nutrition assistance benefit program`.

6.  Select **Duplicate**.

7.  Once the playbook has been created, select **Board view** to open a view of the Playbook’s stages and activities.

8.  Review the playbook’s stages and activities and make changes as needed.

    By default, the Social Benefits Playbook Packaged Application has four stages: Intake, Review, Process, and Decision. All intake activities are available for constituents to complete on the Government Service Portal.

9.  Select the More Actions icon \(three dots down icon\) next to each activity, then select **Configure subflow in Flow Designer**.

10. Review the subflows that power each activity, and make changes as needed.

    A subflow is a sequence of reusable actions and data inputs. Each default playbook activity in the Social Benefits Playbook Packaged Application has a default corresponding subflow.

11. Select **Activate** once you have made any changes.


## Configure the playbook record generator for a social benefit program in Social Benefits Playbook

Configure the record generator for a benefit program.

### About this task

Playbooks require a record to be created or updated before a process can start.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Record Generators**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_vjx_kcg_t3c"><thead><tr><th>

Record Generator form field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Social Benefit Case

</td></tr><tr><td>

Process Definition

</td><td>

Enter the name of the social benefit program.For example, for a Nutrition Assistance benefit program, enter **Nutrition Assistance**.

</td></tr><tr><td>

Create Record Activity Nam

</td><td>

 

</td></tr><tr><td>

Create Record Form View

</td><td>

recordgenerator

</td></tr><tr><td>

Template Fields: Product

</td><td>

Enter the name of the social benefit program.For example, for a Nutrition Assistance benefit program, enter **Nutrition Assistance**.

</td></tr><tr><td>

Template Fields: Service

</td><td>

Enter the service being provided for the social benefit program. For example, for a Nutrition Assistance benefit program, enter **Apply for Nutrition Assistance**.

</td></tr></tbody>
</table>4.  Select **Submit**.


### Result

A new record generator has been created. This will capture details of.

## Create a catalog item for a social benefit program

Create a playbook content item so that users can navigate to the Nutrition Assistance application from the service catalog on the Government Service Portal.

### About this task

Playbooks require a record to be created or updated before a process can start.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Content Items**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Playbook Content Item form field|Description|
    |--------------------------------|-----------|
    |Name| |
    |Catalogs| |
    |Category| |
    |Short Description| |
    |Table|Social Benefit Case|
    |Playbook Experience| |
    |Playbook Experience Record Generator|Enter `sn_gsm_social_benefits_case`.|
    |Portal Page| |
    |Title| |

4.  Select **Submit**.

5.  Select the newly created content item.

6.  In the **Available For** related list, select **Edit...**.

7.  Select **SNC External** in the Collection list, then select **&gt;** to add it to the Available For list.

8.  Select **Save**.

9.  In the **Not Available For** related list, select **Edit...**.

10. Select **SNC External** in the Collection list, then select **&lt;** to remove it from the Not Available For list.

11. Select **Save**, then select **Update**.


### Result

A catalog item has been created and can now be accessed by constituents using the Government Service Portal once it is published. To verify that the content item was created, navigate to the Government Service Portal and select **Services** &gt; **Social Benefits** and verify the playbook content item displays in the catalog.

### What to do next

Update the service definition for this playbook duplicate to include the record generator for this social benefit program by navigating to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**, and entering `sn_gsm_social_benefits_case` in the record generator field. For more information on how to create and update service definitions for social benefits, see .

