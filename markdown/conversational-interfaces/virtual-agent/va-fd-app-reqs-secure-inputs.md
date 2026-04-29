---
title: Workflow Studio scoped application requirements for secure inputs
description: Adhere to the following scoped application requirements to implement secure \(password2\) inputs in your Virtual Agent topics.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with Workflow Studio workflows, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Workflow Studio scoped application requirements for secure inputs

Adhere to the following scoped application requirements to implement secure \(password2\) inputs in your Virtual Agent topics.

You can add secure inputs to Virtual Agent topics in two ways:

-   [Create a secure custom input control](../task/create-custom-control.md) that uses a Workflow Studio action or subflow with secure \(password2 type\) inputs.
-   Add an [Action utility node](../reference/va-action.md) to a topic that refers to a Workflow Studio action or subflow that has a single password2 field as an input.

The [Key Management Framework](https://www.servicenow.com/docs/access?context=understanding-kmf&version=australia&pubname=australia-platform-security&ft:locale=en-US) \(KMF\) must be installed and configured for your instance. The scoped application that uses the secure fields must also have the following:

-   A **sys\_kmf\_crypto\_module** record, with a related Symmetric Key Wrapping/Unwrapping **sys\_kmf\_module\_crypto\_spec** record
-   A **sys\_kmf\_crypto\_caller\_policy** record with the following properties:
    -   Policy name: &lt;modify the auto-generated name&gt;
    -   Crypto module: **com\_glide\_cs\_glideencrypter**
    -   Type: **Scope**
    -   Target Scope: &lt;your application's scope&gt;
    -   Application: &lt;the name of your scoped application&gt;
    -   Active: **true**
    -   Result: **Track**
-   A Workflow Studio action or subflow that accepts one or more password2 input fields
-   A [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US) in the Workflow Studio action that unwraps the password2/KMF passwords as follows:

    ```
    var op = new 
    sn_kmf_ns.KMFCryptoOperation("global.com_glide_cs_glideencrypter","SYMMETRIC_UNWRAPPING").withAlgorithm("AES").withOutputFormat("KMFNONE");
    var old_pw_clear_data = op.doOperation(inputs.old_pw);
    var new_pw_clear_data = op.doOperation(inputs.new_pw);
    var new_pw_confirmed_clear_data = op.doOperation(inputs.new_pw_confirmed);
    ```


For more information about password2 encryption with KMF, see [Password2 encryption with KMF](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[Integrating Virtual Agent with Workflow Studio workflows](va-flow-designer-integration.md)

