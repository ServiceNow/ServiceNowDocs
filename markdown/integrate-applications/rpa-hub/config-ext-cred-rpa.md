---
title: Steps to configure an external credential vault in RPA Hub
description: Use this list of steps to guide you through all the tasks of configuring an external credential vault in RPA Hub.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [External credential vault in RPA Hub, Credential Management in RPA Hub, Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Steps to configure an external credential vault in RPA Hub

Use this list of steps to guide you through all the tasks of configuring an external credential vault in RPA Hub.

Complete all the tasks for a step before moving on to the next step.

Do the steps in the order that they’re presented.

<table id="table_ar4_w1b_5vb"><thead><tr><th>

Task

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

1. Create a subflow to integrate your external credential vault. For more information, see [Create a subflow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-subflow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

</td><td>

For reference, see the sample **Demo CyberArk Subflow** in your ServiceNow instance.

</td></tr><tr><td>

1.A. Verify that the subflow that you’re creating to integrate with the External Credential Vault, must have an input type as JSON. This input takes the value from the **Subflow Input** field of the Robot Credential, Application Credential, or Time-based One-time Password \(TOTP\) Authenticator.

For example, the robot credential or application credential or TOTP authenticators that are using the **Demo CyberArk** external credential vault, must align with the following JSON format:

```
{ 
"appID" : "",
"query" : ""
}
```

Populate values for **appID** and **query**.

</td><td>

 

</td></tr><tr><td>

1.B. You can use the REST Step in the subflow to connect with the external credential vault. You can also use other integration steps such as SOAP. For more information, see [Workflow Studio steps](https://www.servicenow.com/docs/access?context=steps&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

</td><td>

 

</td></tr><tr><td>

1.C. Verify that the output of your subflow must be aligned with the following JSON schema.```
{
    "$schema": "http://json-schema.org/draft-07/schema#",
    "type": "object",
    "properties": {
        "result": {
            "type": "object",
            "properties": {
                "status": {
                    "type": "string",
                    "enum": ["success", "failure"]
                },
                "data": {
                    "type": "object",
                    "properties": {
                        "username": {
                            "type": "string"
                        },
                        "sensitiveValue": {
                            "type": "string"
                        },
                        "additionalData": {
                            "type": "object"
                        }
                    },
                    "required": ["sensitiveValue"]
                },
                "error": {
                    "type": "object",
                    "properties": {
                        "errorType": {
                            "type": "string"
                        },
                        "errorMessage": {
                            "type": "string"
                        },
                        "additionalErrorData": {
                            "type": "object"
                        }
                    },
                    "required": ["errorMessage"]
                }
            },
            "required": ["status"]
        }
    },
    "required": ["result"]
};
```

</td><td>

This schema is used by the Robotic Process Automation \(RPA\) GraphQL APIs to validate the subflow output. If the output isn’t aligned with this schema, an error is encountered. Error Message: `The JSON received from the subflow deviates from the expected JSON schema. Rectify the JSON structure by aligning it with the specified schema in the documentation.`

</td></tr><tr><td>

1.D. You can align with the expected JSON schema \(mentioned in 1.C\) by defining a JSON output with the name 'result' for the Subflow. For success status, this result output must be assigned with a JSON object of the following structure. Populate values for the keys defined in the JSON. The **status** and **sensitiveValue** keys are required.```
{
  "status": "success", //Mandatory
  "data": {
    "username": "",
    "sensitiveValue": "" //Mandatory
    "additionalData": {}
  }
}
```

For failure status, this result output must be assigned with a JSON object of the following structure. Populate values for the keys defined in the JSON. The **status** and **errorMessage** keys are required.

```
{
  "status": "failure", //Mandatory
  "error": {
    "errorType": "",
    "errorMessage": "", //Mandatory
     "additionalErrorData": {}
  }
}
```

</td><td>

 

</td></tr><tr><td>

2. Create an external credential vault record. For more information, see [Create an external credential vault record in RPA Hub](../task/create-ext-cred-rpa.md).

</td><td>

For reference, see the sample **Demo CyberArk** external credential vault in your ServiceNow instance.

</td></tr><tr><td>

3. Establish a connection with an external credential vault by using the ServiceNow Connections and Credentials. For more information about creating an active connection, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). While configuring the connection record, verify to align with your organizational security requirements.

</td><td>

For reference, see the sample **Demo CyberArk Subflow** that uses **RPA CyberArk** connection and credential alias. Create a connection record in this connection and credential alias to establish connection with your CyberArk external vault.

</td></tr><tr><td>

4. To use the external credential vault record, that you created in step 2, navigate to either robot credential, application credential, or TOTP authenticator and select the **External Credential** check box. Also, select a record in the **External Credential Vault** field and populate the **Subflow Input** field with a valid JSON object. The JSON must contain the necessary information for retrieving credentials from the external credential vault.

</td><td>

For more information about configuring these fields, see [Create a robot credential in RPA Hub](../task/create-credential-set-botprocess.md), [Create an application credential in RPA Hub](../task/create-application-credential.md), and [Create a TOTP authenticator in RPA Hub](../task/map-totp-credential-set-rpa.md).

</td></tr></tbody>
</table>