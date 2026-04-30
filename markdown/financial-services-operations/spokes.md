---
title: Integrating with spokes
description: By integrating spokes with the Financial Services Operations \(FSO\) applications, flow designers can provide the actions within Workflow Studio for specific applications.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating applications, Financial Services Operations \(FSO\)]
---

# Integrating with spokes

By integrating spokes with the Financial Services Operations \(FSO\) applications, flow designers can provide the actions within Workflow Studio for specific applications.

A spoke is a scoped application containing Workflow Studio content dedicated to a particular application or record type. You can integrate a ServiceNow application with a FSO banking application spoke such as Jack Henry jXchange Socure, or FRISS.

|Plugin name|Description|Plugin directory|
|-----------|-----------|----------------|
|[Equifax Spoke](https://www.servicenow.com/docs/access?context=equifax-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|By using the Equifax spoke integration, you can access important information about the credit history for a customer, fraud alerts, digital identity verification, transaction screening, and other relevant data.|\[com.sn\_equifax\_spoke\]|
|[Ethoca spoke](https://www.servicenow.com/docs/access?context=ethoca-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|By using the Ethoca spoke integration, you can access detailed merchant information and subscription control, view digital receipts, and manage their disputes.|\[com.sn\_ethoca\_spoke\]|
|[Jack Henry jXchange Spoke](https://www.servicenow.com/docs/access?context=jha-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|Flow designers can use the Jack Henry jXchange spoke to access the actions to automate the financial processes within ServiceNow. You can use this integration to do tasks such as account management, transaction processing, or fraud detection.|\[com.sn.jha.spoke\]|
|[Socure Spoke](https://www.servicenow.com/docs/access?context=socure-fso&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|By using the Socure spoke integration, you can improve your customer onboarding, authentication processes and for identity verification tasks. Flow designers can incorporate these identity verification processes into their workflows. Tasks include validating user information, performing risk assessments, or preventing fraudulent activities.|\[com.sn\_socure\_spoke\]|
|[Mastercard Spoke](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|By using the Mastercard spoke integration, you can perform tasks such as searching transactions, creating claims, and processing chargebacks.|\[com.sn\_mastercard\_spoke\]|
|[Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|Dispute agents can use the [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) to seamlessly invoke Visa APIs under Visa Resolve Online \(VROL\) for Visa card dispute process.|\[com.sn\_visa\_spoke\]|
|[Verifi Spoke](https://www.servicenow.com/docs/access?context=verifi-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|Dispute agents can use the [Verifi Spoke](https://www.servicenow.com/docs/access?context=verifi-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) to resolve disputes at the pre-dispute stage, prevent formal disputes and costly chargebacks, and manage the dispute resolution process more effectively and efficiently.|\[com.sn\_verifi\_spoke\]|

|Spoke|Description|Plugin|
|-----|-----------|------|
|[FRISS Spoke](https://www.servicenow.com/docs/access?context=friss-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|The FRISS spoke enables insurance companies to enhance their fraud prevention measures and protect their organizations from financial losses. It provides the actions that are designed for fraud prevention and risk assessment tasks. Flow designers can incorporate the fraud detection processes into their workflows by using actions. Actions include analyzing the customer data, identifying suspicious activities, and generating fraud alerts.|\[com.sn\_friss\_spoke\]|
|[Guidewire Spoke](https://www.servicenow.com/docs/access?context=guidewire-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|The Guidewire spoke integration provides actions within Workflow Studio for managing insurance-related tasks. The spoke actions include creating policies, updating claims information, and retrieving billing data.|\[com.sn\_guidewire\_spoke\]|

**Parent Topic:**[Integrate applications](fso-integrate-other-applications.md)

