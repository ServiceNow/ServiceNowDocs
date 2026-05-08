---
title: Default NER data patterns
description: Use Named Entity Recognition \(NER\) based discovery to help discover sensitive data that does not follow fixed patterns.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Configure patterns, Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Default NER data patterns

Use Named Entity Recognition \(NER\) based discovery to help discover sensitive data that does not follow fixed patterns.

Several Data Privacy capabilities support using Named Entity Recognition \(NER\) model data patterns to discover data such as names, organizations, nationalities, and political affiliations. Data patterns with the type Model use this feature \(see [Configure Data Discovery patterns](../task/configure-data-discovery-patterns.md) for more details\).

**Warning:** This feature requires an additional $0 SKU to be signed by the customer in order to be enabled. Also, customers must have the latest version of the GenAI Controller `sn.generative.ai` installed on their instance \(which requires the admin role\).

NER data patterns can be used for:

-   Running Data Discovery jobs using [Data Discovery policies](../concept/data-discovery-policies.md).
-   Running Anonymization jobs using [Data Anonymization Policies](../../data-privacy-store/concept/dps-data-anonymization.md).

    **Note:** To anonymize any NER data pattern within text in a classified column, you need to select the Data Pattern Anonymization technique when creating the anonymization policy. Then, ensure that each NER data pattern is added to [Active Data Patterns](../task/dds-active-data-patterns.md).

-   [Real time anonymization](../../data-privacy-store/concept/real-time-anonymization.md) of entries containing NER data patterns.

    **Note:** This capability requires adding the NER data pattern to [Active Data Patterns](../task/dds-active-data-patterns.md).

-   Masking NER data patterns when configuring [Data Privacy for Now Assist](../concept/now-assist-for-data-privacy-landing.md).

<table id="table_wfd_1ll_gxb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Named Entity Recognition

</th><th>

Keywords

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Address

</td><td>

A full or partial location identifier, including street names, unit / plot numbers, but excludes city, state, country and zip code.

</td><td>

ADDRESS

</td><td>

 

</td><td>

-   **Matching**
    -   135 Roslea Rd Hayward
    -   \[135, Roslea Rd\]
-   **Non matching**
    -   New York, NY
    -   Apt. 11

</td></tr><tr><td>

City

</td><td>

The name of a city or town from regions and countries around the world.

</td><td>

CITY

</td><td>

 

</td><td>

-   **Matching**
    -   Hayward
    -   Cleburne
-   **Non matching**
    -   Switzerland
    -   87591

</td></tr><tr><td>

Country

</td><td>

The name of a sovereign nation or territory.

</td><td>

COUNTRY

</td><td>

 

</td><td>

-   **Matching**
    -   USA
    -   India
-   **Non matching**
    -   U-S-A
    -   U.S.A.

</td></tr><tr><td>

Date &amp; Time

</td><td>

Absolute or relative dates or periods or times smaller than a day.

</td><td>

DATE\_TIME

</td><td>

 

</td><td>

-   **Matching**
    -   22-07-1992
    -   22/07/1992
    -   07/22/1992
    -   07-22-1992
    -   07 12 1992
-   **Non matching**

55 II IOO5


</td></tr><tr><td>

Job position

</td><td>

A specific role or set of responsibilities within an organization, designated to be filled by an employee.

</td><td>

JOB\_POSITION

</td><td>

 

</td><td>

-   **Matching**
    -   senior software engineer
    -   Director
    -   CSR
    -   Lecturer
-   **Non matching**

sr software engineer


</td></tr><tr><td>

Location

</td><td>

Name of politically or geographically defined location \(cities, provinces, countries, international regions, bodies of water, mountains

</td><td>

LOCATION

</td><td>

 

</td><td>

-   **Matching**
    -   Himalayas
    -   Great Lakes
    -   Mount Rainier
-   **Non matching**
    -   Bay Of Bengal
    -   The south

</td></tr><tr><td>

Nationality, religious or political groups \(NRPs\)

</td><td>

A person's nationality, religious or political group.

</td><td>

NRP

</td><td>

 

</td><td>

-   **Matching**
    -   American
    -   Indian
    -   Indo-american
-   **Non matching**
    -   Bald
    -   Handsome

</td></tr><tr><td>

Organization

</td><td>

Name of organization.

</td><td>

ORGANIZATION

</td><td>

 

</td><td>

-   **Matching**

Abraham &amp; Lincoln co.

-   **Non matching**

Now india co


</td></tr><tr><td>

Person

</td><td>

A full person name, which can include first names, middle names or initials, and last names.

</td><td>

PERSON

</td><td>

Fred Luddy, Abel Tuter, Abraham Lincoln

</td><td>

-   **Matching**
    -   Fred Luddy
    -   Abel Tuter
    -   Abraham Lincoln
-   **Non matching**
    -   Fred
    -   Toyota

</td></tr><tr><td>

Salary

</td><td>

A numeric value representing an individual's earnings, often accompanied by currency symbols.

</td><td>

SALARY

</td><td>

 

</td><td>

-   **Matching**

my salary is $500, my salary is ₹500, my pay is 1.234,56 €

-   **Non matching**

40/hour


</td></tr><tr><td>

State

</td><td>

States, Provinces, Prefectures and regions around the world.

</td><td>

STATE

</td><td>

 

</td><td>

-   **Matching**
    -   CA
    -   IN
-   **Non matching**
    -   Australia
    -   Pacific Northwest

</td></tr></tbody>
</table>