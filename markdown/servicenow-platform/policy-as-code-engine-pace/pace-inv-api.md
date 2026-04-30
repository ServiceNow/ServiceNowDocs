---
title: Sample API
description: The following is a sample invocation request when the PaCE API is executed.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Policy invocation API, Write and test policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Sample API

The following is a sample invocation request when the PaCE API is executed.

```
var request = {"documentIds":
         [{"table":"sn_cdm_deployable","sysId":"d1be8f5e87d80110eec7dbdd3fbb357d"}],"service":"CDM","category":"CDM","data":{"snapshotId":"2bcec7de87d80110eec7dbdd3fbb3529"},"options":{"verboseResponse":true,"logLevel":"debug","type":"standard","failFast":false, "executionTag":"cdm"}}
          
          
         try {



            var api = new sn_pace.InvocationAPI();



            var execResponse = api.execute(request);



            gs.info(" Got execution response:\n " +  JSON.stringify(execResponse,null,4));
                             
                                                 
                                    
         } catch (err) {



            //var errJSON = JSON.parse(err);



            //gs.info(errJSON.code);



            gs.info(" Error message is:" + err + "\n stack:" +  err.stack);



            // gs.info(" Error is:" + err);



         }
```

