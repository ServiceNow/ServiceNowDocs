---
title: Reassign the External Content Connectors Service Account user to the global domain
description: Fix issues with missing user permissions for users on your instance by reassigning the External Content Connectors Service Account user to the global domain.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: topic
last_updated: "2026-02-03"
reading_time_minutes: 2
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Reassign the External Content Connectors Service Account user to the global domain

Fix issues with missing user permissions for users on your instance by reassigning the External Content Connectors Service Account user to the global domain.

## Symptom

On an instance with domain separation configured, if you assign the External Content Connectors Service Account user to a domain other than the global domain, external content connector user permission crawls can only map source system user and group permissions correctly for instance users assigned to the same domain. Instance users assigned to other domains are unable to search private content indexed by your external content connectors.

## Cause

The External Content Connectors application includes an External Content Connectors Service Account user. When you run user permission crawls for your external content connectors, this user account assigns the retrieved source system user and group permissions to users on your instance.

When the External Content Connectors Service Account user is assigned to a domain other than the global domain, it can only map source system user and group permissions to instance users in its own domain. Instance users assigned to any other domain don't get correctly mapped source system user and group permissions and can't search private content retrieved by your external content connectors.

As an example, suppose you have an instance with domain separation configured where you assign the External Content Connectors Service Account user to the PKD/BR 1.0/VK domain. With this configuration, external content connector user permission crawls can only map source system user and group permissions to your instance users who are assigned to the same PKD/BR 1.0/VK domain. Instance users assigned to any other domain don't get source system user and group permissions mapped correctly and can't search private content retrieved by your external content connectors.

## Resolution

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Open the user record with ID **xcc-connector-service-account** and name **External Content Connectors Service Account**.

3.  On the User form, configure the layout to show the **Managed domain**, **Domain**, and **Domain Path** fields.

    To learn how to show or hide fields on a form, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#).

4.  Select the **Managed domain** option.

5.  Set the value of the **Domain** field to `global`.

    This is the default value for the field.

6.  Set the value of the **Domain Path** field to `/`.

    This is the default value for the field.

7.  Select **Update**.

    The External Content Connectors Service Account user is reassigned to the global domain with default settings.

8.  Update your user permission mappings by rerunning user permission crawls for your affected external content connectors.


**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

