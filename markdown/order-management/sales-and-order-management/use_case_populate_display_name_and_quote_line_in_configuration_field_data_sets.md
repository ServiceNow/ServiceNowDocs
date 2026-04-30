---
title: Use case: Populate display names and quote lines in Configuration Field Data Set objects
description: Learn how to set up custom objects and Apex triggers in SFDC to populate the display names of ServiceNow CPQ fields.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 7
breadcrumb: [Use cases, Using ServiceNow CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Populate display names and quote lines in Configuration Field Data Set objects

Learn how to set up custom objects and Apex triggers in SFDC to populate the display names of ServiceNow CPQ fields.

As part of the ServiceNow CPQ Managed Package, the functionality of the Configuration Field Data Set object in SFDC is to return the Configuration ID of the configuration, every field variable name used by the blueprint, the value of that field, and the label of that value after every save from the ServiceNow CPQ configurator:

![Field Data list](../images/cpq-configuration-field-data-sets-1.png)

However, there might be some extra necessities about the configuration in ServiceNow CPQ outside of these fields created by the Managed Package that an organization needs for downstream processes. For instance, we might want to populate the display names of the ServiceNow CPQ fields, or easily jump to the Quote Line of the associated Configuration Field Data objects for an easy connection to the BOM.

![Field data list](../images/cpq-configuration-field-data-sets-2.png)

With a little setup of custom objects and Apex Triggers in SFDC, these fields can automatically be populated after every configuration is saved.

## Prerequisites

Enable “Push Config Data to Logik Salesforce Object” in the Admin Settings if you have not done so already. This will start creating the Configuration Field Data Sets objects in SFDC.

![Admin settings](../images/cpq-admin-settings-push-config-data.png)

**Note:** The creation of these Configuration Field Data Sets will occur every time a configuration is saved from ServiceNow CPQ, even if the quote itself is not saved. This can lead to a lot of data being created in your Salesforce org. If you do not have a use case for pulling every field used by the Blueprint into SFDC, it is best to keep this setting disabled and rely on the Extended Information property in the BOM Data.

## Populate the display name

1.  In SFDC Setup, navigate to the Object Manager.
2.  Create a new custom object called “LGK Label” with the following attributes:

    -   Record Name: Logik Label
    -   Data Type: Auto Number
    -   Display Format: LGKLB-\{0000\}
    -   Allow Search: Checked
    -   Launch New Custom Tab Wizard after saving this custom object: Checked
    Leave the rest of the values as default and click **Save**.

3.  On the New Custom Object Tab page, click the Tab Style field and select any style.
4.  Click **Next**, click **Next** again, and then click **Save**.
5.  Click **Fields &amp; Relationships** on LGK Label, and then click **New**. Create a new field with the following attributes:

    -   Data Type: TextArea
    -   Field Label: label
    -   Field Name: label
    Click **Next**, click **Next** again, and then click **Save**.

6.  Click New. Create a new field with the following attributes:

    -   Data Type: TextArea
    -   Field Label: variablename
    -   Field Name: variablename
    Click **Next**, click **Next** again, and then click **Save**.


This new LGK Label object will be where we will host the Field Variable Name and Field Label Name in SFDC. The labels will not automatically be imported. They also must be manually updated/imported every so often with changes and additions to the Fields in CPQ Admin. We will go over methods of bulk import later in this guide.

1.  In Object Manager, search “Configuration Field Data”.
2.  Click **Fields &amp; Relationships**, and then click **New**. Create a new field with the following attributes:

    -   Data Type: TextArea
    -   Field Label: Display name
    -   Field Name: Display\_Name
    Click **Next**, click **Next** again, and then click **Save**.

3.  Click **Triggers**, and then click **New**.
4.  Paste the following code into the Apex code block:

    ```
    trigger UpdateConfigurationLabels on LGK__ConfigurationFieldData__c (before insert) {
    	// Step 1: Collect FieldKeys from records to be inserted
    	Set<String> fieldKeys = new Set<String>();
    	for(LGK__ConfigurationFieldData__c confData : Trigger.new) {
    		fieldKeys.add(confData.LGK__FieldKey__c);
    	}
    	
    	// Step 2: Query LGK_Label__c based on collected FieldKeys
    	Map<String, LGK_Label__c> labelMap = new Map<String, LGK_Label__c>();
    	for(LGK_Label__c label : [SELECT label__c, variablename__c FROM LGK_Label__c WHERE variablename__c IN :fieldKeys]) {
    		labelMap.put(label.variablename__c, label);
    	}
    	
    	// Step 3: Loop through records to be inserted and update Display_Name__c
    	for(LGK__ConfigurationFieldData__c confData : Trigger.new) {
    		LGK_Label__c matchedLabel = labelMap.get(confData.LGK__FieldKey__c);
    		if(matchedLabel != null) {
    			confData.Display_Name__c = matchedLabel.label__c;
    		} else if(confData.LGK__ValueLabel__c != null) {
    			confData.Display_Name__c = confData.LGK__ValueLabel__c;
    		}
    	}
    ```


The framework is complete. Add the new Display Name field to the Configuration Field Data Set layout. All thatʼs left is to import the field label names into the LGK Labels objects. Depending on how you use ServiceNow CPQ Fields, there are three methods of accomplishing this.

<table><tbody><tr><td>

Manual ServiceNow CPQ Label Creation

 1.  Create a new Logik Label Object from the LGK Labels tab
2.  Enter the “variablename” to exactly match the ServiceNow CPQ variable name
3.  Enter the “label” to be any label you wish

</td><td>

Pros:

 -   Good if you have a low number of fields for which you need the display name
-   Allows you to customize the field label names to be different than how they appear in the ServiceNow CPQ Admin and the Layout

 Con: Can be a tedious process for a large number of fields

</td></tr><tr><td>

Bulk Import from exporting all ServiceNow CPQ fields

 1.  From the ServiceNow CPQ Admin Field’s Tab, click **Export**
2.  Open the CSV file and delete all data besides columns “B” and “C”
3.  Rename the headers to “label” and “variablename,” and save
4.  In SFDC, go to the LGK Label tab and click **Import**
5.  Select “LGK Labels”
6.  Select “Add new records”
7.  Select your saved CSV file
8.  Upload

</td><td>

Pros:

 -   Good for a large number of fields
-   Global fields used across Blueprints will be labeled consistently in SFDC

 Cons:

 -   Set field label names, partner fields, and system fields are not imported by this method, so the display name will default to the value of the field
-   These fields can be manually added as LGK Label objects using the manual label creation method

</td></tr><tr><td>

Bulk Import from exporting the Blueprint Layout

 1.  From the ServiceNow CPQ Blueprint youʼd like to use, go to your Layout, and click **Export**
2.  Open the CSV
3.  Filter column “A” by “field”
4.  Delete all data except columns “A”, “D”, and “E”
5.  Copy column “D” and “E” to a new CSV, renaming any field’s labels you’d like
6.  In SFDC, go to the LGK Label tab and click **Import**
7.  Select “LGK Labels”
8.  Select “Add new records”
9.  Select your saved CSV file
10. Upload

</td><td>

Pros:

 -   Good for a large number of fields
-   Populates the display name in the layout for all fields, including set fields,system fields, and partner fields

 Cons:

 -   Only fields that are used in the layout will populate the display name. Fields that are only associated with the Blueprint will still create Configuration Field Data Set objects whose labels will be null
-   Fields that are used in multiple Blueprints will only populate the display name field with the first field label imported this way

</td></tr></tbody>
</table>If there are any fields that you’d like to show a different display name than what you have imported, you can easily edit the Label object to whatever label you wish and it will begin populating the Configuration Field Data Sets that way after the update.

## Populate the quote line

1.  In SFDC Setup, Navigate to the Object Manager.
2.  Search “Configuration Field Data”.
3.  Click **Fields &amp; Relationships**, and then click **New**. Create a new field with the following attributes:

    -   Data Type: Lookup Relationship
    -   Related to: Quote Line
    -   Field Label: Quote Line
    -   Field Name: Quote\_Line
    Click **Next**, click **Next** again, and then click **Save**.

4.  In Object Manager, search "Quote Line".
5.  Click **Triggers**, and then click **New**.
6.  Paste the following code into the Apex code block:

    ```
    trigger PopulateConfigFieldData on SBQQ__QuoteLine__c (after insert, after update) {
    	// Step 1: Collect the Configuration Ids from the new Quote Lines
    	Set<String> configIds = new Set<String>();
    	Map<String, Id> quoteLineMap = new Map<String, Id>(); // Mapping Configuration UUID to Quote Line Id
    
    	for (SBQQ__QuoteLine__c ql : Trigger.new) {
    		if (String.isNotBlank(ql.LGK__ConfigurationId__c)) {
    			configIds.add(ql.LGK__ConfigurationId__c);
    			quoteLineMap.put(ql.LGK__ConfigurationId__c, ql.Id); // Storing Quote Line Id
    		}
    	}
    	
    	if (configIds.isEmpty()) {
    		return;
    	}
    	
    	// Step 2: Query the Configuration Field Data records
    	List<LGK__ConfigurationFieldData__c> confFieldsToUpdate = [SELECT Id,LGK__ConfigurationId__c FROM LGK__ConfigurationFieldData__c WHERE LGK__ConfigurationId__c IN:configIds];
    
    	// Step 3: Update the Field Data records
    	for (LGK__ConfigurationFieldData__c cf : confFieldsToUpdate) {
    		Id quoteLineId = quoteLineMap.get(cf.LGK__ConfigurationId__c);
    		if (quoteLineId != null) {
    			cf.Quote_Line__c = quoteLineId; // Assigning the Quote Line Id
    		}
    	}
    
    	update confFieldsToUpdate;
    ```


Now, every time a Quote is saved in SFDC, the Quote Line of the Parent Configurable Product will populate into the Configuration Field Data Set. Remember to add this custom field to the Configuration Field Data Sets layout to see it in the tab.

**Note:** Configuration Field Data Sets are created immediately after you click **Save** in the ServiceNow CPQ Configurator. When you enter the Quote Line Editor, the Quote Line field will not be populated because it hasnʼt been created or updated yet. Only once you save from the Editor will the quote line appear in the field.

**Parent Topic:**[Use cases](use-cases.md)

