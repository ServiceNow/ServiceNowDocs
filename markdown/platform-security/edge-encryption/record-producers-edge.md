---
title: Encrypt data from a record producer
description: Configure your Edge Encryption proxy server to allow inserts from a record producer by creating encryption rules from the record producer record.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Encrypt data from a record producer

Configure your Edge Encryption proxy server to allow inserts from a record producer by creating encryption rules from the record producer record.

## Before you begin

Role required: security\_admin

Record producers allow end users to create task-based records, such as incident records, from the Service Catalog and Service Portal. If a record producer attempts to insert data into a field marked for encryption, an invalid insert message displays and the data is not saved to the field.

Encrypting data from a record producer requires an encryption configuration defined for the target field. Check that you have created an encryption configuration for the target field and table before creating an encryption rule from a record producer. See [Create a field encryption configuration](../concept/c_ConfigureCloudEdge.md#). To encrypt attachments from a record producer, [Configure attachment encryption](../concept/c_EncryptingAttachments.md#).

## Procedure

1.  Log in to your instance through the Edge Encryption proxy server.

2.  Navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

3.  Create a record producer record or open an existing record producer record.

4.  Under **Related Links**, select **Create Edge Encryption Rule**.

    Two inactive encryption rules are automatically created to encrypt data sent from the record producer to the field marked for encryption.

    |Encryption rule|Description|
    |---------------|-----------|
    |&lt;RecordProducerName&gt;|Rule created to process POST parameters from the Service Catalog and map variables to fields in the instance.|
    |&lt;RecordProducerName&gt;Json|Rule created to process a JSON payload from the Service Portal and map variables to fields in the instance.|

5.  Activate the necessary encryption rules created by the record producer.

    1.  Navigate to **Edge Encryption Configuration** &gt; **Rules** &gt; **All**.

    2.  Depending on where the record producer will be used, open the associated encryption rule created by the record producer and select the **Active** flag.

        If using the record producer in the Service Catalog, activate the &lt;RecordProducerName&gt; encryption rule. If using the record producer in the Service Portal, activate the &lt;RecordProducerName&gt;Json encryption rule.

6.  Examine the Encryption rule **Action** field and add any necessary field names or statements.

    If a record producer directly maps a variable to a field in a table, the encryption rule automatically maps the variable to the correct field. However, if a variable is indirectly mapped through various scripts on the platform, you may need to update the rules to map each variable to the correct field.

    The below encryption rule was created from the Report Outage record producer and processes POST parameters from the Service Catalog to map variables to fields in the instance. Replace `'FILL ME IN'` with the target field.

    ![Edge Encryption Rule: Report Outage](../images/report-outage.png)

    The below encryption rule was created from the Report Outage record producer and processes a JSON payload from the Service Portal to map variables to fields in the instance. Add additional statements to map any scripted variables to the target fields.

    ![Edge Encryption Rule: ReportOutageJson](../images/report-outage-json.png)

    When the payload from the record producer is examined, the error\_message element contains the value for the short\_description field. By adding the following statement, you can map the scripted variable error\_message to the short\_description field.

    ```
    if (jsonElement.getName() == 'error_message')
            jsonElement.valueFor(tableName, 'short_description');
    ```

    The value of the **Action** field becomes:

    ```
    function ReportOutageJsonAction(request) {
    	var tableName = 'incident';
    	// Some fields are set in script, additional parameter lines may need to be added
    	// current.comments is accessed via script from notes; // assignment to current.comments does NOT replace existing values
    	// current.short_description is accessed via script from short_description;
    	// current.description is accessed via script from current.short_description;
    	// current.caller_id is accessed via script from gs.getUserID();
    	var jsonContent = request.getAsJsonContent();
    	for (var jsonElementItr = jsonContent.getIterator('variables'); jsonElementItr.hasNext();) {
    		var jsonElement = jsonElementItr.next();
    		if (jsonElement.getName() == 'error_message')
    			jsonElement.valueFor(tableName, 'short_description');
                  } else {
    		        jsonElement.valueFor(tableName, jsonElement.getName());
    	}
    }
    ```


## Result

The two encryption rules enable the record producer to insert values into fields marked for encryption from either the Service Catalog or Service Portal.

**Parent Topic:**[Configuring Edge Encryption](../concept/edge-config.md)

