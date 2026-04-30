---
title: Submit block list entries directly from the Block List Entry Table
description: For observables determined to be malicious, and not associated with a specific Now Platform security incident, you submit Block List entries from the block list.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit block list entries directly from the Block List Entry Table

For observables determined to be malicious, and not associated with a specific Now Platform security incident, you submit Block List entries from the block list.

## Before you begin

Role required: Security Incident Administrator \(sn\_si.analyst\)

## About this task

When you want to block an observable that you have determined is malicious or allow an observable you have determined is not malicious, and the observable is not associated with a specific ServiceNow AI Platform security incident record, you submit Block List entries directly from the block list. Examples of these types of Block List entries might be URLs or domains for specific sites.

## Procedure

1.  Navigate to **All** &gt; **Check Point NGTP Integration** &gt; **Block Request Entries**.

    ![Block Request List Entries](../image/submit-from-table.png)

2.  Click the **Block Request Lists** module.

3.  In Check Point Block Request List Entries list, click **New**.

4.  In the **Entry value** field, enter a value for your observable.

    The two possible outcomes of this entry:

    -   The remaining fields on the form are completed automatically.
    -   A matching observable is found, and a message is displayed that a matching observable exists. Select the Block List you want to attach this entry to and click Submit. Select the Block List you want to attach this entry to prior to setting the Expiration period.
    A message is displayed that instructs you to complete the form. A matching observable has not been found, and you must complete the form. After you complete it, select the Block List you want to attach the observable to and click Submit. An observable record is created. The following figure shows an example of an existing domain observable and how the fields are completed automatically.

    ![New record](../image/list-entry-new-record.png)

5.  Click the search icon to select the Block List you want to attach the entry to.

6.  Click **Submit**.

7.  If you have email approval configured in your workflow, an approval email request is sent.

    If a message is displayed that requests you to fill in the rest of the information manually, fill in the fields.

    ![New record with no matching observables](../image/new-record-no-match-observ.png)

<table id="table_kpf_lrk_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Observable type

</td><td>

Observable type that is supported from the dialog.

</td></tr><tr><td>

Block List name

</td><td>

Block List you want to the entry to.**Note:** Select the Block List you want to attach the entry to prior to setting the Expiration period.

</td></tr><tr><td>

Enable override \(default is selected\)

</td><td>

Lookup result or source. When configured, permits you to enter a Lookup result and the source used to find the results. These fields are typically populated when a security incident record is created. In this case, there is no lookup result or source, and you fill in these fields in manually.

</td></tr><tr><td>

Lookup Result

</td><td>

Select **Unknown** or **Malicious**.

</td></tr><tr><td>

Source

</td><td>

Source that performs a threat lookup on the Block List entry, for example, ThreatCrowd, etc

</td></tr><tr><td>

Expiration period

</td><td>

The expiration period inherited from the Block List by default. You can override this value, but only during the creation of the entry.0 indicates that the Block List entry never expires.

 If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of 1, and there is no maximum value.

 For example, if you enter 30 days at 2:01 PM on May 1, the Block List entry will expire at 2:01 PM on May 31. However, scheduler checks for expired entries at 00:00 every day and changes the state of the entry to ‘expired’ at 00:00 June 1.

</td></tr></tbody>
</table>8.  Click **Submit**.

    If you have changed the default expiration period of the Block List entry, a warning confirmation dialog box is displayed indicating that the period differs from the selected Block List.

    ![Expiration period message](../image/confirm-dialog.png)

<table id="table_mwz_wjl_rgb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Yes

</td><td>

Confirms your expiration override, saves the record, and returns you to the Check Point Block List Entries. If you have email approval configured in your workflow, an approval email request is sent.

</td></tr><tr><td>

No

</td><td>

Cancels the override. At this point, you can change the value for the **Expiration period**.After changing the value, click Submit to return to the Check Point Block Entries list.

</td></tr></tbody>
</table>9.  If not displayed, navigate to **Check Point Block Request List Entries**, and note that the status for the entry is **Pending**.

    ![List entry ready for approval](../image/list-entry-ready-for-appv.png)

    The entry is now ready for approval.


