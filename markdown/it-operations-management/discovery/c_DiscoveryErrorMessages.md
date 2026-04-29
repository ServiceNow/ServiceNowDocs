---
title: Discovery error messages
description: Error messages and warnings in the system are documented to enable users to recognize the issues they are having and to take steps to resolve their problems.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 6
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery error messages

Error messages and warnings in the system are documented to enable users to recognize the issues they are having and to take steps to resolve their problems.

## Common error messages

-   **Input/output errors**
    -   CONNECTION\_FAILED
    -   CONNECTION\_TIMEOUT
    -   CONNECTION\_REFUSED
    -   CONNECTION\_CIPHER\_UNSUPPORTED
    -   CONNECTION\_PROTOCOL\_UNSUPPORTED
    -   CONNECTION\_LOST
    -   INVALID\_CONNECTION\_PARAMETER
    -   FILE\_NOT\_FOUND
    -   IO\_ERROR
-   **Authentication errors**
    -   NO\_CREDENTIALS
    -   AUTHENTICATION\_FAILED
    -   INVALID\_CREDENTIALS\_TYPE
-   **SSH errors**
    -   SSH\_SHELL\_UNSUPPORTED
    -   SSH\_SCRIPT\_TRANSFER\_FAILED
    -   SSH\_INVALID\_SESSION
-   **Windows errors**

    POWER\_SHELL\_VERSION\_UNSUPPORTED

-   **Command errors**
    -   COMMAND\_TIMEOUT
    -   INVALID\_COMMAND
    -   COMMAND\_FILTER\_ERROR
    -   COMMAND\_PARSER\_ERROR
    -   COMMAND\_KEY\_MAPPER\_ERROR
    -   COMMAND\_VALUE\_NORMALIZER\_ERROR
    -   TERMINAL\_SESSION\_LOST\_ERROR
    -   TERMINAL\_SESSION\_ENVIRONMENT\_MODIFICATION\_ERROR
-   **Generic component errors**
    -   INVALID\_COMPONENT
    -   INVALID\_COMPONENT\_PARAMETER
    -   INVALID\_OPERATION

## General error messages

-   **Message: org.xml.sax.SAXParseException: The entity name must immediately follow the '&amp;' in the entity reference**

    A version of this message occurs if you have used special characters in a password that is saved in an XML file.

-   **Message: Identified, ignored extra IP**

    This message can appear at the end classification phase of Discovery if a targeted IP address belongs to a device that is being discovered at the same time.

    For example, a Windows server has two NIC cards with two IP addresses. Discovery targets both IP addresses within the same Discovery schedule. This message is generated to note that second IP address is ignored because we don't want to update the same CI twice within the same Discovery run.

    This message is a warning and is expected. No action is needed.

-   **Message: Authentication failures**

    The discovery process could not discover the CI because the discovery application could not authenticate. To resolve, add the credentials of that machine in to the discovery credentials table.

-   **Message: Identified, not updating CI, now finished**

    No match on any of the CI Identifiers.

-   **Message: The impersonation of user failed**

    This message originates in the Powershell. Check that the domain is specified along with the user name in the credentials.

-   **Message: Connection failed to WMI service. Error: Permission denied**

    This message originates in WMI. Check that the MID Server service is running with the correct credentials and has access to the target device.

    To check this, run the following command from the command prompt on the MID Server host:

    ```
    wmic /node:target /user:user /password:password path win32_operatingsystem
    target = IP address of target device
    user = user account used by the mid server service
    password = password used by the mid server service
    ```

-   **Message: Connection failed to WMI service. Error: The remote server machine does not exist or is unavailable**

    This message originates in WMI. Check that the MID Server service account has access to the targeted machine. Check if a domain admin account is used as the MID Server service account. Check if any existing firewalls are open to the connection. To check this, run the following command from the command prompt on the MID Server host.

    Execute for runner\_type=WMI:

    ```
    wmic /node:"<target>" /user:"<user>" /password:"<password>" path win32_operatingsystem
    From within a Powershell console on the mid server host, execute for runner_type=Powershell:
    gwmi win32_operatingsystem -computer <ip> -credential '<username>'
    ```

-   **Message: Provider is not capable of the attempted operation**

    WMI repository was corrupted. After following the "WMI: Repository Corruption, or Not?" article on the [Microsoft TechNet site](https://technet.microsoft.com/en-us/), the problem was corrected.

-   **Message: The result file can't be fetched because it doesn't exist**

    PRB581515 - Powershell does not work when customer has locked down write rights to admin share.

-   **Message: Please run sneep as root to ensure correct serial number from fserial data source**

    The Oracle **Sneep** command line tool must be installed for the Solaris - Serial Number probe to work correctly. There is a [known limitation](https://wikis.oracle.com/display/proactive/SneepFAQ) with Fujitsu PRIMEPOWER devices. To work around this limitation, run the Solaris discovery with root credentials.


## Discovery sensor error messages

-   **Message: The multisensor will not process because its major version = X while probe\_name responding script's major version = Y**

    This error message indicates that there is a major version mismatch.

-   **Message: Payload length exceeds limit of 5000000**

    This error message indicates that the Discovery probe results exceed the limit. The MID Server will discard the results and return a warning message. To resolve, set the value of the **mid.discovery.max\_payload\_size** MID Server property to any negative number \(for example, -1\) to disable the payload limit and allow payloads of any size to be sent to the instance.

-   **Message: The multisensor will not process because its responding script's major version = X while its referenced probe probe\_name major version = Y**

    This error message indicates that there is a major version mismatch.

-   **Message: sensor\_name sensor's major version = X while its related probe's major version = Y**

    This error message indicates that there is a major version mismatch in the probe and sensor versions and the sensor will stop processing until this condition is resolved.

-   **Message: sensor\_name multisensor's minor version = X while probe\_name responding script's minor version = Y**

    This error message indicates that there is a minor version mismatch.

-   **Message: sensor\_name multisensor's responding script's minor version = X while its referenced probe probe\_name minor version = Y**

    This error message indicates that there is a minor version mismatch.

-   **Message: sensor\_name sensor's minor version = X while its related probe's minor version = Y**

    This error message indicates that there is a minor version mismatch in the probe and sensor versions. Processing will continue, but you may want to resolve this condition.

-   **Message: Sensor error when processing . . . : No sensors defined**

    Every active probe looks for a corresponding sensor to process the data that is collected by the probe. This error message indicates that the corresponding sensor for the probe is missing or inactive.

-   **Message: Sensor error when processing . . . : typeError: . . .**

    This error message indicates that the sensor has one of the core error constructors in JavaScript.

-   **Message: Sensor error when processing ...: Exception while processing sensor: XML Parse Problem: !\[CDATA\]**

    This XML parsing error occurs when the discovery sensor fails to parse the input ECC queue payload. The payload is not formatted according to XML specifications. Possible solutions include:

    -   Escape problematic characters. For example, change **&lt;** to **&amp;lt** and **&amp;** to **&amp;amp**.
    -   Escape entire blocks of text with CDATA sections, or put encoding declarations at the start of the text.
    -   Remove any whitespace characters \(space, tabs, newlines\) before the XML declarations.
-   **Message: Sensor error when processing Linux - Network ARP Tables: Exception while running probe post processing script: No XML data**

    The system displays the No XML data error when the XML sensor processor fails to ﬁnd the expected XML data in the probe output. During sensor processing, Discovery attempts to retrieve the probe results but finds the probe output empty. Verify that the probe returns the correct output for the sensor to process.

-   **Message: Sensor error when processing Shazzam: Exception while running probe post processing script: Probe not found: null**

    The Probe not found error occurs when the sensor processor fails to ﬁnd the probe record supposedly associated with the sensor. During sensor processing, Discovery gets the probe record from the probe cache and stores it for later reference. The "Probe not found" error occurs either when the sys\_id of the probe cannot be found or there is an issue with the probe cache.

    See [Find the cause of a "Probe not found" error](../task/t_FindTheCauseOfAProbeNotFoundError.md) for more information.


-   **[Find the cause of a sensor error message](../task/t_FindTheCauseOfASensorErrorMessage.md)**  
Use this procedure to identify a Discovery sensor error.
-   **[Find the cause of a "No Sensor Defined" error message](../task/t_IdentifyCauseNoSenDefEM.md)**  
Every active probe looks for a corresponding sensor to process the data that is collected by the probe. The "No Sensors Defined" message indicates that the corresponding sensor for the probe is missing or inactive.
-   **[Fix the cause of a sensor error message](../task/t_FixTheCauseOfASensorErrorMessage.md)**  
To fix a Discovery sensor error message, you must fix the JavaScript file containing the code that generated the error.
-   **[Find the cause of a "Probe not found" error](../task/t_FindTheCauseOfAProbeNotFoundError.md)**  
Verify the correct sys\_id of the probe associated with the **probe** parameter in the payload of the ECC Queue input record.

**Parent Topic:**[Discovery monitoring and issue resolution](c_DiscoveryTroubleshooting.md)

