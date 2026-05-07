---
title: Cloud scripts and cloud script templates
description: In the Cloud Provisioning and Governance application, script execution is divided into cloud scripts and cloud script templates. Use scripts in blueprints, resource blocks, OS profiles, and use policy scripts to set request form attributes. Policy scripts cannot override user data.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud scripts and cloud script templates

In the Cloud Provisioning and Governance application, script execution is divided into cloud scripts and cloud script templates. Use scripts in blueprints, resource blocks, OS profiles, and use policy scripts to set request form attributes. Policy scripts cannot override user data.

## Cloud scripts

Cloud scripts are simple java scripts that use platform features. An example of a sample cloud script:

```
function evaluateTemplate() {
	// Template Resolver is a helper function which we will use to fetch a template and replace its parameters,
	// var templateResolver=new TemplateResolver(); this comes inbuild
	// templateAttributes below will passed from the user.
	var listDir=templateResolver.getTemplate('Install',templateAttributes);
	return listDir;
}

```

Each cloud script contains certain parameters. Parameters are the attributes that you want to access. A parameter contains a name, a default value, and an override value. The default value can be a string literal, a resource block parameter or a complex script expression used in resource blocks.

A cloud script, by default, has access to the **templateResolver** object. The **templateResolver** object has, by default, a getTemplate method, whose first parameter is the cloud script template name. **templateAttributes** are the cloud script parameters created as part of a cloud script. If needed, customizations can be done in **templateAttributes**. As an example, see the following code snippet if the value of **DevName** parameter needs to be changed from John to Emily.

```
function evaluateTemplate() {
	// Template Resolver is a helper function which we will use to fetch a template and replace its parameters,
	// var templateResolver=new TemplateResolver(); this comes inbuild
	// templateAttributes below will passed from the user.
	templateAttributes['DevName'] = 'Emily';
	var customNodeName;
	var now_GR = new GlideRecord('some_custom_table_to_query');
	gr.addQuery('some_parameter','some_value');
	gr.query();
	if(gr.next())
	 	customNodeName=gr.getValue('some_custom_node_name');
		
	templateAttributes['NodeName'] = customNodeName;
	var listDir=templateResolver.getTemplate('Install',templateAttributes);
	return listDir;
}
evaluateTemplate();

```

## Cloud script templates

Cloud script templates are actual executables which are passed to target a virtual machine for execution. Cloud templates can be of any type \(Shell/PowerShell/CloudInit\) depending on the execution context. You need to create a cloud template first and then associate it with a cloud script.

## Cloud scripts as CloudInit

Cloud providers provide a way to execute scripts at boottime for virtual machines. In the Cloud Management application, you can specify a cloudinit script at various levels:

-   Image level: At the time of creating a cloud script, you can specify an image against which this script should be executed. Once an OS profile which contains this specific image gets selected, the default cloud script against this image is executed. In the example below, an Apache cloud script is associated with a particular image.

    ![Apache cloud script associated with an image.](../image/apache-cloud-script.png)

-   OS profile level: You can run a cloudinit against a specific cloud provider and against a specific AMI/image. You can also be generic and associate a cloudinit to an OS profile, irrespective of the underlying image. In the following example, multiple images are associated with the OS profile. You can map any cloud script to the OS profile in the Cloud Script OS Profile Mappings tab. The mapping of a cloud script with an OS profile takes precedence over the image-level cloud script association.

    ![cloud script default at OS profile](../image/os-profile-example.png)

    In this example, the Apache cloud script is mapped to the Centos OS profile. If needed, you can override the script parameters in the OS Profile Mapping Overrides section.

-   Resource blocks: While mapping a cloud script to an OS profile, you can choose whether to execute the cloud script for a specific resource block used in a blueprint and against a particular resource alias. See [Create an OS profile](../task/create-os-profile.md).

## Cloud scripts as Postinit

You can use cloud scripts as Postinit scripts in a resource block. Once you create a resource block with a virtual machine to be provisioned, you can add an ExecuteScript operation. The ExecuteScript operation takes a script parameter \(a pool of cloud scripts\) and you can select any script to execute. Use the **ScriptParameters** attribute in the ExecuteScript operation to override any script parameter. You can provide a JSON map of script parameter and its override value. All expressions that are supported by Cloud Management work in the **ScriptParamters** attribute.

