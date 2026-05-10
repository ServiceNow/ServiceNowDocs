---
title: Expanded Model and Asset Classes
description: The Expanded Model and Asset Classes application adds model and asset classes that extend base classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, identifier entries, and dependent relationships. The application also adds model categories and API categories.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Enterprise Asset Management, IT Asset Management]
---

# Expanded Model and Asset Classes

The Expanded Model and Asset Classes application adds model and asset classes that extend base classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, identifier entries, and dependent relationships. The application also adds model categories and API categories.

**Note:** This application is compatible with the Rome and later family releases.

For more information on the CMDB, see [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_ITILConfigurationManagement.md).

In addition to extending CMDB model and asset classes, the Expanded Model and Asset Classes application creates model categories that associate model and asset classes with CMDB configuration item \(CI\) classes. The Enterprise Asset Management application uses these classes and model categories to create asset and model records that can be used to track and manage enterprise assets. Discovery tools, such as the ServiceNow® Discovery application, can also use these classes and model categories to create asset and model records for discovered CIs. See [Model categories](model-hierarchy.md) for more information on model categories.

The Expanded Model and Asset Classes application also adds the API and Managed API model categories, which allow the Configuration Management Database \(CMDB\) application to create and associate application models with API and Managed API CMDB CI classes. API CMDB CI classes provide classifications for APIs \(application programming interfaces\), which are sets of definitions and protocols that enable computer programs to communicate with each other. Managed API CMDB CI classes provide classifications for APIs that are discovered through gateways or management services, such as Amazon API Gateway. By associating application models with these CMDB CI classes, the Configuration Management Database \(CMDB\) application can create version-agnostic representations of your APIs. These representations can then provide a more holistic view of each API during reporting and analysis. For more information on API and Managed API CMDB CI classes, see [API extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-api.md).

## Enterprise model and asset classes added by the application

The Expanded Model and Asset Classes application adds enterprise model classes that extend the base Product model \[cmdb\_model\] class and enterprise asset classes that extend the Base asset \[alm\_base\] class. For more information on these enterprise model and asset classes, see [Enterprise model and asset classes](enterprise-model-asset-classes.md).

## Service model classes added by the application

The Expanded Model and Asset Classes application adds the following child classes to the base Service model \[cmdb\_service\_product\_model\] class. These child classes provide classifications for various service model types.

<table id="table_zvh_kvn_xyb"><thead><tr><th>

Service model child class

</th><th>

Role required for read access

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card service model\[sn\_ent\_card\_service\_model\]

</td><td>

sn\_ent.card\_service\_model\_viewer

</td><td>

Classifies service models that are based on card offerings from banks and financial institutions, such as credit cards and gift cards.

</td></tr><tr><td>

Deposit model\[sn\_ent\_deposit\_account\_model\]

</td><td>

sn\_ent.deposit\_account\_model\_viewer

</td><td>

Classifies service models that are based on deposit accounts offered by banks and financial institutions, such as savings and checking accounts.

</td></tr><tr><td>

Loan model\[sn\_ent\_loan\_account\_model\]

</td><td>

sn\_ent.loan\_account\_model\_viewer

</td><td>

Classifies service models that are based on loan options offered by banks and financial institutions, such as personal loans and mortgage loans.

</td></tr><tr><td>

Line of credit model\[sn\_ent\_line\_of\_credit\_model\]

</td><td>

sn\_ent.line\_of\_credit\_model\_viewer

</td><td>

Classifies service models that are based on lines of credit offered by banks and financial institutions, such as overdrafts on savings and checking accounts.

</td></tr><tr><td>

Financial service model\[sn\_ent\_financial\_services\_model\]

</td><td>

sn\_ent.financial\_services\_model\_viewer

</td><td>

Classifies service models that are based on financial services offered by banks and financial institutions, such as safe lockers and wire services.

</td></tr><tr><td>

Investment model\[sn\_ent\_investment\_model\]

</td><td>

sn\_ent.investment\_model\_viewer

</td><td>

Classifies service models that are based on wealth management options offered by banks and financial institutions, such as mutual funds and retirement planning.

</td></tr><tr><td>

Personal lines insurance product model\[sn\_ent\_b2c\_ins\_policy\_model\]

</td><td>

sn\_ent.b2c\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on personal lines insurance policies offered by insurance carriers, such as coverage and payment plans for personal auto insurance.

</td></tr><tr><td>

Commercial lines insurance product model\[sn\_ent\_b2b\_ins\_policy\_model\]

</td><td>

sn\_ent.b2b\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on commercial lines insurance policies offered by insurance carriers, such as coverage and payment plans for commercial property insurance.

</td></tr><tr><td>

Group life insurance product model\[sn\_ent\_group\_life\_ins\_policy\_model\]

</td><td>

sn\_ent.group\_life\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on group life insurance policies offered by insurance carriers, such as coverage and payment plans for group term life insurance.

</td></tr><tr><td>

Individual life product model\[sn\_ent\_indiv\_life\_ins\_policy\_model\]

</td><td>

sn\_ent.indiv\_life\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on individual life insurance policies offered by insurance carriers, such as coverage and payment plans for individual whole life insurance.

</td></tr><tr><td>

Medical insurance model \[sn\_ent\_medical\_insurance\_model\]

</td><td>

sn\_ent\_medical\_insurance\_model\_viewer

</td><td>

Classifies medical insurance models, including health insurance plans and government insurance programs such as Medicare or Medicaid.

</td></tr><tr><td>

Social benefit model\[sn\_ent\_social\_benefit\_model\]

</td><td>

sn\_ent.social\_benefit\_model\_viewer

</td><td>

Classifies service models that are based on social insurance programs and means-tested assistance programs, such as social security and the Supplemental Nutrition Assistance Program \(SNAP\).

</td></tr><tr><td>

Investigative service model\[sn\_ent\_investigative\_service\_model\]

</td><td>

N/A

</td><td>

Classifies service models that are based on the types of cases that government and private agencies investigate, such as fraud and assault.

</td></tr></tbody>
</table>## Contract model classes added by the application

<table id="table_y2z_wrg_zyb"><thead><tr><th>

Contract model class

</th><th>

Role required for read access

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Permit model\[sn\_ent\_permit\_model\]

</td><td>

contract\_manager

</td><td>

The Permit model is an extension of the Contract model table and is used to model licenses and permits that have been issued and entitles the recipients to perform certain activities or make use of specific resources.

</td></tr></tbody>
</table>## Firmware model and Discovered firmware model classes

The Expanded Model and Asset Classes application adds the Firmware model \[sn\_ent\_firmware\_model\] and Discovered firmware model \[sn\_ent\_discov\_firmware\_model\] classes. These firmware model class tables extend the tables that the CMDB CI Data Foundation application installs.

The Firmware installation \[cmdb\_firmware\_install\] table added with the CMDB CI class model application stores the installation records based on the firmware embedded into assets. Based on the records in the Firmware installation table, the Discovered firmware model and Firmware model tables store the details of the firmware.

## AI model classes added by the application

The Expanded Model and Asset Classes application adds the AI system component product model \[cmdb\_ai\_systems\_component\_product\_model\] class, which extends the Software component model \[cmdb\_sw\_component\_model\] class. The application also adds the AI content product model \[cmdb\_ai\_content\_product\_model\] class, which extends the Content product model \[cmdb\_content\_product\_model\] class. Both the Software component model \[cmdb\_sw\_component\_model\] class and Content product model \[cmdb\_content\_product\_model\] class extend the base Product model \[cmdb\_model\] class.

The AI system component product model \[cmdb\_ai\_systems\_component\_product\_model\] class classifies product models that are based on AI system components, such as machine learning, Natural Language Processing \(NLP\), and generative or agentic AI.

The AI content product model \[cmdb\_ai\_content\_product\_model\] class includes classifications for various AI content model types, which are categorized into the following child classes:

<table id="table_dps_shh_s2c"><thead><tr><th>

AI content product model child class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI model product model\[cmdb\_ai\_model\_product\_model\]

</td><td>

Classifies content models for the AI models that are used to generate AI system responses without any human intervention. Examples of AI models include Now LLM and GPT 3.5 Turbo.

</td></tr><tr><td>

AI dataset product model\[cmdb\_ai\_dataset\_product\_model\]

</td><td>

Classifies content models for the datasets that are used to train and test AI models. Examples of datasets include Wikipedia and Google Open Images.

</td></tr><tr><td>

AI prompt product model\[cmdb\_ai\_prompt\_product\_model\]

</td><td>

Classifies content models for the prompts, or instructions, that are given to AI models to generate AI system responses without any human intervention. Examples of prompts include sets of instructions to generate x-char summaries for given inputs in specific tones or voices.

</td></tr></tbody>
</table>## AI asset classes added by the application

The Expanded Model and Asset Classes application adds the AI digital asset \[alm\_ai\_digital\_asset\] class, which extends the Information asset \[alm\_information\_asset\] class. The Information asset \[alm\_information\_asset\] class extends the base Asset \[alm\_asset\] class. The AI digital asset \[alm\_ai\_digital\_asset\] class includes classifications for various AI asset types, which are categorized into the following child classes:

<table id="table_tmp_2kh_s2c"><thead><tr><th>

AI digital asset child class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI system digital asset\[alm\_ai\_system\_digital\_asset\]

</td><td>

Classifies the software artifacts that provide machine learning \(ML\) and AI capabilities for generating outputs, such as decisions, recommendations, content, and predictions. Examples include incident summarization and fraud detection capabilities.

</td></tr><tr><td>

AI model digital asset\[alm\_ai\_model\_digital\_asset\]

</td><td>

Classifies the AI models that are used to generate AI system responses without any human intervention. Examples include Now LLM and GPT 3.5 Turbo.

</td></tr><tr><td>

AI dataset digital asset\[alm\_ai\_dataset\_digital\_asset\]

</td><td>

Classifies the datasets that are used to train and test AI models. Examples include Wikipedia and Google Open Images.

</td></tr><tr><td>

AI prompt digital asset\[alm\_ai\_prompt\_digital\_asset\]

</td><td>

Classifies the prompts, or instructions, that are given to AI models to generate AI system responses without any human intervention. Examples include sets of instructions to generate x-char summaries for given inputs in specific tones or voices.

</td></tr></tbody>
</table>