---
title: Manage file observables
description: Manage file observables provides stringent security measures to store the suspicious files and enables the files type observables for sandbox integration.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage file observables

Manage file observables provides stringent security measures to store the suspicious files and enables the files type observables for sandbox integration.

## Before you begin

Role required: sn\_ti\_malicious\_attachment\_access \(upload\)

Upload the file type observables:

-   Automatically: When the security incidents are created for the phishing emails, the attachments in the phishing email are created as file type observables.

-   Manually: A security analyst can also upload the suspicious files to create file type observables.


## About this task

You can create and view file type observables for a security incident. The suspicious files which are part of the observables are stored in a specific location, which can be accessed by the security analyst to download the file only with a specific role.

## Procedure

1.  Navigate to a security incident.

2.  Select **Observables** from the **Show All Related Lists** tab.

    If there are any attachments in the phishing email, then by default those attachments are created as file type observables in the corresponding security incident. Each attachment is created as two observables such as file type and file hash observable.

3.  To upload the secure attachments manually:

    -   Select **Upload Secure Attachment**.
    -   On the Upload Secure Attachments, select **Choose file** to upload one or more files. Each file is considered as a single observable record.
    -   Select **Create File Observables** to create the file type observables such as one is the file type and other one is the file hash which is a unique identifier.
    Select the file type observable to process for further integrations such as sandbox, threat lookup. In addition, you can also download the attachments from the file type observable.

    **Note:**

    The threat lookup \(VirusTotal\) retrieves the file from the secured attachments for the new file type observables and the following system properties are not applicable for the new file type observables.

    -   sn\_ti.scan.delete\_attachment\_after\_hash
    -   sn\_ti.scan.use\_file\_hash
    For a quick reference, the file type observable is mapped as a child to the hash observable and hash observable is mapped as a child to file observable.

    If the phishing email attachments are exceeding more than the defined size then the observables are not created. You must modify the system properties to support the larger size files.

    |System property|Description|
    |---------------|-----------|
    |glide.email.inbound.max\_total\_attachment\_size\_bytes|If you're forwarding the phishing email directly, use this system properties value to increase the file size from 18MB to a desired file size.|
    |com.glide.attachment.max\_get\_size|If you're forwarding the phishing email as an attachment, use this system property value to create the following system properties under global scope to increase the file size from 5MB to the desired size.|

    You can also create file type observable as follows:

    1.  Select **New**.
    2.  Select the **Observable type Category: File**
    3.  Select **Upload** to attach a file.

