---
title: Configuring data synchronization in Service Graph Connector for Jamf
description: You can configure the connection properties for synchronizing only delta data from a Jamf instance.Disable delta synchronization to import all the Jamf data.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Jamf, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring data synchronization in Service Graph Connector for Jamf

You can configure the connection properties for synchronizing only delta data from a Jamf instance.

The delta data synchronization feature is available in Jamf version 2.14 and higher. The connector provides the ability to import only delta data from a Jamf instance. With delta synchronization enabled, the importing process of Jamf data is quicker because the connector imports only the changes in Jamf data. The **Last success import time** field of a data source displays the timestamp of the most recent successful pull run. The delta pull period is calculated by subtracting the last successful run date and time from the current date and time that is Delta period = Current date timestamp - Last success import date timestamp.

The application includes the **is\_delta\_enabled\_for\_computers** and **is\_delta\_enabled\_for\_mobiles** connection properties to enable delta synchronization for computers and mobile devices, respectively. By default, the **is\_delta\_enabled\_for\_computers** and **is\_delta\_enabled\_for\_mobiles** properties are set to `false`. To enable delta data synchronization, set these properties to `true`.

**Note:**

-   The **is\_delta\_enabled\_for\_computers** connection property is available only if the **use\_jamf\_pro\_api** property is set to `true`.
-   The **is\_delta\_enabled\_for\_mobiles** connection property is available only if the **use\_jamf\_mobile\_pro\_api** property is set to `true`.

See [Service Graph Connector for Jamf properties](../reference/cmdb-sgc-jamf-props.md).

When you want to import full data from your Jamf instance, you must disable the **is\_delta\_enabled\_for\_computers** and **is\_delta\_enabled\_for\_mobiles** properties by setting these properties to `false`. See [Disable delta synchronization](sgc-cmdb-jamf-data-sync.md#).

**Note:** When the full import of data is completed, set the **is\_delta\_enabled\_for\_computers** and **is\_delta\_enabled\_for\_mobiles** properties back to `true` to pull delta data later. If you leave the properties set to `false`, full data is imported with every pull, which takes considerable time.

## Disable delta synchronization

Disable delta synchronization to import all the Jamf data.

### Before you begin

Role required: admin

### About this task

The delta data synchronization feature is available in Jamf version 2.14 and higher.

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Jamf** &gt; **Connections**.

2.  From the list of connections, open the connection for which you want to disable delta synchronization.

    The connection properties are displayed in the Service Graph Connection Properties related list.

    -   To disable delta synchronization for computers, open the **is\_delta\_enabled\_for\_computers** property.
    -   To disable delta synchronization for mobile devices, open the **is\_delta\_enabled\_for\_mobiles** property.
3.  In the **Value** field, enter `false`.

4.  Select **Update**.


