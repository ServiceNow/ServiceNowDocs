---
title: Use the Email Domain Spoofing Detection playbook
description: Use this playbook to find a similarity match between the Phisher's sender email domain with a trusted domain name exists in the observable repository. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Email Domain Spoofing Detection playbook.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook for Email Domain Spoofing Detection, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the Email Domain Spoofing Detection playbook

Use this playbook to find a similarity match between the Phisher's sender email domain with a trusted domain name exists in the observable repository. The following steps give you a walkthrough of the actions, tasks, and subflows that are available in the Email Domain Spoofing Detection playbook.

## Before you begin

Role required:

-   sn\_si.admin
-   flow\_designer

Make sure you have installed Security Operations Spoke \(`sn_sec_spoke`\).

## Procedure

1.  When the playbook is triggered and starts executing, in Action 1, the playbook extracts the email domain from the phishing email.

2.  In Action 2, the playbook retrieves all the domain/email address type observables tagged by the security tag 'Domain Spoofing Candidate'.

3.  In Action 3, the playbook calculates the similarity between the Get Tagged domain and Email domain using the Levenshtein algorithm.

    ![Calculate the similarity between the two domains using the Levenshtein algorithm](../image/playbook-email-spoof-similarity.png "Email Domain Spoofing Detection playbook")

4.  In Action 4, the playbook looks up for the System Property record based on the following conditions:

    -   Name is sn\_sec\_spoke.domain\_spoof\_threshold, \(OR\)
    -   Name is from a to z, and if multiple records are found then return only the first record.
5.  In Action 5, based on the investigation done so far, the playbook checks if the similarity of the two domains exceeds the threshold or not.

    If the similarity of the two domains doesn't exceed the threshold, a manual response task is created in Action 5 and the flow ends. If the similarity of the two domains exceeds the threshold, then Actions 6 and 7 are executed.

    ![Response tasks to check if the similarity of the two domains exceeds the threshold.](../image/playbook-email-spoof-detect-threshold.png "Similarity exceeds the threshold")

6.  In Action 6, the playbook adds the Email Domain Spoofing security tag to the security incident.

7.  In Action 7, the playbook adds a worknote link to the context using the script option.

8.  In Action 8, the flow ends.


**Parent Topic:**[Playbook for Email Domain Spoofing Detection](../concept/playbook-email-spoof-detection.md)

