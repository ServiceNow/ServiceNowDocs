---
title: Creating an assessment template from legacy assessment metric types
description: You can use the assessment designs that you have already created by migrating the metric types to the Smart Assessment Engine assessment templates. You can leverage the existing assessment designs to support SAE assessment automation, analysis, and reporting.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Creating an assessment template from legacy assessment metric types

You can use the assessment designs that you have already created by migrating the metric types to the Smart Assessment Engine assessment templates. You can leverage the existing assessment designs to support SAE assessment automation, analysis, and reporting.

## Overview of the migration process

The sets of questions that are defined in the ServiceNow® Assessments and Surveys application are saved as metric types and are what you are migrating into SAE. When you migrate a legacy metric type to an SAE assessment template, the original metrics are saved as question types. For more information on which metric types are supported and how they are mapped to SAE, see [How legacy metric types are migrated to sections in templates](../reference/sae-how-legacy-metrics-migrated.md).

The migration process does not support all metric types in the ServiceNow® Assessments and Surveys application. The following table lists the metric types that are not supported.

|Metric Type|Description|
|-----------|-----------|
|Custom|Metric type used to create a nonstandard question.|
|Duration|Metric type used to create a question related to the time duration. For example, a question about the planned duration or actual duration in an assessment.|
|Image scale|Metric type used to create a question where users select an image to use for scales.|
|Percentage|Metric type used to create a question where users enter a percentage.|
|Rankings|Metric type used to create a question where users select a different order number for each option to rank them.|
|Ratings|Metric type used to create a question where users can enter a rating.|

**Note:** Migrating metrics in a data-type template that enables the image flag to be selected aren't supported.

## Migration Process

Generate an assessment template from an existing metric type by following this process:

1.  Fill in a form:
    -   Specify which metric type to migrate.
    -   Specify the assessment template category that you want the template to be associated with. An assessment template category specifies the group of users that can access the template.
2.  Start the migration process. The following activities then transform the metric type data into an SAE assessment template:

    -   Metric categories become sections in the template.
    -   Metrics become questions in the template.
    -   Metric definitions become response options in the template.
    -   The template is given the name of the original metric type.
    -   The template is mapped to the template categories that you specified on the form.
    **Note:** The template definitions are migrated as response options if the metric data type is a template.

    For more information, see [How legacy metric types are migrated to sections in templates](../reference/sae-how-legacy-metrics-migrated.md).

3.  On the Assessment Workspace, validate the assessment template and update it as needed. After the template is published, you can use it to generate assessments.

    **Note:** The migrated assessment templates are in the draft state after migration. You must review and publish the template before you can use it for assessments.


For more information about migrating the legacy metric types, see [Migrate a legacy metric type to an assessment template](../task/sae-asmnt-tmplt-migrate-metrics-to.md).

**Related topics**  


[How legacy metric types are migrated to sections in templates](../reference/sae-how-legacy-metrics-migrated.md)

[Results of migrating a metric category to an assessment template](../reference/sae-migrate-asmnt-template-form.md)

