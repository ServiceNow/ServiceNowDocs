---
title: Manage applications
description: Learn how to manage the applications you publish to the ServiceNow application repository.
locale: en-US
release: yokohama
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Manage applications

Learn how to manage the applications you publish to the ServiceNow application repository.

After you have designed, developed, and successfully tested a custom application, you can publish your application to the ServiceNow application repository to share it to other instances in your company. You can see, manage and customize only the applications that are published by your own organization or scoped applications that are installed via plugins using the ServiceNow Application Repository. You can't see or manage, or customize applications that are published by other organizations.

**Note:** Do not combine the usage of both Update Sets and the Application Repository for scoped app development. This will result in numerous issues, including skipped changes, commit errors, and more. Once you have installed an application from the Application Repository, you must continue to develop and publish to the Application Repository for all future development. If you decide to develop an application using update sets, you must continue to use that method exclusively.

## Overview of managing applications

The Application Repository is part of the ServiceNow Store. ServiceNow customer instances are connected to a particular Store instance \(for example, Commercial or Regulated Market\). Customer applications published to the Application Repository are stored in a multi-tenant artifact storage, but the storage is designed so that customers cannot see or access other customers' published applications.

Application Repository has a limit of 20 versions of a given application. If your team is generating more builds or versions of your application than 20 at a time, the oldest is deleted.

Application Repository has a file size limit for applications at 1GB. Applications over this file size are not accepted during the publishing process.

