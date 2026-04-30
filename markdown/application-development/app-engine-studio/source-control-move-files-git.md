---
title: Move application files in a Git repository
description: Move application files linked to source control to any folder of the repository when working in App Engine Studio \(AES\). Allow application developers to store supporting content such as automated tests in the same repository as the applications they support.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use AES with a Git source control repository, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Move application files in a Git repository

Move application files linked to source control to any folder of the repository when working in App Engine Studio \(AES\). Allow application developers to store supporting content such as automated tests in the same repository as the applications they support.

## Before you begin

-   [Link an application or application-customization to source control](source-control-link-application.md)
-   Role required: Source control credentials with write access

## About this task

Linking an application to source control generates a properties text file called `sn_source_control.properties` at the root level of the repository. The properties file specifies the folder containing the application files. The integration tracks changes to these application files by generating a `checksum.txt` file. When the checksum matches, the integration skips the validation and sanitization process. When the checksum does not match, the integration validates and sanitizes the application files as part of the source control operation. The integration ignores all repository content outside the application path.

**Note:** You can set system properties **glide.source\_control.checksum\_required** to enable optional checksum validations and sanitizations and **glide.source\_control.checksum\_quick\_install** to bypass sanitization steps on checksum matches. See [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

## Procedure

1.  Login to the source control repository linked to the application.

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

Login to your instance and perform [Source control operations in App Engine Studio](../reference/source-control-operations.md) from App Engine Studio.

**Parent Topic:**[Use AES with a Git source control repository](../concept/aes-source-control-use.md)

