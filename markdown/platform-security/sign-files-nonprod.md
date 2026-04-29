---
title: Create a job to sign specific records or attachments on a trusted instance
description: Sign a specific record, or group of records you define on a trusted instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sign Records and Files, Using Code Signing, Code Signing, Platform Security]
---

# Create a job to sign specific records or attachments on a trusted instance

Sign a specific record, or group of records you define on a trusted instance.

## Before you begin

Role required: security\_admin or sn\_kmf.cryptographic\_manager

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Security Jobs** &gt; **Create New**.

2.  At the **What type of Security Job would you like to create?** prompt, select **Signing Job**.

    A new **Signing Job** record displays.

3.  In the form, fill in the fields as needed:

<table id="table_i5q_n3z_rxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this job.

</td></tr><tr><td>

Type

</td><td>

Type of security job. To sign specific records, select the **Sign Specific Records** option. To sign specific attachments, select **Sign Specific Attachments**.

</td></tr><tr><td>

State

</td><td>

State of this job. This field begins with the value of **New**. This field is read only.

</td></tr><tr><td>

Table

</td><td>

Table containing the records or attachments you want to sign.If signing attachments, select the table with records that the attachments are associated with, not the Attachment \[sys\_attachment\] table.

**Tip:** Check the Key Management Framework \(KMF\) Signature Record \[sn\_kmf\_record\_signature\] table to ensure that there aren’t already signatures for the table you’ve selected.

</td></tr><tr><td>

Filter Records

</td><td>

Filter conditions used to limit which records appear in the **Select records for signing** table.

</td></tr><tr><td>

Select records for signing

</td><td>

List of records on the table selected in the **Table** field, limited by filter created in the **Filter Records** field.

 Move records from the **Available** window to the **Selected** window to include them in the signing job.

</td></tr><tr><td>

Time window start

</td><td>

The start of the time window to run this job. The job will run after the time entered in this field.A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr><tr><td>

Time window end

</td><td>

The end of the time window to run this job. The job runs before the time entered in this field. If the job hasn’t yet completed, the job will pause and resume at the next time window start. The end time must be after the start time.A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr><tr><td>

Summary

</td><td>

Summary of the execution of this job. This field is read only.

</td></tr></tbody>
</table>4.  Right-click the form header, and select **Save**.

5.  Open the job that you saved, and click **Start**.

    This action signs the signing job, and it’s ready for export.

6.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**

7.  Find and open the update set for your signing job.

    In the customer updates tab, you can see that this update set includes the signing job and the signature record.

8.  Select **Export to XML**.

    This action creates an XML file containing your update set on your local device.

9.  On your protected instance, navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets** &gt; **.**

10. At the bottom of the page, select **Import Update Set from XML**.

11. Select the **Choose File** button, and select the XML file created in previous steps.

12. Select **Upload**.

    Your update set is loaded, and appears in the **Retrieved Update Sets** list.

13. In the **Retrieved Update Sets** list, open the record for your imported update set.

14. Select the **Preview Update Set** button.

    After the preview completes successfully, you’ll see the **Commit Update Set** button appear.

15. Select **Commit Update Set**.


**Parent Topic:**[Sign specific records or attachments](../concept/sign-specific-records.md#)

