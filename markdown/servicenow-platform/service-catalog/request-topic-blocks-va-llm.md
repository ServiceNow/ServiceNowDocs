---
title: Topic blocks to request catalog items through conversational experience
description: You can design a topic conversation in Virtual Agent powered Now LLM by including reusable topic blocks to perform request submission tasks.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Conversational catalog request reference, Now Assist in Conversational Catalog Request, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Topic blocks to request catalog items through conversational experience

You can design a topic conversation in Virtual Agent powered Now LLM by including reusable topic blocks to perform request submission tasks.

## Request catalog item through Now LLM

You can use this topic block to request for a catalog item through a conversational and streamlined experience based on generative AI. For information about configuring Now Assist in conversational catalog request, see [Configure Now Assist in Conversational Catalog Request](https://www.servicenow.com/docs/access?context=configure-gen-ai-catalog-item&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

|Parameter|Description|
|---------|-----------|
|catalog\_item\_id|sys\_id of the catalog item that should be requested.|
|context\_json|Context of the conversation in JSON format.|
|execute\_contextual\_search|Option to specify if the contextual search should be run for a record producer based on its configuration. For information on defining contextual search for a record producer, see [Define contextual search for record producer](https://www.servicenow.com/docs/access?context=t_CntxtSearchRP&version=australia&pubname=australia-platform-administration&ft:locale=en-US).|
|confirm\_catalog\_item|Option to specify whether the user must confirm the catalog item before continuing with the next step. If this is set to `false`, user can answer the catalog items questions by skipping the confirmation.|
|show\_end\_state\_card|Option to display the end state card information about the generated record to the user.|

<table id="table_jrd_dvg_lzb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record\_id

</td><td>

sys\_id of the record that is generated after the item submission.If the catalog item is not supported in the conversation mode or if the user does not have access to the item, -1 is returned.

</td></tr><tr><td>

record\_table

</td><td>

Name of the table in which the record is generated.

</td></tr><tr><td>

status

</td><td>

Status of the request. Possible options are success or error.

</td></tr><tr><td>

variables

</td><td>

Questions related to the catalog item.

</td></tr><tr><td>

message

</td><td>

Message that gives additional information in case of any failure.

</td></tr><tr><td>

used\_LLM

</td><td>

Option that indicates if Now LLM was used while requesting the item, that is, if slot filling was done for questions defined in a catalog item using generative AI.

</td></tr></tbody>
</table>## Things to remember that make items conversational or non-conversational

The following conditions must be met when a user requests a catalog item in the conversation mode in Virtual Agent powered by Now LLM.

-   A catalog item cannot have more than the number of questions specified in the **sn\_now\_assist\_cr.llm.conversational.request.question.limit** property. By default, this number is set to 500. For more information about this property, see [Service Catalog properties](../reference/r_ServiceCatalogProperties.md).
-   Lookup select box variables can't have an advanced reference qualifier, such as a reference qualifiers containing JavaScript. If a catalog item with the Lookup select box contains such advanced reference qualifiers, the item becomes non-conversational. Also, if a catalog item contains the Lookup select box variable with more than 20 choices, the item becomes non-conversational. This behavior is managed by a value of the **sn\_now\_assist\_cr.llm.lookup\_select\_choice\_limit** system property, which has a default value as 20.
-   A catalog item can have scripted catalog UI policies. But when a catalog item has scripted UI policies containing unsupported methods or functions, the catalog item becomes non-conversational.
-   The following methods or classes are supported in the catalog client scripts or scripted UI policies for a catalog item to be conversational:
    -   moment
    -   window.location.href
    -   top.location.href
    -   top.window.open
    -   window.open
    -   open
    -   Array
    -   Boolean
    -   Date
    -   Error
    -   GlideAjax
    -   GlideRecord
    -   JSON
    -   Math
    -   Number
    -   Object
    -   RegExp
    -   String
    -   alert
    -   console.info
    -   console.error
    -   console.debug
    -   console.warn
    -   console.log
    -   console.clear
    -   console.count
    -   console.countReset
    -   console.dir
    -   console.dirxml
    -   console.table
    -   decodeURI
    -   decodeURIComponent
    -   encodeURI
    -   evalexec
    -   g\_form.addErrorMessage
    -   g\_form.addInfoMessage
    -   g\_form.addOption
    -   g\_form.clearMessages
    -   g\_form.clearOptions
    -   g\_form.clearValue
    -   g\_form.getActionName
    -   g\_form.getDisplayValue
    -   g\_form.getEditableFields
    -   g\_form.getIntValue
    -   g\_form.getReference
    -   g\_form.getSysId
    -   g\_form.getTableName
    -   g\_form.getUniqueValue
    -   g\_form.getValue
    -   g\_form.hasField
    -   g\_form.hideAllFieldMsgs
    -   g\_form.hideErrorBox
    -   g\_form.hideFieldMsg
    -   g\_form.isMandatory
    -   g\_form.isNewRecord
    -   g\_form.isReadOnly
    -   g\_form.isVisible
    -   g\_form.removeOption
    -   g\_form.save
    -   g\_form.setDisabled
    -   g\_form.setDisplay
    -   g\_form.setLabel
    -   g\_form.setLabelOf
    -   g\_form.setMandatory
    -   g\_form.setReadOnly
    -   g\_form.setReadonly
    -   g\_form.setValue
    -   g\_form.setVariablesReadOnly
    -   g\_form.setVisible
    -   g\_form.showErrorBox
    -   g\_form.showFieldMsg
    -   g\_form.submit
    -   g\_user
    -   ga.addParam
    -   ga.getXML
    -   indexOf
    -   isLoading
    -   isNaN
    -   newValue
    -   oldValue
    -   onChange
    -   parseFloat
    -   parseInt
    -   this
    -   toFixed
    -   trim
    -   undefined
    -   escape
    -   unescape
-   A catalog item can have catalog client scripts. But when a catalog item has catalog client scripts containing unsupported methods or functions, the catalog item becomes non-conversational.
-   The variables containing pricing implications aren't supported.
-   You can specify the upper limit for the number of records of reference type variables corresponding to a table in the **sn\_now\_assist\_cr.llm.reference\_question\_choices.limit** property. By default, the limit is 2000000. If you specify the value more than 2000000, then it might impact the response time.
-   The UI page variable type is ignored in Virtual Agent like the UI page is ignored in Service Portal. For more information, see [Types of service catalog variables](../reference/r_VariableTypes.md).
-   To support the custom variables, users must associate topic blocks with the custom variables to represent them in the conversational interfaces. If the users don't associate topic blocks, the catalog item containing the custom variables, becomes non-conversational.
-   If you know that a variable makes a catalog item non-conversational, you can remove such variable from the conversational interfaces by selecting **Remove from Conversational Interfaces** option. Find the option in the Availability tab of the question form in ServiceNow AI Platform.
-   Use the **sn\_now\_assist\_cr.enable\_question\_grouping** property to group semantically related questions and prompt them together to reduce conversation turns. The property is inactive by default.
-   The field messages aren't shown to the requester in the following scenarios:

    -   If the field message appears for the question that's already answered.
    -   If the question is not shown to the requester because the question is read-only, hidden, or already auto-filled.
-   The following variable attributes are supported:

    -   ref\_ac\_order\_by
    -   allowed\_extensions
    -   max\_file\_size
    **Note:** All the other variable attributes are ignored in Virtual Agent.

-   A catalog item can have a single-row variable set but not a multi-row variable set.
-   If a catalog item has a default value configured for a question, the default value is displayed in Virtual Agent, which enables the user to proceed with the default value without having to select it manually. The user can also choose a different value other than the default value.
-   User can't skip the following type of questions for a catalog item:
    -   Lookup Multiple Choice
    -   Select Box
    -   Lookup Select Box
    -   Yes/No
    -   Numeric Scale \(If **Do not select first choice** configuration is not selected\)
    -   Multiple Choice \(If **Do not select first choice** configuration is not selected, or **Include none choice** configuration is selected\)
-   If the user is using Virtual Agent in a different supported collaboration tool like Microsoft Teams:
    -   Searching for a value using the search icon in choice type of fields is not supported.

        ![Searching for a choice field in Microsoft Teams](../image/msteams-choice.png "Choice type fields in Microsoft Teams")

        ![Searching for choice field in Virtual Agent](../image/va-choice.png "Choice type fields in Virtual Agent")

    -   Searching for a value in reference type of fields is performed in the form of a question.

        ![Searching for reference fields in Microsoft Teams](../image/msteams-reference.png "Reference type fields in Microsoft Teams")

        ![Searching for reference field in Virtual Agent](../image/va-reference.png "Reference type field in Virtual Agent")


**Note:** If you've installed the Now Assist in Conversational Catalog Request application, these conditions corresponds to the catalog item's conversational mode in the Virtual Agent powered by Now LLM.

## Translation of Now LLM

You can use the enable\_alternative\_translation property to enable translation of Now LLM. By default, the translation is turned off.

**Note:**

When the user profile language and session language differ, the Now LLM translated\_text call doesn’t appear. However, if the system property is enabled, the Now LLM call displays and translation occurs.

The following conditions must be met when a user requests a catalog item in the conversation mode in Virtual Agent powered by Now LLM.

**Note:** If you've installed the Now Assist in Conversational Catalog Request application, these conditions corresponds to the catalog item's conversational mode in the Virtual Agent powered by Now LLM.

**Parent Topic:**[Conversational catalog request reference](../reference/conversational-catalog-request-reference.md)

**Related topics**  


[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

[Catalog builder preview topic conversation](catalog-builder-preview-topic.md)

[Now LLM Service updates](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

