---
title: Create or update a catalog item from a Google Cloud Deployment Manager \(GDM\) template
description: Instead of generating a catalog item based on a blueprint, you can generate a catalog item based on a template that is held in the GDM configuration management system. The system parses the attributes in both the template file and optional supporting files and then generates a blueprint and a catalog item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/cloud-configuration-governance/catalog-item-from-gcp-template.html
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create a cloud catalog item, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create or update a catalog item from a Google Cloud Deployment Manager \(GDM\) template

Instead of generating a catalog item based on a blueprint, you can generate a catalog item based on a template that is held in the GDM configuration management system. The system parses the attributes in both the template file and optional supporting files and then generates a blueprint and a catalog item.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## About this task

Cloud Provisioning and Governance supports Google Cloud Platform templates managed by Cloud Deployment Manager \(GDM\) that were created in YAML, Python, or Jinja2.

The procedure to create a catalog item from a template involves the following steps:

1.  Create and save a catalog item record that references the template. The catalog item is in **Draft** state. In a later step, you activate the catalog item to make it available to cloud users.
2.  Create a cloud template record. The cloud template specifies a configuration installable \(a directory structure that includes the template file\) to use as the source of the catalog item.

    **Note:** You can update the cloud template record later, by referencing an updated configuration installable. Instructions are included in this procedure.

3.  Google Cloud Platform only: If the template file depends on supporting files \(typically updates or template code that specifies attribute settings\), you add the files to the **Dependent Templates** related list.
4.  Activate the cloud template to generate a resource block and blueprint that are associated with the catalog item and to make the cloud template available for use by the catalog item.
5.  Activate the catalog item so that cloud users in the Cloud User Portal can use it to provision resources.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Catalog Items**.

2.  Click **New** and then enter a unique and meaningful **Name**, **Short description**, and **Description**.

3.  Specify the **Source** as **Cloud Template** and the **Template Type** as **Google Cloud Deployment Manager**.

    \[Omitted image "gcp-new-catalog-item.png"\] Alt text: Define a catalog item based on a template

4.  Right-click in the header and select **Save**.

5.  On the Cloud Templates related list, click **New** and enter a unique **Name** and **Short description**.

    \[Omitted image "gcp-new-template.png"\] Alt text: Associate a template with catalog item

6.  Specify the content of the template and select one of three options.

    -   Paste the text of the template file into the form:

        1.  Set **Ingestion method** to **Use Template Body**.
        2.  You typically use either a custom template that you created or a template in a public GitHub or Bitbucket repository. Open the template file in a text editor and copy the full text of the file.
        3.  On the Cloud Template Versions form, paste the text into the **Body** text box.
        \[Omitted image "gcp-in-cloud-tmplt-body.png"\] Alt text: Open the template file and copy/paste the template code into the Body field

    -   Specify the URL of the template file:

        1.  Set **Ingestion method** to **Import from URL**.
        2.  In a browser, go to the template file. Copy/paste the full URL of the template into the **Cloud template URL** text box.
        \[Omitted image "gcp-in-cloud-tmplt-url.png"\] Alt text: Paste the template URL

    -   Upload the template file:
        1.  Set **Ingestion method** to **Upload a file**.
        2.  Click the **Click to add** link for the **Upload file** field.

            \[Omitted image "gcp-in-cloud-tmplt-file.png"\] Alt text: Upload a template file

        3.  Click **Choose File**, select the file, and then click **OK**. The system adds the template and the filename appears in the **Upload file** field. The results of the import process appear in the **Validation status** and **Validation message** fields.
7.  The template code appears in the **Body** text box.

    If the file does not include a `path` entry under `imports:`, then skip this step. If the file does include an entry, then the template file depends on at least one dependent file \(typically updates or files that specify attribute settings\). Perform the following procedure for each dependent file \(`cloudsql.jinja` in the example\):

    \[Omitted image "template-dependent-filename.png"\] Alt text: path entry for a dependant template file in the main template file

    1.  In a text editor, open the dependent template file \(`cloudsql.jinja` in the example\).

    2.  Copy the full text of the file.

    3.  On the **GDM Dependent Templates** related list, click **New**.

    4.  Paste the full text of the dependent template file into the **File content** text box.

    5.  Enter the exact name of the dependent template file into the **File name** text box.

        \[Omitted image "gdm-depend-template-form.png"\] Alt text: path entry for a dependant template file in the main template file

    6.  Click **Submit**.

        The file appears in the **GDM Dependent Templates** related list.

    7.  Repeat the procedure for each dependent template file.

8.  On the Cloud Template Versions form, click **Activate**.

    The system generates the catalog item and a blueprint with the name that you specified for the catalog item.

9.  On the Cloud Catalog Item form, select the **Active** check box, and then click **Submit**.

    The system displays the catalog item on the Cloud Catalog Items page and publishes the catalog item to the Cloud Service Catalog for use by end users.

    \[Omitted image "gcp-new-cloud-card.png"\] Alt text: New card for a catalog item

    **Note:** As with any catalog item, you can add or remove a user-viewable field. Click the card to open the catalog item form. On the **Variable Sets** tab, edit the variables.


## What to do next

Verify that the catalog item appears in the Cloud User Portal.

