---
title: Create New Excel download/upload request form
description: Use the Create New Excel download/upload request form to capture all the information that you need to create a download/upload request for Digital resilience third-party registers using the Third-party Risk Management application. As a third-party risk manager or third-party risk assessor you can create an Excel download/upload request record.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a Microsoft Excel download request, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create New Excel download/upload request form

Use the Create New Excel download/upload request form to capture all the information that you need to create a download/upload request for Digital resilience third-party registers using the Third-party Risk Management application. As a third-party risk manager or third-party risk assessor you can create an Excel download/upload request record.

<table id="table_aqy_k2x_rvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the request. For example, legal\_entity\_template.

</td></tr><tr><td>

Type

</td><td>

Types of download request. The choices are as follows:-   **Excel master template**
-   **Plain-csv reporting package**
-   **Assessments**
-   **Branches**
-   **Contracts**
-   **Functions**
-   **Legal entities**
-   **Supply chains**
-   **Third parties**
-   **Third-party engagements**

</td></tr><tr><td>

Number

</td><td>

Number of the request. This field is auto-filled.

</td></tr><tr><td>

Request type

</td><td>

Type of the request. The choices are as follows:-   **Upload**
-   **Download**

</td></tr><tr><td>

State

</td><td>

State of the record. This field is auto-filled to **Draft** state.

</td></tr><tr><td class="sub-head" colspan="2">

Entity maintaining the register of info

</td></tr><tr><td colspan="2">

**Note:** These fields, including options for currency conversion and third‑party total expense aggregation, appear when you select **Excel master template** or **Plain‑CSV reporting package** as the **Type**.

</td></tr><tr><td>

LEI of the entity maintaining the register of information

</td><td>

Entity maintaining and updating the register of information using the LEI, 20-character, alpha-numeric code based on the ISO 17442 standard.

</td></tr><tr><td>

Name of entity

</td><td>

Legal name of the entity that maintains and updates the register of information.

</td></tr><tr><td>

Country of entity

</td><td>

Country where the license or the registration of the entity, as listed in the information register, was issued.

</td></tr><tr><td>

Type of entity

</td><td>

Types of the entity. The options include the following:-   **Credit institutions**
-   **Investment firms**
-   **Central counterparties \(CCPs\)**
-   **Asset management companies**
-   **Account information service providers**
-   **Electronic money institutions**
-   **Crypto-asset service providers**
-   **Central security depository**
-   **Trading venues**
-   **Trade repositories**
-   **Payment institution**
-   **Other financial entity**
-   **Securitization repository**
-   **Crowdfunding service providers**
-   **Administrator of critical benchmarks**
-   **Credit rating agency**
-   **Institutions for occupational retirement provision**
-   **Insurance intermediaries, reinsurance intermediaries and ancillary insurance intermediaries**
-   **Insurance and reinsurance undertakings**
-   **Data reporting service providers**
-   **Managers of alternative investment funds**
-   **Non-financial entity: Other than ICT intra-group service provider**
-   **Non-financial entity: ICT intra-group service provider**
-   **Issuers of asset-referenced tokens**

</td></tr><tr><td>

Competent authority

</td><td>

The competent authority according to Article 46 of Regulation \(EU\) 2022/2554 to which the register of information is reported.

</td></tr><tr><td>

Date of reporting

</td><td>

The ISO 8601 \(yyyy-mm-dd\) code of the date of reporting

</td></tr><tr><td>

Enable currency conversion

</td><td>

Option to convert each contract’s annual expense into a single base currency using historical exchange rates from the European Central Bank \(ECB\).**Note:** The Reference Date on the report determines the exchange rate used. Converted amounts appear only in the generated package; source records are unchanged.

For more information, see [Currency conversion and third-party total expense aggregation](../concept/tprm-dora-currency-aggregation.md)

</td></tr><tr><td>

Enable third‑party total expense aggregation

</td><td>

Option to aggregate annual expenses across all contracts belonging to the same third‑party provider or third‑party engagement.**Note:** Aggregation only happens if all eligibility rules are met: All contracts for the provider must meet provider eligibility criteria \(for example, single‑provider contracts and currency alignment\). If currency conversion is not enabled, all contracts must already be in base currency. If currency conversion is enabled, all conversions must succeed.

For more information, see [Currency conversion and third-party total expense aggregation](../concept/tprm-dora-currency-aggregation.md)

</td></tr><tr><td>

Base currency

</td><td>

Currency used for reporting monetary values in the report.For example, US Dollar or Euro.

**Note:** Before downloading the register of information, you must specify your reporting currency. The system then displays available currencies based on administrator-configured exchange rates.

</td></tr><tr><td>

Report type

</td><td>

Specifies whether the report covers a single entity **Individual** or a **Consolidated** group of entities.

</td></tr></tbody>
</table>