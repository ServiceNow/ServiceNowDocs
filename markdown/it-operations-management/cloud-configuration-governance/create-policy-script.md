---
title: Create a policy action script
description: Use policy action scripts to get, update, or set values in cloud requests.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a policy action script

Use policy action scripts to get, update, or set values in cloud requests.

## Before you begin

Role required: sn\_cmp.cloud\_governor or admin.

## About this task

For more information on using scripts, see [Cloud scripts and cloud script templates](../concept/cloud-scripts-and-templates.md).

## Procedure

1.  On the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  On the **Policy Action Scripts** tab, click **New**, enter a unique and descriptive **Name** and **Description**, fill in the form, and then click **Submit**.

    After you enter a name, a script appears with a variable that uses the name that you entered.

    |Field|Description|
    |-----|-----------|
    |Action Script Category|Choose another category or keep the one you created in an earlier step.|
    |Script|Modify the `customScripts` function in the script. This is the only part of the script that you need to modify.|


## Example

The following example script determines whether the user belongs to a user group and then overrides the user-specified application server node name value with the value **MyNodeName**.

```

customScript : function(formData){
  var groups = this.parameters.userData.groups; 
    if( groups.length > 0){ 
      formData.App_Server_NodeName = "MyNodeName"; 
    }
  return formData;
},

```

This example returns a random number:

```

customScript : function(formData){
  var min = 10000;
  var max = 99999;
  var num = Math.floor(Math.random() * (max - min + 1)) + min;
  formData.randomNumber = num + "";  
  return formData;
},

```

This example script adds three hours to the lease date using the base-system [GlideDateTime](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_scripting_jakarta_server_side_scripting/app_store_learnv2_scripting_jakarta_glidedatetime?v=jakarta) class.

```

var SetLeaseShort = Class.create();
SetLeaseShort.prototype = Object.extendsObject(sn_cmp.PolicyExecutionBase, {
	customScript : function(formData){
		// Manipulation of form parameters are supported. Changes in any other attributes
              // will be ignored.
		// The data available for manipulation is as follows:
		// Form Data -  for example: StackName can be accessed through formData.StackName
		// formData.StackName = "MyStack";
		// User Data  - for example: User Id can be accessed through this.parameters.userData
		// if(this.parameter.userData.userId == 'servicenowuserId')
		// this.info("id = " + formData.StackName);
		
		// var leaseValue = now();
		// leaseValue = leaseValue.setHours(leaseValue.getHours()+4);
		// formData.LeaseEndDate = leaseValue;
		
		if (formData.hasOwnProperty("LeaseEndDate")) {
			gdt = new GlideDateTime();
			// 10800 = 3 hours
			gdt.addSeconds(10800);
			formData.LeaseEndDate = gdt.getDisplayValue();
		}	
		return formData;
	},
	execute: function() {
		if(this.parameters !=  null && this.parameters.formData != null){
        	var inputData = JSON.parse(JSON.stringify(this.parameters.formData));
		    var outputFormData = this.customScript(inputData);
            if( outputFormData != null){
                this.parameters.formData = outputFormData;
            }
       	}
		var output = {};
		output.answer = this.parameters;
		return JSON.stringify(output);
	},
	type : 'SetLeaseShort'
});	

var SetLeaseShortObj = new SetLeaseShort(inputAttributes);
var outputParams = SetLeaseShortObj.execute();
gs.info( "Output of script is = " + outputParams);

```

This example script sets the user-specified **Azure Wordpress DNS** name field from the form to the same name as the stack name:

```
var WordpressFill = Class.create();
WordpressFill.prototype = Object.extendsObject(sn_cmp.PolicyExecutionBase, {
	customScript : function(formData){
		// Manipulation of form parameters are supported. Changes in any other attributes
        // will be ignored.
		// The data available for manipulation is as follows:
		// Form Data -  for example: StackName can be accessed through formData.StackName
		// formData.StackName = "MyStack";
		// User Data  - for example: User Id can be accessed through this.parameters.userData
		// if(this.parameter.userData.userId == 'servicenowuserId')
		//this.info("id = " + formData.StackName);
		
		formData.Azure_Wordpress_v6_vmDnsName = formData.StackName;
		
		return formData;
	},
	execute: function() {
		if(this.parameters !=  null && this.parameters.formData != null){
        	var inputData = JSON.parse(JSON.stringify(this.parameters.formData));
		    var outputFormData = this.customScript(inputData);
            if( outputFormData != null){
                this.parameters.formData = outputFormData;
            }
       	}
		var output = {};
		output.answer = this.parameters;
		return JSON.stringify(output);
	},
	type : 'WordpressFill'
});	

var WordpressFillObj = new WordpressFill(inputAttributes);
var outputParams = WordpressFillObj.execute();
gs.info( "Output of script is = " + outputParams);
```

**Related topics**  


[Example policy action script that tags resources](add-tag-for-policy-1.md)

