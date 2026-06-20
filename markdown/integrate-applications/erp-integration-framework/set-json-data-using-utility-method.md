---
title: Create payload for execution with segment handler utility
description: When working with IDoc entities, you can create the execution payload with the segment handler utility.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/set-json-data-using-utility-method.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, idoc, entity, entities, execution, payload, segment, handler, utility, api, segment handler, payload creation, JSON, script]
audience: administrator
breadcrumb: [Create and change SAP business entities with IDoc, Add an entity to a model, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Create payload for execution with segment handler utility

When working with IDoc entities, you can create the execution payload with the segment handler utility.

## Before you begin

Role required: admin

When using the API withJSON\(Object data\), you can create the JSON manually or use the segment handler utility method explained in this topic. For detailed information about the API, see the following:

-   
-   
-   

## Procedure

1.  Navigate to **System Definition** &gt; **Scripts - Background**.

2.  Create or paste a code snippet.

    For example:

    ```
    var obj = new SegmentHandler('460d3ff2ff5de210d3a2fffffffffff8');
    
    // Create first E1EDK01
    let k01_1 = obj.addSegment("E1EDK01")
        .addField("BELNR", "1000")
        .addField ("CURCY", "USD");
    
    // Create another E1EDK01
    let k01_2 = obj.addSegment("E1EDK01")
        .addField("BELNR", "2000")
        .addField("CUECY", "EUR");
        
    // Create E1EDP01 with nested segments
    let p01 = obj.addSegment("E1EDP01")
        .addField("MENGE", "50")
        .addField("POSEX", "0010");
    
    let p20 = p01.addSegment("E1EDP20")
        .addField("AMENG", "10")
        .addField("WMENG", "5");
    
    p20.addSement("E1EDP19")
        addField("IDTNR", "MAT01"):
    
    gs.info(JSON.stringify(obj.getData(), null, 2));
    
    ```

3.  Select **Run Script**.

    The payload is generated, for example:

    ```
    sn_erp_integration: {
        "data": {
            "E1EDP01": [
                {
                    "MENGE": "50",
                    "POSEX": "0010",
                    "E1EDP20": [
                        {
                            "AMENG": "10",
                            "WMENG": "5",
                            "E1EDP19": [
                                {
                                    "IDTNR": "MAT01"
                                }
                            ]
                        }
                    ]
                }
            ],  
            "E1EDK01": [
                {
                    "BELNR": "1000",
                    "CURCY": "USD"
                },
                {
                    "BELNR": "2000",
                    "CURCY": "EUR"
                }
            ]
        }
    }       
    
    ```

    Add the JSON in the withJSON\(Object data\) API and execute it in the query engine.


**Parent Topic:**[Create and change SAP business entities with IDoc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/create-and-change-sap-business-entities-with-idoc.md)

