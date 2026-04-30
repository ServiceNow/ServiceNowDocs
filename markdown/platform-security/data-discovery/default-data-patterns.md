---
title: Default data patterns
description: Review the default data pattern regular expressions included in Data Discovery. These default data patterns can be used to filter table entries for further classification.
locale: en-US
release: zurich
product: Data Discovery
classification: data-discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure patterns, Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Default data patterns

Review the default data pattern regular expressions included in Data Discovery. These default data patterns can be used to filter table entries for further classification.

The following are available default patterns for data discovery.

<table id="table_wfd_1ll_gxb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Regular Expression

</th><th>

Keywords

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Age

</td><td>

A person's age between 0-99

</td><td>

\\b\(\[0-9\]\|\[1-9\]\[0-9\]\|1\[012\]\[0-9\]\)\\b

</td><td>

age

</td><td>

-   **Matching**

24

-   **Non matching**
    -   103
    -   -2

</td></tr><tr><td>

Date of birth

</td><td>

Date of birth using the DD/MM/YYYY format

</td><td>

\\b\[0-3\]?\[0-9\]/\[0-3\]?\[0-9\]/\(?:\[0-9\]\{2\}\)?\[0-9\]\{2\}\\b

</td><td>

dob, birthday, date of birth

</td><td>

-   **Matching**
    -   06/18/2012
    -   1/1/19

</td></tr><tr><td>

Email

</td><td>

Standard email address

</td><td>

\\b\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\(?:\\.\[\\w!\#$%&amp;'\*+/=?\`\{\|\}~^-\]+\)\*@\(?:\[a-zA-Z0-9-\]+\\.\)+\[a-zA-Z\]\{2,6\}\\b

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

-   **Matching**

AHUYA31581L000000


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

-   **Matching 4 digit IP**

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

-   **Matching**

4444434342424242


</td></tr><tr><td>

Credit Card- American Express

</td><td>

American Express credit card number

</td><td>

\\b3\[47\]\[0-9\]\{13\}\\b

</td><td>

 

</td><td>

-   **Matching**

378225246366005


</td></tr><tr><td>

Credit Card- Mastercard

</td><td>

Mastercard credit card number

</td><td>

\\b\(?:5\[1-5\]\[0-9\]\{2\}\|222\[1-9\]\|22\[3-9\]\[0-9\]\|2\[3-6\]\[0-9\]\{2\}\|27\[01\]\[0-9\]\|2720\)\[0-9\]\{12\}\\b

</td><td>

 

</td><td>

-   **Matching**

5555444455554444


</td></tr><tr><td>

Credit Card- Diners Club

</td><td>

Diners Club credit card number

</td><td>

\\b3\(?:0\[0-5\]\|\[68\]\[0-9\]\)\[0-9\]\{11\}\\b

</td><td>

 

</td><td>

-   **Matching**

3056930009020004


</td></tr><tr><td>

Credit Card- Discover

</td><td>

Discovery credit card number

</td><td>

\\b6\(?:011\|5\[0-9\]\{2\}\)\[0-9\]\{12\}\\b

</td><td>

 

</td><td>

-   **Matching**

6011025690875424


</td></tr><tr><td>

Credit Card- CCV

</td><td>

Credit card security number

</td><td>

\\b\[0-9\]\{3,4\}\\b

</td><td>

cvv,verification code,security code

</td><td>

-   **Matching**

124


</td></tr><tr><td>

Credit Card- Expire Date

</td><td>

Credit card expiration in MM/YYYY format

</td><td>

\\b\(\(\[1-9\]\)\|\(0\[1-9\]\|1\[0-2\]\)\)\\/?\(\[0-9\]\{4\}\|\[0-9\]\{2\}\)\\b

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

-   **Matching**

001-22-111


</td></tr><tr><td>

USA- Phone Number

</td><td>

USA phone number**Warning:** Does not use the USA calling code.

</td><td>

\\b\\\(?\(\[0-9\]\{3\}\)\\\)?\[-. \]?\(\[0-9\]\{3\}\)\[-. \]?\(\[0-9\]\{4\}\)\\b

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

-   **Matching**

770022122


</td></tr><tr><td>

USA- Taxpayer ID

</td><td>

USA taxpayer ID number

</td><td>

\\b\(9\\d\{2\}\)\(\[ \\-\]?\)\(\[7\]\\d\|8\[0-8\]\)\(\[ \\-\]?\)\(\\d\{4\}\)\\b

</td><td>

 

</td><td>

-   **Matching**

927 70 5828


</td></tr><tr><td>

USA- California State Driver License number

</td><td>

State of California, USA driver license number

</td><td>

\\b\[a-zA-Z\]\\d\{7\}\\b

</td><td>

 

</td><td>

-   **Matching**

A0002144


</td></tr><tr><td>

USA - Bank Routing number

</td><td>

US Bank Routing \(ABA\) number

</td><td>

\\b\(\(0\[0-9\]\)\|\(1\[0-2\]\)\|\(2\[1-9\]\)\|\(3\[0-2\]\)\|\(6\[1-9\]\)\|\(7\[0-2\]\)\|80\)\(\[0-9\]\{7\}\)\\b

</td><td>

 

</td><td>

-   **Matching**

125210305


</td></tr></tbody>
</table>