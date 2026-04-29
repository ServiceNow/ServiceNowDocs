---
title: Encryption options in Healthcare and Life Sciences Service Management Core
description: Healthcare and Life Sciences Service Management Core provides encryption support to secure sensitive information.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Encryption options in Healthcare and Life Sciences Service Management Core

Healthcare and Life Sciences Service Management Core provides encryption support to secure sensitive information.

Encryption prevents unauthorized users from viewing sensitive healthcare data.

The Column Level Encryption Enterprise option on the ServiceNow AI Platform is supported in the Healthcare and Life Sciences Service Management Core application.

## Field Encryption Enterprise

Field Encryption Enterprise provides an enhanced encryption capability compared to Encryption Support and utilizes the Key Management Framework \(KMF\).

When as an administrator, you install the Healthcare and Life Sciences Service Management Core application, the crypto modules and encryption configurations to encrypt sensitive fields along with the KMF are also installed automatically. For managing and auditing cryptographic operations on your ServiceNow instance, as an administrator, you can choose to optionally activate the Field Encryption Enterprise plugin \(com.glide.now.platform.encryption\).

For more information about obtaining Field Encryption Enterprise, see [Activate Field Encryption](https://www.servicenow.com/docs/access?context=activate-platform-encryption&version=australia&pubname=australia-platform-security&ft:locale=en-US). For more information about selecting the parent crypto module, see [Create a cryptographic module](https://www.servicenow.com/docs/access?context=create-cryptographic-module&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For more information on Field Encryption Starter and Field Encryption Enterprise, see .

<table id="table_btm_wgb_mvb"><thead><tr><th>

Table

</th><th>

Field

</th></tr></thead><tbody><tr><td>

sn\_hcls\_allergy

</td><td>

recorded\_date

</td></tr><tr><td>

sn\_hcls\_allergy

</td><td>

onset\_date

</td></tr><tr><td>

sn\_hcls\_allergy

</td><td>

onset\_age

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

billed\_drg\_code

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

service\_provider\_id

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

name

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

payment\_date

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

adjudicated\_date

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

accepted\_date

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

patient\_account\_no

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

submitted\_date

</td></tr><tr><td>

sn\_hcls\_claim\_header

</td><td>

medical\_record\_no

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

service\_start\_date

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

original\_tcn

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

service\_end\_date

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

ndc\_code

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

tooth\_code

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

revenue\_code

</td></tr><tr><td>

sn\_hcls\_claim\_line

</td><td>

line\_title

</td></tr><tr><td>

sn\_hcls\_condition

</td><td>

recorded\_date

</td></tr><tr><td>

sn\_hcls\_condition

</td><td>

onset\_age

</td></tr><tr><td>

sn\_hcls\_condition

</td><td>

onset\_date

</td></tr><tr><td>

sn\_hcls\_encounter

</td><td>

end\_time

</td></tr><tr><td>

sn\_hcls\_encounter

</td><td>

start\_time

</td></tr><tr><td>

sn\_hcls\_immunization

</td><td>

status\_reason

</td></tr><tr><td>

sn\_hcls\_immunization

</td><td>

admin\_date

</td></tr><tr><td>

sn\_hcls\_insurance\_info\_task

</td><td>

group\_number

</td></tr><tr><td>

sn\_hcls\_insurance\_info\_task

</td><td>

rx\_pcn

</td></tr><tr><td>

sn\_hcls\_insurance\_info\_task

</td><td>

member\_number

</td></tr><tr><td>

sn\_hcls\_insurance\_info\_task

</td><td>

rx\_group

</td></tr><tr><td>

sn\_hcls\_insurance\_info\_task

</td><td>

rx\_bin

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

reason\_desc

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

status\_reason

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

effective\_date\_time

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

reason\_code

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

start\_date

</td></tr><tr><td>

sn\_hcls\_medication

</td><td>

end\_date

</td></tr><tr><td>

sn\_hcls\_medication\_prescription

</td><td>

external\_id

</td></tr><tr><td>

sn\_hcls\_medication\_prescription

</td><td>

status\_reason

</td></tr><tr><td>

sn\_hcls\_member\_plan

</td><td>

group\_number

</td></tr><tr><td>

sn\_hcls\_member\_plan

</td><td>

rx\_pcn

</td></tr><tr><td>

sn\_hcls\_member\_plan

</td><td>

member\_number

</td></tr><tr><td>

sn\_hcls\_member\_plan

</td><td>

rx\_group

</td></tr><tr><td>

sn\_hcls\_member\_plan

</td><td>

rx\_bin

</td></tr><tr><td>

sn\_hcls\_observation

</td><td>

observed\_date

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

work\_phone

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

name

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

birth\_date

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

occupation

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

middle\_name

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

external\_id

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

primary\_email

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

secondary\_email

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

address\_line

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

family\_name

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

marital\_status

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

ssn

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

race

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

ethnicity

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

given\_name

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

mobile\_phone

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

home\_phone

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

deceased\_date\_time

</td></tr><tr><td>

sn\_hcls\_patient

</td><td>

guarantor\_id

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

secondary\_email

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

name

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

external\_id

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

family\_name

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

mobile\_phone

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

work\_phone

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

given\_name

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

birth\_date

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

work\_email

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

primary\_email

</td></tr><tr><td>

sn\_hcls\_practioner

</td><td>

home\_phone

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

date\_fax\_received

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

date\_fax\_received

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

primary\_preauth\_num

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

secondary\_preauth\_num

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

valid\_from

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

reason

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

notes

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

approved\_date

</td></tr><tr><td>

sn\_hcls\_pre\_auth\_header

</td><td>

valid\_to

</td></tr><tr><td>

sn\_hcls\_procedure

</td><td>

performed\_date\_time

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences Service Management Core reference](../reference/hcls-serv-mgmt-core-reference.md)

