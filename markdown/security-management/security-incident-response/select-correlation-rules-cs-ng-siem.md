---
title: Set correlation rules
description: After creating a CrowdStrike Next-Gen SIEM detection profile, select correlation rules to map corresponding detections to a security incident. Correlation rules are refreshed every time a profile is opened and new rules are available for selection. The CrowdStrike Next-Gen SIEM integration supports multiple profiles.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set correlation rules

After creating a CrowdStrike Next-Gen SIEM detection profile, select correlation rules to map corresponding detections to a security incident. Correlation rules are refreshed every time a profile is opened and new rules are available for selection. The CrowdStrike Next-Gen SIEM integration supports multiple profiles.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  If you're not continuing from the previous section of the detection profile definition process, access the profile you're defining.

    1.  Navigate to **All** &gt; **CrowdStrike Next-Gen SIEM** &gt; **Detection Profile**.

    2.  Select the profile you're continuing to define.

    3.  Select **Correlation Rules** in the progress bar.

2.  Clear the **All Correlation Rules selected** check box.

3.  In the Correlation Rule List search field, enter the correlation rule name created in the CrowdStrike portal.

4.  Select the correlation rule.

5.  Use the right arrow to move the rule from **Available** to the **Selected** column.

6.  Complete this section of the detection profile definition process by selecting **Continue**.


## What to do next

Map individual CrowdStrike Next-Gen SIEM detection fields to the fields on the ServiceNow AI Platform Security Incident Response security incident. For more information, see [Map detection fields](map-crowdstrike-next-gen-inc.md).

