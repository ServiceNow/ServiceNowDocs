---
title: Default data patterns
description: Review the default data pattern regular expressions included in Data Discovery. These default data patterns can be used to filter table entries for further classification.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure patterns, Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Default data patterns

Review the default data pattern regular expressions included in Data Discovery. These default data patterns can be used to filter table entries for further classification.

Data Discovery supports using a Named Entity Recognition \(NER\) model to discover data, such as names, organizations, nationalities, and political affiliations. Data patterns with the type **Model** use this feature.

The following table details the default patterns for data discovery.

<table id="table_wfd_1ll_gxb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Regular Expression

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
    -   55 II IOO5

</td></tr><tr><td>

Job position

</td><td>

A specific role or set of responsibilities within an organization, designated to be filled by an employee.

</td><td>

 

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

 

</td><td>

ORGANIZATION

</td><td>

 

</td><td>

-   **Matching**
    -   Abraham &amp; Lincoln co.
-   **Non matching**
    -   Now india co

</td></tr><tr><td>

Person

</td><td>

A full person name, which can include first names, middle names or initials, and last names.

</td><td>

 

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

</td></tr><tr><td>

Age

</td><td>

A person's age between 0-129

</td><td>

\\b\(\[0-9\]\|\[1-9\]\[0-9\]\|1\[012\]\[0-9\]\)\\b

</td><td>

 

</td><td>

age

</td><td>

-   **Matching**
    -   24
    -   Age is 100
-   **Non matching**
    -   -2
    -   I am 100 years old
    -   Age is 130

</td></tr><tr><td>

Date of birth

</td><td>

Date of birth using the DD/MM/YYYY format

</td><td>

\\b\[0-3\]?\[0-9\]/\[0-3\]?\[0-9\]/\(?:\[0-9\]\{2\}\)?\[0-9\]\{2\}\\b

</td><td>

 

</td><td>

dob, birthday, date of birth

</td><td>

-   **Matching**
    -   06/18/2012
    -   1/1/19
-   **Non matching**

August 21, 1974

08-21-74


</td></tr><tr><td>

Email

</td><td>

Standard email address

</td><td>

\\b\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\(?:\\.\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\)\*@\(?:\[a-zA-Z0-9-\]+\\.\)+\[a-zA-Z\]\{2,6\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**
    -   johndoe@emailserver.com
    -   historyprofessor@collegehigh.edu
-   **Non matching**
    -   notanemail.com
    -   bademail@.org

</td></tr><tr><td>

Vehicle identification number

</td><td>

A vehicle identification number \(VIN\)

</td><td>

\\b\[A-HJ-NPR-Z0-9\]\{17\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

AHUYA31581L000000

-   **Non matching**

112-32-3478


</td></tr><tr><td>

IP Address

</td><td>

Standard IP address

</td><td>

-   **4 digit IP**

\\b\(?:\(?:25\[0-5\]\|2\[0-4\]\[0-9\]\|\[01\]?\[0-9\]\[0-9\]?\)\\.\)\{3\}\(?:25\[0-5\]\|2\[0-4\]\[0-9\]\|\[01\]?\[0-9\]\[0-9\]?\)\\b

-   **6 digit IP**

\\b\(\(\(?:\[0-9A-Fa-f\]\{1,4\}\(?::\[0-9A-Fa-f\]\{1,4\}\)\*\)?\)::\(\(?:\[0-9A-Fa-f\]\{1,4\}\(?::\[0-9A-Fa-f\]\{1,4\}\)\*\)?\)\)\|\(\(?:\[0-9a-fA-F\]\{1,4\}:\)\{7\}\[0-9a-fA-F\]\{1,4\}\)\\b


</td><td>

 

</td><td>

 

</td><td>

-   **Matching digit IP**

102.28.46.103

-   **Matching 6 digit IP**

914b:d45a:61ea:6346:59bc:3085:ee8b:0ccb


</td></tr><tr><td>

Credit Card- Visa

</td><td>

Visa credit card number

</td><td>

\\b4\[0-9\]\{12\}\(?:\[0-9\]\{3\}\)?\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

4444434342424242

-   **Non matching**

28554


</td></tr><tr><td>

Credit Card- American Express

</td><td>

American Express credit card number

</td><td>

\\b3\[47\]\[0-9\]\{13\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

378225246366005

-   **Non matching**

1199


</td></tr><tr><td>

Credit Card- Mastercard

</td><td>

Mastercard credit card number

</td><td>

\\b\(?:5\[1-5\]\[0-9\]\{2\}\|222\[1-9\]\|22\[3-9\]\[0-9\]\|2\[3-6\]\[0-9\]\{2\}\|27\[01\]\[0-9\]\|2720\)\[0-9\]\{12\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

5555444455554444

-   **Non matching**

1223455


</td></tr><tr><td>

Credit Card- Diners Club

</td><td>

Diners Club credit card number

</td><td>

\\b3\(?:0\[0-5\]\|\[68\]\[0-9\]\)\[0-9\]\{11\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

3056930009020004

-   **Non matching**

7721


</td></tr><tr><td>

Credit Card- Discover

</td><td>

Discovery credit card number

</td><td>

\\b6\(?:011\|5\[0-9\]\{2\}\)\[0-9\]\{12\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

6011025690875424

-   **Non matching**

999


</td></tr><tr><td>

Credit Card- CCV

</td><td>

Credit card security number

</td><td>

\\b\[0-9\]\{3,4\}\\b

</td><td>

 

</td><td>

cvv,verification code,security code

</td><td>

-   **Matching**

124

-   **Non matching**

33441


</td></tr><tr><td>

Credit Card- Expire Date

</td><td>

Credit card expiration in MM/YYYY format

</td><td>

\\b\(\(\[1-9\]\)\|\(0\[1-9\]\|1\[0-2\]\)\)\\/?\(\[0-9\]\{4\}\|\[0-9\]\{2\}\)\\b

</td><td>

 

</td><td>

expire,exp

</td><td>

-   **Matching**
    -   02/2027
    -   04/23
-   **Non matching**

03/9


</td></tr><tr><td>

USA- Social security number

</td><td>

USA citizen social security number

</td><td>

\\b\(?!666\|000\|9\\d\{2\}\)\\d\{3\}-\(?!00\)\\d\{2\}-\(?!0\{4\}\)\\d\{4\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

001-22-111

-   **Non matching**

3321146781


</td></tr><tr><td>

USA- Phone Number

</td><td>

USA phone number**Warning:** Does not use the USA calling code.

</td><td>

\\b\\\(?\(\[0-9\]\{3\}\)\\\)?\[-. \]?\(\[0-9\]\{3\}\)\[-. \]?\(\[0-9\]\{4\}\)\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

2065550199

-   **Non matching**

1 555 238 0199


</td></tr><tr><td>

USA- Passport Number

</td><td>

9 digit USA passport number

</td><td>

\\b\[a-zA-Z0-9\]\\\\d\{8\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

770022122

-   **Non matching**

67431


</td></tr><tr><td>

USA- Taxpayer ID

</td><td>

USA taxpayer ID number

</td><td>

\\b\(9\\d\{2\}\)\(\[ \\-\]?\)\(\[7\]\\d\|8\[0-8\]\)\(\[ \\-\]?\)\(\\d\{4\}\)\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

927 70 5828

-   **Non matching**

87620


</td></tr><tr><td>

USA- California State Driver License number

</td><td>

State of California, USA driver license number

</td><td>

\\b\[a-zA-Z\]\\d\{7\}\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

A0002144

-   **Non matching**

1111


</td></tr><tr><td>

USA - Bank Routing number

</td><td>

US Bank Routing \(ABA\) number

</td><td>

\\b\(\(0\[0-9\]\)\|\(1\[0-2\]\)\|\(2\[1-9\]\)\|\(3\[0-2\]\)\|\(6\[1-9\]\)\|\(7\[0-2\]\)\|80\)\(\[0-9\]\{7\}\)\\b

</td><td>

 

</td><td>

 

</td><td>

-   **Matching**

125210305

-   **Non matching**

1998


</td></tr></tbody>
</table>