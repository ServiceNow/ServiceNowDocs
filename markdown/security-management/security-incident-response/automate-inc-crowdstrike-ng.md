---
title: Automate detection updates and closures
description: Automate detection updates and closures based on the Security Incident Response incident status. The CrowdStrike Next-Gen SIEM integration enables detections to create security incidents and also to update the incidents after they are created or closed.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Next-Gen SIEM integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate detection updates and closures

Automate detection updates and closures based on the Security Incident Response incident status. The CrowdStrike Next-Gen SIEM integration enables detections to create security incidents and also to update the incidents after they are created or closed.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  If you are not continuing from the previous section of the Scheduling process, access the profile you are defining.

    1.  Navigate to **All** &gt; **CrowdStrike Next-Gen SIEM** &gt; **Detection Profile**.

    2.  Select the profile you are continuing to define.

    3.  Select **Additional Options** in the progress bar.

2.  On the form, fill in the fields.

    |Category|Field|Description|
    |--------|-----|-----------|
    |Security Incident Creation Updates|Update CrowdStrike Next-Gen detection Status upon SIR Incident Creation|Option to use the automated detection update functionality. The CrowdStrike Next-Gen SIEM detection status is updated in CrowdStrike Next-Gen SIEM detection with the comments after the SIR incident is created in the ServiceNow AI Platform.|
    |Initial detection status update|Initial detection status that is updated in the CrowdStrike Next-Gen SIEM environment, either New or In Progress.|
    |Initial comments posted back to detection|Initial comments that are posted to the detection in the CrowdStrike Next-Gen SIEM environment.|
    |Detection Closure Updates|Close CrowdStrike Next-Gen detection upon SIR Incident Closure|Option to use the automated detection status update functionality. CrowdStrike Next-Gen SIEM detections are closed in the CrowdStrike Next-Gen SIEM portal with the comments given after the SIR incident is closed in the ServiceNow AI Platform.|
    |Closure detection status update|Status update in the CrowdStrike Next-Gen SIEM detection when the security incident is closed in SIR.|
    |Closure Comments Posted back to detection|Comments posted to the detection in the CrowdStrike Next-Gen SIEM detection when the security incident is closed in SIR.|
    |Pull Closed detections|Pull Closed detections|Option to fetch closed detections during ongoing ingestion and one-time retrieval. Closed SIR incidents will not be updated with new data from CrowdStrike Next-Gen SIEM|
    |Detection Comments and SIR Work notes synchronization|Update SIR Automation Activity with CrowdStrike Next-Gen detection comments|Option to update your CrowdStrike Next-Gen SIEM comments in the SIR Automation Activity. The comment in the SIR Automation Activity appears with the prefix `Comment from CrowdStrike`.|
    |Update CrowdStrike Next-Gen SIEM detection comments with SIR work notes|Option to update your SIR work notes in the CrowdStrike Next-Gen SIEM detection comments. The comment in CrowdStrike Next-Gen SIEM appears with the prefix `Comment from ServiceNow`.|

3.  Select **Finish**.

4.  Activate the profile.

    1.  Select the **Name** section of the progress bar.

    2.  Select the **Active** check box.

    3.  Select **Continue**.


