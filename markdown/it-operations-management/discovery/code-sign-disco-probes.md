---
title: Discovery on Code Signing instances
description: Discovery is supported on instances with Code Signing enabled. Code signing validates the integrity of Discovery components before execution to help prevent unauthorized scripts from running on MID Servers and target machines.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery on Code Signing instances

Discovery is supported on instances with Code Signing enabled. Code signing validates the integrity of Discovery components before execution to help prevent unauthorized scripts from running on MID Servers and target machines.

## How it works

When Code Signing is enabled, Discovery validates signatures on components that contain scripts or commands before execution. Validation occurs at both the instance level and the MID Server level.

The instance validates signatures on probes and probe parameters. If a probe is tampered with, the instance rejects it and doesn't send it to the MID Server for processing. If probe parameters aren't trusted, they aren't added to the probe. The probe still launches, but without the untrusted parameters.

The MID Server validates signatures on patterns, MID script includes, and MID script files. If a pattern's signature is invalid, the MID Server won't download it. If the pattern was previously downloaded, it's deleted. Discovery can't run that pattern on any machine until it's re-signed.

Signatures are included automatically with Discovery applications and plugins. When your platform and store apps meet the requirements, code signing for Discovery works without manual signing. For more information about how code signing works, see [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Benefits

The following examples highlight the primary advantages of using code signing:

-   **Security protection**: Blocks unsigned or tampered payloads from executing on MID Servers and target machines, helping prevent malicious actors from running dangerous commands even if an instance is compromised.
-   **Authenticity verification**: Confirms that probes, parameters, and sensors originate from a trusted source and haven’t been modified since signing.
-   **Compliance support**: Strengthens audit capabilities by helping prevent unauthorized script execution without impacting discovery performance.
-   **Integrity assurance**: Validates that sensitive fields in Discovery components haven’t been altered after signing.

## Requirements

Code signing for Discovery requires the following dependencies:

-   You must be using the Australia version of the ServiceNow AI Platform.
-   You must have the following ServiceNow Store applications and versions installed:
    -   Discovery Admin Workspace v1.13.0
    -   Visibility Content v6.13.10
    -   Discovery and Service Mapping Patterns v1.30.2
-   You must have Code Signing enabled with the Circle of Trust established. For more information, see [Configuring Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Supported discovery types

Code signing for Discovery supports the following discovery methods:

-   IP-based Discovery
-   Cloud Discovery

    **Note:** Cloud Discovery requires additional configuration. For more information, see [Configure Cloud Discovery for code-signed instances](../task/config-cloud-disco-code-sign.md).


## Signature validation scope

Code signing validates signatures on Discovery tables that contain scripts or commands executed on target machines or MID Servers. This includes probes, probe parameters, sensors, patterns, and more.

## Limitations

Pattern debugger isn’t available on code-signed instances.

**Related topics**  


[Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)

