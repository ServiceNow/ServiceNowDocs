---
title: Legacy - Author elective and customer updates
description: When you install an application from the application repository or ServiceNow store, you can set a series of properties to define the behavior of delete and choice processing. These kinds of choices are called an "author-elective" feature.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - Production deployment tips, Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Author elective and customer updates

When you install an application from the application repository or ServiceNow® store, you can set a series of properties to define the behavior of delete and choice processing. These kinds of choices are called an "author-elective" feature.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

## Overview of author elective

You can find details on these properties in the [Skipped records that occur during application installation](https://www.servicenow.com/docs/access?context=generation-skip-records-app-installs&version=australia&pubname=australia-platform-administration&ft:locale=en-US) topic. With these properties, you can opt in and out of deletes and choice updates depending on whether you are using your own or a third-party application.

When you install from source control, however, these records do not skip, except when a global application file is claimed by a different global application. Other than **com.glide.apps.include\_my\_deletes** and **com.glide.apps.include\_global\_deletes** that disable the processing of the author\_elective\_update folder altogether, those properties are not effective for source installed apps.

**Note:** An “absent” file detected in Delta loading for source control is vastly different than a Delete payload housed inside the author\_elective\_update folder. Author\_elective\_update properties do not prevent Delta loading in source control from deleting the file.

Similarly, update sets protect customizations that you make in an instance against incoming changes that force a preview decision. Before you commit an update set, a preview must be run to attempt to detect collisions. You must address all preview problems before committing the changes. Source control may ask you to stash a local change, but the outcome of the installation is to load what is present in the source even if a change had been made locally.

Loading what is present in the source is challenging when properties must have different versions based on the target of the installation. For example, it’s difficult to resolve when a property containing an integration URL differs based on instance production role. The **is\_private** flag is effective with a source control installation and does not overwrite the property if set, mitigating this concern.

**Parent Topic:**[Legacy - Production deployment tips](tips-production-deployment.md)

