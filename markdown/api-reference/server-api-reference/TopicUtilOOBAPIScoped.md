---
title: TopicUtilOOB - Scoped
description: The TopicUtilOOB script include contains functions that enable you to query and manipulate records in the Topic \[sn\_api\_notif\_mgmt\_topic\] table. This class operates at the service layer that interacts with the Data Access Object \(DAO\) class.Creates a record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table using DAO insert.Returns the name of the subflow to call to obtain topics from an external system.Triggers the subflow that is responsible for obtaining topic records from an external system.Validates the passed in topic record payload and inserts records in the Topic \[sn\_api\_notif\_mgmt\_topic\} table containing this data.Determines whether any other topic record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table contains the specified combination of fields as its composite key, indicating a duplicate topic.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TopicUtilOOB- Scoped

The `TopicUtilOOB` script include contains functions that enable you to query and manipulate records in the Topic \[sn\_api\_notif\_mgmt\_topic\] table. This class operates at the service layer that interacts with the Data Access Object \(DAO\) class.

These functions are called when the **Get Topics** button is selected on the Topics form. If you want to change the default functionality of this script include, you must override the functions contained in this script include in the `TopicUtil` script include.

Both script includes run in the `sn_api_notif_mgmt` namespace.

For additional information on topics, see [Handling the external events using Telecommunications API notification](https://www.servicenow.com/docs/access?context=telecommunications-api-notification&version=xanadu&pubname=xanadu-telecom-service-ops&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TopicUtilOOB - createTopic\(Object topicObj\)

Creates a record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table using DAO insert.

Typically you will call this function within the [validateAndInsertTopic](TopicUtilOOBAPIScoped.md#) function that also performs various validations on the content.

<table id="table_s5t_gxw_1zb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicObj

</td><td>

Object

</td><td>

Object that contains the fields to store in the topic record. For the base implementation the object has the following format. If you modify or extend the Topics table, this object should reflect that structure. Ensure that you include any required fields.```
"topicObj": {
  "content_query": "String";
  "description": "String";
  "header_query": "String";
  "namespace": "String";
  "topic_id": "String";
  "topic_name": "String";
  "type": "String";
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the created topic record.|

The following code example shows how to call this function.

```
validateAndInsertTopics: function(topicsResponse) {
  if (!gs.nil(topicsResponse)) {
    var topicsArr = topicsResponse.response;
    for (var i = 0; i < topicsArr.length; i++) {
      var name = topicsArr[i].name;
      var headerQuery = topicsArr[i].headerQuery;
      var contentQuery = topicsArr[i].contentQuery;
      var namespace = topicsArr[i].namespace;
      var id = topicsArr[i].id;
      var description = topicsArr[i].description;
      var topicGr = TopicDAO.getTopicByNameHeaderContentNamespace(name, headerQuery, contentQuery, namespace,'');
      if (topicGr && !topicGr.hasNext()) {
        var topicObj = new sn_tmt_core.BaseObject();
        topicObj.setValue('topic_name', name);
        topicObj.setValue('header_query', headerQuery);
        topicObj.setValue('content_query', contentQuery);
        topicObj.setValue('namespace', namespace);
        topicObj.setValue('description', description);
        topicObj.setValue('topic_id', id);
        topicObj.setValue('type', Constants.TYPE_INGRESS);
        this.createTopic(topicObj);
      }
    }
  }
}
```

The following code example shows how to override this function.

```
var TopicUtil = Class.create();
TopicUtil.prototype = 
  Object.extendsObject(TopicUtilOOB, { 

  // Define overriding functions here. Pass a topic record object with 
  // values for a single Topic table record.

  createTopic: function(topicObj){ 
    return this.topicDAO.create(topicObj); 
  } 

  type: TopicUtil 

});
```

## TopicUtilOOB - getSubFlowName\(\)

Returns the name of the subflow to call to obtain topics from an external system.

Typically this function is called from the [triggerSubflow\(\)](TopicUtilOOBAPIScoped.md#) function. This subflow is responsible for contacting an external system and obtaining any topic records that need to be inserted in the Topics \[sn\_api\_notif\_mgmt\_topic\] table.

The name of the subflow is defined in `Constants.GET_TOPICS_SUBFLOW`. For the demo implementation this subflow is `sn_ind_tmf642.event_alarm_notifications_api` and generates a "mock" response \(doesn't call an external system\) to show the end-to-end processing.

You can change this functionality to include the name of your own subflow by overriding the name of the subflow to execute in the `sn_api_notif_mgmt.Constants` script include.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the subflow to use to obtain topics from an external system.|

The following code example shows how to override this function.

```
var TopicUtil= Class.create();  
TopicUtil.prototype = 
  Object.extendsObject(TopicUtilOOB, { 

  // Define overriding function here. In TopicUtilOOB it returns the flow name of a GET outbound API call that mocks the GET call.
  // Override this function to return a flow that returns topics from an external system. 

  getSubflowName: function(){ 
    return <flow_name>; // Return the name here
  } 

  type: TopicUtil 

});
```

## TopicUtilOOB - triggerSubflow\(\)

Triggers the subflow that is responsible for obtaining topic records from an external system.

This function is called when the user selects the **Get Topics** button on the Topics form.

The name of the subflow that gets triggered is defined in `Constants.GET_TOPICS_SUBFLOW`. For the demo implementation this subflow is `sn_ind_tmf642.event_alarm_notifications_api` and generates a "mock" response \(doesn't call an external system\) to show the end-to-end processing.

You need to change this functional to include the name of your own subflow by overriding the name of the subflow to execute in the `sn_api_notif_mgmt.Constants` script include.

Within the subflow you must create a REST step, connection alias, or other implementation to provide an endpoint URL that retrieves topics from your external network. When the topics are returned by that subflow, you call the [validateAndInsertTopics](TopicUtilOOBAPIScoped.md#) function to verify the passed back topic payload and insert/update the records in the Topic table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to override this function.

```
var TopicUtil = Class.create();
TopicUtil.prototype = 
  Object.extendsObject(TopicUtilOOB, { 

  // Define overriding functions here. Override this function to call your own GET API outbound call subflow.
  triggerSubflow: function(){
    var result =''; // Pass the subflow here 

    try {
      var flowOp = sn_fd.FlowAPI.getRunner().subflow(result).inBackground().withInputs().run();
      if (flowOp) { 
        gs.addInfoMessage(gs.getMessage('Please refresh the list to see new Topics.'));
      } 
    } catch (ex) {
      gs.addInfoMessage(gs.getMessage(ex + ' Please check if the trigger is defined and passed correctly')); 
    }
  } 

  type: TopicUtil 

});
```

## TopicUtilOOB - validateAndInsertTopics\(Array topicsResponse\)

Validates the passed in topic record payload and inserts records in the Topic \[sn\_api\_notif\_mgmt\_topic\} table containing this data.

The passed topics payload is obtained from the "GET API endpoint" used to retrieve topics from an external system. For more information on triggering this GET API, see [triggerSubflow\(\)](TopicUtilOOBAPIScoped.md#).

You can change this functionality to include your own validation rules and topic record fields by overriding this function in the `TopicUtil` script include.

<table id="table_d5m_bcx_1zb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicsResponse

</td><td>

Array of objects

</td><td>

Topic record payload returned by the external system through the GET API endpoint within the subflow. This payload should match the structure of the Topics \[sn\_api\_notif\_mgmt\_topic\] table. Each object within the array is a separate topic. For example, in the demo implementation this is:```
"topicResponse": [
  {
    "name": "String";
    "header_query": "String";
    "content_query": "String";
    "namespace": "String";
    "id": "String";
    "description": "String"
  },
  {
    "name": "String";
    "header_query": "String";
    "content_query": "String";
    "namespace": "String";
    "id": "String";
    "description": "String"
  }
]
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to override this function.

```
var TopicUtil= Class.create();  
TopicUtil.prototype = 
  Object.extendsObject(TopicUtilOOB, { 

  // Define overriding functions here. Override this function to include custom 
  // validations on topic payload parameters and insert the record into the Topics table. 

  validateInsertTopics: function(topicsResponse){ 

    // Provide validation on the passed payload. 
    this.createTopic(topicObj);
  } 

type: TopicUtil 

});
```

## TopicUtilOOB - verifyTopics\(String topicname, String headerQuery, String contentQuery, String namespace, String previousSysId\)

Determines whether any other topic record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table contains the specified combination of fields as its composite key, indicating a duplicate topic.

<table id="table_thz_wdx_1zb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

topicname

</td><td>

String

</td><td>

Name of the topic.

</td></tr><tr><td>

headerQuery

</td><td>

String

</td><td>

Filter to apply to the content of the event header properties. This query defines the type of events to listen to for the associated topic. You can pass this parameter as a nested query.For example: `"headerQuery": "eventType=AlarmCreateNotification&domain=Paris",`

For additional information, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).

</td></tr><tr><td>

contentQuery

</td><td>

String

</td><td>

Filter to apply to the content of the event. This query is a deeper event filter that is used to find information such as event severity or probable cause. You can pass this parameter as a nested query.For example: `"contentQuery": "event.alarm.perceivedSeverity=CRITICAL",`

For additional information, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).

</td></tr><tr><td>

namespace

</td><td>

String

</td><td>

Namespace in which the associated topic resides. Topics can’t be duplicated within a domain, but can be contained in multiple domains.

</td></tr><tr><td>

previousSysId

</td><td>

String

</td><td>

Optional. Sys\_id of the topic to update. Only pass this value when updating an existing topic.

</td></tr></tbody>
</table><table id="table_uhz_wdx_1zb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether another record in the Topic table contains the specified combination of fields.

 Possible values:

-   true: Another record in the Topic table contains the combination of fields.
-   false: No other record in the Topic table contains the combination of fields.

</td></tr></tbody>
</table>The following code example shows how to override this function.

```

var TopicUtil= Class.create();
TopicUtil.prototype = 
  Object.extendsObject(TopicUtilOOB, {

  // Define overriding functions here. Override this function to provide custom validations on 
  // the passed parameters and to verify whether an insert is possible or not. 

  verifyTopics: function(topicname, headerQuery, contentQuery, namespace, previousSysId) { 

    // Write modified code here to get any combination of records present in the current Topic table. 
    // In the current implementation, the function checks if there is a duplicate topic record that contains the
    // passed parameters. 

  },

type: TopicUtil 

});
```

