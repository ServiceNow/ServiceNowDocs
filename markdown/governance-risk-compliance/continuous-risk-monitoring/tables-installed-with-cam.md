---
title: Tables installed with CAM
description: Tables are added with the activation of the CAM plugin.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Tables installed with CAM

Tables are added with the activation of the CAM plugin.

|Table|Description|
|-----|-----------|
|Acceptance Task \(sn\_irm\_cont\_auth\_acceptance\_task\)|Task created when an issue is formally accepted as part of the authorization process.|
|Authorization Boundary \(sn\_irm\_cont\_auth\_authorization\_boundary\)|Stores details defining the boundary of an authorization package, including system scope and components.|
|Baseline Control \(sn\_irm\_cont\_auth\_baseline\_control\_objective\)|Used to create baseline controls for an authorization package from the Control Objective Library.|
|Boundary Filter \(sn\_irm\_cont\_auth\_boundary\_filter\)|Generates system elements for an authorization boundary based on defined filters.|
|Information Type \(sn\_irm\_cont\_auth\_information\_type\)|Library of predefined information types for classification and compliance purposes.|
|Information Type Definition \(sn\_irm\_cont\_auth\_information\_type\_definition\)|Selected information types associated with an authorization package.|
|Licensed Workflow Configuration \(sn\_irm\_cont\_auth\_licensed\_workflow\_config\)|Stores licensed workflow configurations for compliance frameworks.|
|Issue to Authorization Package \(sn\_irm\_cont\_auth\_m2m\_issue\_auth\_pack\)|Many-to-many relationship between issues and authorization packages for tracking dependencies.|
|Milestone \(sn\_irm\_cont\_auth\_milestone\_task\)|Task created when an issue is remediate, marking a milestone in the authorization process.|
|Organizational Defined Parameter \(sn\_irm\_cont\_auth\_odp\)|Stores organizationally defined parameters used in compliance and authorization workflows.|
|OSCAL Import \(sn\_irm\_cont\_auth\_oscal\_import\)|Records details of OSCAL imports for compliance frameworks.|
|OSCAL Import Status \(sn\_irm\_cont\_auth\_oscal\_import\_status\)|Tracks the status of OSCAL \(Open Security Controls Assessment Language\) import processes.|
|OSCAL Transformation \(sn\_irm\_cont\_auth\_oscal\_transformation\)|Stores data related to OSCAL transformation processes for mapping and conversion.|
|OSCAL UUID to Object Mapping \(sn\_irm\_cont\_auth\_oscal\_uuid\_to\_object\_mapping\)|Maps OSCAL UUIDs to specific records or entities in the database for traceability.|
|Overlay \(sn\_irm\_cont\_auth\_overlay\)|Stores overlay configurations applied to authorization packages for tailoring controls.|
|Authorization Package \(sn\_irm\_cont\_auth\_pack\)|Core table for storing authorization package details, including scope and controls.|
|Authorization Package Approvals \(sn\_irm\_cont\_auth\_pack\_approvals\)|Tracks approval requests and statuses for authorization packages.|
|Package Step Duration \(sn\_irm\_cont\_auth\_pack\_step\_duration\)|Tracks the duration of individual steps within an authorization package workflow.|
|RedRAMP Controls \(sn\_irm\_cont\_auth\_ssp\_controls\)|Stores SSP \(System Security Plan\) controls; usage may require verification.|
|System Element \(sn\_irm\_cont\_auth\_system\_element\)|Represents system components or elements included in an authorization boundary.|
|OSCAL UUID Mapping for CAM control \(sn\_irm\_cont\_auth\_system\_oscal\_uuid\_to\_item\_mapping\)|Identifies inheritance relationships during OSCAL import processes for CAM controls.|
|Workflow Configuration \(sn\_irm\_cont\_auth\_workflow\_configuration\)|Stores workflow configuration details for specific frameworks.|
|Workflow Configuration Element \(sn\_irm\_cont\_auth\_configuration\_element\)|Stores configuration elements for authorization workflows.|
|Impact \(sn\_irm\_cont\_auth\_workflow\_impact\)|Stores impact configuration data for frameworks, used in risk and compliance analysis.|
|Version \(sn\_irm\_cont\_auth\_workflow\_version\)|Stores version details of workflow configurations for frameworks.|

**Parent Topic:**[CAM reference](../concept/reference-grc-cam.md)

