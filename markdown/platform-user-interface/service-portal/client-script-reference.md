---
title: Supported client script types and APIs
description: Some client scripts are not supported in Service Portal. Others must have a UI type set to All or Mobile / Service Portal. If using a client script in the Service Portal, only client-side APIs supported in a mobile environment can be used.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Portal and client scripts, Supported features in Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Supported client script types and APIs

Some client scripts are not supported in Service Portal. Others must have a UI type set to **All** or **Mobile / Service Portal**. If using a client script in the Service Portal, only client-side APIs supported in a mobile environment can be used.

## Client script support in Service Portal

<table id="table_SPScriptSupport"><thead><tr><th>

Client script

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog client scripts

</td><td>

Service Portal requires that the **UI Type** field be set to **All** or **Mobile / Service Portal**. Client Scripts marked as **Desktop** rely on legacy APIs that are not supported in Service Portal. Before flagging a script as Mobile / Service Portal or All, make sure you are only using supported client-side APIs.

</td></tr><tr><td>

Validation scripts

</td><td>

Service Portal requires that the **UI Type** field be set to **All** or **Mobile / Service Portal**. Client Scripts marked as **Desktop** rely on legacy APIs that are not supported in Service Portal. Before flagging a script as Mobile / Service Portal or All, make sure you are only using supported client-side APIs.

 Validate user input in a specific field type using a validation script. In new instances, Service Portal includes XML, Script, Script \(Plain\), Email, and Version validation scripts by default. If upgrading from a previous release, the Mobile and Service Portal version is not active by default. You must activate the Mobile and Service Portal version of the validation script to validate user input in the Service Portal. See [Activate Service Portal validation scripts](../task/activate-sp-validation-scripts.md).

 **Note:** To call a UI script within a Validation script, use the g\_ui\_scripts global object. For more information, see GlideUIScripts. Verify that the UI script has the **Global** field set to false and **UI Type** set to Mobile / Service Portal or All.

</td></tr><tr><td>

UI scripts

</td><td>

Service Portal requires that the **UI Type** field be set to **All** or **Mobile / Service Portal**. Client Scripts marked as **Desktop** rely on legacy APIs that are not supported in Service Portal. Before flagging a script as Mobile / Service Portal or All, make sure you are only using supported client-side APIs.

</td></tr><tr><td>

UI Actions

</td><td>

All server-side UI actions are supported in Service Portal, although setRedirectURL\(\) operations are ignored because Service Portal forms handle redirection in a different way than the platform.

 The form widget ignores any UI Actions marked as **Client**.

</td></tr><tr><td>

UI Policies

</td><td>

Supported, although you should use only declarative UI Policies. Avoid scripting unless the outcome cannot be achieved through the condition builder.

</td></tr><tr><td>

UI Macros

</td><td>

Not supported as UI macros use Jelly.

</td></tr><tr><td>

Formatters

</td><td>

Not supported as formatters use Jelly.

</td></tr></tbody>
</table>## Supported client-side APIs

Supported client scripting APIs for use in onLoad, onChange, and onSubmit client scripts.

For detailed class and method information, see the Client API reference.

<table id="table_skq_rjp_h1b"><thead><tr><th>

Class

</th><th>

Available methods

</th></tr></thead><tbody><tr><td>

g\_form

</td><td>

-   addDecoration\(fieldName, icon, title\)
-   addErrorMessage\(message\)
-   addInfoMessage\(message\)
-   addOption\(fieldName, value, label, index\)
-   clearOptions\(fieldName\)
-   getActionName\(\)
-   getBooleanValue\(fieldName\)
-   getDecimalValue\(fieldName\)
-   getEncodedRecord\(\)
-   getFieldNames\(\)
-   getIntValue\(fieldName\)
-   getLabel\(fieldName\)
-   getReference\(fieldName, callback\)
-   getRelatedListNames\(\)
-   getSectionNames\(\)
-   getSysId\(\)
-   getTableName\(\)
-   getValue\(fieldName\)
-   hasField\(fieldName\)
-   hideAllFieldMsgs\(type: "info \| error"\)
-   hideErrorBox\(fieldName\)
-   hideFieldMsg\(fieldName, clearAll\)
-   hideRelatedList\(listTableName\)
-   hideRelatedLists\(\)
-   isMandatory\(fieldName\)
-   isNewRecord\(\)
-   isReadOnly\(fieldName\)
-   isVisible\(fieldName\)
-   removeDecoration\(fieldName, icon, title\)
-   removeOption\(fieldName, value\)
-   save\(\)
-   serialize\(onlyDirtyFields\)
-   setFieldPlaceholder\(fieldName, placeholder\)
-   setLabel\(fieldName, label\)
-   setMandatory\(fieldName, isMandatory\)
-   setReadOnly\(fieldName, isReadOnly\)
-   setSectionDisplay\(sectionName, isVisible\)
-   setValue\(fieldName, value, displayValue\)
-   setVisible\(fieldName, isVisible\)
-   showErrorBox\(fieldName, message, scrollForm\)
-   showFieldMsg\(fieldName, message, type: "info \| error", scrollForm\)
-   showRelatedList\(relatedTableName\)
-   showRelatedLists\(\)
-   submit\(submitActionName\)

 **Note:** Using the `variables.var_name` notation with the g\_form API is not supported in Service Portal. g\_form as a global object cannot be used in a widget client controller or in a UI script.

</td></tr><tr><td>

g\_list

</td><td>

-   get\(fieldName\)
-   addItem\(value, displayValue\)
-   removeItem\(value\)
-   reset\(\)
-   setQuery\(queryString\)
-   setDefaultOperator\(operator\)
-   getDefaultOperator\(\)

</td></tr><tr><td>

g\_service\_catalog

</td><td>

isOrderGuide\(\)

</td></tr><tr><td>

GlideAjax

</td><td>

-   addParam \(name, value\)
-   getParam \(name\)
-   getXML\(callback\)
-   getXMLAnswer\(callback\)
-   getJSON\(callback\)
-   setErrorCallback\(errorCallback\)
-   getURL\(\)
-   getParams\(\)
-   execute\(\)
-   successCalback\(data, status, xhr\)
-   errorCallback\(xhr\)
-   setScope\(scope\)

 **Note:**

-   Because the mobile platform does not allow synchronous GlideAjax calls, the getXMLWait\(\) method in a GlideAjax call does not work in the Service Portal. Instead, use one of the asynchronous calls such as getXML\(Function callback\) or getXMLAnswer\(Function callback\).
-   GlideAjax cannot be used in a widget client controller.

</td></tr><tr><td>

GlideRecord

</td><td>

-   addQuery\(encodedQuery\)
-   addQuery\(fieldName, operator, value\)
-   getEncodedQuery\(\)
-   get\(id\)
-   getTableName\(\)
-   hasNext\(\)
-   insert\(callback\)
-   gotoTop\(\)
-   next\(\)
-   loadRow\(rowObj\)
-   getValue\(fieldName\)
-   setValue\(fieldName, value\)
-   isDotWalkField\(fieldName\)
-   addOrderBy\(fieldName\)
-   setDisplayFields\(fieldNames\)
-   query\(callback\)
-   setRows\(rowsArray\)
-   setTableName\(tableName\)
-   setLimit\(maxInt\)
-   getLimit\(\)

</td></tr><tr><td>

i18NV3

</td><td>

getMessage\(String messageKey, Function callback\)

</td></tr></tbody>
</table>**Parent Topic:**[Service Portal and client scripts](../concept/unsupported_client_scripts.md)

