---
title: Processor script functions
description: The processor script contains functions that help you extract the translatable content and save the translated content which is included when you configure an artifact.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Artifact configurations, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Processor script functions

The processor script contains functions that help you extract the translatable content and save the translated content which is included when you configure an artifact.

## getTranslatedContent\(params\)

This function is responsible for extracting the translatable content for the Localization Framework to use and consume that content and contains the following parameters:

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table name of the artifact record.|
|sysId|String|The sys\_id of the artifact record.|
|language|String|The language into which the artifact has to be translated \(target language\).|

**Note:** This script function is available by default when you configure the processor script. This script function requires that you configure its parameters to build the LFDocumentContent object.

## saveTranslatedContent\(documentContent\)

This function is responsible for saving the translations back to the system and has a parameter which is an object of LFDocumentContent.

All the processor scripts extend LFArtifactProcessorSNC which defines the default implementation of this function, that is, saving the translations to standard tables. Defining this function in the processor script overrides the default behavior.

**Note:** This script function is commented by default when a new processor script is created. For more information, see [Read script helper functions for LFDocumentContentBuilder](lf-document-content-builder.md).

**Parent Topic:**[Artifact configurations](../concept/framework-configuration.md)

