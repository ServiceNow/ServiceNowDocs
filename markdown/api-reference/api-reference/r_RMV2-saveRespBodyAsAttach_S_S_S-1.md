---
title: RESTMessageV2 - saveResponseBodyAsAttachment\(String tableName, String recordSysId, String fileName\)
description: Configures the REST message to save the returned response body as an attachment record.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# RESTMessageV2 - saveResponseBodyAsAttachment\(String tableName, String recordSysId, String fileName\)

Configures the REST message to save the returned response body as an attachment record.

When you use this function with a REST message that is sent through a MID server, the MID server user must have any roles required to read and write attachment records, as well as any roles required to read and write records on the table specified in the **tableName** parameter.

The response body does not need to be a binary file to be saved as an attachment. Response bodies using text formats, such as JSON or XML can also be saved. If the instance fails to save the attachment, call getErrorMessage\(\) on the related RESTResponseV2 object for error details.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Specify the table that contains the record you want to attach the saved file to.|
|recordSysId|String|Specify the sys\_id of the record you want to attach the saved file to.|
|fileName|String|Specify the file name to give to the saved file.|

|Type|Description|
|----|-----------|
|void| |

```
(function sampleRESTMessageV2() {
  try{
    var request  = new sn_ws.RESTMessageV2();        
    request.setHttpMethod('get');

    var attachment_sys_id  = '<attachment_record_sys_id>', 
      tablename = 'incident',
      recordSysId = '<incident_sys_id>',            
      response,            
      httpResponseStatus,             
      filename ='<filename>';

    //endpoint - ServiceNow REST Attachment API        
    request.setEndpoint('https://<instance_name>.service-now.com/api/now/attachment/' + attachment_sys_id  +'/file');        
    request.setBasicAuth('<username>', '<password>');

    //RESTMessageV2 - saveResponseBodyAsAttachment(String tableName, String recordSysId, String fileName)        
    request.saveResponseBodyAsAttachment(tablename, recordSysId, filename);        

    response = request.execute();        
    httpResponseStatus = response.getStatusCode();  
      
    gs.info(" http response status_code:  " + httpResponseStatus);    
  }
  catch(ex){
    var message  = ex.getMessage();        
    gs.info(message);    
  }
})();
```

