---
title: Configuring Playbooks-on-portal for a custom case type
description: As an admin, you can configure the playbooks-on-portal experience for a custom case type that extends the base License and Permit case.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-11-04"
reading_time_minutes: 1
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configuring Playbooks-on-portal for a custom case type

As an admin, you can configure the playbooks-on-portal experience for a custom case type that extends the base License and Permit case.

## Before you begin

Role required: admin

## Procedure

1.  To first duplicate the playbook process, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  In the Processes list, select **Licenses/Permits Playbook**.

3.  Select the More Actions menu and select **Duplicate**.

4.  Fill in the **Label** field with the desired name for the playbook.

5.  Select **Duplicate**.

6.  Modify the playbook for the particular license use case, then select **Activate**.

7.  Navigate to **All** &gt; **Record Generators**.

8.  Select **New**.

9.  On the form, fill in the fields with the following:

    |Field|Entry|
    |-----|-----|
    |Table|License and Permit Case or the extended License and Permit table. This is the table the record generator will trigger for.|
    |Process Definition|Playbook created in the previous section.|
    |Create Record Activity Name|Answer Eligibility Questions \(first Playbook activity\).|
    |Create Record Form View|LicensePermitRecordGenerator|
    |Template Fields: Product|Drivers License|
    |Template Fields: Service|Driver’s license – New Request|

10. Select **Submit**.

11. Navigate to **All** &gt; **Service Definitions**.

12. Select **Drivers License – New Request**.

13. Select the search icon next to the Playbook record generator.

14. Select the pre-created playbook record generator for the extended case type.

15. In a new window, navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Content Items**.

16. Select **New**.

17. On the form, fill in the fields with the following information:

    |Field|Entry|
    |-----|-----|
    |Name|Driver license application|
    |Catalogs|Government Services|
    |Category|Licenses|
    |Short Description|Application for an individual to obtain permission to legally operate a motor vehicle on any road, freeway, or other way accessible to the public.|
    |Table|Select the table License and Permit Case, or the extended table created.|
    |Playbook Experience|CSM Configurable Workspace|
    |Playbook Experience Record Generator|Previously Created Record Generator|
    |Portal Page|GSM Intake|
    |Title|Drivers License Application|

18. Select **Submit**.

19. Select the Playbook Content Item that is created.

20. In the **Available For** related list, Select **Edit**.

21. In the Collections dropdown, select **SNC External** and add it to the Available List.

22. Select **Save**.

23. In the **Not Available For** related list, select **Edit**.

24. Select **SNC External** and add it to the collection.

25. Select **Save**.

26. Verify the playbook content item you created displays in the Services list on the Government Service Portal.


