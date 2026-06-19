---
title: Submit observables from a security incident record to a URL category list
description: Submit observables that are attached to a security incident record to a configured URL category list by using the allow or block request. Adding observables to the allow or block list for security scans allows users to review content from these URLs and gain access to trusted content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/submit-entries-from-a-security-incident-record-for-url-category-list.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit observables from a security incident record to a URL category list

Submit observables that are attached to a security incident record to a configured URL category list by using the allow or block request. Adding observables to the allow or block list for security scans allows users to review content from these URLs and gain access to trusted content.

## Before you begin

Role required: sn\_si.analyst

## About this task

You submit observable entries by using the allow or block request action from the Associated Observables related list. Observables are artifacts found on a network or operating system that are likely to indicate an intrusion. Use the list of [URL Categories configured previously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/create-zscaler-internet-access-url-category-manually.md) to select the observable that you want to submit. After you submit the request, an approval request is sent to your approval group.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to associate with the Zscaler allow or block request.

3.  Select **Show All Related Lists** and the **Associated Observables** tab.

    If you do not find any observables, Select **New**.

4.  Select an observable and then from the actions menu, select **Allow/Block Request**.

5.  In the Allow/Block Request dialog box, select whether to perform the allow or block request on the observable.

6.  Select **Submit**.

7.  View the Work notes to see the status of your submission and the security tags.

    Select the links in the Work notes for more information about the status or to analyze the details on the Workflow Studio. Security tags are metadata on the responding record and define who should have access to specific types of security content.

8.  To view the status of the observable that you selected, navigate to **Zscaler Integration** &gt; **Zscaler URL Category List Entries**.

9.  In the Zscaler URL Category List Entries page, select the observable to view the record.


