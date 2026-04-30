---
title: Configure a scripted writeback action that saves a signature input
description: Configure an action item's scripted writeback action that can save the signature input in your input form screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure input form screens with signature inputs, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a scripted writeback action that saves a signature input

Configure an action item's scripted writeback action that can save the signature input in your input form screen.

## Before you begin

You must create an input form screen with signature inputs. For more information, see [Configure input form screens with signature inputs](configure-signature-inputs.md).

In addition, you must have configured an action item to use for this input form screen. For more information, see [Configure an action item](sg-studio-create-action-item.md).

Role required: admin

## About this task

Admins can write scripts that perform the action and then save the signature inputs. Alternatively, they can write scripts that save the signature first before performing the action.

You can use the `MobileSignatureHandler` script include to save signature inputs. The `MobileSignatureHandler` script include saves the signature into the sys\_attachment table and creates a relevant record in the signature\_image table.

You can also write custom code to handle saving your signature inputs. For information about server-side scripting, see [Server-side scripting](https://www.servicenow.com/docs/access?context=c_ServerScripting&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Action Items**.

2.  Select the action item that you want to use for the signature input.

3.  Add the signature saving script in the **Execution Script** field.

    For example, the following writeback action item script shows how the `MobileSignatureHandler` can be used to save the signature input:

    ```
    (function WriteBackAction(parm_input, parm_variable, actionResult) {
        var gr = new GlideRecord("incident");
        gr.get(parm_variable['sys_id']);
        var shortDesc = parm_input['shortDescInput'];
        gr.setValue("short_description", shortDesc);
        gr.update();
          // in this example "signatureInput" is the name of a sys_sg_input of type signature
          // SignatureType will return either "Image" or "Text"
        var signatureType = parm_input['signatureInput']["SignatureType"];
          // SignatureValue will return a String containing the base64 respresentation of the image in the case of a drawn signature
          // or a String with the name of the user if they typed their name
        var signatureValue = parm_input['signatureInput']["SignatureValue"];
        var table = "incident";
        var documentId = parm_variable['sys_id'];
        var signatureHandler = new sn_mobile.MobileSignatureHandler();
        if (signatureType == "Image")
            signatureHandler.insertSignatureImage(table, documentId, signatureValue);
        else if (signatureType == "Text")
            signatureHandler.insertTypedSignature(table, documentId, signatureValue);
    })(parm_input, parm_variable, actionResult);
    ```

4.  Select **Update** to save the configuration.


