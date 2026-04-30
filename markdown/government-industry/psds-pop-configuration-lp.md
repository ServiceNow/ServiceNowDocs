---
title: Configuring Playbooks-on-portal for a custom case type
description: As an admin, you can configure the playbooks-on-portal experience for a custom case type that extends the base License and Permit case.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [License and Permit Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configuring Playbooks-on-portal for a custom case type

As an admin, you can configure the playbooks-on-portal experience for a custom case type that extends the base License and Permit case.

## Before you begin

Role required: admin

## About this task

Admins can create variants of the License &amp; Permit Playbook process to use for a custom case type.

## Procedure

1.  Duplicate the playbook process by navigating to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  In the Playbooks list, select the **Licenses/Permits Playbook**.

3.  Select the More Actions \(…\) menu and select **Duplicate**.

4.  Fill in the **Label** field with the desired name for the playbook and add a description.

    The trigger type should be **Record Create**.

5.  Select **Duplicate**.

6.  Modify the playbook for the particular license use case, then select **Activate**.

7.  Navigate to **All** &gt; **Record Generators**.

8.  Select **New**.

9.  On the form, fill in the fields with the following:

<table id="table_mdc_2bz_gdc"><thead><tr><th>

Field

</th><th>

Entry

</th></tr></thead><tbody><tr><td>

Table

</td><td>

License and Permit Case, or the extended License and Permit table. *This is the table the record generator will trigger for.*

</td></tr><tr><td>

Process Definition

</td><td>

Name of the playbook created in the previous section.

</td></tr><tr><td>

Create Record Activity Name

</td><td>

Answer Eligibility Questions.*This is the first activity in the Playbook.*

</td></tr><tr><td>

Create Record Form View

</td><td>

LicensePermitRecordGenerator

</td></tr><tr><td>

Template Fields: Product

</td><td>

Drivers License

</td></tr><tr><td>

Template Fields: Service

</td><td>

Driver’s license – New Request

</td></tr></tbody>
</table>10. Select **Submit**.

11. Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

12. Select **Drivers License – New Request** service definition.

13. Select the search icon next to the Playbook record generator.

14. Select the magnifying glass icon to open the list of playbook record generators, and select the previously-created playbook record generator for the extended case type.

15. In a new window, navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Content Items**.

16. Select **New**.

17. On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Name|Driver license application|
    |Catalogs|Government Services|
    |Category|Licenses|
    |Short Description|Application for an individual to obtain permission to legally operate a motor vehicle on any road, freeway, or other way accessible to the public.|
    |Table|Select the **License and Permit Case \(OR the extended table created** table.|
    |Playbook Experience|CSM Configurable Workspace|
    |Playbook Experience Record Generator|Previously-created Record Generator|
    |Portal Page|GSM Intake|
    |Title|Drivers License Application|

18. Select **Submit**.

19. Select the newly created Playbook Content Item.

20. Select **Edit** in the **Available For** related list.

21. Select **SNC External** from the Collections dropdown, and add it to the Available List.

22. Select **Save**.

23. Select the **Not Available For** related list, then select **Edit**.

24. Select **SNC External** and add it to the collection.

25. Select **Save**.

26. Verify the playbook content item you created displays under **Services** &gt; **Licenses/Permits** on the Government Service Portal.


