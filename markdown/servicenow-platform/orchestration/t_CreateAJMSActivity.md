---
title: Create a JMS activity
description: Create a custom JMS activity to retrieve or send messages to external systems using the Java Messaging Service.Configure your system to use Java Messaging Service \(JMS\) with a custom Orchestration JMS activity.You use execution parameters to create the input process script in the Preprocessing form.Use these parameters to create a post-processing script.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a JMS activity

Create a custom JMS activity to retrieve or send messages to external systems using the Java Messaging Service.

## Before you begin

Role required: activity\_creator or workflow\_admin

## About this task

The JMS activity supports third party JMS providers whose JMS client application is written with a typical Java EE pattern and can support these operations:

-   Using JNDI to find a ConnectionFactory object.
-   Using JNDI to find one or more destination objects.
-   Using the ConnectionFactory to create a JMS connection object.
-   Using the JMS connection to create one or more JMS session objects.
-   Using a JMS session and the destinations to create the MessageProducer and MessageConsumer objects.
-   Starting the JMS connection to enable delivery or consumption of messages.

**Note:** The JMS activity designer has been tested with the JMS providers ActiveMQ and Tibco EMS. When connecting to a JMS provider, refer to your third party user documentation.

## Procedure

1.  Create or verify your [JMS credential](https://www.servicenow.com/docs/access?context=r_JMSCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) .

    Your JMS credentials must have permission for the target database and proper configuration for the corresponding JMS connection. Credentials must be set up before you can create a JMS activity.

2.  Create or verify your [JMS connection](t_CreateAJMSActivity.md#) .

    Your JMS connection must be configured with valid JMS credentials set up before you can create a JMS activity.

3.  Create a [custom activity](https://www.servicenow.com/docs/access?context=create-custom-activities&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

    This action creates a custom activity using a template.

4.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the JMS Execution Command.

<table id="choicetable_py3_zmj_4y"><tbody><tr><td id="d151080e161">

**Configure your credential**

</td><td>

Fill in the fields necessary for your database connection.

</td></tr><tr><td id="d151080e170">

**Connection Factory**

</td><td>

Name of the JMS Connection Factory. You should create or verify your JMS connection. This configuration links the name of the Initial Context Factory with the URL of the JMS provider.

</td></tr><tr><td id="d151080e179">

**Destination Type**

</td><td>

Type of destination used for this message:-   **Queue**: Message is queued for point-to-point communications.

**Note:** The **GET** operation is only supported for the Queue destination type.

-   **Topic**: Message is used for publish and subscribe communication.


</td></tr><tr><td id="d151080e206">

**Destination Name**

</td><td>

Name of the queue or topic destination that is configured on the JMS provider.

</td></tr><tr><td id="d151080e215">

**Message Type**

</td><td>

The JMS message type value. Only the **Text Message** type is supported. The queue or topic destination must be configured to receive or send only Text Message. Other message types are dropped, since the JMS Activity cannot process them.

</td></tr><tr><td id="d151080e228">

**Operation**

</td><td>

The programmatic operation to perform on the destination. The choices are **PUT** or **GET**.

</td></tr><tr><td id="d151080e243">

**Timeout \(Secs\)**

</td><td>

Allowed time to wait for a message in the message queue before it times out, in seconds. The default is **30**.

</td></tr><tr><td id="d151080e255">

**Custom message headers**

</td><td>

The custom header values in a name/value pair format, that is available on the JMS destination. **Note:** This is only supported for a **PUT** operation.

</td></tr><tr><td id="d151080e270">

**Message payload**

</td><td>

Actual message content or payload that is sent to the JMS destination.**Note:** This is only supported for a **PUT** operation.

</td></tr><tr><td id="d151080e285">

**Credential tag**

</td><td>

A tag for an individual credential for a JMS activity in an Orchestration workflow.

</td></tr><tr><td id="d151080e294">

**Required MID Server capabilities**

</td><td>

MID Server to use, by capabilities.

</td></tr></tbody>
</table>
## What to do next

-   Use [auto-mapping](automap-output-variable-inputs.md) to generate outputs and parsing rules
-   If you do not use auto-mapping, you can manually [create output variables](t_CreateAnOutputVariable.md#) and [create parsing rules](t_CreateAParsingRule.md#)

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## Create a JMS connection for an Orchestration activity

Configure your system to use Java Messaging Service \(JMS\) with a custom Orchestration JMS activity.

### Before you begin

Role required: admin

### About this task

The MID Server must have the correct JMS connection factories for your organization. Configure those values in the **mid.property.jms.command.allowed\_factory\_names** property, found in **MID Server** &gt; **Properties**. The default values for this property can be changed to any value or comma-separated list of values that the third-party JMS provider advertises.

### Procedure

1.  Navigate to **MID Server** &gt; **JAR Files**.

2.  Click **New** and add.

<table id="choicetable_yqs_2c4_5y"><tbody><tr><td id="d151080e456">

**Name**

</td><td>

A unique and descriptive name for identifying the file in the instance.

</td></tr><tr><td id="d151080e465">

**Version**

</td><td>

A version number for the file, if one is available.

</td></tr><tr><td id="d151080e474">

**Source**

</td><td>

Location of the JAR file for reference purposes. Source information is not used by the system.

</td></tr><tr><td id="d151080e483">

**Description**

</td><td>

Short description of the JAR file and its purpose in the instance.

</td></tr></tbody>
</table>3.  Click the paper clip icon in the banner and attach the JMS driver jar file.

    The JMS driver jar file should be available as part of JMS provider installation. Few JMS vendors make them available as a separate product. Refer to the JMS provider documentation to determine which JMS client driver jar files require the client applications to connect to the JMS provider. For example, if you are trying to connect to ActiveMQ V5.10 \(JMS provider\), you need the `activemq-all-5.10.1.jar` file.

4.  Navigate to **Orchestration** &gt; **Credentials &amp; Connections** &gt; **JMS Connection Factory**.

5.  Click **New**, add the following, and click **Submit**.

<table id="choicetable_gqc_pd4_5y"><tbody><tr><td id="d151080e537">

**Name**

</td><td>

Unique name of this connection factory.

</td></tr><tr><td id="d151080e546">

**Initial Context Factory**

</td><td>

Name of the JNDI class that is used to create the InitialContext. **Note:** For example, to connect to ActiveMQ V5.10 \(JMS Provider\), the value is `org.apache.activemq.jndi.ActiveMQInitialContextFactory`.

</td></tr><tr><td id="d151080e561">

**Provider URL**

</td><td>

Location of the running JMS provider installation. **Note:** For example, to connect to ActiveMQ V5.1: `tcp://ipAddressOrHostName:61616`.

</td></tr></tbody>
</table>6.  Navigate to **Orchestration** &gt; **Credentials**.

7.  Click **New**, select **JMS Credentials**, and provide the user name and password the MID should use to communicate with the JMS provider.

    For more information, see [JMS credentials](https://www.servicenow.com/docs/access?context=r_JMSCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) [JMS credentials](https://www.servicenow.com/docs/access?context=r_JMSCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

8.  Click **Submit**.

    You are ready to create a custom JMS activity.


## JMS template execution parameters

You use execution parameters to create the input process script in the **Preprocessing** form.

You must use the `executionParam.` prefix with all variables in this table.

<table id="table_o2p_3q4_4r"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Jms ds

</td><td>

jms\_ds

</td><td>

Reference

</td><td>

Selected JMS data source.

</td></tr><tr><td>

Destination type

</td><td>

destination\_type

</td><td>

Enumerated

</td><td>

 

</td></tr><tr><td>

Destination name

</td><td>

destination\_name

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Message type

</td><td>

message\_type

</td><td>

Enumerated

</td><td>

 

</td></tr><tr><td>

Operation

</td><td>

operation

</td><td>

Enumerated

</td><td>

 

</td></tr><tr><td>

Time out

</td><td>

time\_out

</td><td>

Integer

</td><td>

Length of time to wait for the query to return results.

</td></tr><tr><td>

Custom headers

</td><td>

custom\_headers

</td><td>

Array of JavaScript objects

</td><td>

 

</td></tr><tr><td>

Message payload

</td><td>

message\_payload

</td><td>

String

</td><td>

 

</td></tr><tr><td>

Credential tag

</td><td>

credential\_tag

</td><td>

String

</td><td>

List of required MID Server capabilities.

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

 

</td></tr><tr><td>

ValueCapabilities

</td><td>

valueCapabilities

</td><td>

Array of hashmap

</td><td>

Capability values used to select the MID Server. For more information, see [MID Server capabilities](../../../product/mid-server/reference/r_MIDServerCapabilities.md). If there are additional capabilities that are assigned by value, use this example to customize the MID Server selection:```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'};
executionParam.valueCapabilities.push(valueCapability);
```

</td></tr></tbody>
</table>## JMS template post-processing parameters

Use these parameters to create a post-processing script.

|Name|Variable|Type|Usage|
|----|--------|----|-----|
|Status|status|String|Status of the operation \(Put or Get\) on the JMS destination.|
|StandardHeaders|standardHeaders|String|All the standard headers, as specified by JMS, that are obtained as part of the JMS message during a Get operation. This field is applicable only for Get operations.|
|CustomHeaders|customHeaders|String|All custom headers added by a producer or publisher application that are obtained as part of the JMS message during a Get operation. This field is applicable only for Get operations.|
|MessagePayload|messagePayload|String|Message payload that is obtained as part of the JMS message during a Get operation. This field is applicable only for Get operations.|
|EccSysID|eccSysID|String|Contains the reference ID associated with the ECC Queue input message returned by the activity.|
|ErrorMessages|errorMessages|String|Contains any error messages retrieved from the JMS command. This value is **null** if there are no error messages.|

