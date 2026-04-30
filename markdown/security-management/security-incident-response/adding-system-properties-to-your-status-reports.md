---
title: Add system properties
description: Add system properties to control MSIM application behavior. Following are the default system properties that are introduced as part of the Major Security Incident Management status reports.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Major Security Incident status reports, Managing MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add system properties

Add system properties to control MSIM application behavior. Following are the default system properties that are introduced as part of the Major Security Incident Management status reports.

|Property Name|Description|
|-------------|-----------|
|sn\_msi.export\_img|Use this property to control the exporting of images. The default value is set to ON.|
|sn\_msi.export\_img\_log|Use this property to enable logging in to the browser console. The default value is set to OFF.|
|sn\_msi.export\_img\_parallel\_threshold|Use this property to control the maximum number of parallel requests to generate the images from report widget configurations. The default value is set to 14.|
|sn\_msi.img\_export\_log|Use this property to enable the console logs in the browser.|
|sn\_msi.img\_export\_poll\_interval|Use this property to control the time gap between polls that checks if the image is generated or not. The default poll interval time is set to 3000 milliseconds.|
|sn\_msi.export\_poll\_request\_timeout|Use this property to control the maximum time the system can poll for exported image. The default value is 120000 milliseconds.|
|sn\_msi.msi\_report\_uib\_element\_js\_path|Use this property to control the generic path to capture the image out of the UIB page portion.|
|sn\_msi.report\_default\_style\_objects|Use this property to change the CSS of the generated PDFs such as font size, font color, or field value. For example, if sn\_msi.workspace\_manager would prefer to change the font color of the left panel of the generated PDF status report then the workspace manager can modify the system property font color and render the PDF in a desired view.|

**Parent Topic:**[Configure Major Security Incident status reports](manage-status-reports-for-major-security-incident-management.md)

**Related topics**  


[Create a Report Template](../task/create-report-template.md)

[Create a Report Section Template](../task/create-report-section-template.md)

[Create a Report Subsection Template](../task/create-report-subsection-template.md)

[Create Report Subsection Element template](../task/create-report-subsection-element-template.md)

