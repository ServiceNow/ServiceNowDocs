---
title: Disable ServiceNow Root of Trust
description: Run a scheduled job on your trusted non-production instance to disable Root of Trust.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Change your Root of Trust configuration, Configuring Code Signing, Code Signing, Platform Security]
---

# Disable ServiceNow Root of Trust

Run a scheduled job on your trusted non-production instance to disable Root of Trust.

## Before you begin

Role required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

Code Signing must be enabled on your production and trusted instances. You can verify by checking that the **com.snc.kmf.signature.validation.flag** system property is set to `true`.

This procedure is part of a series of procedures to change to a customer Root of Trust \(ROT\) on your instances. For an overview of this process, see [Change your Root of Trust configuration](../concept/change-rot-overview.md).

## Procedure

1.  Log into your trusted instance.

2.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

3.  Open the **Disable ServiceNow Root of Trust** scheduled job.

4.  Select the **Export signed job to production**.

5.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

6.  Find and open the **Disable ServiceNow Root of Trust** update set.

7.  Select **Export XML** to export your update set as an XML file.

8.  Log in to your production instance.

9.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

10. At the bottom of the list, select **Import Update Set from XML**.

11. In the **Import XML** form, select **Choose File** and select the XML file you downloaded in the previous steps.

12. Select **Upload**.

13. Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**, and open the **Disable ServiceNow Root of Trust** update set.

14. Select **Preview Update Set**.

15. After the preview is completed, select **Commit Update Set**.

16. Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

17. Open the scheduled job imported in the update set.

18. Select the **Execute Now** button to run the job.


## Result

Executing the scheduled job sets the ROT property to true. Your instance is configured to use the customer root of trust.

**Parent Topic:**[Change your Root of Trust configuration](../concept/change-rot-overview.md)

