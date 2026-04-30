---
title: Validate a parameter value with the AllowedPattern property
description: The AllowedPattern property in an Azure Resource Manager \(ARM\) and CloudFormation \(CF\) template performs input validation before sending a provisioning request.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Validate a parameter value with the AllowedPattern property

The **AllowedPattern** property in an Azure Resource Manager \(ARM\) and CloudFormation \(CF\) template performs input validation before sending a provisioning request.

## Before you begin

Role required: sn.cmp.cloud\_service\_designer

## About this task

You can provide rules to validate a parameter value before sending the provisioning request to the cloud. To be notified with an error message if the validation fails, specify the **ConstraintDescription** property in the template. You can customize the error message in the **ConstraintDescription** property to make the message clear and explicit. Usually, the CF templates already have the **AllowedPattern** and **ConstraintDescription** properties. If these properties are not present, you can add them as mentioned in the following procedure:

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Templates**.

2.  Select a template or click **New** to create a new cloud template.

    If you select an existing template, rename the template.

3.  In the **Body** text box, make the following changes in an ARM and a CF template.

    1.  In an ARM template, make these changes:

        -   In the parameters metadata section, enter **SNC::Parameter::Metadata**.
        -   Add the **AllowedPattern** key and enter a valid value range.
        -   Add the **ConstraintDescription** key and enter an error message.
        ```
        "parameters": {
                 "newStorageAccountName": {
                     "type": "string",
                      "metadata": {
                          "description": "Unique DNS Name for the Storage Account where the Virtual Machine's disks will be placed.",
                           "SNC::Parameter::Metadata": {
                               "allowedPattern": "[0-9a-z]{1,11}",
                                "ConstraintDescription": "must be an alphanumeric "
                                                      
                                   }}} 
               
            
        
        ```

    2.  In a CF template, make these changes:

        -   Add the **AllowedPattern** key and enter a valid value range.
        -   Add the **ConstraintDescription** key and enter an error message.
        ```
        "Parameters" : {
                        "SSHLocation" : {
                        "Description" : "The IP address range that can be used to SSH to the EC2 instances",
                        "Type": "String",
                        "MinLength": "9",
                        "MaxLength": "18",
                        "Default": "0.0.0.0/0",
                         "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
                         "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
        
            } 
          }
        ```

4.  Click **Submit**.


