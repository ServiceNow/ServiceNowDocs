---
title: Legacy - Using MID Server with source control
description: The ServiceNow MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy - Link an application or application-customization to source control, Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Using MID Server with source control

The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

## How bundle files work with MID Server

The **.bundle** file helps source control function with a MID Server. A bundle file is the way Git packages a local repository in a single file. This makes sharing or moving the repository simpler and more streamlined. The file is then sent to the MID Server, which passes it on to the remote repository.

The `outgoing.bundle` \(commit operations\) and `incoming.bundle` \(apply remote changes\) are attached to the MID Server attachment table \[ecc\_agent\_attachment\] for any request that goes to the MID Server. The `outgoing.bundle` is created on the instance while the `incoming.bundle` is created on the MID Server.

After an operation completes successfully, the bundle file is “promoted” into a `golden.bundle` that is attached to the Repository configuration table \[sys\_repo\_config\]. It’s used to initialize the repository on a node that has not performed any Source Control operations yet.

The Auto Flush tool \[sys\_auto\_flush\] is a "table cleaner" that removes any `ecc_agent_attachment` record older than 30 days. This action removes the corresponding attachment as well.

The bundle files are kept on the MID Server and then saved to the Import directory on the MID Server.

On the MID Server, the bundle file is saved in the Import folder. This folder is under the user directory defined by the system property \(user.dir\), which users can configure. The bundle file is removed as part of the system flushing at the end of every operation.

## Working with the MID Server

**Note:** Source control operations can take more time for larger applications when using an MID server, as the entire app is bundled after an export and is dependant on the size of the app.

-   Avoid conflicts with Discovery and create files for the system attachment \[sys\_attachment\] table: [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   Learn about system properties restrictions: [Configure attachment system properties](https://www.servicenow.com/docs/access?context=t_DisablingTheDragAndDropFeature&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Parent Topic:**[Legacy - Link an application or application-customization to source control](../task/t_LinkAnApplicationToSourceControl.md)

