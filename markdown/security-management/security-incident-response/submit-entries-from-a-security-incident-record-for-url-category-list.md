---
title: Submit observables from a security incident record to a URL category list
description: Submit observables that are attached to a security incident record to a configured URL category list by using the allow or block request. Adding observables to the allow or block list for security scans allows users to review content from these URLs and gain access to trusted content.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit observables from a security incident record to a URL category list

Submit observables that are attached to a security incident record to a configured URL category list by using the allow or block request. Adding observables to the allow or block list for security scans allows users to review content from these URLs and gain access to trusted content.

## Before you begin

Role required: sn\_si.analyst

## About this task

You submit observable entries by using the allow or block request action from the Associated Observables related list. Observables are artifacts found on a network or operating system that are likely to indicate an intrusion. Use the list of [URL Categories configured previously](create-zscaler-internet-access-url-category-manually.md#context_gqd_3ql_vpb) to select the observable that you want to submit. After you submit the request, an approval request is sent to your approval group.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

    In this example, you see how to select a security incident and an observable, and how to add an allow list.

    ![Selecting a security incident and an observable, and adding to an allow list.](../image/zscaler-submit-observable.gif "Adding an allow list")

2.  Select the security incident that you want to associate with the Zscaler allow or block request.

3.  Click **Show All Related Lists** and the **Associated Observables** tab.

    If you do not find any observables, click **New**.

4.  Select an observable and then from the actions menu, click **Allow/Block Request**.

5.  In the Allow/Block Request dialog box, select whether to perform the allow or block request on the observable.

6.  Click **Submit**.

7.  View the Work notes to see the status of your submission and the security tags.

    Click the links in the Work notes for more information about the status or to analyze the details on the Workflow Studio. Security tags are metadata on the responding record and define who should have access to specific types of security content.

8.  To view the status of the observable that you selected, navigate to **Zscaler Integration** &gt; **Zscaler URL Category List Entries**.

9.  In the Zscaler URL Category List Entries page, click the observable to view the record.


