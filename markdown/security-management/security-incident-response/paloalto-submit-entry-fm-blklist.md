---
title: Submit EDL entries from the blocklist for Palo Alto Networks Next-Generation Firewall
description: For observables determined to be malicious, and not associated with a specific ServiceNow AI Platform security incident, you submit External Dynamic List \(EDL\) entries from the blocklist.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit EDL entries from the blocklist for Palo Alto Networks Next-Generation Firewall

For observables determined to be malicious, and not associated with a specific ServiceNow AI Platform security incident, you submit External Dynamic List \(EDL\) entries from the blocklist.

## Before you begin

Role required: sn\_si.analyst

## About this task

When you want to block an observable that you have determined is malicious, or allow an observable you have determined is not malicious, and the observable is not associated with a specific ServiceNow AI Platform security incident record, you submit EDL entries directly from the blocklist. Examples of these types of EDL entries might be URLs or domains for specific sites.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Entries**.

    ![Firewall EDL Entries on the application navigator.](../image/edl-entries-list.png)

2.  Click the **Firewall EDL Entries** module.

3.  In the Palo Alto Networks Firewall External Dynamic List Entries list, click **New**.

4.  In the new record that is displayed, in the **Entry value** field, enter a value for your observable.

    The two possible outcomes of this entry:

    -   **The remaining fields on the form are completed automatically.**

        A matching observable is found, and a message is displayed that a matching observable exists. Select the EDL you want to attach this entry to and click **Submit**. Select the EDL you want to attach this entry to prior to setting the Expiration period.

    -   **A message is displayed that instructs you to complete the form.**

        A matching observable has not been found, and you must complete the form. After you complete it, select the EDL you want to attach the observable to and click **Submit**. An observable record is created.

    The following figure shows an example of an existing domain observable and how the fields are completed automatically.

    ![Matching observable exists.](../image/4-30-existing-obsv-url.png)

5.  Click the search icon to select the EDL you want to attach the entry to.

6.  Click **Submit**.

    If you have email approval configured in your workflow, an approval email request is sent.

7.  If a message is displayed that requests you to fill in the rest of the information manually, fill in the fields.

    ![No matching observable exists.](../image/4-30-notexisting-obsv-url.png)

<table id="choicetable_r4s_ryh_vdb"><thead><tr><th align="left" id="d309760e198">

Field

</th><th align="left" id="d309760e201">

Description

</th></tr></thead><tbody><tr><td id="d309760e207">

**Observable type**

</td><td>

Observable type that is supported from the dialog.

</td></tr><tr><td id="d309760e216">

**EDL name**

</td><td>

EDL you want to attach the entry to. **Note:** Select the EDL want to attach the entry to prior to setting the Expiration period.

</td></tr><tr><td id="d309760e228">

**Enable override \(default is selected\)**

</td><td>

Lookup result or source. When configured, permits you to enter a **Lookup result** and the source used to find the results. These fields are typically populated when a security incident record is created. In this case, there is no lookup result or source, and you fill in these fields in manually.

</td></tr><tr><td id="d309760e240">

**Lookup result**

</td><td>

Select **Unknown** or **Malicious**.

</td></tr><tr><td id="d309760e256">

**Source**

</td><td>

Source that performs a threat lookup on the EDL entry, for example, ThreatCrowd, etc.

</td></tr><tr><td id="d309760e265">

**Expiration period**

</td><td>

The expiration period inherited from the EDL by default. You can override this value, but only during the creation of the entry.`0` indicates that the EDL entry never expires.

 If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of `1`, and there is no maximum value.

 For example, if you enter `30` days at 2:01 PM on May 1, the EDL entry will expire at 2:01 PM on May 31.

</td></tr></tbody>
</table>8.  Click **Submit**.

    If you have changed the default expiration period of the EDL entry, a warning confirmation dialog box is displayed indicating that the period differs from the selected EDL.

    ![Confirmation dialog box for expiration period.](../image/4-20-expiry-confirm-4-2.png)

9.  Choose one option to configure the expiration period.

<table id="choicetable_mrw_213_vdb"><thead><tr><th align="left" id="d309760e321">

Option

</th><th align="left" id="d309760e324">

Description

</th></tr></thead><tbody><tr><td id="d309760e330">

**Yes**

</td><td>

Confirms your expiration override, saves the record, and returns you to the **Palo Alto Networks Firewall External Dynamic List Entries** list. If you have email approval configured in your workflow, an approval email request is sent.

</td></tr><tr><td id="d309760e342">

**No**

</td><td>

Cancels the override. At this point, you can change the value for the **Expiration period**.After changing the value, click **Submit** to return to the **Palo Alto Networks Firewall External Dynamic List Entries** list.

</td></tr></tbody>
</table>10. If not displayed, navigate to the **Palo Alto Networks Firewall External Dynamic List Entries** list and note that the status for the entry is Pending.

    ![Firewall EDL Entries list with pending entry.](../image/4-30-boston-entry-pending.png)

    The entry is now ready for approval.


## What to do next

Approve EDL entries.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Submit EDL entries from a security incident record for Palo Alto Networks Next-Generation Firewall](paloalto-submit-edl-snsi.md)

**Next topic:**[Approve EDL entries for Palo Alto Networks Next-Generation Firewall](paloalto-apprv-edl-entries-sncr.md)

**Related topics**  


[EDL entry exceptions for Palo Alto Networks Next-Generation Firewall](../reference/paloalto-edl-execptions.md)

