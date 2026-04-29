---
title: FireEye Get File Capability
description: File acquisition requests instruct an Endpoint Security Agent to obtain a file from its host endpoint. File acquisitions are used for static or dynamic analysis of potential or verified compromises, as well as for evidence retention during insider threat investigations. Get File capability should be created as a separate profile.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# FireEye Get File Capability

File acquisition requests instruct an Endpoint Security Agent to obtain a file from its host endpoint. File acquisitions are used for static or dynamic analysis of potential or verified compromises, as well as for evidence retention during insider threat investigations. Get File capability should be created as a separate profile.

## Before you begin

Role required: admin

Triggering Get File Profile and create a FireEye HX capability profile with **Get File** capability.

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Select the security incident that you want to review.

3.  Click **Run EDR Profile\(s\)**in the related links section.

4.  Browse and select Get File profile from the list of available profiles.

5.  Provide the **File name** and **File path**.

    **Note:** Enter the name of the file for which you want to acquire. Specify a precise path name or another appropriate path-based Windows environment variable. You must specify the drive letter or path names. Different endpoints may have different drive mappings. If you explicitly specify a folder name, you can end the path with a backslash. However, the final backslash is not mandatory.

6.  Click **Submit**.

7.  Review the work notes and activities section.

8.  View the tags and check the results in the **Get File** related list.

    **Note:** The Get File profile is now triggered manually.

    ![Get File related list](../image/get-file-related-list.png)

    **To review a downloaded file acquisition:**

    -   Open the file acquisition .zip file.
    -   Enter the password required to open the file. Password can be viewed by hovering over download link in FireEye HX Console. Follow the below steps to view the password:
        -   Login to FireEye HX console.
        -   Navigate to **Acquisitions** and filter by Acquisition type – File.
        -   Select the desired record.

            **Note:** You will be able to see the details of the file acquired on the right tab.

        -   Hover over the **Download** link available at the top to get the password.
        -   Open and review the files within the .zip file using any text or XML editor.

            **Note:**

            -   It is recommended that the file retrieved is added as an observable manually, so that it can be tracked as an evidence against the security incident. This will also help view the files in future, when password is forgotten or changed.
            -   The maximum file size supported for Get File action is 1024 MB, and this value can be configured by changing **com.glide.attachment.max\_size**, and the default timeout is 60 minutes that can be configured from the FireEye HX Default Settings page.

                ![Get File update and delete options. Attachments rename and download options.](../image/get-file.png)

            -   Get File can also be triggered from configuration item related list.

                ![Get File update and delete options. Attachments rename and download options.](../image/get-file-related-list-01.png)


