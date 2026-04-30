---
title: Predictive Intelligence Workbench Migration Utility
description: Predictive Intelligence Workbench managers can easily migrate existing compatible Predictive Intelligence solution definitions into Predictive Intelligence Workbench. The Migration Utility enables a simplified configuration and expanded reporting functions.
locale: en-US
release: xanadu
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench administration, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Predictive Intelligence Workbench Migration Utility

Predictive Intelligence Workbench managers can easily migrate existing compatible Predictive Intelligence solution definitions into Predictive Intelligence Workbench. The Migration Utility enables a simplified configuration and expanded reporting functions.

**Important:**

Starting with the Xanadu release, ITSM Predictive Intelligence Workbench is being prepared for future deprecation. It will be completed deprecated and will no longer be supported from the **Yokohama** release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The Predictive Intelligence Workbench Migration Utility enables existing Predictive Intelligence users with the piwb\_manager role to convert a solution definition to a use case. The active solution is then converted into a model associated with the new use case.

A Related Link on the Predictive Intelligence Classification Definition form enables users to migrate a solution definition from Predictive Intelligence directly into Predictive Intelligence Workbench.

![Migration Utility Related Link on Classification Definition form](../image/itsm-piwb-migration-related-link.png "Migration Utility Related Link on Classification Definition form")

The Related Link only appears on the form when there is an active solution definition and that solution is not associated with a Predictive Intelligence Workbench use case.

Users can also access the Migration Utility as a module in the Predictive Intelligence Workbench application.

Clicking the **Migrate this solution to PI Workbench** Related Link or clicking the**Migration Utility** module, takes you to the Migration Utility detail page for the solution definition.

![Migration Utility detail page](../image/itsm-piwb-migration-utility-page.png "Migration Utility detail page")

Clicking **Migrate** from the Migration Utility details page alerts you that a new use case will be created in Predictive Intelligence Workbench. You can then follow guided setup to integrate a new model.

![Migration Utility alert pop-up](../image/itsm-piwb-migration-solution-popup.png "Migration Utility alert pop-up")

Clicking **Migrate** from this pop-up alert finalizes the migration.

![Migration is complete pop-up](../image/itsm-piwb-migration-utility-migration-done.png)

