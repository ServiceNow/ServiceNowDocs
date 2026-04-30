---
title: Using the Operational Technology Manager
description: After you complete all required set up tasks, including installing the Operational Technology \(OT\) extension classes and assigning user roles, perform the following tasks to create the foundational data and relationships for the ServiceNow Operational Technology solution.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Operational Technology Manager, Operational Technology]
---

# Using the Operational Technology Manager

After you complete all required set up tasks, including installing the Operational Technology \(OT\) extension classes and assigning user roles, perform the following tasks to create the foundational data and relationships for the ServiceNow® Operational Technology solution.

|Task|Purpose|
|----|-------|
|1. Populate a Microsoft Excel spreadsheet with your existing Operational Technology data.|Positions your existing data in the correct columns on a Microsoft Excel spreadsheet to ensure the success of your data upload.|
|2. Import your Excel spreadsheet.|Uploads your existing Operational Technology data to the Configuration Management Database \(CMDB\).|
|3. Run the Discovery for Operational Technology function.|Discovers Operational Technology \(OT\) devices in designated Purdue levels in your Industrial Control System \(ICS\) networks|
|4. Use the selections on the Operational Technology \(OT\) menu.|Enables editing or viewing detailed information for the OT devices in your enterprise.|

-   **[Service Graph Connector for Microsoft Excel](service-graph-connector-for-OT-excel.md)**  
The Service Graph Connector for Microsoft Excel function enables you to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet. You use it in the Integration Hub Extract Transform Load \(ETL\) to upload this data to the Configuration Management Database \(CMDB\).
-   **[Discovery for Operational Technology](discovery-for-operational-technology.md)**  
You can run the Discovery for Operational Technology function to discover IT class Operational Technology \(OT\) devices in designated Purdue levels in your Industrial Control System \(ICS\) networks. IT class items include switches, routers, and computers that exist both in data centers and in your factories.
-   **[Edit or view OT devices after import or discovery](../task/view-ot-assets.md)**  
Use the options on the Operational Technology \(OT\) menu to edit or view detailed information for the OT devices in your enterprise.
-   **[Managing Network Intrusion Detection System appliances](../task/managing_network_intrusion_detection_system_nids_appliances.md)**  
If you have the cmdb\_nids\_admin or admin role, you can assign metadata attributes to Network Intrusion Detection System \(NIDS\) class records from the NIDS menu in the ServiceNow AI Platform.
-   **[Modeling an Operational Technology system service](modeling-ot-system.md)**  
You can model an Operational Technology \(OT\) system service to create other control systems, such as a distributed control system \(DCS\).
-   **[Automatically convert your IT records to OT devices](../task/automatically-convert-it-records-to-ot-devices.md)**  
Create a scheduled job that automatically converts your IT hardware to Operational Technology \(OT\) devices by using the Bulk Update Ruleset for Reassigning IT to OT feature. This scheduled job adds OT entity details to all the IT hardware that you want to convert at once.
-   **[Use CMDB groups to add OT context to IT CIs](../task/use-cmdb-groups-it-ot-conversion.md)**  
Use Configuration Management Database \(CMDB\) groups to group IT configuration items \(CIs\) based on additional information, like installed software. Then you can add Operational Technology \(OT\) context to the IT CIs.

**Parent Topic:**[Operational Technology Manager](operational-technology-manager.md)

