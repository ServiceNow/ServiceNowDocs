---
title: Legacy - Move application files in a GIT repository
description: Move application files linked to source control to any folder of the repository. Allow application developers to store supporting content such as automated tests in the same repository as the applications they support.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Move application files in a GIT repository

Move application files linked to source control to any folder of the repository. Allow application developers to store supporting content such as automated tests in the same repository as the applications they support.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   [Legacy - Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md)
-   Role required: Source control credentials with write access

## About this task

Linking an application to source control generates a properties text file called `sn_source_control.properties` at the root level of the repository. The properties file specifies the folder containing the application files. The integration tracks changes to these application files by generating a `checksum.txt` file. When the checksum matches, the integration skips the validation and sanitization process. When the checksum does not match, the integration validates and sanitizes the application files as part of the source control operation. The integration ignores all repository content outside the application path.

**Note:** You can set system properties **glide.source\_control.checksum\_required** to enable optional checksum validations and sanitizations and **glide.source\_control.checksum\_quick\_install** to bypass sanitization steps on checksum matches. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

## Procedure

1.  Login to source control repository linked to the application.

2.  Create the destination folder where you will move the application files.

    For example, create the folders `src/app`.

3.  Move the folder containing your application files to the destination folder.

    For example, move the folder `demo_my_app` to `src/app`.

4.  Navigate to the root level of the repository.

5.  Open the `sn_source_control.properties` text file in a text editor.

6.  For the `path=` property, enter the folder path where you moved the application files.

    For example, enter `path=src/app`.

7.  Save the properties file.


## What to do next

Login to your instance and perform [source control operations](../reference/r_AvailableSourceControlOperations.md) from Studio.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

