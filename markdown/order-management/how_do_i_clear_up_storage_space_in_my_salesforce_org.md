---
title: Free storage space in a Salesforce org
description: How to clear up space in a Salesforce test environment that is near its storage limit.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Free storage space in a Salesforce org

How to clear up space in a Salesforce test environment that is near its storage limit.

Occasionally, administrators work in a Salesforce test environment that is approaching its storage limit. If Salesforce complains that you are over your storage allocation, it’s time to free up space.

One option is to remove records from the ConfigurationBOM table. For managed packages v1.0 or greater, remove Configuration Line Item and Configuration Field Data Sets instead.

**Warning:** These steps delete data. Follow them only in non-production environments.

1.  Setup cog in SFDC → Developer Console → Debug \[Open Execute Anonymous Window\]

    ![Menu](../images/cpq-using-apex-anonymous-window.png)

2.  Paste and execute the following:

    ```
    delete [SELECT id FROM LGK__ConfigurationBOM__c];
    ```

    For CPQ managed packages v1.0 or greater, run this delete instruction against the following objects:

    -   LGK\_\_ConfigurationLineItem\_\_c
    -   LGK\_\_ConfigurationFieldData\_\_c
    **Note:** Salesforce only allows DML statements such as these to run in batches of 10,000 or fewer records at a time. If the record has more than 10,000 records, modify the query in step 2 with the following, and run the modified query as many times as necessary.

    ```
    delete [SELECT id FROM LGK__ConfigurationBOM__c LIMIT 10000];
    ```

3.  Use the following script to clear the Trash:

    ```
    List<Id> delCLI = new List<Id>(new Map<Id,SObject>([SELECT Id FROM LGK__ConfigurationLineItem__c ORDER BY CreatedDate ASC LIMIT 10000]).keySet());
    Database.delete(delCLI);
    Database.emptyRecycleBin(delCLI);
    List<Id> delCFD = new List<Id>(new Map<Id,SObject>([SELECT Id FROM LGK__ConfigurationFieldData__c ORDER BY CreatedDate ASC LIMIT 10000]).keySet());
    Database.delete(delCFD);
    Database.emptyRecycleBin(delCFD);
    ```

    Alternately, in Salesforce Admin → 9 dot menu → search Recycle Bin, navigate to Recycle Bin → Empty Org Recycle Bin.


