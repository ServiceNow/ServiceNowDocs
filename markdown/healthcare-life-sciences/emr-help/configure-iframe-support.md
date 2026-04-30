---
title: Configure iFrame support for EMR Help in ServiceNow
description: Configure EMR Help to launch within a frame in Epic Hyperspace and Hyperdrive.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure iFrame support for EMR Help in ServiceNow

Configure EMR Help to launch within a frame in Epic Hyperspace and Hyperdrive.

## Before you begin

Role required: admin

For any ServiceNow page or portal to be launched within an iframe, an HTTP Response Header must be configured with the correct content security policy. This content security policy dictates which third party websites can load a ServiceNow page or portal inside an iframe.

## Procedure

1.  Set your scope to **Global** and elevate your role to **security\_admin**.

2.  Navigate to **All** &gt; **HTTP Response Headers** \(or type in sys\_response\_header.list\).

3.  Select the **Global** response header.

4.  Add the domain name for your Epic hyperspace instance to the list of values.

    For example, \*.yourdomain.com

5.  Confirm that **Active** is set to true.

6.  Select **Submit**.


## Result

![image.configureiframe]

## What to do next

For additional configuration steps within Epic, see the [How to configure EMR Help to launch within an iFrame in Epic's Hyperdrive \[KB1207128\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1207128) article in the Now Support knowledge base.

