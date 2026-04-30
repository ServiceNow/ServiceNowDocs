---
title: Visa Spoke
description: Integrate the ServiceNow instance with the Visa spoke to invoke Visa Resolve Online \(VROL\) APIs for Visa card dispute process and card-on-file payments using Visa Stop Payment Service \(VSPS\).
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 19
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Visa Spoke

Integrate the ServiceNow instance with the Visa spoke to invoke Visa Resolve Online \(VROL\) APIs for Visa card dispute process and card-on-file payments using Visa Stop Payment Service \(VSPS\).

## Subscription information

This spoke requires a subscription. Contact your account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Spoke version

Visa spoke v2.0.1 is the latest version.

## Key features

The feature includes creating actions to invoke Visa APIs through VROL and VSPS to manage the entire card dispute process and card-on-file payments, including tasks such as:

-   Retrieve enriched transaction information
-   Perform transaction searches
-   Initiate the creation of dispute cases
-   Submit Visa questionnaire
-   Initiate pre-arbitration and arbitration on existing dispute cases

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Visa spoke provides actions to invoke Visa APIs under VROL and VSPS to manage the entire card dispute process. Available actions include:

-   **Actions with sensitive information** - These actions contain sensitive information in the request and response body. You should use a Tokenization solution when invoking these VROL and VSPS APIs.

    **Important:** You should disable flow execution logs for Visa APIs that contain Personally Identifiable Information \(PII\) data. To do this, set the property **com.snc.process\_flow.reporting.level** in System Properties to OFF.

    |Category|Action|Description|
    |--------|------|-----------|
    |Visa Stop Payment Service|Cancel Multiple Stop Instructions Request Builder|Constructs the request payload for the Cancel API, enabling clients to cancel multiple stop instructions.|
    |Cancel Multiple Stop Instructions Response Parser|Parses the response of the Cancel API, which can be used to cancel multiple stop instructions.|
    |Create Stop Payment Instruction by Merchant Identifier Request Builder|Builds the request payload for the API that adds one or more merchant-level stop instructions, accepting a duration, merchant identifiers, PAN, and a start date, along with optional parameters.|
    |Create Stop Payment Instruction by Merchant Identifier Response Parser|Parses the response of the added merchant API, which issuers or acquirers can use to add one or more merchant-level stop instructions.|
    |Create Stop Payment Instruction by PAN Request Builder|Adds a PAN-level stop instruction for a specified duration and start date, with optional additional notes and payment frequency.|
    |Create Stop Payment Instruction by PAN Response Parser|Parses the response of the Add PAN Stop Instruction API, which enables issuers to place a stop instruction on a given PAN for a specified duration and start date.|
    |Create Stop Payment Instructions by Merchant Category Code Request Builder|Builds the request payload for the API that creates stop payment instructions based on merchant category codes \(MCC\), accepting PAN, start date, duration, merchant category codes, and optional additional details.|
    |Create Stop Payment Instructions by Merchant Category Code Response Parser|Parses the response of the create stop payment instruction by merchant category code API. This action can be used to verify the status and details of stop instructions processed based on merchant category codes.|
    |Look up All Linked Stop Payment Instructions by Stop Instruction ID Request Builder|Builds the request payload for the API that finds all stop instruction details linked to a given stop instruction, accepting a stop instruction ID and search type.|
    |Look up All Linked Stop Payment Instructions by Stop Instruction ID Response Parser|Parses the response of the linked API. Issuers or acquirers can use this API to find all stop instruction details linked to a given stop instruction.|
    |Look up Eligible Transactions for Stop Payment by PAN and Date Range Request Builder|Builds the request payload for the API that retrieves eligible transactions. This action accepts a PAN, a date range, a start date, and an optional filter for recurring and installment transactions.|
    |Look up Eligible Transactions for Stop Payment by PAN and Date Range Response Parser|Parses the response of the eligible transactions API. This action can be used to get a list of transactions that are eligible for placing a stop instruction based on a given PAN and date range.|
    |Look up Stop Instruction Details by Stop Instruction ID Request Builder|Constructs the request payload for the Retrieve API, which fetches stop instruction details using a provided stop instruction ID.|
    |Look up Stop Instruction Details by Stop Instruction ID Response Parser|Parses the response from the Retrieve API, which can be used to fetch stop instruction details based on the stop instruction ID.|
    |Look up Stop Payment Instructions by PAN Request Builder|Retrieves stop payment instructions associated with a given PAN, enabling you to search for both active and inactive instructions based on the provided parameters.|
    |Look up Stop Payment Instructions by PAN Response Parser|Parses the response received from the Lookup Stop Payment Instructions by PAN API.|
    |Look up Stopped Transactions by PAN Request Builder|Builds the request payload for the Stopped Transactions by PAN API, which enables clients to retrieve stopped transactions by PAN.|
    |Look up Stopped Transactions by PAN Response Parser|Parses the response of the Stopped Transactions by PAN API, which can be used to retrieve stopped transactions by PAN.|
    |Look up Stopped Transactions by Stop Instruction ID Request Builder|Builds the request payload for the API that enables you to retrieve a list of stopped transactions using a stop instruction ID.|
    |Look up Stopped Transactions by Stop Instruction ID Response Parser|Parses the response of the stopped transactions by stop ID API, which enables you to retrieve a list of stopped transactions using a stop instruction ID.s|
    |Update Stop Instructions Duration by Stop Instruction ID Request Builder|Builds the request payload for the API that extends the end date of multiple stop instructions. It accepts an array of stop instruction IDs and their corresponding durations.|
    |Update Stop Instructions Duration by Stop Instruction ID Response Parser|Parses the response of the extended API, which enables issuers or acquirers to extend the end date of multiple stop instructions.|
    |Update Stop Payment Instruction by Merchant Category Code Request Builder|Builds the request payload for the Update MCC API, which enables you to modify an existing stop instruction based on a Merchant Category Code \(MCC\).|
    |Update Stop Payment Instruction by Merchant Category Code Response Parser|Parses the response of the Update MCC API, which enables you to modify an existing stop instruction based on a Merchant Category Code \(MCC\).|
    |Update Stop Payment Instruction by Merchant Identifier Request Builder|Builds the request payload for the Update Merchant API, which updates a merchant-level stop instruction.|
    |Update Stop Payment Instruction by Merchant Identifier Response Parser|Parses the response of the Update Merchant API, which can be used to update a merchant-level stop instruction.|

    |Category|Action|Description|
    |--------|------|-----------|
    |Order Insight Digital Management|Card Holder Purchase Inquiry Request Builder|Produces request payload for CardholderPurchaseInquiry. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to request additional merchant information regarding a transaction. It can also be used to retrieve purchase information for non-VisaNet transactions.|
    |Card Holder Purchase Inquiry Response Parser|Parses response of CardholderPurchaseInquiry. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to request additional merchant information regarding a transaction. It can also be used to retrieve purchase information for non-VisaNet transactions.|
    |Transaction Inquiry Management|Look up All Transaction Details Request Builder|Enables you to retrieve details of all the scheduled reports for the organization or for a particular report that you want to know.|
    |Look up All Transaction Details Response Parser|Parses response of getAllTransDetails. Issuers can use this API an alternative method to retrieve complete Transaction Details for transactions using 1–10 VisaNet Transaction IDs as the search parameters.|
    |Look up Transaction Details from Case Request Builder|Produces request payload for the getTransactionsFromCase. Issuers can use this API to get the TI details for the selected transaction in the case. That is, the original transaction being is disputed. Also, it returns summaries for the selected and non-selected transactions returned from the TI search that are also stored with the case.|
    |Look up Transaction Details from Case Response Parser|Parses response of getTransactionsFromCase. Issuers can use this API to get the TI details for the selected transaction in the case. That is, the original transaction is disputed. Also, it returns summaries for the selected and non-selected transactions returned from the TI search that are also stored with the case.|
    |Look up Transaction Details Request Builder|Produces request payload for the getTransDetails. Issuers can use this API to get detail-level data for the returned transaction.|
    |Look up Transaction Details Response Parser|Parses response of getTransDetails. Issuers can use this API to get detail-level data for the returned transaction.|
    |Look up Transaction Inquiry Results Request Builder|Produces request payload for the getTransInquiryResults. This will accepts a Transaction Inquiry \(TI\) Event ID and returns transaction summary information.|
    |Look up Transaction Inquiry Results Response Parser|Parses response of the getTransInquiryResults. This will accepts a Transaction Inquiry \(TI\) Event ID and returns transaction summary information.|
    |Submit Multiple Transaction Inquiry Request Builder|Produces request payload for the submitMultiTranInquiry. This will provides an alternative method to search for transactions using 1–10 VisaNet Transaction IDs as the search parameters.|
    |Submit Multiple Transaction Inquiry Response Parser|Parses response of the submitMultiTranInquiry. This will provides an alternative method to search for transactions using 1–10 VisaNet Transaction IDs as the search parameters.|
    |Submit Transaction Inquiry Request Builder|Produces request payload for the submitTranInquiry. This action i used to search for transactions using a set of search criteria.|
    |Submit Transaction Inquiry Response Parser|Produces request payload for the submitTranInquiry. This action is used to search for transactions using a set of search criteria.|
    |Fraud Report Management|Submit Fraud Report Request Builder|Produces request payload for SubmitFraudReport. This API enables you to submit a fraud report to Visa Resolve Online \(VROL\), including all the required fraud data as listed in the Interface Element Spreadsheet \(IES\).|
    |Submit Fraud Report Response Parser|Parses response for SubmitFraudReport. This API enables you to submit a fraud report to Visa Resolve Online \(VROL\), including all the required fraud data as listed in the Interface Element Spreadsheet \(IES\).|
    |Look up Dispute Filing Details Request Builder|This action builds the input payload for the API getDisputeFiling Details.|
    |Look up Dispute Filing Details Response Parser|Parses response of the getDisputeFilingDetails. The getDisputeFilingDetails are used to retrieve message with dispute case filing and the image details along with dispute filing item type.|
    |Look up Fraud Report Details Request Builder|Enables you to request additional information regarding a previously submitted fraud report in a real time.|
    |Look up Fraud Report Details Response Parser|This action parses the response body returned by VROL system after calling the API get fraud report details.|
    |Dispute Financials Management|Look up Dispute Financial Advice Details Request Builder|Produces request payload for the GetDisputeFinancialAdviceDetails API. It enables Real-Time Systems Interface \(RTSI\) users to request the dispute financial advice data.|
    |Look up Dispute Financial Advice Details Response Parser|Parses response of the GetDisputeFinancialAdviceDetails API. It enables Real-Time Systems Interface \(RTSI\) users to request the dispute financial advice data.|
    |Look up Dispute Financial Details Request Builder|Produces request payload for the GetDisputeFinancialDetails API. This API retrieves disputed financial details in a case for acquirer or issuer.|
    |Look up Dispute Financial Details Response Parser|Parses response of the GetDisputeFinancialDetails API. This API retrieves dispute financial details in a case for acquirer or issuer.|
    |Case Management|Submit Manual Case Creation Request Builder|Parses response for SubmitFraudReport. This API enables you to submit a fraud report to Visa Resolve Online \(VROL\), including all the required fraud data as listed in the Interface Element Spreadsheet \(IES\).|
    |Submit Manual Case Creation Response Parser|Produces request payload for the SubmitManualCaseCreation API. It enables a user to create a case without any transactions.|
    |Look up Case Details Request Builder|Produces request payload for GetCaseDetails. This API enables a user to request details of a specific VROL case, including transaction information, dispute jurisdiction, case type, and other case-related fields, when supplying the VisaCaseNumber and MemberRole. The information returned in the response depends on the role of the user making the request, and what stage and state the case is in|
    |Look up Case Details Response Parser|Parses response for GetCaseDetails. This API enables a user to request details of a specific VROL case, including transaction information, dispute jurisdiction, case type, and other case-related fields, when supplying the VisaCaseNumber and MemberRole. The information returned in the response depends on the role of the user making the request, and what stage and state the case is in.|
    |Questionnaire Management|Look up Acceptance Notification Details Request Builder|Produces request payload for GetAcceptanceNotificationDetails. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to retrieve the acceptance notification details for disputes or dispute responses that were accepted and closed.|
    |Look up Acceptance Notification Details Response Parser|Parses response of GetAcceptanceNotificationDetails. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to retrieve the acceptance notification details for disputes or dispute responses that were accepted and closed.|
    |Look up Dispute Details Request Builder|Produces request payload for the getDisputeDetails. Issuers can use this API to request for the dispute questionnaire data to be returned in image format, as well as in XML.|
    |Look up Dispute Details Response Parser|Parses response of getDisputeDetails. Issuers can use this API to request for the dispute questionnaire data to be returned in image format, as well as in XML.|
    |Look up Dispute Response Details Request Builder|Produces request payload for GetDisputePreArbResponseDetails. This API enables Real-Time Systems Interface \(RTSI\) users to request for the Pre-Arbitration Response questionnaire data to be returned in image format, as well as in XML|
    |Look up Dispute Response Details Response Parser|Produces request payload for GetDisputePreArbResponseDetails. This API enables Real-Time Systems Interface \(RTSI\) users to request for the Pre-Arbitration Response questionnaire data to be returned in image format, as well as in XML.|
    |Queues Management|Look up Queue Request Builder|Produces request payload for GetQueue API. This API obtains information on any specified queue during the lifecycle of dispute such as incoming collaboration queue, and rejected dispute forms.|
    |Look up Queue Response Parser|Parses response of the GetQueue API. This API obtains information on any specified queue during the lifecycle of dispute such as incoming collaboration queue, and rejected dispute forms.|
    |Case Filing Management|Look up Contact Message Details Request Builder|Produces request payload for GetContactMessageDetails. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to request for the contact message questionnaire data to be returned in image format, as well as in XML.|
    |Look up Contact Message Details Response Parser|Parses response of GetContactMessageDetails. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to request for the contact message questionnaire data to be returned in image format, as well as in XML. The returned image is in TIFF or PDF format. To retrieve the dispute as an image, you must set &lt;IncludeDisputeAsImageInd&gt;=true.|
    |Look up Contact Message Response Details Request Builder|Produces request payload for the getContactMessageResponseDetails. This action enables Real-Time Systems Interface \(RTSI\) users to retrieve the details of a contact message response.|
    |Look up Contact Message Response Details Response Parser|Parses response of the getContactMessageResponseDetails. This action enables Real-Time Systems Interface \(RTSI\) users to retrieve the details of a contact message response.|
    |Hypersearch Request Management|Hypersearch Request Builder|Produces request payload for HyperSearch. This API accepts case matching parameters and returns information about all the cases found.|
    |Hypersearch Response Parser|Parses response of HyperSearch. This API accepts case matching parameters and returns information about all the cases found.|
    |Batch Queues Management|Look up Batch Queue Request Builder|Produces request payload for GetBatchQueue API. This API retrieves transactions from given RTSI Batch Queue.|
    |Look up Batch Queue Response Parser|Parses response of the GetBatchQueue API. This API retrieves transactions from given RTSI Batch Queue.|
    |Batch Queues Management|Look up Batch Queue Request Builder|Produces request payload for GetBatchQueue API. This API retrieves transactions from given RTSI Batch Queue.|
    |Look up Batch Queue Response Parser|Parses response of the GetBatchQueue API. This API retrieves transactions from given RTSI Batch Queue.|
    |Dispute Pre-Arbitration Management|Look up Dispute Pre Arbitration Response Details Request Builder|Parses response for GetDisputePreArbResponseDetails. This API enables Real-Time Systems Interface \(RTSI\) users to request for the Pre-Arbitration Response questionnaire data to be returned in image format, as well as in XML. The returned image is in TIFF or PDF format. To retrieve the dispute as an image, you must set &lt;IncludeDisputeAsImageInd&gt;=true. The image data is returned in the &lt;Image&gt; group in the SIGetDisputePreArbResponseDetailsResponse|
    |Look up Dispute Pre Arbitration Response Details Response Parser|Produces request payload for GetDisputePreArbResponseDetails. This API enables Real-Time Systems Interface \(RTSI\) users to request for the Pre-Arbitration Response questionnaire data to be returned in image format, as well as in XML.|
    |Look up Dispute Pre Arbitration Details Request Builder|Produces request payload for the GetDisputePreArbDetails API. To request for the Pre-Arbitration questionnaire data to be returned in image format, as well as in XML|
    |Look up Dispute Pre Arbitration Details Response Parser|Parses response of the GetDisputePreArbDetails API. To request for the Pre-Arbitration questionnaire data to be returned in image format, as well as in XML.|
    |Exception File Listing Management|Look up Inquiry Exception Request Builder|This action builds the request payload for the API that inquires about exception.|
    |Look up Inquiry Exception Response Parser|This action parses the response body returned by VROL system after calling the API Look up Inquiry Exception.|
    |Look up Exception Details Request Builder|This action builds the request payload for the API getExceptionDetails.|
    |Look up Exception Details Response Parser|This action parses the response body returned by VROL system after calling the getExceptionDetails API.|
    |Submit Exception Request Builder|Produces request payload for the submitException. Issuers can use submitExceptionRequest to add, update, or delete an exception file listing from a new or existing case. It’s also used to repair a rejected exception file listing.|
    |Submit Exception Response Parser|Parses response of the submitException. Issuers can use submitExceptionRequest to add, update, or delete an exception file listing from a new or existing case. It’s also used to repair a rejected exception file listing.|
    |Miscellaneous Fees Management|Look up Miscellaneous Fee Details Request Builder|Produces request payload for the getMiscFeeDetails. GetMiscFeeDetailsRequest enables clients to request details for a miscellaneous fee.|
    |Look up Miscellaneous Fee Details Response Parser|Parses response of the getMiscFeeDetailsRequest. GetMiscFeeDetailsRequest enables clients to request details for a miscellaneous fee.|
    |Submit Miscellaneous Fee Request Builder|Produces request payload for the SubmitMiscFee API. It enables clients to request a miscellaneous fee with data.|
    |Submit Miscellaneous Fee Response Parser|Parses response of the SubmitMiscFee API. It enables clients to request a miscellaneous fee with data.|
    |Fraud Monitoring Program Management|Look up GMFP Details Request Builder|This action builds the request payload for the API GetGMFPDetails|
    |Look up GMFP Details Response Parser|This action parses the response body returned by VROL system after calling the GMFP Details API.|

-   **Actions with non-sensitive information** - You can directly invoke these Visa APIs from your ServiceNow instance.

    |Category|Action|Description|
    |--------|------|-----------|
    |Dispute Financials Management|Initiate Dispute from Transaction or Case|Enables you to initiate dispute from transaction or case.|
    |Change Dispute Status|Parses response of CardholderPurchaseInquiry. This API provides Real-Time Systems Interface \(RTSI\) users with the capability to request additional merchant information regarding a transaction. It can also be used to retrieve purchase information for non-VisaNet transactions|
    |Case Management|Look up Image|Retrieves an image added to a newly created case.|
    |Upload Image|UploadImage is used to add an image to a case.|
    |Download and Attach Image|Downloads and attaches a Visa case image to a ServiceNow record.|
    |Update Case Resolution Status|Enables you to update the case resolution status of a case. This may close the case, depending on the status change made.|
    |Create Case from Transaction|Issuers use this API to create a case from a Transaction Inquiry request.|
    |Questionnaire Management|Submit Dispute Questionnaire|This action enables Real-Time Systems Interface \(RTSI\) users to submit or save the dispute questionnaire.|
    |Look up Fraud Bundle Dispute Questionnaire Status|Provides Real-Time Systems Interface \(RTSI\) users with the capability to retrieve details of a submitted fraud bundle dispute.|
    |Submit Fraud Bundle Dispute Questionnaire|Provides Real-Time Systems Interface \(RTSI\) users with the capability to submit or save the fraud bundle dispute questionnaire. This request can include images.|
    |Batch Queues Management|Mark Batch Queue Item as Read|Marks transactions as read to remove them from the Real-Time Systems Interface \(RTSI\) Batch Queue.|
    |Queues Management|Ignore GMFP|Enables the issuer to change the status of the VFMP transaction to 'Ignored' by sending a request using the GMFPItemID, once they’ve reviewed each Visa Fraud Monitoring Program \(VFMP\) transaction in the queue.|
    |Close Miscellaneous Fee|Provides the functionality to remove miscellaneous fee transactions.|
    |Close Message|Provides the functionality to remove Request Proof of Posting \(RPP\) message transactions.|
    |Accept Dispute|Accepts the dispute liability or accepts the other side's decision, and removes the dispute transaction from the queue.|
    |Transaction Inquiry Management|Close Transaction|This action is used to close certain transactions and remove them from their respective queues.|
    |Select Associated Transactions|AssociatedTranSelection enables you to confirm or refute the associations of some or all of the associated transactions within a group to a selected transaction in a case.|
    |Look up Associated Transaction List|Enables you to retrieve a list of associated transactions by supplying the associated transaction group ID.|
    |Look up Associated Transaction Selection|Enables you to confirm or refute the associations of some or all of the associated transactions within a group to a selected transaction in a case.|
    |Dispute Pre-Arbitration Management|Create Dispute Pre Arbitration|Initiates the creation of a Pre-Arbitration using this API.|
    |Create Dispute Pre Arbitration Response|Provides Real-Time Systems Interface \(RTSI\) users with the capability to respond to a Pre-Arbitration.|
    |Case Filing Management|Submit Contact Message Response|SubmitContactMessageResponse enables Real-Time Systems Interface \(RTSI\) users to submit a response to a contact message.|
    |Submit Dispute Filing|Submit a dispute case filing request, withdrawal, or appeal.|
    |Report Distribution Management|Look up Report Output|Enables you to retrieve the report for a particular run date in CSV format.|
    |Look up Active Schedule|Enables you to retrieve details of all the scheduled reports for your organization or for a particular report that the user wants to know.|
    |Batch Queue Management|Mark Batch Queue Item as Read|Marks transactions as read to remove them from the Real-Time Systems Interface \(RTSI\) Batch Queue.|


## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For more information about setting up the spoke, see [Set up Visa Spoke](../task/set-up-visa-spoke.md#).

