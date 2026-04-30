---
title: Read script helper functions for LFDocumentContentBuilder
description: The LFDocumentContentBuilder provides utility functions to build document content. Use these functions to write the logic to extract the translatable content from any artifacts regardless of them using standard tables or not for translations.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Artifact configurations, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Read script helper functions for LFDocumentContentBuilder

The LFDocumentContentBuilder provides utility functions to build document content. Use these functions to write the logic to extract the translatable content from any artifacts regardless of them using standard tables or not for translations.

## initialize \(version, targetLanguage, sys\_id, tableName\)

Use this function as a constructor for LFDocumentContentBuilder and includes the following parameters:

<table id="table_okx_rqv_xnb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version

</td><td>

String

</td><td>

The version type of the document content to be generated. For Xanadu, this value is v1.

</td></tr><tr><td>

targetLanguage

</td><td>

String

</td><td>

The target language of the localization task document content. The target language is the same as the language available from the read script function argument.

</td></tr><tr><td>

Sys\_id

</td><td>

String

</td><td>

The sys\_id of the artifact record.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td>

The table name of the artifact record.

</td></tr></tbody>
</table>## processString \(string, groupName, label\)

Use this function to add the LFDocumentContentElement in the document content for the given string and includes the following parameters.

|Name|Type|Description|
|----|----|-----------|
|string|String|The value for which a document content entry is created.|
|groupName|String|The name of the group to which element should belong.|
|label|String|The unique label identifier for the created element.|

## processStringArray \(stringArray, groupName, label\)

Use this function to add elements \(object of LFDocumentContentElement\) in the document content for the given strings and includes the following parameters.

|Name|Type|Description|
|----|----|-----------|
|stringArray|List of Strings|The list of values for which document content entry is created.|
|groupName|String|The name of the group these strings belongs to.|
|label|String|The unique label identifier for these strings.|

## processScript \(scriptContent, groupName, label\)

Use this function to add an element in the document content for the strings present as input of getMessage, gs.getMessage, or gs.getMessageLang in the provided Script. It has the following parameters:

|Name|Type|Description|
|----|----|-----------|
|scriptContent|String|The Script to be processed to get the strings present as input of getMessage, gs.getMessage, or gs.getMessageLang.|
|groupName|String|The name of the group for this input.|
|label|String|The unique label identifier for this input.|

For example,

```
`var documentContentBuilder = new LFDocumentContentBuilder("v1", language, sysId, tableName);`
`Var name = "name";`
`documentContentBuilder .processScript("gs.getMessage('Hello {0}, How are you', name)", "Script_Group", "Script_Label");`
```

## processTranslatableFieldsForSingleRecord \(glideRecord, groupName\)

Use this function to create elements for the given glideRecord object, in document content for all its translatable fields. These translatable fields can be of translated\_field, translated\_text or translated\_html types. It includes the following parameters:

|Name|Type|Description|
|----|----|-----------|
|glideRecord|GlideRecord|The GlideRecord object to be processed for translatable fields. The GlideRecord should be pointing to the valid table record.|
|groupName|String|The name of the group for this input.|

## processTranslatableFieldsForMultipleRecords \(tableName, encodedQuery, groupName\)

Use this function to fetch all the qualified records for the given tableName and encodedQuery and adds elements \(object of LFDocumentContentElement\) in the document content for all the translatable fields. It includes the following parameters:

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table to fetch records.|
|encodedQuery|String|The encoded query for filtering records from the processTranslatableFieldsForSingleRecord table.|
|groupName|String|The name of the group for this input.|

## processElement\(\)

Use this function to add an element \(object of LFDocumentContentElement\) to LFDocumentContent object.

| | | |
|---|---|---|
|element|LFDocumentContentElement|Element to be added to the document content.|

## build\(\)

Returns the LFDocumentContent object.

**Note:** The getFinalJSON function has been deprecated in the Xanadu release and it is recommended to use the build\(\) function.

A sample script to build the document content.

```
getTranslatableContent: function(params) {
    var tableName = params.tableName;
    var sysId = params.sysId;
    var language = params.language;
    var lfDocumentContentBuilder = new global.LFDocumentContentBuilder("v1", language, sysId, tableName);
    // This will create a new object of LFDocumentContent and stores it internally
    lfDocumentContentBuilder.processTranslatableFieldsForSingleRecord(gr, "Basic Info");
    var field = LFDocumentContentHelper.createField(originalValue, translatedValue);
    field.setTextType(LFDocumentContentHelper.PLAIN_TEXT_TYPE);
    // All the other relevant attributes can be set
    var element = LFDocumentContentHelper.createElement(groupName, label);
    element.addField(field);
    lfDocumentContentBuilder.processElement(element); // Adds element to the LFDocumentContent object
    return lfDocumentContentBuilder.build(); // return the LFDocumentContent object
}

```

## Sample script to extract data from the LFDocumentContent

```
saveTranslatedContent: function(documentContent) {
    // LFDocumentContent object is passed as an argument to the saveTranslatedContent 
    var targetLanguage = documentContent.getLanguage();
    var version = documentContent.getVersion();
    var elements = documentContent.getElements(); // Array of LFDocumentContentElement objects
    for (var idx = 0; idx < elements.length; idx++) {
        var element = elements[idx];
        var groupName = element.getGroupName();
        var fields = element.getFields(); // Array of LFDocumentContentField objects
        for (var fieldIdx = 0; fieldIdx < fields.length; fieldIdx++) {
            var field = fields[fieldIdx];
            var originalValue = field.getOriginalValue();
            var translatedValue = field.getTranslatedValue();
            // Get all the other required members and process them appropriately
        }
    }
}
```

**Parent Topic:**[Artifact configurations](../concept/framework-configuration.md)

