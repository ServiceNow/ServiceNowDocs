---
title: Cryptographic Modules in Healthcare and Life Science Service Management Core
description: Healthcare and Life Sciences Service Management Core contains the following cryptographic modules.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Cryptographic Modules in Healthcare and Life Science Service Management Core

Healthcare and Life Sciences Service Management Core contains the following cryptographic modules.

## sn\_hcls.clinical\_data

Crypto module: clinical\_data AES-256.

<table id="table_wcy_dwy_tbc"><thead><tr><th>

Table

</th><th>

Column

</th></tr></thead><tbody><tr><td>

sn\_hcls\_allergy

</td><td>

recorded\_date

</td></tr><tr><td>

sn\_hcls\_encounter

</td><td>

sn\_hcls\_encounter

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

end\_date

</td></tr><tr><td>

sn\_hcls\_condition

</td><td>

recorded\_date

</td></tr><tr><td>

sn\_hcls\_allergy

</td><td>

onset\_date

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

reason\_desc

</td></tr><tr><td>

sn\_hcls\_observation

</td><td>

observed\_date

</td></tr><tr><td>

sn\_hcls\_allergy

</td><td>

onset\_age

</td></tr><tr><td>

sn\_hcls\_medication\_prescription

</td><td>

external\_id

</td></tr><tr><td>

sn\_hcls\_procedure

</td><td>

performed\_date\_time

</td></tr><tr><td>

sn\_hcls\_immunization

</td><td>

status\_reason

</td></tr><tr><td>

sn\_hcls\_encounter

</td><td>

start\_time

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

status\_reason

</td></tr><tr><td>

sn\_hcls\_condition

</td><td>

onset\_age

</td></tr><tr><td>

sn\_hcls\_medication\_prescription

</td><td>

status\_reason

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

effective\_date\_time

</td></tr><tr><td>

sn\_hcls\_condition

</td><td>

onset\_date

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

reason\_code

</td></tr><tr><td>

sn\_hcls\_immunization

</td><td>

admin\_date

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

start\_date

</td></tr></tbody>
</table>|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Clinical data viewer|Role|sn\_hcls.clinical\_data\_viewer|
|Clinical data system access|System Access| |
|Clinical data - admin|Role|admin|
|Clinical data manager|Role|sn\_hcls.manager|

## sn\_hcls.foundation\_data

Crypto module: foundation\_data AES-256.

|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Foundation data viewer|Role|sn\_hcls.foundation\_data\_viewer|
|Foundation data - admin|Role|admin|
|Foundation data system access|System Access| |
|Foundation data manager|Role|sn\_hcls.manager|

## sn\_hcls.health\_insurance\_data

Crypto module: health\_insurance\_data AES-256.

|Table|Column|
|-----|------|
|sn\_hcls\_pre\_auth\_header|date\_fax\_received|
|sn\_hcls\_pre\_auth\_header|primary\_preauth\_num|
|sn\_hcls\_insurance\_info\_task|group\_number|
|sn\_hcls\_pre\_auth\_header|secondary\_preauth\_num|
|sn\_hcls\_insurance\_info\_task|rx\_pcn|
|sn\_hcls\_member\_plan|group\_number|
|sn\_hcls\_pre\_auth\_header|valid\_from|
|sn\_hcls\_insurance\_info\_task|member\_number|
|sn\_hcls\_pre\_auth\_header|reason|
|sn\_hcls\_pre\_auth\_header|notes|
|sn\_hcls\_member\_plan|rx\_pcn|
|sn\_hcls\_member\_plan|member\_number|
|sn\_hcls\_member\_plan|rx\_group|
|sn\_hcls\_insurance\_info\_task|rx\_group|
|sn\_hcls\_insurance\_info\_task|rx\_bin|
|sn\_hcls\_member\_plan|rx\_bin|
|sn\_hcls\_pre\_auth\_header|approved\_date|
|sn\_hcls\_pre\_auth\_header|valid\_to|

|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Health Insurance data system access|System Access| |
|Health Insurance data viewer|Role|sn\_hcls.health\_insurance\_data\_viewer|
|Health Insurance data manager|Role|sn\_hcls.manager|
|Health insurance data - admin|Role|admin|
|Access to fix script for health insurance|Script| |

## sn\_hcls.patient\_data

Cryptographic module: patient\_data AES-256.

|Table|Column|
|-----|------|
|sn\_hcls\_patient|name|
|sn\_hcls\_patient|work\_phone|
|sn\_hcls\_patient|marital\_status|
|sn\_hcls\_patient|ethnicity|
|sn\_hcls\_patient|birth\_date|
|sn\_hcls\_patient|occupation|
|sn\_hcls\_patient|middle\_name|
|sn\_hcls\_patient|primary\_email|
|sn\_hcls\_patient|race|
|sn\_hcls\_patient\_identifier|value|
|sn\_hcls\_patient|secondary\_email|
|sn\_hcls\_patient|address\_line|
|sn\_hcls\_patient|family\_name|
|sn\_hcls\_patient|given\_name|
|sn\_hcls\_patient|mobile\_phone|
|sn\_hcls\_patient|home\_phone|
|sn\_hcls\_patient|deceased\_date\_time|
|sn\_hcls\_patient|guarantor\_id|

|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Patient data system access|System Access| |
|Patient data - admin|Role|admin|
|Patient data viewer|Role|sn\_hcls.patient\_data\_viewer|
|Patient data manager|Role|sn\_hcls.manager|

## sn\_hcls.practitioner\_data

Cryptographic module: practitioner\_data AES-256.

|Table|Column|
|-----|------|
|sn\_hcls\_practitioner|secondary\_email|
|sn\_hcls\_practitioner|name|
|sn\_hcls\_practitioner|external\_id|
|sn\_hcls\_practitioner|family\_name|
|sn\_hcls\_practitioner|mobile\_phone|
|sn\_hcls\_practitioner|work\_phone|
|sn\_hcls\_practitioner|given\_name|
|sn\_hcls\_practitioner|birth\_date|
|sn\_hcls\_practitioner|work\_email|
|sn\_hcls\_practitioner|primary\_email|
|sn\_hcls\_practitioner|home\_phone|

|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Practitioner data - admin|Role|admin|
|Practitioner data viewer|Role|sn\_hcls.practitioner\_data\_viewer|
|Practitioner data manager|Role|sn\_hcls.manager|
|Practitioner data - HclsUtils|Script| |
|Practitioner data system access|System Access| |

## sn\_hcls.revenue\_cycle\_data

Cryptographic module: revenue\_cycle\_data AES-256.

|Table|Column|
|-----|------|
|sn\_hcls\_claim\_line|service\_start\_date|
|sn\_hcls\_claim\_header|billed\_drg\_code|
|sn\_hcls\_claim\_header|service\_provider\_id|
|sn\_hcls\_claim\_line|original\_tcn|
|sn\_hcls\_claim\_header|name|
|sn\_hcls\_claim\_line|service\_end\_date|
|sn\_hcls\_claim\_header|payment\_date|
|sn\_hcls\_claim\_header|adjudicated\_date|
|sn\_hcls\_claim\_header|accepted\_date|
|sn\_hcls\_claim\_line|ndc\_code|
|sn\_hcls\_claim\_line|tooth\_code|
|sn\_hcls\_claim\_line|revenue\_code|
|sn\_hcls\_claim\_header|patient\_account\_no|
|sn\_hcls\_claim\_line|line\_title|
|sn\_hcls\_claim\_header|submitted\_date|
|sn\_hcls\_claim\_header|medical\_record\_no|

|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Revenue cycle manager|Role|sn\_hcls.manager|
|Revenue cycle system access|System Access| |
|Revenue cycle data - admin|Role|admin|
|Revenue cycle data viewer|Role|sn\_hcls.revenue\_cycle\_data\_viewer|
|Access to fix script for Revenue module|Script| |

## sn\_vaccine\_sm.vm\_crypto\_module

Cryptographic module: vm\_crypto\_module AES-256.

|Table|Column|
|-----|------|
|sn\_vaccine\_sm\_personal\_info|occupation|
|sn\_vaccine\_sm\_personal\_info|preferred\_id|
|sn\_vaccine\_sm\_personal\_info|zip|
|sn\_vaccine\_sm\_personal\_info|province|
|sn\_vaccine\_sm\_request|age\_group|
|sn\_vaccine\_sm\_personal\_info|healthcare\_worker|
|sn\_vaccine\_sm\_personal\_info|age\_group|
|sn\_vaccine\_sm\_request|any\_infections|
|sn\_vaccine\_sm\_questionnaire|recently\_sick|
|sn\_vaccine\_sm\_personal\_info|gender|
|sn\_vaccine\_sm\_personal\_info|country|
|sn\_vaccine\_sm\_personal\_info|ethnicity|
|sn\_vaccine\_sm\_request|long\_term\_health\_issue\_details|
|sn\_vaccine\_sm\_questionnaire|recent\_vaccination|
|sn\_vaccine\_sm\_request|health\_history|
|sn\_vaccine\_sm\_request|any\_reaction|
|sn\_vaccine\_sm\_personal\_info|other\_occupation|
|sn\_vaccine\_sm\_personal\_info|street|
|sn\_vaccine\_sm\_request|long\_term\_health\_issues|
|sn\_vaccine\_sm\_personal\_info|city|
|sn\_vaccine\_sm\_questionnaire|any\_other\_comments|
|sn\_vaccine\_sm\_questionnaire|pregnant|

|Policy Name|Type|Target Role|
|-----------|----|-----------|
|Vaccine crypto clinician|Role|sn\_vaccine\_sm.clinician|
|Vaccine crypto manager|Role|sn\_vaccine\_sm.manager|
|Vaccine crypto admin|Role|admin|
|Vaccine crypto user|Role|sn\_vaccine\_sm.user|
|Vaccine crypto system access|System Access| |

**Parent Topic:**[Healthcare and Life Sciences Service Management Core reference](hcls-serv-mgmt-core-reference.md)

