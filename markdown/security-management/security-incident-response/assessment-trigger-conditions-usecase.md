---
title: Assessment trigger conditions examples
description: The following examples provide different scenarios on how mandatory and optional assessment trigger conditions are generated.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure an assessment trigger condition, Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Assessment trigger conditions examples

The following examples provide different scenarios on how mandatory and optional assessment trigger conditions are generated.

-   On the Assessment Trigger Condition form, generate mandatory assessments when the **Priority** and **Business Impact** for a security incident is set to **Critical** on the **Assessment Trigger Rule** page. In such scenario, the security analysts cannot close the incident until the mandatory assessments are completed.

    ![This image describes the post incident review mandatory assessment.](../image/trigger-conditions-exm01.png "Mandatory assessment example")

-   As you can see, in this example, If a security incident is in a **Review** state, security analysts cannot close the security incident without completing the **Post Incident Review Assessment**. An assessment link is available to take the assessment to the security analysts who are assigned \(or who had requested for the assessment\) to the incident.
-   On the Assessment Trigger Condition form, generate optional assessments when the **Priority** and **Business Impact** for a security incident is set to **High**. In this example, if the security analysts do not complete the assessments and close the security incident, the assessments are automatically canceled.
-   In case, if the mandatory or optional assessments does not match the security incident, assessments are not generated for such security incidents. A security analyst can close the security incident without completing the Post Incident Review assessment.

