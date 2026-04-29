---
title: Define an SCCM configuration
description: To create catalog items for SCCM software deployment or to configure your instance to revoke software through SCCM, you must first associate that software with a collection through an SCCM configuration.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, CSD from SCCM, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Define an SCCM configuration

To create catalog items for SCCM software deployment or to configure your instance to revoke software through SCCM, you must first associate that software with a collection through an SCCM configuration.

## Before you begin

Before you create an SCCM configuration record, make sure you have discovered the SCCM applications, collections, and deployments and set up the necessary software models.

Role required: sn\_client\_sf\_dist.csd\_admin or admin.

## About this task

The SCCM configuration process associates software with SCCM collections. To deploy software from an SCCM server, the user or device must be a member of an SCCM collection associated with an **install** deployment. Client Software Distribution \(CSD\) allows you to revoke unentitled software using an SCCM server when that software can be removed using an **uninstall** collection. Users requesting revokable software from the Service Catalog also have the ability to define lease start and stop dates and request lease extensions.

![SCCM table references.](../images/SCCMTableRelationshipsDiagram.png "SCCM table references")

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **SCCM** &gt; **SCCM Applications**.

2.  Open an application that has a configured software model.

3.  Under **Related Links**, click **Create Software Configuration**.

4.  Complete the form, using the fields in the table.

    ![SCCM configuration form.](../images/SCCMConfigurationForm.png "SCCM configuration form")

<table id="table_jrj_05d_gk"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Recognizable name for this SCCM software configuration.

</td></tr><tr><td>

SCCM application

</td><td>

Name of an application hosted on the SCCM server.

</td></tr><tr><td>

SCCM collection

</td><td>

Name of the collection associated with the **install** deployment for the selected application on the SCCM server. Only those collections associated with the application are available for selection.

</td></tr><tr><td>

SCCM uninstall collection

</td><td>

Name of the collection associated with the **uninstall** deployment for the selected application on the SCCM server. You must specify an uninstall collection to:-   Define a lease end date for deployed software.
-   Allow lease extensions.
-   Revoke software from a user's machine.


</td></tr><tr><td>

Discovery model

</td><td>

Discovery model that links the unentitled software installation with the SCCM configuration. From the SCCM configuration record, Client Software Distribution can determine which collection to use to revoke the software. Unentitled software is software found on the user's machine that the user is not entitled to use.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring SCCM](../concept/configure-sccm-ihub.md)

