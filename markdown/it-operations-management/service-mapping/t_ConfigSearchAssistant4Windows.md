---
title: Configure Search Assistant for Windows
description: The Search Assistant feature of Pattern Designer allows you to search within files or registries. Upload grep files on to your instance to enable this feature to search on Windows servers.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure Search Assistant for Windows

The Search Assistant feature of Pattern Designer allows you to search within files or registries. Upload grep files on to your instance to enable this feature to search on Windows servers.

## Before you begin

Role required: admin or service\_mapping\_admin

## About this task

Grep is a utility that the Search Assistant feature uses to search files for matches. Grep is native to Unix-based systems, therefore you must upload it only for Windows-based configuration items \(CI\). Once you upload grep files onto the instance, it transfers them onto all MID Server which distribute the files onto all Windows-based CIs in your organization.

## Procedure

1.  Download the following files onto the computer from the Internet.

    -   egrep.exe
    -   libiconv2.dll
    -   libintl3.dll
    -   pcre3.dll
    -   regex2.dll
    For example, you can download the zip files for the **Dependencies** and **Binaries** folders at the following location: [http://gnuwin32.sourceforge.net/packages/grep.htm](http://gnuwin32.sourceforge.net/packages/grep.htm)

2.  Extract the files.

    After you extract the downloaded folders, the files are located as follows:

    -   grep-2.5.4-bin/bin/egrep.exe
    -   grep-2.5.4-dep/bin/libiconv2.dll
    -   grep-2.5.4-dep/bin/libintl3.dll
    -   grep-2.5.4-dep/bin/pcre3.dll
    -   grep-2.5.4-dep/bin/regex2.dll
3.  Navigate to **Pattern Designer** &gt; **Uploaded Files**.

4.  Click **New**.

5.  Enter the original file name in the **Name** field on the **Logical Name** tab, for example `egrep.exe`.

6.  Click **OS Types** and select **Windows**.

    ![Selecting the operating system option for uploading a file.](../image/UploadFileOSType.png)

7.  Click **OS Architectures** and select both 32-bit and 64-bit option.

8.  Click the **Manage Attachments** icon.

9.  Click **Choose Files**.

10. In the **Downloads** folder on your computer, navigate to the file which name you entered before, for example `egrep.exe`.

11. Click **Choose**.

12. Close the Attachments window.

13. Repeat [Step 3](t_ConfigSearchAssistant4Windows.md#clickNewStep) to [Step 11](t_ConfigSearchAssistant4Windows.md#CloseAttachmentWindow) to upload the rest of the files:

    -   libiconv2.dll
    -   libintl3.dll
    -   pcre3.dll
    -   regex2.dll
14. Connect to each Windows MID Server and update the PATH environmental variable with the location of the `bin` directory where `egrep.exe` is installed.


