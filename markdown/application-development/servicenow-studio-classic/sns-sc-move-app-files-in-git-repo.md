---
title: Move application files in a Git repository
description: Move application files that are linked to source control to any folder of the repository when working in ServiceNow Studio. Moving application files enables application developers to store supporting content, such as automated tests, in the same repository as the applications they support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-sc-move-app-files-in-git-repo.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Move application files in a Git repository

Move application files that are linked to source control to any folder of the repository when working in ServiceNow Studio. Moving application files enables application developers to store supporting content, such as automated tests, in the same repository as the applications they support.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/link-app-to-source-control.md)

Role required: Source control credentials with write access

## About this task

Linking an application to source control generates a properties text file called `sn_source_control.properties` at the root level of the repository. The properties file specifies the folder containing the application files. The integration tracks changes to these application files by generating a `checksum.txt` file. When the checksum matches, the integration skips the validation and sanitization process. When the checksum does not match, the integration validates and sanitizes the application files as part of the source control operation. The integration ignores all repository content outside the application path.

**Note:** You can set system properties **glide.source\_control.checksum\_required** to enable optional checksum validations and sanitizations and **glide.source\_control.checksum\_quick\_install** to bypass sanitization steps on checksum matches. For more information, see .

## Procedure

1.  Log in to the source control repository linked to the application.

2.  Create the destination folder where you will move the application files.

    For example, create the folders `src/app`.

3.  Move the folder containing your application files to the destination folder.

    For example, move the folder `demo_my_app` to `src/app`.

4.  Navigate to the root level of the repository.

5.  Open the `sn_source_control.properties` text file in a text editor.

6.  For the `path=` property, enter the folder path where you moved the application files.

    For example, enter `path=src/app`.

7.  Save the properties file.


**Parent Topic:**[Source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/source-control-in-servicenow-studio.md)

