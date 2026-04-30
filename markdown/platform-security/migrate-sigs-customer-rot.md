---
title: Migrate signatures to use a customer certificate
description: Run a signing job to migrate your signatures to a customer Root of Trust \(ROT\).
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Root of Trust Settings, Configure, Code Signing, Platform Security]
---

# Migrate signatures to use a customer certificate

Run a signing job to migrate your signatures to a customer Root of Trust \(ROT\).

## Before you begin

Role required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

Code Signing must be enabled on your protected and trusted instances. You can verify by checking that the **com.snc.kmf.signature.validation.flag** system property is set to `true`.

This procedure is part of a series of procedures to change a customer Root of Trust \(ROT\) on your instances. For an overview of this process, see [Change your Root of Trust configuration](../concept/change-rot-overview.md).

## Procedure

1.  Log in to your protected instance.

2.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

3.  Find and open the **ROT - Generate Updateset of records to migrate signatures using customer certificate** scheduled job.

4.  At the bottom of the form, select **Execute Now**.

5.  Navigate to **All** &gt; **System Security** &gt; **Security Jobs** &gt; **Create New**.

6.  At the prompt, select **Signing Job**.

7.  In the **Signing Job** form, fill in the fields as needed.

    |Field|Value|
    |-----|-----|
    |Name|Create a unique name for your job.|
    |Type|Select **Sign Update Set**.|
    |Table|Select the update set created in the previous steps. The update set has a name beginning with `change_root_of_trust_updateSet`.|

8.  Right-click the form header and select **Save** to save this record.

9.  Right-click the form header and select **Export** &gt; **XML \(This Record\)** to export this record as an XML file.

10. Log in to your trusted instance.

11. Navigate to **All** &gt; **System Security** &gt; **Security Jobs** &gt; **All**.

12. Right-click the list header and select **Import XML**.

13. In the **Import XML** form, select **Choose File** and select the XML file you downloaded in the previous steps.

14. Select **Upload**.

15. From the list, open the imported security job.

16. Select **Export Code Signing job to production**.

    This action signs the job and places it in a new update set you can import into your protected instance.

    **Important:** After signing the job, you must perform the next steps within 10 minutes. If you exceed this time period, you can re-sign the job using these steps, which creates another signed update set.

17. Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

18. Find the update set created in the previous steps.

    The name starts with `SIGN_UPDATE_SET_updateSet`.

19. Select **Export XML** to export your update set as an XML file.

20. Log in to your protected instance.

21. Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

22. At the bottom of the list, select **Import Update Set from XML**.

23. In the **Import XML** form, select **Choose File** and select the XML file you downloaded in the previous steps.

24. Select **Upload**.

25. Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**, and open the update set starting with `SIGN_UPDATE_SET_updateSet`.

26. Select **Preview Update Set**.

27. After the preview is completed, select **Commit Update Set**.

28. Navigate to **All** &gt; **System Security** &gt; **Security Jobs** &gt; **All**.

29. Open the imported security job.

30. Select **Start** to run the security job.

    After the security job is completed, information regarding the status of the job appears in the **Summary** field.

    When the job is in Done state, all signatures of update set records must use the customer provided certificate as verification certificate. You can verify this on the KMF Signature Records \[sn\_kmf\_record\_signature\] table.


## What to do next

To continue the Root of Trust configuration process, see [Disable ServiceNow Root of Trust](disable-sn-rot.md).

**Parent Topic:**[Change your Root of Trust configuration](../concept/change-rot-overview.md)

