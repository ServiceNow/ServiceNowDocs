---
title: Results post cloning for application customizations
description: The results to expect post cloning for application customization display the expected behaviors based on the state of the application, and the actions to recover your application customizations.
locale: en-US
release: australia
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Preserve applications and customizations in development during a system clone, Manage customizations to applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Results post cloning for application customizations

The results to expect post cloning for application customization display the expected behaviors based on the state of the application, and the actions to recover your application customizations.

The following are the expectations based on the state of the application customizations, and the actions to recover your customizations.

|State of the App Customization on Source Instance|State of the App Customization in the Target \(Development\) instance pre-clone|State of the App Customization in Target \(Development\) instance post clone|Action to take to recover App Customization in the Target \(development\) instance post clone|
|-------------------------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
|Base application is not installed|Base application version 1.0 and App Customization version 1.0|Base application is not installed|Reinstall Base application and App Customization|
|Base application not installed|Base application version 1.0 and App Customization in Source Control|Base application is not installed, and the sys\_repo\_config has an empty app field.|Remove the repository configuration \(sys\_repo\_config\) record \(the app field has been emptied\) and import again from Source Control and install Base application.|
|Base application version 1.0|Base application version 1.0 App Customization version 1.0|Base application version 1.0|Reinstall App Customization|
|Base application version 1.0|Base application version 1.0 and App Customization in Source Control|Base application version 1.0, repo\_config is retained and the App Customization version displays as none in the all apps page.|Apply the remote changes from the Git repository.|
|Base application version 1.0 and App Customization version 1.0|Base application version 2.0 and App Customization version 2.0|Base application version 1.0 and App Customization version 1.0|Reinstall App Customization version 2.0 and Base application version 2.0|
|Base application version 1.0 and App Customization version 1.0|Base application version 2.0 and App Customization version 2.0 in Source Control|Base application version 1.0 and App Customization version 1.0, sys\_reconfig is retained|Apply the remote changes from the Git repository.|
|Base application version 2.0 and App Customization version 2.0|Base application version 1.0 and App Customization version 1.0|Base application version 2.0 and App Customization version 2.0 is installed.|Both Base and App Customization are at the latest versions.|
|Base application version 2.0 and App Customization version 2.0|Base application version 1.0 and App Customization version 1.0 in Source Control|Base application version 2.0 and App Customization version 2.0 is installed with repo\_config retained, so the branch version is on 1.0|Both Base and App Customization are at the latest versions.|

