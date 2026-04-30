---
title: IBQConfigBase API - Scoped
description: Script include that must be extended for Sales Customer Relationship Management Request Tracker to track the requests. This script include provides overridable methods that define how requests should be executed.Creates a parent record which gets added to the record\_id of the Inbound Request \[sn\_tmt\_core\_inbound\_queue\_list\] record before processing the request.Determines whether a flow should run in sync or async mode.Defines the logic for processing an inbound request record.Sets the execute\_after value and updates state to Pending on the current inbound request record to configure the order in which records are processed in the Inbound Request table.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 18
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IBQConfigBase API - Scoped

Script include that must be extended for Sales Customer Relationship Management Request Tracker to track the requests. This script include provides overridable methods that define how requests should be executed.

The Sales and Service API Core \(com.sn\_tmt\_core\) plugin must be activated for IBQConfigBase script include to be available in an instance. This script include belongs to the `sn_tmt_core` namespace and requires the admin role.

See also:

-   [Lead to Cash Core](https://www.servicenow.com/docs/access?context=lead-to-cash&version=zurich&pubname=zurich-order-management&ft:locale=en-US)
-   [Inbound Request](https://www.servicenow.com/docs/access?context=som_request_tracker&version=zurich&pubname=zurich-order-management&ft:locale=en-US)

## Extending the IBQConfigBase API

Define a script include with the overridable methods of the IBQConfigBase API.

1.  Create a script include. The name must start with `IBQConfig`, for example, IBQConfigQuoteToOrderFlowSNC.
2.  Extend the IBQConfigBase API.

    For example:

    ```
    IBQConfigQuoteToOrderFlowSNC.prototype = Object.extendsObject(sn_tmt_core.IBQConfigBase, { 
    ...
    });
    ```

3.  Override any necessary methods provided by the IBQConfigBase API.

    For example:

    ```
    getRunMode: function(inboundQueueParams) {
        return this.quoteUtil.getQuoteSize(inboundQueueParams.source_record_ids, this.threshold);
    },
    
    generateParentRecord: function(inboundQueueParams, additionalParams, context) {
        var result = "";
        var entityMappingGr = this.getMapingConfigIdFromSysId(inboundQueueParams.requested_flow);
        var sourceToTargetConfigID = entityMappingGr.getValue("mapping_config_id");
        var sourceHeaderId = inboundQueueParams.source_record_ids;
        if (gs.nil(inboundQueueParams.requested_flow))
            throw "sourceToTargetConfigID cannot be null";
        if (gs.nil(inboundQueueParams.source_record_ids))
            throw "source record id cannot be null";
        var util = new sn_l2c_core.PrimitiveUtil();
        if (gs.nil(additionalParams))
            additionalParams = {};
        additionalParams[this.SKIP_LINES_KEY] = "true";
    },
    
    processInboundQueueRequest: function(inboundQueueGR) {
        gs.info("processRequest inboundQueueGR " + JSON.stringify(inboundQueueGR));
        var result = this.quoteUtil.createOrderFromQuoteUsingMetadata(inboundQueueGR.getValue('source_record_ids'), 'sn_l2c_quote_to_order', null, null, inboundQueueGR.getValue('record_id'));
        return result;
    }
    ```

4.  Create a new metadata entry in Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to define how a request should be processed.
5.  Link the script include created to the **configuration\_api** field of metadata record to use the custom logic defined while processing the request. The script include is referenced in the **configuration\_api** field while creating Inbound Request Configuration metadata.

## Use case: IBQConfigQuoteToOrderFlow

You can use the IBQConfigBase API to create an order from a quote using inbound request configuration metadata. IBQConfigQuoteToOrderFlow is a custom script include that can be created by extending the IBQConfigBase API. The logic for the overridable methods must be added in the IBQConfigQuoteToOrderFlow script include.

**Note:** This script include extends the IBQConfigBase API and is used in the method examples. For information on using the PrimitiveUtil API, refer to [LeadtoCashCore - Scoped](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#).

```
var IBQConfigQuoteToOrderFlowSNC = Class.create();
IBQConfigQuoteToOrderFlowSNC.prototype = Object.extendsObject(sn_tmt_core.IBQConfigBase, {

    initialize: function() {
		this.quoteUtil = new sn_quote_mgmt.OrderIntegration();
        this.SKIP_LINES_KEY = "skipLines";
		this.threshold = 15;
    },

    getRunMode: function(inboundQueueParams) {
        return this.quoteUtil.getQuoteSize(inboundQueueParams.source_record_ids, this.threshold);
    },


    generateParentRecord: function(inboundQueueParams, additionalParams, context) {
        var result = "";
        var entityMappingGr = this.getMapingConfigIdFromSysId(inboundQueueParams.requested_flow);
        var sourceToTargetConfigID = entityMappingGr.getValue("mapping_config_id");
        var sourceHeaderId = inboundQueueParams.source_record_ids;
        if (gs.nil(inboundQueueParams.requested_flow))
            throw "sourceToTargetConfigID cannot be null";
        if (gs.nil(inboundQueueParams.source_record_ids))
            throw "source record id cannot be null";
        var util = new sn_l2c_core.PrimitiveUtil();
        if (gs.nil(additionalParams))
            additionalParams = {};
        additionalParams[this.SKIP_LINES_KEY] = "true";

        // additional parameters are retrieved using the PrimitiveUtil() utility methods provided by the Lead to Cash Core application
        var service = util.getPrimitivesEPService(sourceToTargetConfigID, context);
        var isEmpty = false;
        if (service) {
            var createInstanceOutput = service.createInstance(sourceHeaderId, null, false, additionalParams);
            if (gs.nil(sourceHeaderId))
                isEmpty = this.__isEmpty(createInstanceOutput.lineItems);
            else
                isEmpty = this.__isEmpty(createInstanceOutput);
            if (!isEmpty) {
                var effectOutput = service.effect(createInstanceOutput, null, additionalParams);
                if (!this.__isEmpty(effectOutput)) {
                    var commitOutput = service.commitInstance(effectOutput, additionalParams);
                    return commitOutput;
                }
            }
        }
        return result;
    },

    processInboundQueueRequest: function(inboundQueueGR) {
        gs.info("processRequest inboundQueueGR " + JSON.stringify(inboundQueueGR));
        var result = this.quoteUtil.createOrderFromQuoteUsingMetadata(inboundQueueGR.getValue('source_record_ids'), 'sn_l2c_quote_to_order', null, null, inboundQueueGR.getValue('record_id'));
        return result;
    },

    __isEmpty: function(sourceObj) {
        if (gs.nil(sourceObj))
            return true;
        return Object.keys(sourceObj).length === 0;
    },
    getMapingConfigIdFromSysId(requestedFlow) {
        var gr = new GlideRecord("sn_l2c_core_entity_mapping");
        gr.addQuery("sys_id", requestedFlow);
        gr.query();
        if (gr.next()) {
            gs.info("mapping id received to corresponding requestedFlow");
            return gr;
        }
    },

    type: 'IBQConfigQuoteToOrderFlowSNC'
});
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IBQConfigBase – generateParentRecord\(Object ibqParams\)

Creates a parent record which gets added to the record\_id of the Inbound Request \[sn\_tmt\_core\_inbound\_queue\_list\] record before processing the request.

Having a parent record created before processing is ideal for asynchronous processing and allows you to add activities to your script include that can be performed while processing. For example, displaying a message on the screen.

<table id="id_dpy_1kb_z2c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ibqParams

</td><td>

Object

</td><td>

JSON object containing the details of Inbound Request record to be created.```
{
  "account": "String",
  "consumer": "String",
  "contact": "String",
  "payload": {Object},
  "record_id": "String",
  "requested_flow": "String",
  "source_record_ids": [Array],
  "source_table": "String",
  "table": "String"
}
```

</td></tr><tr id="ibqc-account"><td>

account

</td><td>

String

</td><td>

Optional. Information about the account associated with the record.Table: Account \[customer\_account\]

</td></tr><tr id="ibqc-consumer"><td>

consumer

</td><td>

String

</td><td>

Optional. Information about the consumer associated with the record.Table: Consumer \[csm\_consumer\]

</td></tr><tr id="ibqc-contact"><td>

contact

</td><td>

String

</td><td>

Optional. Information about the contact associated with the record.Table: Contact \[customer\_contact\]

</td></tr><tr id="ibqc-payload"><td>

payload

</td><td>

Object

</td><td>

Optional. JSON object needed to process the request using the PrimitiveUtil\(\) API. For usage information, see [LeadToCashCore](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#).```
"payload": {
  "additionalParams": {Object},
  "context": {Object},
  "inputParams": {Object}
  "source": [Array of Objects],
  "target": [Array of Objects]
}
```

</td></tr><tr id="ibqc-payload.additionalParams"><td>

payload.additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.```
"additionalParams": {
  "action": "String",
  "actionReason": "String"
  "endDate": "Date",
  "skipLines": "Boolean",
  "startDate": "Date"
}
```

</td></tr><tr id="ibqc-payload.additionalParams.action"><td>

payload.additionalParams.action

</td><td>

String

</td><td>

Optional. Specifies the type of declarative action being executed. For more information, see [Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).Possible values:

-   disconnect
-   modify
-   resume
-   suspend

</td></tr><tr id="ibqc-payload.additionalParams.actionReason"><td>

payload.additionalParams.actionReason

</td><td>

String

</td><td>

Optional. Property used in flows using declarative actions. Reason for the action.

</td></tr><tr id="ibqc-payload.additionalParams.endDate"><td>

payload.additionalParams.endDate

</td><td>

String

</td><td>

Optional. End date required to execute flows using declarative actions.Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr id="ibqc-payload.additionalParams.skipLines"><td>

payload.additionalParams.skipLines

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to fetch line items for the specified entity.Valid values:

-   true: Skip returning line items information for the entity.
-   false: Return line items information for the entity.

Default: false

</td></tr><tr id="ibqc-payload.additionalParams.startDate"><td>

payload.additionalParams.startDate

</td><td>

String

</td><td>

Optional. Start date to execute flows using declarative actions.Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr id="ibqc-payload.context"><td>

payload.context

</td><td>

Object

</td><td>

Optional. Additional parameter options for displaying attribute values and for invoking more than one instance at a time.```
"context": {
  "isMultiSelect": "Boolean",
  "sourceToTargetConfigID": "String"
}
```

</td></tr><tr id="ibqc-payload.context.isMultiselect"><td>

payload.context.isMultiSelect

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to pass multiple entities as input to create the instance.Valid values:

-   true: Enables passing multiple line items in a comma-separated list.
-   false: Only one input item can be passed in the script.

Default: false

</td></tr><tr id="ibqc-payload.context.sTTCID"><td>

payload.context.sourceToTargetConfigID

</td><td>

String

</td><td>

Optional. Mapping configuration ID for the source-to-target mapping.Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr><tr id="ibqc-payload.inputParams"><td>

payload.inputParams

</td><td>

Object

</td><td>

Optional. This object is a placeholder for any input parameters required to invoke the usage of a specific flow.```
"inputParams": {}
```

</td></tr><tr id="ibqc-payload.source"><td>

payload.source

</td><td>

Array

</td><td>

Optional. JSON object containing details of the source entity to retrieve data from.```
"source": [
  {
    "headerId": "String",
    "lineIds": []
  }
]
```

</td></tr><tr id="ibqc-payload.headerId"><td>

payload.source.headerId

</td><td>

String

</td><td>

Optional. Header sys\_id of source entity to retrieve data from.-   Required if you don't provide the **lineIds** parameter.
-   Pass  null  if you aren't passing any header sys\_ids.

</td></tr><tr id="ibqc-payload.source.lineIds"><td>

payload.source.lineIds

</td><td>

Array

</td><td>

Optional. Array containing source line item sys\_id\(s\) of an entity to retrieve entity data from.Required if you don't provide  the header ID, and if the entity structure starts with line items such as sold product.

</td></tr><tr id="ibqc-payload.target"><td>

payload.target

</td><td>

Array

</td><td>

Optional. JSON object containing details of the target entity.```
"target": [
  {
    "headerId": "String",
    "lineIds": []
  }
]
```

</td></tr><tr id="ibqc-payload.target.headerId"><td>

payload.target.headerId

</td><td>

String

</td><td>

Optional. Header sys\_id of target entity to retrieve data from. Required if you don't provide the **lineIds** parameter. Pass  null  if you aren't passing any header sys\_ids.

</td></tr><tr id="ibqc-payload.target.lineIds"><td>

payload.target.lineIds

</td><td>

Array

</td><td>

Optional. Array containing target line item sys\_id\(s\) of an entity to retrieve entity data from. Required if you don't provide  header ID  and if the entity structure starts with line items such as sold product.

</td></tr><tr id="ibqc-record"><td>

record\_id

</td><td>

String

</td><td>

Optional. Sys\_id of the target record if already present.

</td></tr><tr id="ibqc-requested_flow"><td>

requested\_flow

</td><td>

String

</td><td>

Optional. Mapping configuration ID for source-to-target mapping. This property is required for flows using [Entity configuration and mapping](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&version=zurich&pubname=zurich-order-management&ft:locale=en-US).Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr><tr id="ibqc-source_records_ids"><td>

source\_record\_ids

</td><td>

Array

</td><td>

Array containing the sys\_ids of the source records.

</td></tr><tr id="ibqc-source_table"><td>

source\_table

</td><td>

String

</td><td>

Name of the table that contains the source record of the flow.

</td></tr><tr id="ibqc-table"><td>

table

</td><td>

String

</td><td>

Name of the table that contains the target record of the flow.

</td></tr></tbody>
</table><table id="table_qw2_3ct_y2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON object

</td><td>

A JSON object containing header ID of the target record created.```
{
 "headerID": "String",
 // additional parameters, if any, per flow see payload.inputParams
}
```

</td></tr><tr><td>

headerID

</td><td>

Sys\_id of the header of the target record created. This value is used to populate record\_id field while creating the Inbound Request record.

</td></tr></tbody>
</table>The following example shows how to invoke the generateParentRecord\(\) method.

**Note:** IBQConfigQuoteToOrderFlow is a custom script include that can be created by extending the IBQConfigBase API. The logic for the overridable methods must be added in the IBQConfigQuoteToOrderFlow script include.

```
var ibqParams = {
  "source_record_ids": "f83e29574df02210f877142d1adc9531",
  "requested_flow": "0feb6d9da36271105c24939ef31e61dc",
  "initiated_by": "admin",
  "source_table": "sn_quote_mgmt_core_quote",
  "table": "sn_ind_tmt_orm_order",
  "payload": {}
}; 

var service = new sn_quote_mgmt.IBQConfigQuoteToOrderFlow(); 
var parentRecord = service.generateParentRecord(ibqParams); 

gs.info("Parent record = "+JSON.stringify(parentRecord));
```

Output:

```
Parent record = {"headerID":"d11bd507dc6c6a10f877720033b5d0b9", ...} 
```

## IBQConfigBase – getRunMode\(Object ibqParams\)

Determines whether a flow should run in sync or async mode.

<table id="id_dpy_1kb_z2c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ibqParams

</td><td>

Object

</td><td>

JSON object containing the details of Inbound Request record to be created.```
{
  "account": "String",
  "consumer": "String",
  "contact": "String",
  "payload": {Object},
  "record_id": "String",
  "requested_flow": "String",
  "source_record_ids": [Array],
  "source_table": "String",
  "table": "String"
}
```

</td></tr><tr id="ibqc-account"><td>

account

</td><td>

String

</td><td>

Optional. Information about the account associated with the record.Table: Account \[customer\_account\]

</td></tr><tr id="ibqc-consumer"><td>

consumer

</td><td>

String

</td><td>

Optional. Information about the consumer associated with the record.Table: Consumer \[csm\_consumer\]

</td></tr><tr id="ibqc-contact"><td>

contact

</td><td>

String

</td><td>

Optional. Information about the contact associated with the record.Table: Contact \[customer\_contact\]

</td></tr><tr id="ibqc-payload"><td>

payload

</td><td>

Object

</td><td>

Optional. JSON object needed to process the request using the PrimitiveUtil\(\) API. For usage information, see [LeadToCashCore](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#).```
"payload": {
  "additionalParams": {Object},
  "context": {Object},
  "inputParams": {Object}
  "source": [Array of Objects],
  "target": [Array of Objects]
}
```

</td></tr><tr id="ibqc-payload.additionalParams"><td>

payload.additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.```
"additionalParams": {
  "action": "String",
  "actionReason": "String"
  "endDate": "Date",
  "skipLines": "Boolean",
  "startDate": "Date"
}
```

</td></tr><tr id="ibqc-payload.additionalParams.action"><td>

payload.additionalParams.action

</td><td>

String

</td><td>

Optional. Specifies the type of declarative action being executed. For more information, see [Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).Possible values:

-   disconnect
-   modify
-   resume
-   suspend

</td></tr><tr id="ibqc-payload.additionalParams.actionReason"><td>

payload.additionalParams.actionReason

</td><td>

String

</td><td>

Optional. Property used in flows using declarative actions. Reason for the action.

</td></tr><tr id="ibqc-payload.additionalParams.endDate"><td>

payload.additionalParams.endDate

</td><td>

String

</td><td>

Optional. End date required to execute flows using declarative actions.Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr id="ibqc-payload.additionalParams.skipLines"><td>

payload.additionalParams.skipLines

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to fetch line items for the specified entity.Valid values:

-   true: Skip returning line items information for the entity.
-   false: Return line items information for the entity.

Default: false

</td></tr><tr id="ibqc-payload.additionalParams.startDate"><td>

payload.additionalParams.startDate

</td><td>

String

</td><td>

Optional. Start date to execute flows using declarative actions.Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr id="ibqc-payload.context"><td>

payload.context

</td><td>

Object

</td><td>

Optional. Additional parameter options for displaying attribute values and for invoking more than one instance at a time.```
"context": {
  "isMultiSelect": "Boolean",
  "sourceToTargetConfigID": "String"
}
```

</td></tr><tr id="ibqc-payload.context.isMultiselect"><td>

payload.context.isMultiSelect

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to pass multiple entities as input to create the instance.Valid values:

-   true: Enables passing multiple line items in a comma-separated list.
-   false: Only one input item can be passed in the script.

Default: false

</td></tr><tr id="ibqc-payload.context.sTTCID"><td>

payload.context.sourceToTargetConfigID

</td><td>

String

</td><td>

Optional. Mapping configuration ID for the source-to-target mapping.Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr><tr id="ibqc-payload.inputParams"><td>

payload.inputParams

</td><td>

Object

</td><td>

Optional. This object is a placeholder for any input parameters required to invoke the usage of a specific flow.```
"inputParams": {}
```

</td></tr><tr id="ibqc-payload.source"><td>

payload.source

</td><td>

Array

</td><td>

Optional. JSON object containing details of the source entity to retrieve data from.```
"source": [
  {
    "headerId": "String",
    "lineIds": []
  }
]
```

</td></tr><tr id="ibqc-payload.headerId"><td>

payload.source.headerId

</td><td>

String

</td><td>

Optional. Header sys\_id of source entity to retrieve data from.-   Required if you don't provide the **lineIds** parameter.
-   Pass  null  if you aren't passing any header sys\_ids.

</td></tr><tr id="ibqc-payload.source.lineIds"><td>

payload.source.lineIds

</td><td>

Array

</td><td>

Optional. Array containing source line item sys\_id\(s\) of an entity to retrieve entity data from.Required if you don't provide  the header ID, and if the entity structure starts with line items such as sold product.

</td></tr><tr id="ibqc-payload.target"><td>

payload.target

</td><td>

Array

</td><td>

Optional. JSON object containing details of the target entity.```
"target": [
  {
    "headerId": "String",
    "lineIds": []
  }
]
```

</td></tr><tr id="ibqc-payload.target.headerId"><td>

payload.target.headerId

</td><td>

String

</td><td>

Optional. Header sys\_id of target entity to retrieve data from. Required if you don't provide the **lineIds** parameter. Pass  null  if you aren't passing any header sys\_ids.

</td></tr><tr id="ibqc-payload.target.lineIds"><td>

payload.target.lineIds

</td><td>

Array

</td><td>

Optional. Array containing target line item sys\_id\(s\) of an entity to retrieve entity data from. Required if you don't provide  header ID  and if the entity structure starts with line items such as sold product.

</td></tr><tr id="ibqc-record"><td>

record\_id

</td><td>

String

</td><td>

Optional. Sys\_id of the target record if already present.

</td></tr><tr id="ibqc-requested_flow"><td>

requested\_flow

</td><td>

String

</td><td>

Optional. Mapping configuration ID for source-to-target mapping. This property is required for flows using [Entity configuration and mapping](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&version=zurich&pubname=zurich-order-management&ft:locale=en-US).Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr><tr id="ibqc-source_records_ids"><td>

source\_record\_ids

</td><td>

Array

</td><td>

Array containing the sys\_ids of the source records.

</td></tr><tr id="ibqc-source_table"><td>

source\_table

</td><td>

String

</td><td>

Name of the table that contains the source record of the flow.

</td></tr><tr id="ibqc-table"><td>

table

</td><td>

String

</td><td>

Name of the table that contains the target record of the flow.

</td></tr></tbody>
</table><table id="table_qw2_3ct_y2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Information about the run mode to be used to execute the request.Possible values:

-   async
-   sync

</td></tr></tbody>
</table>The following example shows how to invoke the getRunMode\(\) method using the source sys\_id provided by the source\_record\_ids property. If the line items count is greater than 10, then **runMode** is `async`.

**Note:** IBQConfigQuoteToOrderFlow is a custom script include that can be created by extending the IBQConfigBase API. The logic for the overridable methods must be added in the IBQConfigQuoteToOrderFlow script include.

```
var ibqParams = {
  "source_record_ids": "04ba9004f11f3110f8777d7194f166f6",
  "requested_flow": "0feb6d9da36271105c24939ef31e61dc",
  "initiated_by": "admin",
  "source_table": "sn_quote_mgmt_core_quote",
  "table": "sn_ind_tmt_orm_order",
  "payload": {}
};

var service = new sn_quote_mgmt.IBQConfigQouteToOrderFlow();

var runMode = service.getRunMode(ibqParams);

gs.info("RunMode = "+JSON.stringify(runMode));
```

Output:

```
RunMode = "async"
```

The following example shows how to invoke getRunMode\(\) method. It uses the source sys\_id provided in source\_record\_ids. Here the line items count is fewer than 10, so the **runMode** is sync.

**Note:** IBQConfigQuoteToOrderFlow is a custom script include that can be created by extending the IBQConfigBase API. The logic for the overridable methods must be added in the IBQConfigQuoteToOrderFlow script include.

```
var ibqParams = {
  "source_record_ids": "0b0f5cc8f11f3110f8777d7194f16610",
  "requested_flow": "0feb6d9da36271105c24939ef31e61dc",
  "initiated_by": "admin",
  "source_table": "sn_quote_mgmt_core_quote",
  "table": "sn_ind_tmt_orm_order",
  "payload": {}
};

var service = new sn_quote_mgmt.IBQConfigQouteToOrderFlow();

var runMode = service.getRunMode(ibqParams);

gs.info("RunMode = "+JSON.stringify(runMode));
```

Output:

```
RunMode = "sync"
```

## IBQConfigBase – processInboundQueueRequest\(GlideRecord ibqGr\)

Defines the logic for processing an inbound request record.

<table id="table_pw2_3ct_y2c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ibqGr

</td><td>

GlideRecord

</td><td>

[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) reference to the Inbound Request record that has triggered the flow.Table: Inbound Request \[sn\_tmt\_core\_inbound\_queue\] 

</td></tr></tbody>
</table><table id="table_qw2_3ct_y2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

A JSON object containing the processing details of the Inbound Request record.```
{
  "error": "String",
  "response": {Object},
  "status": "String",
  "target": "String"
}
```

</td></tr><tr><td>

error

</td><td>

Value indicating the error encountered while processing the request.Data type: String

</td></tr><tr><td>

response

</td><td>

A JSON object containing the response of processing the Inbound Request record. For flows created by the Lead to Cash Core PrimitiveUtil API, this output can be provided using the [commitInstance\(\)](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#) method.Data type: Object

</td></tr><tr><td>

status

</td><td>

Value indicating the status of the request processing.Possible values:

-   failure – The operation has failed.
-   partial\_success – There were few failures while processing the JSON object. Refer to processing logs in the Log \[syslog\] table to troubleshoot specific errors. 
-   success – The operation was successful.

Data type: String

</td></tr><tr><td>

target

</td><td>

Optional. Sys\_id of the target record to be used for further processing, such as UI acknowledgment. The target can either be created during the flow or can be passed as input to the **ibqParams** of the generateParentRecord\(\) method depending on the requirement.Data type: String

</td></tr></tbody>
</table>The following example shows how to invoke processInboundQueueRequest\(\) method.

**Note:** This method is called during the flow using [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US). In the following example, the Lead to Cash Core PrimitiveUtil [commitInstance\(\)](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#) method is used to provide the output.

```
var gr = new GlideRecord('sn_tmt_core_inbound_queue');
gr.get('c48ea9974df02210f877142d1adc951a');

var service = new sn_quote_mgmt.IBQConfigQuoteToOrderFlow();
var processRequest = service.processInboundQueueRequest(gr);

gs.info("processRequest = "+JSON.stringify(processRequest));
```

Output:

```
processRequest = {
  "response": {
    "status": "success",
    "error": "",
    "message": "Commit operation successfully processed.",
    "displayMessage": "Commit operation successfully processed.",
    "dataObject": {
      "sys_id": "a6f4568bdce0aa10f877720033b5d069",
      "table": "sn_ind_tmt_orm_order",
      "attributes": {
        "account": {
          "value": "9e2fd2ee11b43110f877366201dea674"
        },
        "quote": {
          "value": "c8841a4bdce0aa10f877720033b5d0f8"
        }
      },
      "_glide_action": "UPDATE",
      "_source_object": {
        "sys_id": "c8841a4bdce0aa10f877720033b5d0f8",
        "table": "sn_quote_mgmt_core_quote"
      },
      "lineItems": [
        {
          "sys_id": "-1",
          "table": "sn_ind_tmt_orm_order_line_item",
          "attributes": {
            "short_description": {
              "value": "Home Automation Bundle"
            },
            "account": {
              "value": "9e2fd2ee11b43110f877366201dea674"
            }
          },
          "_glide_action": "INSERT",
          "_source_object": {
            "sys_id": "afc4528bdce0aa10f877720033b5d0d0",
            "table": "sn_quote_mgmt_core_quote_line_item"
          },
          "characteristics": [],
          "lineItems": [
            {
              "sys_id": "-1",
              "table": "sn_ind_tmt_orm_order_line_item",
              "attributes": {
                "short_description": {
                  "value": "Door Sensor"
                },
                "account": {
                  "value": "9e2fd2ee11b43110f877366201dea674"
                }
              },
              "_glide_action": "INSERT",
              "_source_object": {
                "sys_id": "77c4528bdce0aa10f877720033b5d0d5",
                "table": "sn_quote_mgmt_core_quote_line_item"
              },
              "characteristics": [],
              "lineItems": [],
              "pricingAdjustments": [
                {
                  "sys_id": "-1",
                  "table": "sn_ind_tmt_orm_pricing_adjustment",
                  "attributes": {
                    "name": {
                      "value": "door sensor bundle discount"
                    }
                  },
                  "_glide_action": "INSERT",
                  "_source_object": {
                    "sys_id": "f3c4928bdce0aa10f877720033b5d02f",
                    "table": "sn_quote_mgmt_core_pricing_adjustment"
                  },
                  "_commitObjectInfo": {
                    "sys_id": "e6955acbdce0aa10f877720033b5d082",
                    "status": "success"
                  }
                }
              ],
              "coveredProducts": [],
              "attributeAdjustment": [],
              "_commitObjectInfo": {
                "sys_id": "26955acbdce0aa10f877720033b5d07d",
                "status": "success"
              }
            }
          ],
          "pricingAdjustments": [],
          "coveredProducts": [],
          "attributeAdjustment": [],
          "_commitObjectInfo": {
            "sys_id": "22955acbdce0aa10f877720033b5d078",
            "status": "success"
          }
        }
      ],
      "_commitObjectInfo": {
        "status": "success"
      }
    },
    "headerID": "a6f4568bdce0aa10f877720033b5d069",
    "rootLineIDs": [
      "22955acbdce0aa10f877720033b5d078"
    ]
  },
  "status": "success",
  "error": "",
  "target": "a6f4568bdce0aa10f877720033b5d069"
}
```

## IBQConfigBase – setExecuteAfterRequest\(Object ibqParams\)

Sets the `execute_after` value and updates `state` to Pending on the current inbound request record to configure the order in which records are processed in the Inbound Request table.

The setExecuteAfterRequest\(\) method can be overridden to derive the **execute\_after** value from other parameters. By default, this method queries the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table to find the latest record with matching **source\_record\_ids**, **record\_id**, and **resource** values. This method then updates the current record's `execute_after` field with the queried record's sys\_id, marking the current record to be processed after the queried record. As a result, setExecuteAfterRequest\(\) establishes the order in which records are processed.

<table id="table_hbf_vqr_tfc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ibqParams

</td><td>

Object

</td><td>

JSON object containing the details of Inbound Request records to set. These parameters include the record sys\_id to process before the current record, and the workflow name to filter by in the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table.```
{
  "account": "String",
  "consumer": "String",
  "contact": "String",
  "execute_after": "String",
  "payload": {Object},
  "record_id": "String",
  "requested_flow": "String",
  "resource": "String",
  "source_record_ids": [Array],
  "source_table": "String",
  "table": "String"
}
```

</td></tr><tr><td>

account

</td><td>

String

</td><td>

Optional. Information about the account associated with the record.Table: Account \[customer\_account\]

</td></tr><tr><td>

consumer

</td><td>

String

</td><td>

Optional. Information about the consumer associated with the record.Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td>

String

</td><td>

Optional. Information about the contact associated with the record.Table: Contact \[customer\_contact\]

</td></tr><tr><td>

ibqParams.execute\_after

</td><td>

String

</td><td>

Optional. Sys\_id of inbound request to process before the current request.Table: Inbound Request \[sn\_tmt\_core\_inbound\_queue\]

</td></tr><tr><td>

payload

</td><td>

Object

</td><td>

Optional. JSON object needed to process the request using the PrimitiveUtil\(\) API. For usage information, see [LeadToCashCore](../../LeadtoCashCoreScoped/concept/LeadToCashCoreAPI.md#).```
"payload": {
  "additionalParams": {Object},
  "context": {Object},
  "inputParams": {Object}
  "source": [Array of Objects],
  "target": [Array of Objects]
}
```

</td></tr><tr><td>

payload.additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.```
"additionalParams": {
  "action": "String",
  "actionReason": "String"
  "endDate": "Date",
  "skipLines": "Boolean",
  "startDate": "Date"
}
```

</td></tr><tr><td>

payload.additionalParams.action

</td><td>

String

</td><td>

Optional. Specifies the type of declarative action being executed. For more information, see [Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).Possible values:

-   disconnect
-   modify
-   resume
-   suspend

</td></tr><tr><td>

payload.additionalParams.actionReason

</td><td>

String

</td><td>

Optional. Property used in flows using declarative actions. Reason for the action.

</td></tr><tr><td>

payload.additionalParams.endDate

</td><td>

String

</td><td>

Optional. End date required to execute flows using declarative actions.Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr><td>

payload.additionalParams.skipLines

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to fetch line items for the specified entity.Valid values:

-   true: Skip returning line items information for the entity.
-   false: Return line items information for the entity.

Default: false

</td></tr><tr><td>

payload.additionalParams.startDate

</td><td>

String

</td><td>

Optional. Start date to execute flows using declarative actions.Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr><td>

payload.context

</td><td>

Object

</td><td>

Optional. Additional parameter options for displaying attribute values and for invoking more than one instance at a time.```
"context": {
  "isMultiSelect": "Boolean",
  "sourceToTargetConfigID": "String"
}
```

</td></tr><tr><td>

payload.context.isMultiSelect

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to pass multiple entities as input to create the instance.Valid values:

-   true: Enables passing multiple line items in a comma-separated list.
-   false: Only one input item can be passed in the script.

Default: false

</td></tr><tr><td>

payload.context.sourceToTargetConfigID

</td><td>

String

</td><td>

Optional. Mapping configuration ID for the source-to-target mapping.Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr><tr><td>

payload.inputParams

</td><td>

Object

</td><td>

Optional. This object is a placeholder for any input parameters required to invoke the usage of a specific flow.```
"inputParams": {}
```

</td></tr><tr><td>

payload.source

</td><td>

Array

</td><td>

Optional. JSON object containing details of the source entity to retrieve data from.```
"source": [
  {
    "headerId": "String",
    "lineIds": []
  }
]
```

</td></tr><tr><td>

payload.source.headerId

</td><td>

String

</td><td>

Optional. Header sys\_id of source entity to retrieve data from.-   Required if you don't provide the **lineIds** parameter.
-   Pass  null  if you aren't passing any header sys\_ids.

</td></tr><tr><td>

payload.source.lineIds

</td><td>

Array

</td><td>

Optional. Array containing source line item sys\_id\(s\) of an entity to retrieve entity data from.Required if you don't provide  the header ID, and if the entity structure starts with line items such as sold product.

</td></tr><tr><td>

payload.target

</td><td>

Array

</td><td>

Optional. JSON object containing details of the target entity.```
"target": [
  {
    "headerId": "String",
    "lineIds": []
  }
]
```

</td></tr><tr><td>

payload.target.headerId

</td><td>

String

</td><td>

Optional. Header sys\_id of target entity to retrieve data from. Required if you don't provide the **lineIds** parameter. Pass  null  if you aren't passing any header sys\_ids.

</td></tr><tr><td>

payload.target.lineIds

</td><td>

Array

</td><td>

Optional. Array containing target line item sys\_id\(s\) of an entity to retrieve entity data from. Required if you don't provide  header ID  and if the entity structure starts with line items such as sold product.

</td></tr><tr><td>

record\_id

</td><td>

String

</td><td>

Optional. Sys\_id of the target record if already present.

</td></tr><tr><td>

requested\_flow

</td><td>

String

</td><td>

Optional. Mapping configuration ID for source-to-target mapping. This property is required for flows using [Entity configuration and mapping](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&version=zurich&pubname=zurich-order-management&ft:locale=en-US).Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr><tr><td>

ibqParams.resource

</td><td>

String

</td><td>

Name of the flow that creates the record in the Inbound Request table \(for example, a quote or order\). This value is used to find dependent records of the same type to determine the order of record processing.

</td></tr><tr><td>

source\_record\_ids

</td><td>

Array

</td><td>

Array containing the sys\_ids of the source records.

</td></tr><tr><td>

source\_table

</td><td>

String

</td><td>

Name of the table that contains the source record of the flow.

</td></tr><tr><td>

table

</td><td>

String

</td><td>

Name of the table that contains the target record of the flow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

In the following example, the script queries the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table to find the latest record with matching source\_record\_ids, record\_id, and resource values. The script then calls the setExecuteAfterRequest\(\) method to update the current record's execute\_after value with the fetched record's sys\_id and sets its state to pending. As a result, the current record will execute after the record specified in the execute\_after field.

```
var ibqParams = { 
  "source_record_ids": "e32e29fd28d26a14f8775b8f954723b8",
  "record_id":"b9be293128166a14f8775b8f9547239f", 
  "requested_flow": "0feb6d9da36271105c24939ef31e61dc", 
  "initiated_by": "admin", 
  "source_table": "sn_quote_mgmt_core_quote", 
  "table": "sn_ind_tmt_orm_order", 
  "payload": {
  "context": {}}, 
  "resource": "quote_to_order" 
 }; 

new sn_tmt_core.IBQConfigBase().setExecuteAfterRequest(ibqParams);
```

This method does not return any output.

