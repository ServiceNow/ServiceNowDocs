---
title: Managing Network Intrusion Detection System appliances
description: If you have the cmdb\_nids\_admin or admin role, you can assign metadata attributes to Network Intrusion Detection System \(NIDS\) class records from the NIDS menu in the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Managing Network Intrusion Detection System appliances

If you have the cmdb\_nids\_admin or admin role, you can assign metadata attributes to Network Intrusion Detection System \(NIDS\) class records from the NIDS menu in the ServiceNow AI Platform.

A Network Intrusion Detection System helps manage the import of IT and OT devices from supported integrations. Assigning meta data such as location and NIDS network type to NIDS records helps you distinguish between detected OT and IT devices, and automatically adds the related meta data to the created records. Users with the cmdb\_nids\_admin or admin role can edit the **NIDS Assigned Meta Data** tab and view the changes made by the user in the Activity Stream.

**Note:** Manual creation for an NIDS record in the table is restricted from the list view or the form view of the records.

For more information about the NIDS class records, see [Network Intrusion Detection System \(NIDS\) CI extension class](https://www.servicenow.com/docs/access?context=cmdb-network-ids-nids-ci-extension-class&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

If a NIDS record has the Validated field set to true, then when any of the following attributes of the NIDS are changed on the NIDS form, a warning message is displayed.

-   NIDS network type
-   NIDS source name
-   NIDS source ID

If the NIDS record with any detects::detected by relationships is deleted, a warning message is displayed.

You can use the Network Intrusion Detection Systems \(NIDS\) Guided Setup to lead you through:

-   Configuring users and roles for users that do not already have an account in an instance
-   Importing NIDS records from Operational Technology \(OT\) Certified Service Graph Connectors to designate if NIDS appliances are running on OT or IT networks
-   Validating NIDS so that detected devices can be imported. For more information about validating NIDS, see [Validate the NIDS](validate-nids.md).

To access the NIDS Guided Setup, navigate to **Network Intrusion Detection Systems \(NIDS\)** &gt; **NIDS Guided Setup**.

To assign an appliance as a manager for NIDS sensors that detect devices, navigate to **Network Intrusion Detection Systems \(NIDS\)** &gt; **Managers** to edit applicable "management consoles" or "central managers" records.

-   Review the Sensors list to ensure that there is not currently a device assigned as manager.
-   For any devices that do not function as sensors, change **is manager** to **True**.

For information about the `NIDSUtils` script include that copies NIDS-assigned meta data to detected devices, see [Script includes installed with Operational Technology Manager](script_includes_installed_with_operational_technology_manager.md).

-   **[Validate the NIDS](validate-nids.md)**  
Validate the NIDS to import the devices from the ETL that were detected by the sensor. The sensors can only pass the validation if they aren't in learning mode as such sensors aren't eligible for device import.
-   **[Validate multiple NIDS sensors at once](bulk-validation-nids.md)**  
Validate multiple NIDS sensors at once through a bulk validation so that you can edit your records more quickly and efficiently.

**Parent Topic:**[Using the Operational Technology Manager](../concept/using-operational-technology-manager.md)

**Related topics**  


[Network Intrusion Detection System \(NIDS\) CI extension class](https://www.servicenow.com/docs/access?context=cmdb-network-ids-nids-ci-extension-class&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Script includes installed with Operational Technology Manager](script_includes_installed_with_operational_technology_manager.md)

