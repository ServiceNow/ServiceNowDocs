---
title: Creating catalog templates for use in Creator Studio apps
description: As a ServiceNow admin, you can create customized catalog templates in Service Catalog to guide users through adding forms in Creator Studio.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [create form template, create catalog template]
breadcrumb: [Templates and forms, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creating catalog templates for use in Creator Studio apps

As a ServiceNow admin, you can create customized catalog templates in Service Catalog to guide users through adding forms in Creator Studio.

For example, if your users will be building several apps for IT fulfilment, you may want to create a catalog template that contains only IT service requests.

When you add a catalog template to help users create forms in Creator Studio, you must use the following configurations:

-   Create a record producer template.
-   Leave the **Destination table** \(which is called the **Record submission table in Creator Studio**\) as undefined.
-   Ensure that the Creator Studio Users group can access the template. The template can also be available to all users.

Additionally, you may want to use the catalog template to restrict the catalogs that users can choose when creating an app.

For more details on how to add catalog templates, see [Creating or editing catalog item template](https://www.servicenow.com/docs/access?context=create-cat-item-template-cat-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Check out an article on [Creating catalog templates for Creator Studio](https://www.servicenow.com/community/creator-studio-blogs/creator-studio-for-admins-creating-catalog-templates-for-creator/ba-p/3053357).

**Parent Topic:**[Administering templates and forms for Creator Studio](creator-studio-administering-forms.md)

