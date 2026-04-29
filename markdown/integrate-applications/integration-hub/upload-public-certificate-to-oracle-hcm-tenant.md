---
title: Create a trusted issuer
description: Create a trusted issuer on the Oracle HCM tenant site that certifies the authenticity of the public certificate that you had generated on your Mac or Windows machine.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a trusted issuer

Create a trusted issuer on the Oracle HCM tenant site that certifies the authenticity of the public certificate that you had generated on your Mac or Windows machine.

## Before you begin

Role required: admin

You’ve generated the private and public certificates.

Access to the Oracle HCM tenant site.

## Procedure

1.  Log in to the Oracle HCM tenant site.

2.  Select the hamburger menu.

    ![Hamburger menu.](../image/oracle-hcm-spoke-oracle-hcm-tenant-site-hamburger-menu.png)

3.  Navigate to **Tools** &gt; **Security Console**.

4.  On the left panel, select API Authentication.

5.  Select **Create Oracle API Authentication Provider**.

6.  Select **Edit**.

7.  In the Trusted Issuer field, enter a custom name for the trusted issuer.

    **Tip:** Copy and save the name of the trusted issuer at a secured place.

8.  In the Token Type field, select **JWT**.

9.  Select **Save and Close**.

10. On the left panel, select **Inbound API Authentication Public Certificates**.

11. Select **Add New Certificate**.

12. In the Certificate Alias field, enter the name of the trusted issuer that you had created.

13. In the Import Public Certificate field, select **Choose File** to select and upload the public certificate you had generated.

14. Select **Save**.


