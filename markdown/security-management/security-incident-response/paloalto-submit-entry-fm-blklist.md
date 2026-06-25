---
title: Submit EDL entries from the blocklist for Palo Alto Networks Next-Generation Firewall
description: For observables determined to be malicious, and not associated with a specific ServiceNow AI Platform security incident, you submit External Dynamic List \(EDL\) entries from the blocklist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/paloalto-submit-entry-fm-blklist.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
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

2.  Select the **Firewall EDL Entries** module.

3.  In the Palo Alto Networks Firewall External Dynamic List Entries list, select **New**.

4.  In the new record that is displayed, in the **Entry value** field, enter a value for your observable.

    The two possible outcomes of this entry:

    -   **The remaining fields on the form are completed automatically.**

        A matching observable is found, and a message is displayed that a matching observable exists. Select the EDL you want to attach this entry to and select **Submit**. Select the EDL you want to attach this entry to before setting the Expiration period.

    -   **A message is displayed that instructs you to complete the form.**

        A matching observable has not been found, and you must complete the form. After you complete it, select the EDL you want to attach the observable to and select **Submit**. An observable record is created.

5.  Select the search icon to select the EDL you want to attach the entry to.

6.  Select **Submit**.

    If you have email approval configured in your workflow, an approval email request is sent.

7.  If a message is displayed that requests you to fill in the rest of the information manually, fill in the fields.

<table id="choicetable_r4s_ryh_vdb"><thead><tr><th align="left" id="d329588e154">

Field

</th><th align="left" id="d329588e157">

Description

</th></tr></thead><tbody><tr><td id="d329588e163">

**Observable type**

</td><td>

Observable type that is supported from the dialog.

</td></tr><tr><td id="d329588e172">

**EDL name**

</td><td>

EDL you want to attach the entry to. **Note:** Select the EDL want to attach the entry to before setting the Expiration period.

</td></tr><tr><td id="d329588e184">

**Enable override \(default is selected\)**

</td><td>

Lookup result or source. When configured, permits you to enter a **Lookup result** and the source used to find the results. These fields are typically populated when a security incident record is created. In this case, there is no lookup result or source, and you fill in these fields in manually.

</td></tr><tr><td id="d329588e196">

**Lookup result**

</td><td>

Select **Unknown** or **Malicious**.

</td></tr><tr><td id="d329588e212">

**Source**

</td><td>

Source that performs a threat lookup on the EDL entry, for example, ThreatCrowd, etc.

</td></tr><tr><td id="d329588e221">

**Expiration period**

</td><td>

The expiration period inherited from the EDL by default. You can override this value, but only during the creation of the entry.`0` indicates that the EDL entry never expires.

 If you change this value, this entry is active for the number of days you enter. You can enter a minimum value of `1`, and there is no maximum value.

 For example, if you enter `30` days at 2:01 PM on May 1, the EDL entry will expire at 2:01 PM on May 31.

</td></tr></tbody>
</table>8.  Select **Submit**.

    If you have changed the default expiration period of the EDL entry, a warning confirmation dialog box is displayed indicating that the period differs from the selected EDL.

9.  Choose one option to configure the expiration period.

<table id="choicetable_mrw_213_vdb"><thead><tr><th align="left" id="d329588e268">

Option

</th><th align="left" id="d329588e271">

Description

</th></tr></thead><tbody><tr><td id="d329588e277">

**Yes**

</td><td>

Confirms your expiration override, saves the record, and returns you to the **Palo Alto Networks Firewall External Dynamic List Entries** list. If you have email approval configured in your workflow, an approval email request is sent.

</td></tr><tr><td id="d329588e289">

**No**

</td><td>

Cancels the override. At this point, you can change the value for the **Expiration period**.After changing the value, select **Submit** to return to the **Palo Alto Networks Firewall External Dynamic List Entries** list.

</td></tr></tbody>
</table>10. If not displayed, navigate to the **Palo Alto Networks Firewall External Dynamic List Entries** list and note that the status for the entry is Pending.

    The entry is now ready for approval.


## What to do next

Approve EDL entries.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto_integration.md)

**Previous topic:**[Submit EDL entries from a security incident record for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto-submit-edl-snsi.md)

**Next topic:**[Approve EDL entries for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto-apprv-edl-entries-sncr.md)

**Related topics**  


[EDL entry exceptions for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto-edl-execptions.md)

