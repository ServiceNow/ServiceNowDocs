---
title: Warranty Claims SOAP API
description: The Warranty Claims SOAP API handles incoming repair orders from dealer systems and converts them into warranty claims within the Oracle Enterprise Manager \(OEM\)’s platform.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-09"
reading_time_minutes: 10
breadcrumb: [MCO Integration APIs, Reference, Manufacturing Commercial Operations]
---

# Warranty Claims SOAP API

The Warranty Claims SOAP API handles incoming repair orders from dealer systems and converts them into warranty claims within the Oracle Enterprise Manager \(OEM\)’s platform.

This API follows [SOAP 1.1 conventions](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/) and uses [Standards for Technology in Automotive Retail \(STAR\) XML schemas](https://https://schemas.liquid-technologies.com/star/5.3.4/repairorder_xsd.html/star/5.3.4/?page=processsaleslead_xsd.html) for interoperability across automotive service systems.

This API enables the exchange of warranty and repair claim information between ServiceNow Manufacturing Commercial Operations \(MCO\) and a Dealer Management System \(DMS\). Specifically, it allows users to:

-   Create and validate warranty claims in the DMS directly from ServiceNow MCO.
-   Query the status of submitted claims, including adjudication and approval outcomes, and retrieve those results back into ServiceNow.
-   Manage repair claim data across three core MCO tables:
    -   Repair Claim Case \[sn\_repair\_claim\_mgmt\_case\]
    -   Repair Claim Case Line \[sn\_repair\_claim\_mgmt\_case\_line\]
    -   Repair Claim Case Line Charge \[sn\_repair\_claim\_mgmt\_case\_line\_charge\]
-   Support STAR XML message formats through configuration‑driven adapters, enabling standards‑based integrations without custom code.

This documentation is intended for developers, system integrators, and partners implementing a standards-based SOAP integration.

## Standards and conventions

The API adheres to widely used, publicly documented standards.

|Item|Standard|
|----|--------|
|SOAP version|SOAP 1.1 \(default\); 1.2 supported for select partners|
|WSDL|WSDL 1.1|
|XML schema|XSD 1.0 \(STAR XML\)|
|STAR schema version|5.13.4|
|Character encoding|UTF-8|
|Message format|`text/xml`|
|Protocols|HTTPS over TLS 1.2+; optional Mutual TLS for STAR partners|

## Access and authentication

-   Basic Auth \(username/password\)
-   Configurable per endpoint for every DMS

## Granular roles and entities

This SOAP API requires granular roles to access certain MCO features and responsibilities, provide CRU permissions without custom ACLs, and map directly to supported entities. See [Granular roles and entities](../concept/mco-granular-roles-and-entities.md) for information about supported granular roles.

## Endpoint details

The Warranty Claims SOAP API is exposed as a scripted SOAP Web service in ServiceNow MCO.

```
https://<instance_name>.service-now.com/sn_mco_integ_RepairClaimSOAPHandler.do?SOAP
```

WSDL:

```
https://<instance_name>.service-now.com/sn_mco_integ_RepairClaimSOAPHandler.do?WSDL
```

The instance name is fixed per OEM environment \(sandbox, test, production\).

|URL part|Description|
|--------|-----------|
|`<instance_name>`|The ServiceNow instance hosting MCO \(OEM‑specific, fixed per OEM\).|
|`sn_mco_integ_`|MCO integration namespace.|
|`RepairClaimSOAPHandler.do`|Scripted SOAP Web service entry point.|
|`?SOAP`|SOAP invocation.|
|`?WSDL`|WSDL contract for client generation.|

## API operation

Operation Name: `ProcessRepairOrder`

Processes a repair order payload. The operation performs either a create or update action depending on whether a matching business identifier already exists.

This operation:

-   Validates the request against the STAR schema.
-   Validates that values in XML are valid in MCO.
-   Determines whether the repair claim \(document ID\) already exists.
-   Creates a new record if no match is found.
-   Updates an existing record if a match is found.
-   Returns a processing status and reference identifier.

## Request structure

The request body contains a STAR-conforming `ProcessRepairOrder` message wrapped in a SOAP envelope. Key logical elements include:

-   Application metadata \(sender, creation time, destination\).
-   Process verb indicating the requested action.
-   Repair order header information.
-   Vehicle details.
-   Job, labor, parts, and pricing details.
-   Warranty claim information.

All elements must conform to the STAR XML schema version indicated in the payload.

## Request parameters

<table><thead><tr><th>

Name

</th><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity status

</td><td>

activity\_status

</td><td>

Required. Indicates the current life-cycle status of the repair claim case line and drives playbook execution.Table: Repair Claim Case Line \[sn\_repair\_claim\_mgmt\_case\_line\]

Valid values:

-   Claim details completed \[claim\_details\_completed\]
-   Claim jobs completed \[claim\_jobs\_completed\]
-   Claim under review completed \[claim\_under\_review\_completed\]
-   Claim job edit completed \[claim\_job\_edit\_completed\]
-   Claim summary completed \[claim\_summary\_completed\]
-   Close case completed \[close\_case\_completed\]

Data type: Choice \(string\)

</td></tr><tr><td>

Actual end

</td><td>

actual\_end

</td><td>

Optional. Date and time when the repair activity was completed.Format: YYYY-MM-DDThh:mm:ss

Data type: DateTime \(string\)

</td></tr><tr><td>

Actual start

</td><td>

actual\_start

</td><td>

Optional. Date and time when the repair activity started.Format: YYYY-MM-DDThh:mm:ss

Data type: DateTime \(string\)

</td></tr><tr><td>

Asset

</td><td>

asset

</td><td>

Required. Serial number or asset tag of the claim.Table: Asset \[alm\_asset\]

Data type: Reference \(string\)

</td></tr><tr><td>

Causal part

</td><td>

product\_model

</td><td>

Required. Model number of the part identified as the root cause of the issue.Table: Product model \[cmdb\_model\]

Data type: Reference \(string\)

</td></tr><tr><td>

Claimed amount

</td><td>

claimed\_amount

</td><td>

Optional. Claimed cost amount for this specific repair claim case line.Data type: Currency \(string\)

</td></tr><tr><td>

Consumer

</td><td>

consumer

</td><td>

Optional. Consumer or vehicle owner. If consumer ID is unavailable, phone number or email may be provided. Table: Consumer \[csm\_consumer\]

Data type: Reference \(string\)

</td></tr><tr><td>

Correlation ID

</td><td>

correlation\_id

</td><td>

Optional. External correlation identifier used to link this request with upstream or downstream systems.Data type: String

</td></tr><tr><td>

Dealer

</td><td>

requesting\_service\_organization

</td><td>

Required. Reference to the service organization \(dealer\) submitting the request.Internally resolves to a Service Organization \[sn\_customer\_service\_organization\] record, matched by Number.

Data type: Reference \(string\)

</td></tr><tr><td>

Deductible amount

</td><td>

deductible\_amount

</td><td>

Optional. Deductible amount applicable to the repair claim.Data type: Currency \(string\)

</td></tr><tr><td>

External Repair order number

</td><td>

external\_ro\_number

</td><td>

Required. Repair order number from the external dealer or service system.Data type: String

</td></tr><tr><td>

Fault code

</td><td>

fault\_code

</td><td>

Optional. Fault or diagnostic code associated with the reported issue.Data type: String

</td></tr><tr><td>

Install base

</td><td>

install\_base

</td><td>

Optional. Identifies the product or asset being serviced and is resolved by matching the provided value to an existing Install Base Item in ServiceNow.Table: Install base \[sn\_install\_base\_item\]

Valid values:

-   asset number
-   serial number
-   name

Data type: Reference \(string\)

</td></tr><tr><td>

Part in warranty

</td><td>

in\_warranty

</td><td>

Required. Flag that indicates whether the affected part is under warranty.Valid values:

-   `true`: Affected part is under warranty.
-   `false`: Affected part isn't under warranty.

Data type: Boolean

</td></tr><tr><td>

Vehicle in warranty

</td><td>

vehicle\_in\_warranty

</td><td>

Required. Flag that indicates whether the vehicle is under warranty.Valid values:

-   `true`: Vehicle is under warranty.
-   `false`: Vehicle isn't under warranty.

Data type: Boolean

</td></tr><tr><td>

Issue Description

</td><td>

short\_description

</td><td>

Required. Brief summary of the issue.Data type: String

</td></tr><tr><td>

Parent task

</td><td>

parent\_task

</td><td>

Required. Identifier of an existing parent repair claim case or parent task associated with the request.Table: Task \[task\]

Data type: Reference \(string\)

</td></tr><tr><td>

Pre-auth case line

</td><td>

pre\_auth\_case\_line

</td><td>

Optional. Corresponding pre‑authorization repair request, if applicable.Table: Pre‑Auth Repair Request Job \[sn\_pre\_auth\_repair\_request\_job\], Field: Number

Data type: Reference \(string\)

</td></tr><tr><td>

Product Usage

</td><td>

product\_usage

</td><td>

Required. Usage reading of the vehicle at time of repair \(for example, kilometers or miles driven\).Data type: Number \(decimal\)

</td></tr><tr><td>

Quantity

</td><td>

quantity

</td><td>

Required. Number of affected or replaced parts.Data type: Number \(decimal\)

</td></tr><tr><td>

Repair action

</td><td>

repair\_action

</td><td>

Required. Action performed to resolve the issue.Valid values:

-   Repair \[REPAIR\]
-   Replacement \[REPLACEMENT\]
-   Software update \[SOFTWARE\_UPDATE\]

Data type: Choice \(string\)

</td></tr><tr><td>

Repair Claim case

</td><td>

parent\_case

</td><td>

Required. Repair claim case associated with this case line.Table: Customer case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Repair Details

</td><td>

details

</td><td>

Required. Detailed description of the issue, diagnostics, and repair performed.Data type: Translated HTML

</td></tr><tr><td>

Replacement part

</td><td>

replacement\_part

</td><td>

Conditional. If **repair\_action** = `replacement`, specifies the name or model number of the replaced part.Table: Product model \[cmdb\_model\]/Name/Model Number

Data type: Reference \(string\)

</td></tr><tr><td>

Reported date

</td><td>

reported\_date

</td><td>

Required. Date and time the vehicle arrived at the dealer or service center.Format: YYYY-MM-DDThh:mm:ss

Data type: DateTime

</td></tr><tr><td>

Source

</td><td>

source

</td><td>

Optional. Originating system or channel that submitted the repair claim request.Data type: String

</td></tr><tr><td>

Submitted

</td><td>

submitted\_at

</td><td>

Required. Date and time the claim was submitted.Format: YYYY-MM-DDThh:mm:ss

Data type: DateTime

</td></tr><tr><td>

Total claimed amount

</td><td>

total\_claimed\_amount

</td><td>

Required. Total claimed amount for the entire repair claim case.Data type: Currency \(string\)

</td></tr><tr><td>

Type

</td><td>

type

</td><td>

Required. Type of claim being submitted.Valid values:

-   Warranty \[Warranty\]
-   Goodwill \[Goodwill\]
-   Service contract \[Servicecontract\]

Data type: Choice \(string\)

</td></tr><tr><td>

Unit of measure

</td><td>

unit\_of\_measure

</td><td>

Required. Unit of measurement for the product usage. For example, kms or miles.Table: Unit of Measure \[sn\_prd\_pm\_uom\]

Data type: Reference \(string\)

</td></tr><tr><td>

Work notes

</td><td>

work\_notes

</td><td>

Optional. Internal notes or comments related to claim processing.Data type: String

</td></tr></tbody>
</table>## Example SOAP request

**Note:** Namespaces used in examples follow standard SOAP and STAR conventions.

```
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
    xmlns:oagis="http://www.openapplications.org/oagis/9"
    xmlns:star="http://www.starstandard.org/STAR/5"
    xmlns:tran="http://www.starstandards.org/webservices/2009/transport"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

    <soap:Header>
        <!-- Optional header -->
        <tran:payloadManifest>
            <tran:manifest
                contentID="A0"
                element="ProcessRepairOrder"
                namespaceURI="http://www.starstandard.org/STAR/5"
                version="5.13.4.0.0" />
        </tran:payloadManifest>
    </soap:Header>

    <soap:Body>
        <ProcessRepairOrder xmlns="http://www.service-now.com/ProcessRepairOrder">
            <payload>
                <![CDATA[
<star:ProcessRepairOrder
    xmlns:star="http://www.starstandard.org/STAR/5"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    releaseID="5.13.4.0.0"
    systemEnvironmentCode="Production">

    <!-- APPLICATION AREA -->
    <star:ApplicationArea>
        <star:Sender>
            <star:CreatorNameCode>DealerManagementSystem</star:CreatorNameCode>
            <star:SenderNameCode>DEALER001</star:SenderNameCode>
            <star:URI>https://dealer-system.example.com</star:URI>
            <star:DealerNumberID>98765</star:DealerNumberID>
            <star:StoreNumber>ST-001</star:StoreNumber>
            <star:AreaNumber>REGION-01</star:AreaNumber>
            <star:DealerCountryCode>US</star:DealerCountryCode>
            <star:LanguageCode>en-US</star:LanguageCode>
            <star:SystemVersion>DMS_v6.1.0</star:SystemVersion>
        </star:Sender>

        <star:CreationDateTime>2026-01-09T14:30:45</star:CreationDateTime>
        <star:BODID>a1b2c3d4-e5f6-7890-abcd-ef1234567890</star:BODID>

        <star:Destination>
            <star:DestinationNameCode>OEM_MANUFACTURER</star:DestinationNameCode>
        </star:Destination>
    </star:ApplicationArea>

    <!-- DATA AREA -->
    <star:ProcessRepairOrderDataArea>
        <star:Process>
            <star:ActionCode>ADD</star:ActionCode>
        </star:Process>

        <star:RepairOrder>
            <star:RepairOrderHeader>
                <star:DocumentIdentificationGroup>
                    <star:DocumentIdentification>
                        <star:DocumentID>RO-2026-987654qwert</star:DocumentID>
                    </star:DocumentIdentification>
                </star:DocumentIdentificationGroup>

```

Example SOAP response \(success\)

```
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Body>
    <ProcessRepairOrderResponse>
      <status>success</status>
      <message>Repair order processed successfully</message>
      <data>{"reference":"RPC0001005"}</data>
    </ProcessRepairOrderResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

Example SOAP response \(validation error\)

```
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
  <SOAP-ENV:Body>
    <ProcessRepairOrderResponse>
      <status>error</status>
      <message>
        VALIDATION ERRORS
        payload="[{\"field\":\"asset\",\"message\":\"Reference value not found\"}]"
      </message>
    </ProcessRepairOrderResponse>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

## Error handling

The API uses standard SOAP and HTTP mechanisms to report errors like SOAP faults, custom business errors, and HTTP status codes.

SOAP faults are returned when the request can't be parsed or processed at the protocol level, such as when:

-   XML is malformed
-   Namespace is incorrect
-   Required SOAP envelope structure missing
-   Authentication failure
-   System-level processing error

Example SOAP Fault:

```
<soap:Fault>
  <faultcode>soap:Client</faultcode>
  <faultstring>Invalid SOAP message</faultstring>
</soap:Fault>

```

## Custom business errors

Business validation errors occur after successful SOAP parsing and indicate issues with request data, such as:

-   Missing or invalid references
-   Duplicate repair orders
-   Invalid code values
-   Schema or version mismatches

These occur after successful SOAP parsing but during business validation. Errors are returned in the operation response with a status of `error` and a descriptive message. Possible errors:

-   MANDATORY\_FIELD\_MISSING
-   MIN\_VALUE MAX\_VALUE INVALID\_REFERENCE
-   UNSUPPORTED\_VALIDATION\_TYPE
-   SOAP\_ENVELOPE\_EMPTY
-   IN\_WARRANTY\_TRANSFORM\_FAILED
-   VALIDATION\_ERRORS
-   INVOKE\_PROCESSOR\_FAILED
-   INVALID\_DATE\_FORMAT
-   INVALID\_DATE\_VALUE
-   INVALID\_DATETIME\_FORMAT
-   XML\_TO\_JSON\_FAILED
-   INVALID\_DATETIME\_VALUE
-   PAYLOAD\_PARSING\_FAILED
-   EMPTY\_PARSED\_PAYLOAD
-   INVALID\_TRANSLATED\_HTML\_TYPE
-   MAX\_LENGTH\_EXCEEDED
-   MAIN\_PART\_MISSING
-   MULTIPLE\_MAIN\_PARTS

Sample error code:

```
<ProcessRepairOrderResponse> 
<status>error</status> 
<message>VALIDATION ERRORS | payload="[{\"field\":\"asset\",\"message\":\"Reference value not found\"}]"</message> 
</ProcessRepairOrderResponse> 
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

## HTTP Status Codes

|HTTP Code|Description|
|---------|-----------|
|200|OK - Request processed successfully.|
|400|Bad Request - Invalid or malformed request.|
|401|Unauthorized - Authentication failure.|
|403|Forbidden - Access not permitted.|
|500|Internal Server Error - Unexpected processing failure.|

## Outbound STAR Integration

This outbound integration sends claim adjudication and payment results from the OEM Now ServiceNow instance to a Dealer Management System \(DMS\) using STAR‑compliant XML messages.

The integration is triggered by a ServiceNow Business Rule on the Repair Claim Case table \(sn\_repair\_claim\_mgmt\_case\) when:

-   The claim source is DMS
-   The claim state is one of the following:
    -   Approved
    -   Partially Approved
    -   Rejected
    -   Awaiting Information

<table id="table_czt_dds_m3c"><thead><tr><th>

Name

</th><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approved amount

</td><td>

approved\_amount

</td><td>

Required. Approved amount for this specific repair claim case line after adjudication.Data type: Currency

</td></tr><tr><td>

Correlation ID

</td><td>

correlation\_id

</td><td>

Required. Unique identifier used to correlate the outbound response with the original inbound repair claim request.Data type: String

</td></tr><tr><td>

External repair order number

</td><td>

external\_ro\_number

</td><td>

Required. External repair order number associated with the Repair Claim case, as provided by the dealer system.Data type: String

</td></tr><tr><td>

Dealer ID

</td><td>

dealer\_number

</td><td>

Required. Unique identifier of the dealer or service organization that submitted the repair claim.Data type: String

</td></tr><tr><td>

Review action

</td><td>

review\_action

</td><td>

Required. Action taken by the claims agent during the claim review.Possible values:

-   Approve all \[approve\_all\]
-   Reject all \[reject\_all\]
-   Partially approved \[partially\_approved\]
-   Send back \[send\_back\]

Data type: Choice \(string\)

</td></tr><tr><td>

Review comments

</td><td>

review\_comments

</td><td>

Optional. Comments entered by the claims agent during the review and adjudication process.Data type: Translated Text

</td></tr><tr><td>

Service organization

</td><td>

service\_organization

</td><td>

Required. Name of the dealer or service organization associated with the repair claim.Data type: String

</td></tr><tr><td>

State

</td><td>

state

</td><td>

Required. Overall adjudication state of the Repair Claim case at the time of response.Possible values:

-   0 - Draft
-   1 - New
-   2 - Open
-   5 - Pending review
-   6 - Awaiting info
-   8 - Approved
-   9 - Partially approved
-   10 - Rejected
-   3 - Closed complete
-   7 - Closed incomplete
-   4 - Closed cancelled

Data type: Choice \(string\)

</td></tr><tr><td>

Total approved amount

</td><td>

total\_approved\_amount

</td><td>

Required. Total approved amount for the entire Repair Claim case, aggregated across all case lines.Data type: Currency

</td></tr></tbody>
</table>|Status|STAR status code|Decision indicator|
|------|----------------|------------------|
|AWAITING\_INFO|6|R \(Rejected\)|
|APPROVED|8|A \(Approved\)|
|PARTIALLY\_APROVED|9|A \(Approved\)|
|REJECTED|10|D \(Denied\)|

When these conditions are met, ServiceNow generates and sends a STAR `ProcessServiceProcessingAdvisory` message to the DMS. The outbound STAR message communicates claim adjudication outcomes, not claim submission data. The message includes:

-   The repair order or claim reference
-   Overall claim status
-   Total payable or approved amounts
-   Approved amounts at the individual job or operation level

The message conforms to the STAR `ProcessServiceProcessingAdvisory` structure and enables the DMS to synchronize claim status and financial reconciliation data.

Outbound sample payload:

```
<ns:ProcessServiceProcessingAdvisory
    xmlns:ns="http://www.starstandard.org/STAR/5"
    xmlns:ns1="http://www.openapplications.org/oagis/9"
    languageCode="en-US"
    releaseID="1.0"
    systemEnvironmentCode="Production"
    versionID="1.0">
    <ns:ApplicationArea>
        <ns:Sender>
            <ns:CreatorNameCode>Beta Consulting Group Orlando</ns:CreatorNameCode>
            <ns:SenderNameCode>DLR0001001</ns:SenderNameCode>
        </ns:Sender>
        <ns:CreationDateTime>2026-02-26T11:54:25</ns:CreationDateTime>
        <ns:Destination />
    </ns:ApplicationArea>
    <ns:ProcessServiceProcessingAdvisoryDataArea>
        <ns:Process />
        <ns:ServiceProcessingAdvisory>
            <ns:ServiceProcessingAdvisoryHeader>
                <ns:DocumentIdentificationGroup>
                    <ns:DocumentIdentification>
                        <ns:DocumentID>RO-2026-987654qwe1111</ns:DocumentID>
                    </ns:DocumentIdentification>
                </ns:DocumentIdentificationGroup>
                <ns:Payments>
                    <ns:RepairOrderReconciliation>
                        <ns:WarrantyClaimReconciliation>
                            <ns:ToBePaidAmount currencyID="INR">342744.29</ns:ToBePaidAmount>
                            <ns:ClaimStatusCode>Pending review</ns:ClaimStatusCode>
                            <ns:WarrantyNotes />
                            <ns:DispositionReason>
                                <ns:DispositionReasonCode />
                            </ns:DispositionReason>
                        </ns:WarrantyClaimReconciliation>
                        <ns:JobReconciliation>
                            <ns:ApprovedAmount currencyID="INR">342744.29</ns:ApprovedAmount>
                            <ns:ClaimStatusCode>Pending review</ns:ClaimStatusCode>
                            <ns:OperationID>DIAG-ENG-01A1A1</ns:OperationID>
                        </ns:JobReconciliation>
                        <ns:JobReconciliation>
                            <ns:ApprovedAmount currencyID="INR">0.00</ns:ApprovedAmount>
                            <ns:ClaimStatusCode>Pending review</ns:ClaimStatusCode>
                            <ns:OperationID>DIAG-ENG-011</ns:OperationID>
                        </ns:JobReconciliation>
                    </ns:RepairOrderReconciliation>
                </ns:Payments>
            </ns:ServiceProcessingAdvisoryHeader>
        </ns:ServiceProcessingAdvisory>
    </ns:ProcessServiceProcessingAdvisoryDataArea>
</ns:ProcessServiceProcessingAdvisory>
```

## Logging and diagnostics

Requests and responses are logged by the service for diagnostic and troubleshooting purposes in accordance with standard ServiceNow operational practices.

## Related specifications

-   STAR XML Specifications
-   SOAP 1.1 Specification
-   WSDL 1.1 Specification

Refer to the official STAR and W3C documentation for detailed schema and protocol definitions.

**Parent Topic:**[MCO Integration APIs](../integrate/manufacturing-integrate.md)

