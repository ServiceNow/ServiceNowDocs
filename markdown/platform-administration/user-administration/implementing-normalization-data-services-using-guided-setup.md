---
title: Implementing normalization data services using guided setup
description: You can implement Normalization Data Services using a guided setup.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Normalization data services, Creating users, companies, departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Implementing normalization data services using guided setup

You can implement Normalization Data Services using a guided setup.

Normalization Data Services guided setup provides a sequence of tasks that help you configure the Normalization Data Services plugin on your instance. To open Normalization Data Services guided setup, navigate to **Normalization Data Services** &gt; **Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

**Note:** Because the Normalization Data Services feature requires an internet connection to download mapping information, this feature isn’t supported for on-premise instances.

## Activating the plugin

In the first task of the guided setup, you activate the Normalization Data Services plugin \(com.glide.data\_services\_canonicalization.client\). Activating the plugin installs all the necessary schema to support normalizing references to Company records in the customer management database \(CMDB\) and Asset Management.

## Downloading normalized data

In this task, you download the repository of all enterprise vendor names and the mappings to their normalized counterparts. After the download finishes, you can view the downloaded data in the Normalized Company Names \[cds\_client\_name\] table. You can verify mappings in the Normalized Mappings \[cds\_client\_mapping\] table. For example, you can verify that “Dell”, “DELL”, “Dell \(UK\)” are mapped to “Dell Inc.”.

## Updating reference qualifiers

This task modifies the reference qualifiers in reference fields linked to the Companies \[core\_company\] table, helping to ensure that users can only select from a list of normalized company names. For example, when creating a Computer \(cmdb\_ci\_computer\) record, users can only select “Dell Inc.” and not “Dell” or “Dell Incorporated”.

Some reference qualifiers may not get updated. To normalize these reference qualifiers manually, see [KB0784201](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0784201).

## Activating normalization properties

In this task, select the properties you want to activate. See [Normalization properties](../reference/r_NormalizedProperties.md).

Enable the **Normalize existing canonical core\_company records** property if the Companies \[core\_company\] table has two or more records that were both set to Normalized \("canonical=true"\) before any mapping. This option ensures only one \[core\_company\] record is set to Normalized. When you normalize the CMDB tables later in guided setup, the normalization job reassigns the proper normalized value.

For example, prior to mapping, both “DELL Inc” and “Dell Inc.” are set to Normalized \("canonical=true"\). You define a new mapping for “DELL Inc” to “Dell Inc.”. If this property is true, guided setup denormalizes "DELL Inc", and updates the manufacturer field in the CMDB records to “Dell Inc." when the CMDB tables are normalized.

## Normalizing data

To finish the guided setup, complete the remaining tasks by normalizing data in the following tables:

-   Configuration Items \(CMDB\)
-   Configuration Items \(CMDB\) Model
-   Software Asset Management tables

**Parent Topic:**[Normalization data services](c_NormalizationOverview.md)

