---
title: Fetch end points in Now Assist Conversational Help skills
description: The Now Assist Conversational Help skills architecture solves latency by fetching answers hosted at the nearest location, which is best suited to the user.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Now Assist reference, Now Assist, Enable AI experiences]
---

# Fetch end points in Now Assist Conversational Help skills

The Now Assist Conversational Help skills architecture solves latency by fetching answers hosted at the nearest location, which is best suited to the user.

## Fetching solutions hosted on multiple geographical location

The Now Assist Conversational Help skill displays as Get Help on the Now Assist panel. The possible solutions to users queries posted on Now Assist Conversational Help skills are hosted on three main locations: Japan, EMEA and the US.

**Note:** To preserve data privacy standards, end points support for Get Help skill is not available in GCC/ NSC regulated markets.

For optimal performance, the central instance should be situated in the same geographic area as the user's instance. To achieve this alignment, we utilize DISH service, a tool within the user's instance, that helps identify the correct endpoint. The Now Assist Conversational Help skills uses the Mimir lookup service feature, inside the different data centers.

The DISH service communicates with the Mimir lookup table to determine the end points matching the user's location. Once we obtain this endpoint, it gets securely stored in the sys-service table within the customer instance. Moving forward, all the users' queries are routed through the specific endpoint, ensuring consistency and reliability. The Get Help skill uses the endpoint present in the sys-property `com.snc.get_help.endpoint`.

**Note:** The Now Assist Conversational Help skill version is stored in sn\_ads\_now\_help.com.snc\_now\_help\_skill.version, ensuring backward compatibility within the conversational shared services.

**Parent Topic:**[Now Assist reference](../../now-assist-admin/reference/now-assist-reference-landing.md)

