---
title: TopicSubscriptionUtilOOB - Scoped
description: The TopicSubscriptionUtilOOB script include provides methods to query and manipulate records in the Topic subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table. This class operates at the service layer and interacts with the Data Access Object \(DAO\) class.Triggers a spoke subflow to register the passed topic subscription on an external system.Returns the subflow to use for the spoke selector subflow trigger to register topic subscriptions.Returns the name of the topic associated with the passed sys\_id of a record in the Topic Subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table.Returns the sys\_ids of any unregistered topics. Unregistered topics are those topics that are in the Topic \[sn\_api\_notif\_mgmt\_topic\] table, but not in the Topic Subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table.Updates the topic subscription record in the Topic subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table with the values from the mock registration response of an outbound topic registration endpoint call.Stores the current topic subscription record in the Topic subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table using DAO insert.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TopicSubscriptionUtilOOB- Scoped

The TopicSubscriptionUtilOOB script include provides methods to query and manipulate records in the Topic subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table. This class operates at the service layer and interacts with the Data Access Object \(DAO\) class.

These functions are called when the **Register** button is selected on the Topic Subscription form. If you want to change the default functionality of this script include, you need to override the functions contained in this script include in the `TopicSubscriptionUtil` script include.

Both script includes run in the `sn_api_notif_mgmt` namespace.

For additional information on topic subscriptions, see External event management via Telecommunications API notifications.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TopicSubscriptionUtilOOB - executeRegistrationSubflow\(String topicSubID\)

Triggers a spoke subflow to register the passed topic subscription on an external system.

Before triggering the registration flow, the function checks whether the passed topic subscription record contains a callback URL and whether the topic is already registered. If these checks pass, it triggers a demo subflow. This demo subflow is defined as an adapter in the spoke selector and performs a "mock" outbound registration call.

This function is called when a user selects the **Register** button in the Topic subscriptions form. The name of the demo subflow is defined in `Constants.INITIATE_REGISTRATION_PROCESS = "sn_ind_tmf642.initiate_registration_process";`

You need to override this function in the `TopicSubscriptionUtil` script include to define your own custom subflow to register topic subscriptions.

Within this registration subflow you must create a REST step, connection alias, or other implementation to call a registration endpoint on the external system to register a topic. This endpoint should pass the topic name and callback URL to register. In return, the external system endpoint should return the subscription ID, whether the registration was successful, and the registration information to store in the Topic subscription table. This information typically includes the registration status, registration message, and subscription ID fields. Your registration subflow should then call the [updateRegistrationResponse\(\)](TopicSubscriptionUtilAPIScoped.md#) method to store the response payload in the Topic subscription table.

|Name|Type|Description|
|----|----|-----------|
|topicSubID|String|Sys\_id of the topic subscription record to register.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to override this function.

```
var TopicSubscriptionUtil= Class.create();  

TopicSubscriptionUtil.prototype =
 Object.extendsObject(TopicSubscriptionUtilOOB, { 

  // Define overriding functions here. Pass the topicSubID of the record to be registered for subscription 
  executeRegistrationSubflow: function(topicSubID){ 
    var topicSubGr = new TopicSubscriptionUtil(topicSubID).topicSubscriptionDAO.getGlideRecord(); 

    // Customer extensible function to call their defined subflows. Here one can call their own subflow that 
    // will perform registration by giving an endpoint of the external env and parsing and updating the topic Sub 
    // record with Registered information. 
    var registrationFlow = ''; // Pass the subflow name that you want to override here. 
    var inputs = {}; 
    inputs['topic_subscription_rec'] = topicSubGr; 
    try {
      var flowOp = sn_fd.FlowAPI.getRunner().subflow(registrationFlow).inBackground().withInputs(inputs).run(); 

    } catch (ex) { 
      gs.addErrorMessage(gs.getMessage(ex + ' Please check the subflow and inputs defined.')); 

    } 
  }
  type: TopicSubscriptionUtil 
});
```

## TopicSubscriptionUtilOOB - getSubFlowName\(\)

Returns the subflow to use for the spoke selector subflow trigger to register topic subscriptions.

Typically this function is called from the [executeRegistrationSubflow\(\)](TopicSubscriptionUtilAPIScoped.md#) function. This subflow is responsible for contacting an external system and registering a topic subscription. The name of the subflow to use is defined in `Constants.INITIATE_REGISTRATION_PROCESS`.

You can change this functionality to include the name of your own subflow by overriding the name of the subflow to execute in the `sn_api_notif_mgmt.Constants` script include.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the subflow to use. For the demo implementation, this subflow is defined as `Constants.INITIATE_REGISTRATION_PROCESS = "sn_ind_tmf642.initiate_registration_process";`.|

The following code example shows how to override this function.

```
var TopicSubscriptionUtil= Class.create();
TopicSubscriptionUtil.prototype = 
  Object.extendsObject(TopicSubscriptionUtilOOB, { 

  // Define overriding functions here. Define a constants and return. 
  // That is your subflow that has the registration process. In current OOB implementation 
  // it’s a spoke selector implementation.
  getSubFlowName: function(){
    var subflowName = '' // Pass your subflow name here
    return subflowName; 
  } 

 type: TopicSubscriptionUtil 

});
```

## TopicSubscriptionUtilOOB - getTopicName\(topicSubRefID\)

Returns the name of the topic associated with the passed sys\_id of a record in the Topic Subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table.

<table id="table_n5m_grk_bzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicSubRefID

</td><td>

String

</td><td>

Sys\_id of the topic subscription record whose topic name to return. Table: Topic Subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Topic name.|

The following code example shows how to override this function.

```
var TopicSubscriptionUtil = Class.create();
TopicSubscriptionUtil.prototype = 
  Object.extendsObject(TopicSubscriptionUtilOOB, {

  // Define overriding functions here. Pass topicSubId or topicId and get topicname from there. 
  getTopicName: function(topicSubRefID){
    var topicSubGr = new TopicSubscriptionUtil(topicSubRefID).topicSubscriptionDAO.getGlideRecord(); 
    var topicRefID = topicSubGr.getValue('topic'); 
    var topicGr = new TopicUtil(topicRefID).topicDAO.getGlideRecord();
    return topicGr.getValue('topic_name');
  } 
type: TopicSubscriptionUtil 
}); 
```

## TopicSubscriptionUtilOOB - getUnregisteredTopicIds\(\)

Returns the sys\_ids of any unregistered topics. Unregistered topics are those topics that are in the Topic \[sn\_api\_notif\_mgmt\_topic\] table, but not in the Topic Subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List of sys\_ids of the topic records that have not yet been registered.|

The following code example shows update this function.

```
 var TopicSubscriptionUtil= Class.create();
TopicSubscriptionUtil.prototype = 
  Object.extendsObject(TopicSubscriptionUtilOOB, {

  // Define overriding functions here. This method is returning all topic IDs 
  // that are not in the Topic Subscription table. Modify queries here to 
  // return other topics in Topic Subscription table to return either 'Error' or 
  // 'UnRegistered' status topics. 

  getUnregisteredTopicIds: function(){ 
    var topicIds = []; 
    var topicSubscriptionGr = TopicSubscriptionDAO.getInSubscriptionTopic(); 
    if (!gs.nil(topicSubscriptionGr)) {
      while (topicSubscriptionGr.next()) { 
        topicIds.push(topicSubscriptionGr.getValue('topic'));
      }
    } 

    var unregisteredTopicGr = TopicDAO.getUnregisteredTopic(topicIds); 
    if (!gs.nil(unregisteredTopicGr)) { 
      var unregisterTopicIds = []; 
      while (unregisteredTopicGr.next()) { 
        unregisterTopicIds.push(unregisteredTopicGr.getValue('sys_id')); 
      } 
    } 

    return unregisterTopicIds;
  } 

  type: TopicSubscriptionUtil 
});
```

## TopicSubscriptionUtilOOB - updateRegistrationResponse\(Object registrationDetails\)

Updates the topic subscription record in the Topic subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table with the values from the mock registration response of an outbound topic registration endpoint call.

You can override this function in the `TopicSubscriptionUtil` script include to modify the information that is stored in the associated topic subscription record. For more information on executing the subflow that returns the registration details, see [executeRegistrationSubflow\(\)](TopicSubscriptionUtilAPIScoped.md#).

<table id="table_ixn_s3l_bzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

registration​Details

</td><td>

Object

</td><td>

For the demo implementation, this is a mock response returned by the demo registration API call. If you override this function, the response payload should at least contain the following topic subscription fields:

-   registration\_status
-   registration\_message
-   subscription\_id

</td></tr></tbody>
</table><table id="table_jxn_s3l_bzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Error

</td><td>

If the call is successful, nothing is returned. If an error occurred, it returns:-   status\_reason: Returned from a spoke call clarifying the reason for failure when `status_code = 0`.
-   errormessage: Error message that describes the failure when status\_code is not 0 or 1, such as: `'Spoke Request Type output not set, please check request adapter flow'`.

</td></tr></tbody>
</table>The following code example shows how to update this function.

```
var TopicSubscriptionUtil= Class.create();
TopicSubscriptionUtil.prototype = 
  Object.extendsObject(TopicSubscriptionUtilOOB, { 

// Define overriding functions here. Modify this method to parse the registration details 
// output from a spoke selector flow. You can pass different parameters from the registration response 
// and map them to the fields in the Topic Subscription table. 

  updateRegistrationResponse: function(registrationDetails){
    var reqTypeId = Constants.TOPIC_SUB_REQUEST_TYPE;
    var outputMap = new sn_appss.IntegrationRequestConfigAPI().outputJSONToMap(reqTypeId, registrationDetails.result); 
    var updateTopicSubObj = new sn_tmt_core.BaseObject();
    if (Constants.REGISTRATION_RESPONSE_SUCCESS_CODES.indexOf(responseCode) != -1) {
      updateTopicSubObj.setValue('registration_status', Constants.REGISTRATION_STATUS.REGISTERED); 
      updateTopicSubObj.setValue('registration_message', outputMap.response_body.message);
      updateTopicSubObj.setValue('subscription_id', outputMap.response_body.result.id); 
    }
  } 
  type: TopicSubscriptionUtil 

});
```

## TopicSubscriptionUtilOOB - updateTopicSubscriptionRec\(Object topicSubObj\)

Stores the current topic subscription record in the Topic subscription \[sn\_api\_notif\_mgmt\_topic\_subscription\] table using DAO insert.

Typically you will call this function within the [updateRegistrationResponse\(\)](TopicSubscriptionUtilAPIScoped.md#) function.

<table id="table_yyh_bmk_bzb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicSubObj

</td><td>

Object

</td><td>

Fields to update in the associated topic subscription record. This is the payload returned by the registration subflow.For example:

```
"topicSubObj": {
  "registration_message": "String",
  "registration_status": "String",
  "subscription_id": "String"
}
```

For more information, see [executeRegistrationSubflow\(\)](TopicSubscriptionUtilAPIScoped.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the topic subscription record that was updated.|

The following code example shows how to update this function.

```
var TopicSubscriptionUtil= Class.create();
TopicSubscriptionUtil.prototype = 
  Object.extendsObject(TopicSubscriptionUtilOOB, { 

// Define overriding functions here. Pass a topic subscription record object that contains
// the values to update in a record.

  updateTopicSubRec: function(topicSubObj){
    return this.topicSubscriptionDAO.updateTopicSubscription(topicSubObj); 
  } 

type: TopicSubscriptionUtil 

});
```

The following code example shows how to call this function.

```
if (!gs.nil(outputMap) && outputMap.status_code == '1') {
  var responseCode = outputMap.response_body.code;
  var topicSubID = registrationDetails.topicSubID;
  var topicSubGr = new TopicSubscriptionUtil(topicSubID).topicSubscriptionDAO.getGlideRecord();
  var updateTopicSubObj = new sn_tmt_core.BaseObject();
  if (Constants.REGISTRATION_RESPONSE_SUCCESS_CODES.indexOf(responseCode) != -1) {
    updateTopicSubObj.setValue('registration_status', Constants.REGISTRATION_STATUS.REGISTERED);
    updateTopicSubObj.setValue('registration_message', outputMap.response_body.message);
    updateTopicSubObj.setValue('subscription_id', outputMap.response_body.result.id);
  } else {
    updateTopicSubObj.setValue('registration_status', Constants.REGISTRATION_STATUS.ERROR);
    updateTopicSubObj.setValue('registration_message', outputMap.response_body.message);
  }
    new TopicSubscriptionUtil(topicSubGr).updateTopicSubscriptionRec(updateTopicSubObj);
    return '';
} else if (!gs.nil(outputMap) && outputMap.status_code == '0') {
  return outputMap.status_reason;
} else {
  var errorMsg = 'Spoke Request Type output not set, please check request adapter flow';
  return errorMsg;
}
```

