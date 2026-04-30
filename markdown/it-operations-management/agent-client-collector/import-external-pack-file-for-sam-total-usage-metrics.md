---
title: Configure Osqueryd schedule for SAM total usage metrics
description: SAM total usage metrics works by relying on the Osqueryd service running on the target host. Configure the Osqueryd service to run the required schedule Osquery on the host.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Using push-based Discovery and SAM together, ACC Discovery, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Configure Osqueryd schedule for SAM total usage metrics

SAM total usage metrics works by relying on the Osqueryd service running on the target host. Configure the Osqueryd service to run the required schedule Osquery on the host.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Osqueryd installation folder**.

2.  Find and edit the osquery.conf file.

3.  Add the below Osquery pack under the packs keyword.

    For Windows:

    ```
    "packs": {
          "sam-metering": "C:\\ProgramData\\ServiceNow\\agent-client-collector\\cache\\acc-visibility-modules\\bin\\sam-metering.conf"
      }
    
    ```

    For macOS:

    ```
    "packs": {
        "sam-metering": "/Library/Application\ Support/servicenow/agent-client-collector/cache/acc-visibility-modules/bin/sam-metering.conf"
      }
     
    ```


## Result

You can now [Configure Osquery logs for SAM total usage metrics](configure-osquery-logs-for-sam-total-usage-metrics.md).

