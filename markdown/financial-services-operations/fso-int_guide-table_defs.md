---
title: FSO table definitions
description: The Financial Services Operations \(FSO\) product provides multiple tables that you can leverage within your custom FSO applications. This section identifies the most frequently used of these tables and defines the fields contained within them.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 66
breadcrumb: [Using the developer guide, Financial Services Operations \(FSO\)]
---

# FSO table definitions

The Financial Services Operations \(FSO\) product provides multiple tables that you can leverage within your custom FSO applications. This section identifies the most frequently used of these tables and defines the fields contained within them.

-   [Consumer \[csm\_consumer\] table](fso-int_guide-table_defs.md#csm_consumer)
-   [Credit Card \[sn\_bom\_credit\_card\] table](fso-int_guide-table_defs.md#sn_bom_credit_card)
-   [Credit Card Service \[sn\_bom\_credit\_card\_service\] table](fso-int_guide-table_defs.md#sn_bom_credit_card_service)
-   [Inbound Document \[sn\_bom\_document\_inbound\_document\] table](fso-int_guide-table_defs.md#sn_bom_document_inbound_document)
-   [Loan Service Case \[sn\_bom\_loan\_service\] table](fso-int_guide-table_defs.md#sn_bom_loan_service)
-   [Mortgage \[sn\_bom\_mortgage\] table](fso-int_guide-table_defs.md#sn_bom_mortgage)
-   [Payment Inquiry Case \[sn\_bom\_payment\_inquiry\] table](fso-int_guide-table_defs.md#sn_bom_payment_inquiry)
-   [Personal Checking Account \[sn\_bom\_checking\_account\] table](fso-int_guide-table_defs.md#sn_bom_checking_account)
-   [Personal Loan \[sn\_bom\_personal\_loan\] table](fso-int_guide-table_defs.md#sn_bom_personal_loan)

## Consumer \[csm\_consumer\] table

<table id="table_l2l_5m4_wgb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr id="consumertable-active-row"><td>

active

</td><td id="consumertable-active-entry">

Flag that indicates whether the consumer is active.Possible values:

-   true: Consumer active
-   false: Consumer de-activated

Data type: Boolean

Default: true

</td></tr><tr id="consumertable-business_phone-row"><td>

business\_phone

</td><td id="consumertable-business_phone-entry">

Business phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-city-row"><td>

city

</td><td id="consumertable-city-entry">

City in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr id="consumertable-country-row"><td>

country

</td><td id="consumertable-country-entry">

Country in which the consumer resides.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-date_format-row"><td>

date\_format

</td><td id="consumertable-date_format-entry">

Format in which to display dates.Valid values:

-   dd-mm-yyyy
-   dd/mm/yyyy
-   dd.mm.yyyy
-   mm-dd-yyyy
-   yyyy-mm-dd

Data type: String

Maximum length: 40

Default: blank \(system date format\)

</td></tr><tr id="consumertable-email-row"><td>

email

</td><td id="consumertable-email-entry">

Email address of the consumer.Data type: String

Maximum length: 100

</td></tr><tr id="consumertable-fax-row"><td>

fax

</td><td id="consumertable-fax-entry">

Fax number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-first_name-row"><td>

first\_name

</td><td id="consumertable-first_name-entry">

Consumer first name.Data type: String

Maximum length: 50

</td></tr><tr id="consumertable-gender-row"><td>

gender

</td><td id="consumertable-gender-entry">

Gender of the consumer.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-home_phone-row"><td>

home\_phone

</td><td id="consumertable-home_phone-entry">

Home phone number of the consumer.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-household-row"><td>

household

</td><td id="consumertable-household-entry">

Sys\_id of the record that describes the household characteristics.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr id="consumertable-last_name-row"><td>

last\_name

</td><td id="consumertable-last_name-entry">

Consumer last name.Data type: String

Maximum length: 50

</td></tr><tr id="consumertable-middle_name-row"><td>

middle\_name

</td><td id="consumertable-middle_name-entry">

Consumer middle name.Data type: String

Maximum length: 50

</td></tr><tr id="consumertable-mobile_phone-row"><td>

mobile\_phone

</td><td id="consumertable-mobile_phone-entry">

Consumer mobile phone number.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-name-row"><td>

name

</td><td id="consumertable-name-entry">

Consumer full name; first\_name+middle\_name+last\_name.Data type: String

Maximum length: 152

</td></tr><tr id="consumertable-notes-row"><td>

notes

</td><td id="consumertable-notes-entry">

Notes on consumer.Data type: String

Maximum length: 4,000

</td></tr><tr id="consumertable-notification-row"><td>

notification

</td><td id="consumertable-notification-entry">

Indicates whether the consumer should receive notifications.Valid values:

-   1: Disabled
-   2: Enabled

Data type: Number \(Integer\)

Maximum length: 40

Default: 2

</td></tr><tr id="consumertable-number-row"><td>

number

</td><td id="consumertable-number-entry">

Unique number associated with the consumer.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-photo-row"><td>

photo

</td><td id="consumertable-photo-entry">

Photo of the consumer.Data type: Image

</td></tr><tr id="consumertable-preferred_language-row"><td>

preferred\_language

</td><td id="consumertable-preferred_language-entry">

Consumer primary language.Data type: String

Maximum length: 3

</td></tr><tr id="consumertable-prefix-row"><td>

prefix

</td><td id="consumertable-prefix-entry">

Consumer name prefix such as, Dr., Mr., Mrs., or Ms.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-primary-row"><td>

primary

</td><td id="consumertable-primary-entry">

Flag that indicates whether this is the primary consumer.Possible values:

-   true: Primary consumer
-   false: Not primary consumer

Data type: Boolean

Default: false

</td></tr><tr id="consumertable-state-row"><td>

state

</td><td id="consumertable-state-entry">

State in which the consumer resides.Data type: String

Maximum length: 100

</td></tr><tr id="consumertable-street-row"><td>

street

</td><td id="consumertable-street-entry">

Consumer street address.Data type: String

Maximum length: 255

</td></tr><tr id="consumertable-suffix-row"><td>

suffix

</td><td id="consumertable-suffix-entry">

Consumer name suffix such as Jr., Sr., or II.Data type: String

</td></tr><tr id="consumertable-sys_created_by-row"><td>

sys\_created\_by

</td><td id="consumertable-sys_created_by-entry">

User that created the consumer record.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-sys_created_on-row"><td>

sys\_created\_on

</td><td id="consumertable-sys_created_on-entry">

Date and time the consumer record was originally created.Data type: String

</td></tr><tr id="consumertable-sys_domain-row"><td>

sys\_domain

</td><td id="consumertable-sys_domain-entry">

ServiceNow domain in which the consumer information resides.Data type: String

</td></tr><tr id="consumertable-sys_id-row"><td>

sys\_id

</td><td id="consumertable-sys_id-entry">

Unique identifier for the consumer.Data type: String

</td></tr><tr id="consumertable-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="consumertable-sys_mod_count-entry">

Number of times that the associated consumer information has been modified.Data type: Number \(Integer\)

</td></tr><tr id="consumertable-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="consumertable-sys_updated_by-entry">

User that last updated the consumer information.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="consumertable-sys_updated_on-entry">

Date and time when the consumer information was last updated.Data type: String

</td></tr><tr id="consumertable-time_format-row"><td>

time\_format

</td><td id="consumertable-time_format-entry">

Format in which to display time.Valid values:

-   hh.mm.ss a: hh.mm.ss \(12 hour\)
-   hh:mm:ss a: hh:mm:ss \(12 hour\)
-   HH.mm.ss: hh.mm.ss \(24 hour\)
-   HH:mm:ss: hh:mm:ss \(24 hour\)

Data type: String

Maximum length: 40

Default: blank \(system time format\)

</td></tr><tr id="consumertable-time_zone-row"><td>

time\_zone

</td><td id="consumertable-time_zone-entry">

Consumer time zone, such as Canada/Central or US/Eastern.Data type: String

Maximum length: 40

</td></tr><tr id="consumertable-title-row"><td>

title

</td><td id="consumertable-title-entry">

Consumer business title such as Manager, Software Developer, or Contractor.Data type: String

Maximum length: 60

</td></tr><tr id="consumertable-user-row"><td>

user

</td><td id="consumertable-user-entry">

Sys\_id of the consumer user. Data type: String

Table: Consumer User \[csm\_consumer\_user\]

</td></tr><tr id="consumertable-zip-row"><td>

zip

</td><td id="consumertable-zip-entry">

Consumer zip code. Data type: String

Maximum length: 40

</td></tr></tbody>
</table>## Credit Card \[sn\_bom\_credit\_card\] table

<table id="d2072e43"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="sold_product-account-entry">

Sys\_id of the account record associated with the case. Located in the Account \[customer\_account\] table. Data type: String

</td></tr><tr><td>

account\_number

</td><td>

Customer's account number. By default, this is the display value for the record.Data type: String

 Maximum length: 40

</td></tr><tr><td>

accrued\_interest

</td><td>

Amount of accrued interest on the credit card as of the date it is being viewed.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

active

</td><td>

Flag that indicates whether the account is active.Possible values:

-   true: Account is currently active.
-   false: Account is inactive.

 Data type: Boolean

 Default: true

</td></tr><tr><td>

address

</td><td>

Customer address.Data type: String

 Maximum length: 4,000

</td></tr><tr><td>

application\_id

</td><td>

Unique identifier of the application submitted when applying for the credit card.Data type: String

 Maximum length: 255

</td></tr><tr><td>

apr\_card

</td><td>

Annual percentage rate for the credit card transactions.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

apr\_cash

</td><td>

Annual percentage rate for cash advances.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

balance

</td><td>

Total amount charged on the credit card.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

base\_currency

</td><td>

Sys\_id of the base currency used by the credit card. Located in the Currency \[fx\_currency\] table.Data type: String \(Reference\)

</td></tr><tr><td>

billing\_cycle

</td><td>

Billing cycle for which statements should be generated, such as 30-days, 60-days, and so on.Data type: String

 Maximum length: 255

</td></tr><tr><td>

bill\_due\_date

</td><td>

Date on which the next payment is due.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

cash\_advance\_limit

</td><td>

Maximum cash advance amount for the credit card.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

closure\_date

</td><td>

Date that the credit card account was closed.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

consumer

</td><td>

Sys\_id of the associated consumer record. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr><td>

credit\_facility\_id

</td><td>

Unique identifier of the credit facility that is responsible for this credit card account.Data type: String

 Maximum length: 255

</td></tr><tr><td>

customer\_class

</td><td>

Free-form classification of customers, such as Premier, Standard, or VIP.Data type: String

 Maximum length: 40

</td></tr><tr><td>

document\_id

</td><td>

Unique identifier of the documents associated with this credit card account in an external document management system.Data type: String

 Maximum length: 255

</td></tr><tr><td>

embossed\_name\_primary\_applicant

</td><td>

Name of the primary applicant that is embossed on the credit card.Data type: String

 Maximum length: 255

</td></tr><tr><td>

embossed\_name\_secondary\_applicant

</td><td>

Name of the secondary applicant that is embossed on the credit card.Data type: String

 Maximum length: 255

</td></tr><tr><td>

end\_date

</td><td>

Date on which the credit card account will end.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

expire\_date

</td><td>

Date on which the associated credit card expires.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

external\_id

</td><td>

Unique identifier used to cross-reference this credit card account to a record in an external system, such as a credit card insurance ID.Data type: String

 Maximum length: 255

</td></tr><tr><td>

grace\_period

</td><td>

Number of days that a customer has after the **bill\_due\_date** to send in a payment without penalties.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

issue\_date

</td><td>

Date on which the credit card was issued.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

is\_lending\_insured

</td><td>

Flag that indicates whether the account is insured.Possible values:

-   true: Account is insured.
-   false: Account is not insured.

 Data type: Boolean

</td></tr><tr><td>

max\_credit\_limit

</td><td>

Maximum amount that the customer is allowed to charge.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

name

</td><td>

Full name of the primary holder of the credit card account.Data type: String

 Maximum length: 255

</td></tr><tr><td>

number

</td><td id="sold_product-number-entry">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

open\_date

</td><td>

Date when the credit card account was first opened.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

parent\_sold\_product

</td><td id="sold_product-parent_sold_product-entry">

Sys\_id of the parent product associated with this entity. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String \(Reference\)

</td></tr><tr><td>

product

</td><td>

Sys\_id of the of the credit card account fumber for the customer. Located in the Product Model \[cmdb\_model\] table.Data type: String \(Reference\)

</td></tr><tr><td>

requested\_credit\_limit

</td><td>

Credit limit requested by the customer.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

request\_channel

</td><td>

Type of communications channel \(digital or banker assisted\) the customer used to make the credit limit request.Data type: String

 Maximum length: 40

</td></tr><tr><td>

risk\_rating

</td><td>

Risk associated with the credit card account.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

secondary\_consumer

</td><td>

Sys\_id of the secondary customer's account. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

sourced\_channel

</td><td>

Source of the customer's business, such as broker or customer referral.Data type: String

 Maximum length: 40

</td></tr><tr><td>

start\_date

</td><td>

Date on which the of the credit card.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

statement\_frequency

</td><td>

Frequency of statements sent to the customer, such as monthly, quarterly, bi-annually, or annually.Data type: String

 Maximum length: 40

</td></tr><tr><td>

statement\_generation\_date

</td><td>

Date on which the latest statement was generated.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

statement\_generation\_day

</td><td>

Day of the month on which to generate the statement, such as 10 for the 10th of the month.Data type: String

 Maximum length: 40

</td></tr><tr><td>

statement\_mode

</td><td>

Method in which the statement is delivered to the customer, such as physical or online.Data type: String

 Maximum length: 40

</td></tr><tr><td>

status

</td><td>

Current status of the account, such as issued, active, blocked, closed, cancelled, and so on.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_class\_name

</td><td id="sold_product-sys_class_name-entry">

Table that contains the case record.Data type: String

 Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="sold_product-sys_created_by-entry">

Person that initially opened the case.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="sold_product-sys_created_on-entry">

Date and time when the case was initially created.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

sys\_domain

</td><td id="sold_product-sys_domain-entry">

Domain associated with the case.Data type: String

 Maximum length: 32

 Default: global

</td></tr><tr><td>

sys\_id

</td><td>

Unique identifier of the credit card record.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td id="sold_product-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

sys\_updated\_by

</td><td id="sold_product-sys_updated_by-entry">

Person that last updated the case.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="sold_product-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr></tbody>
</table>## Credit Card Service \[sn\_bom\_credit\_card\_service\]

<table id="d2413e40"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="casetable-account-entry">

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr id="credit_card_case-active-row"><td>

active

</td><td id="credit_card_case-active-entry">

Flag that indicates whether the case is open and active.Possible values:

 -   true: Case is active
-   false: Case is closed

 Data type: Boolean

 Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="casetable-active_account_escalation-entry">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="casetable-active_escalation-entry">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="task-activity_due-entry">

Date for which the associated case is expected to be completed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="task-additional_assignee_list-entry">

List of the sys\_ids of the additional persons \(other than primary assignee\) that have been assigned to the account.Data type: Array

Maximum length: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="task-approval-entry">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not requested
-   not required
-   rejected
-   requested

Data type: String

Maximum length: 40

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="task-approval_history-entry">

List of all approvals associated with the case.Data type: String \(Journal\)

Maximum length: 4,000

</td></tr><tr><td>

approval\_set

</td><td id="task-approval_set-entry">

Date and time that the associated action was approved.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

asset

</td><td id="casetable-asset-entry">

Sys\_id of the asset record associated with the case.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

assigned\_on

</td><td id="casetable-assigned_on-entry">

Date and time that the case was assigned to the person identified in the **assigned\_to** parameter.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="credit_card_case-assigned_to-row"><td>

assigned\_to

</td><td id="credit_card_case-assigned_to-entry">

 Data type: String

</td></tr><tr id="credit_card_case-assignment_group-row"><td>

assignment\_group

</td><td id="credit_card_case-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case. Located in the Group \[sys\_user\_group\] table.Data type: String

</td></tr><tr><td>

auto\_close

</td><td id="caseTable-auto_close-entry">

Flag that indicates whether the case was automatically closed.Possible values:

-   true: Case was auto closed
-   false: Case wasn't auto closed

Data type: Boolean

Default: false

</td></tr><tr><td>

business\_duration

</td><td id="task-business_duration-entry">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String \(Duration\)

Maximum length: 40

</td></tr><tr><td>

business\_service

</td><td id="task-business_service-entry">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

calendar\_duration

</td><td id="task-calendar_duration-entry">

Length in calendar hours, days, and weeks that it took to complete the case.Data type: String \(Duration\)

Maximum length: 40

</td></tr><tr><td>

case

</td><td id="casetable-case-entry">

Case short description and case number.Data type: String

Maximum length: 300

</td></tr><tr><td>

case\_report

</td><td id="casetable-case_report-entry">

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr id="credit_card_case-category-row"><td>

category

</td><td id="credit_card_case-category-entry">

Case category.Possible values:

 -   0: Question
-   1: Issue
-   2: Feature

 Data type: Number \(Integer\)

 Maximum length: 40

 Default: 1

</td></tr><tr><td>

cause

</td><td id="casetable-cause-entry">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="casetable-caused_by-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="casetable-change-entry">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

closed\_at

</td><td id="task-closed_at-entry">

Date and time that the case was closed.Data type: String

Maximum length: 40

</td></tr><tr><td>

closed\_by

</td><td id="task-closed_by-entry">

Sys\_id of the user that closed the case. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

close\_notes

</td><td id="task-close_notes-entry">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cmdb\_ci

</td><td id="task-cmdb_ci-entry">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr id="credit_card_case-comments-row"><td>

comments

</td><td id="credit_card_case-comments-entry">

Additional comments about the case.Data type: String \(Journal Input\)

 Maximum length: 4,000

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="task-comments_and_work_notes-entry">

Comments and work notes entered for the case.Data type: String \(Journal List\)

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="task-company-entry">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr id="credit_card_case-consumer-row"><td>

consumer

</td><td id="credit_card_case-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regards to this case. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

contact

</td><td id="casetable-contact-entry">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact\_local\_time

</td><td id="casetable-contact_local_time-entry">

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

contact\_time\_zone

</td><td id="casetable-contact_time_zone-entry">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr id="credit_card_case-contact_type-row"><td>

contact\_type

</td><td id="credit_card_case-contact_type-entry">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

 Data type: String

 Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="task-contract-entry">

Sys\_id of the contract associated with the case.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="task-correlation_display-entry">

Display value for the correlation ID.Data type: String

Maximum length: 100

</td></tr><tr id="credit_card_case-correlation_id-row"><td>

correlation\_id

</td><td id="credit_card_case-correlation_id-entry">

Correlation identifier.Data type: String

 Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="task-delivery_plan-entry">

Sys\_id of the parent execution plan for this case. Located in the Execution Plan \[sc\_cat\_item\_delivery\_plan\] table.Data type: String

</td></tr><tr><td>

delivery\_task

</td><td id="task-delivery_task-entry">

Sys\_id of the execution plan task. Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr id="credit_card_case-description-row"><td>

description

</td><td id="credit_card_case-description-entry">

Detailed description of the problem associated with the case. Data type: String

 Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="task-due_date-entry">

Date that the case is due to be closed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

duration

</td><td>

Duration of the credit card account. Returned as a numeric value.Data type: String

 Maximum length: 40

</td></tr><tr><td>

end\_date

</td><td>

Date when the credit card account ends.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

entitlement

</td><td id="casetable-entitlement-entry">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr id="credit_card_case-escalation-row"><td>

escalation

</td><td id="credit_card_case-escalation-entry">

Current escalation level.Possible values:

 -   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

 Data type: Number \(Integer\)

 Maximum length: 40

 Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="task-expected_start-entry">

Date and time when work is scheduled to begin on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

first\_response\_time

</td><td id="casetable-first_response_time-entry">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="casetable-follow_the_sun-entry">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

follow\_up

</td><td id="task-follow_up-entry">

Date and time of the next follow up action.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

group\_list

</td><td id="task-group_list-entry">

List of sys\_ids of the group records associated with the case.Data type: Array \(List\)

Maximum length: 4,000

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="task-impact-entry">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 3

</td></tr><tr><td>

initiated\_as\_request

</td><td id="casetable-initiated_as_request-entry">

Flag that indicates if this inquiry was initiated as a request by the customer.Possible values:

-   true: Inquiry initiated by customer.
-   false: Inquiry wasn't initiated by customer.

Data type: Boolean

Default: false

</td></tr><tr><td>

knowledge

</td><td id="task-knowledge-entry">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article isn't available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="task-location-entry">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="task-made_sla-entry">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with the SLA.
-   false: Case was not resolved according to the SLA.

Data type: Boolean

Default: true

</td></tr><tr><td>

notes\_to\_comments

</td><td id="casetable-notes_to_comments-entry">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="casetable-notify-entry">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr id="credit_card_case-number-row"><td>

number

</td><td id="credit_card_case-number-entry">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="task-opened_at-entry">

Date and time that the case was opened.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

opened\_by

</td><td id="task-opened_by-entry">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="task-order-entry">

Defines some ordering/sequencing, whose usage depends upon the specific use cases.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr id="credit_card_case-parent-row"><td>

parent

</td><td id="credit_card_case-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated. Located in the Task \[task\] table.Data type: String

</td></tr><tr><td>

partner

</td><td id="casetable-partner-entry">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="casetable-partner_contact-entry">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

priority

</td><td id="task-priority-entry">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 4

</td></tr><tr><td>

proactive

</td><td id="casetable-proactive-entry">

Flag that indicates whether the inquiry is being proactively monitored.Possible values:

-   true: Being proactively monitored.
-   false: Not being monitored.

Data type: Boolean

Default:false

</td></tr><tr><td>

problem

</td><td id="casetable-problem-entry">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr id="credit_card_case-product-row"><td>

product

</td><td id="credit_card_case-product-entry">

Sys\_id of the product model of the asset associated to the case. Located in the Product Model \[cmdb\_model\] table. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

</td></tr><tr><td>

reassignment\_count

</td><td id="task-reassignment_count-entry">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Maximum length: 40

Default: 0

</td></tr><tr><td>

rejection\_goto

</td><td id="task-rejection_goto-entry">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

req\_limit\_amount

</td><td>

Credit limit requested by the customer.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

resolution\_code

</td><td id="casetable-resolution_code-entry">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="casetable-resolved_at-entry">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="casetable-resolved_by-entry">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

route\_reason

</td><td id="task-route_reason-entry">

Reason that the case was routed to a different assignee.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

service\_definition

</td><td>

Sys\_id of the definition of service associated with this account. Located in the Service Definition \[sn\_bom\_service\_definition\] table.Data type: String

</td></tr><tr><td>

service\_offering

</td><td id="task-service_offereing-entry">

Sys\_id of the service offering associated with the payment inquiry. Service offerings uniquely define the level of service in terms of availability, scope, pricing, and packaging options.Data type: String

Table: Service Offering \[service\_offering\]

</td></tr><tr id="credit_card_case-short_description-row"><td>

short\_description

</td><td id="credit_card_case-short_description-entry">

Concise description of the case. Data type: String

 Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="task-skills-entry">

Sys\_ids of the skills needed to complete the case.Data type: String

Maximum length: 4,000

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="task-sla_due-entry">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile

</td><td id="casetable-sn_app_cs_social_social_profile-entry">

Sys\_id of the social media profile associated with the case.Data type: String

Table: Social Profile \[sn\_app\_cs\_social\_social\_profile\]

</td></tr><tr><td>

sold\_product

</td><td>

Sys\_id of the credit card account of the customer. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String

</td></tr><tr><td>

stage

</td><td>

Stage of the case, such as Closed Complete, Closed Rejected, Document Check, Authorization, and so on.Data type: String

 Maximum length: 40

</td></tr><tr><td>

start\_date

</td><td>

Start date of the credit card.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="credit_card_case-state-row"><td>

state

</td><td id="credit_card_case-state-entry">

Current state of the case. Possible values:

 -   1: New
-   2: Open
-   3: Awaiting Info
-   4: Resolved
-   5: Closed

 Data type: Number \(Integer\)

 Maximum length: 40

 Default: 1

</td></tr><tr><td>

subcategory

</td><td id="casetable-subcategory-entry">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="casetable-support_manager-entry">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="casetable-sync_driver-entry">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td id="task-sys_class_name-entry">

Table that contains the case record.Data type: String

Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="task-sys_created_by-entry">

Person that initially opened the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="task-sys_created_on-entry">

Date and time when the case was initially created.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

sys\_domain

</td><td id="task-sys_domain-entry">

Domain associated with the case.Data type: String

Maximum length: 32

Default: global

</td></tr><tr id="credit_card_case-sys_domain_path-row"><td>

sys\_domain\_path

</td><td id="credit_card_case-sys_domain_path-entry">

Domain path.Data type: String

 Maximum length: 255

 Default: /

</td></tr><tr id="credit_card_case-sys_sys_id-row"><td>

sys\_id

</td><td id="credit_card_case-sys_sys_id-entry">

Unique identifier for the case.Data type: String

 Maximum length: 32

</td></tr><tr><td>

sys\_mod\_count

</td><td id="task-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr id="credit_card_case-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="credit_card_case-sys_updated_by-entry">

Person that last updated the case.Data type: String

 Maximum length: 40

</td></tr><tr id="credit_card_case-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="credit_card_case-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

task\_effective\_number

</td><td id="task-task_effective_number-entry">

Identifying number. If the task has a Universal Request associated with it, it's the UR number. Otherwise, it's the current task number.

Data type: String

Maximum length: 40

</td></tr><tr><td>

time\_worked

</td><td id="task-time_worked-entry">

Total amount of time worked on the case.Data type: String \(Timer\)

Maximum length: 40

</td></tr><tr><td>

universal\_request

</td><td id="task-universal_request-entry">

Sys\_id of a universal task that this inquiry is part of.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

upon\_approval

</td><td id="task-upon_approval-entry">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="task-upon_reject-entry">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="task-urgency-entry">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="task-user_input-entry">

Additional user input.Data type: String \(User Input\)

Maximum length: 4,000

</td></tr><tr><td>

variables

</td><td id="task-variables-entry">

Name-value pairs of variables associated with the case.Data type: String \(Variables\)

Maximum length: 40

</td></tr><tr id="credit_card_case-watch_list-row"><td>

watch\_list

</td><td id="credit_card_case-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed. Located in the User \[sys\_user\] table. Data type: Array \(List\)

 Maximum length: 4,000

</td></tr><tr><td>

wf\_activity

</td><td id="task-wf_activity-entry">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="task-work_end-entry">

Date and time work ended on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="credit_card_case-work_notes-row"><td>

work\_notes

</td><td id="credit_card_case-work_notes-entry">

Information about how to resolve the case, or steps taken to resolve it.Data type: String \(Journal Input\)

 Maximum length: 4,000

</td></tr><tr id="credit_card_case-work_notes_list-row"><td>

work\_notes\_list

</td><td id="credit_card_case-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added. Located in the User \[sys\_user\] table. Data type: Array \(List\)

 Maximum length: 4,000

</td></tr><tr><td>

work\_start

</td><td id="task-work_start-entry">

Date and time that work started on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr></tbody>
</table>## Inbound Document \[sn\_bom\_document\_inbound\_document\]

<table id="d2414e43"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr id="inbound_doc-account-row"><td>

account

</td><td id="inbound_doc-account-entry">

Sys\_id of the account record associated with the document. Located in the Account \[customer\_account\] table. Data type: String

</td></tr><tr id="inbound_doc-active-row"><td>

active

</td><td id="inbound_doc-active-entry">

Flag that indicates whether the document is active.Possible values:

 -   true: Document is active
-   false: Document is inactive

 Data type: Boolean

 Default: true

</td></tr><tr id="inbound_doc-case-row"><td>

case

</td><td id="inbound_doc-case-entry">

Sys\_id of the case associated with the document. Located in the Case \[sn\_customerservice\_case\] table.Data type: String

</td></tr><tr id="inbound_doc-category-row"><td>

category

</td><td id="inbound_doc-category-entry">

Sys\_id of the category associated with the document, such as proof of address or proof of income. Located in the Category \[sn\_bom\_document\_category\] table.Data type: String

</td></tr><tr id="inbound_doc-customer-row"><td>

customer

</td><td id="inbound_doc-customer-entry">

Sys\_id of the person to contact with regards to this document. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr id="inbound_doc-customer_document-row"><td>

customer\_document

</td><td id="inbound_doc-customer_document-entry">

Sys\_id of the document that is stored against the customer/account ID. Located in the Customer Document \[sn\_bom\_document\_customer\_document\] table.Data type: String

</td></tr><tr id="inbound_doc-deferred_to-row"><td>

deferred\_to

</td><td id="inbound_doc-deferred_to-entry">

Date until the document submission can be deferred.Data type: String

 Maximum length: 40

</td></tr><tr id="inbound_doc-definition_category-row"><td>

definition\_category

</td><td id="inbound_doc-definition_category-entry">

Sys\_id of the definition category, which defines the relationship between the document definition and the document category. Located in the Definition Category \[sn\_bom\_document\_definition\_has\_category\] table.Data type: String

</td></tr><tr id="inbound_doc-doc_type-row"><td>

doc\_type

</td><td id="inbound_doc-doc_type-entry">

Sys\_id of the type of document. For example, if the document category is Address Proof, the **doc\_type** could be utility bill or driver's license. Located in the Type \[sn\_bom\_document\_type\] table.Data type: String

</td></tr><tr id="inbound_doc-mandatory-row"><td>

mandatory

</td><td id="inbound_doc-mandatory-entry">

Flag that indicates whether the associated document is mandatory to submit the loan request.Possible values:

 -   true: Mandatory
-   false: Optional

 Data type: Boolean

</td></tr><tr id="inbound_doc-name-row"><td>

name

</td><td id="inbound_doc-name-entry">

Name of the document, such as paystub or passport.Data type: String

 Maximum length: 120

</td></tr><tr id="inbound_doc-status-row"><td>

status

</td><td id="inbound_doc-status-entry">

Current status of the document.Possible values:

 -   cancelled
-   deferment requested
-   deferment approved
-   deferment rejected
-   exception requested
-   exception approved
-   not submitted
-   exception rejected
-   submitted
-   verified

 Data type: String

 Maximum length: 20

</td></tr><tr id="inbound_doc-sys_class_name-row"><td>

sys\_class\_name

</td><td id="inbound_doc-sys_class_name-entry">

Table that contains the case record.Data type: String

 Maximum length: 80

</td></tr><tr id="inbound_doc-sys_created_by-row"><td>

sys\_created\_by

</td><td id="inbound_doc-sys_created_by-entry">

Person that initially opened the case.Data type: String

 Maximum length: 40

</td></tr><tr id="inbound_doc-sys_created_on-row"><td>

sys\_created\_on

</td><td id="inbound_doc-sys_created_on-entry">

Date and time when the case was initially created.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="inbound_doc-sys_domain-row"><td>

sys\_domain

</td><td id="inbound_doc-sys_domain-entry">

Domain associated with the case.Data type: String

 Maximum length: 32

 Default: global

</td></tr><tr id="inbound_doc-sys_sys_id-row"><td>

sys\_id

</td><td id="inbound_doc-sys_sys_id-entry">

Unique identifier for the case.Data type: String

 Maximum length: 32

</td></tr><tr id="inbound_doc-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="inbound_doc-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="inbound_doc-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="inbound_doc-sys_updated_by-entry">

Person that last updated the case.Data type: String

 Maximum length: 40

</td></tr><tr id="inbound_doc-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="inbound_doc-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr></tbody>
</table>## Loan Service Case \[sn\_bom\_loan\_service\]

<table id="d2415e40"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="d2081e65">

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

account\_number

</td><td>

Customer's account number.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-active-row"><td>

active

</td><td id="loan_service_case-active-entry">

Flag that indicates whether the case is open and active.Possible values:

 -   true: Case is active
-   false: Case is closed

 Data type: Boolean

 Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="d2081e106">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="d2081e119">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="d2279e93">

Date for which the associated case is expected to be completed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="d2279e106">

List of the sys\_ids of the additional persons \(other than primary assignee\) that have been assigned to the account.Data type: Array

Maximum length: 4,000

Table: User \[sys\_user\]

</td></tr><tr id="loan_service_case-amount_paid-row"><td>

amount\_paid

</td><td id="loan_service_case-amount_paid-entry">

Total amount paid on the loan.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

approval

</td><td id="d2279e121">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not requested
-   not required
-   rejected
-   requested

Data type: String

Maximum length: 40

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="d2279e162">

List of all approvals associated with the case.Data type: String \(Journal\)

Maximum length: 4,000

</td></tr><tr><td>

approval\_set

</td><td id="d2279e176">

Date and time that the associated action was approved.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

asset

</td><td id="d2081e224">

Sys\_id of the asset record associated with the case.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

assigned\_on

</td><td id="d2081e237">

Date and time that the case was assigned to the person identified in the **assigned\_to** parameter.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="loan_service_case-assigned_to-row"><td>

assigned\_to

</td><td id="loan_service_case-assigned_to-entry">

 Data type: String

</td></tr><tr id="loan_service_case-assignment_group-row"><td>

assignment\_group

</td><td id="loan_service_case-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case. Located in the Group \[sys\_user\_group\] table.Data type: String

</td></tr><tr><td>

auto\_close

</td><td id="d2081e284">

Flag that indicates whether the case was automatically closed.Possible values:

-   true: Case was auto closed
-   false: Case wasn't auto closed

Data type: Boolean

Default: false

</td></tr><tr id="loan_service_case-bankruptcy_date-row"><td>

bankruptcy\_date

</td><td id="loan_service_case-bankruptcy_date-entry">

Date on which the associated customer declared bankruptcy.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

business\_duration

</td><td id="d2279e217">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String \(Duration\)

Maximum length: 40

</td></tr><tr><td>

business\_service

</td><td id="d2279e230">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

calendar\_duration

</td><td id="d2279e243">

Length in calendar hours, days, and weeks that it took to complete the case.Data type: String \(Duration\)

Maximum length: 40

</td></tr><tr><td>

case

</td><td id="d2081e358">

Case short description and case number.Data type: String

Maximum length: 300

</td></tr><tr><td>

case\_report

</td><td id="d2081e371">

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr id="loan_service_case-category-row"><td>

category

</td><td id="loan_service_case-category-entry">

Case category.Possible values:

 -   0: Question
-   1: Issue
-   2: Feature

 Data type: Number \(Integer\)

 Maximum length: 40

 Default: 1

</td></tr><tr><td>

cause

</td><td id="d2081e410">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

caused\_by

</td><td id="d2081e423">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

change

</td><td id="d2081e437">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr id="loan_service_case-check_number-row"><td>

check\_number

</td><td id="loan_service_case-check_number-entry">

Number of the customer check used to make a loan payment.Data type: String

 Maximum length: 255

</td></tr><tr><td>

closed\_at

</td><td id="d2279e257">

Date and time that the case was closed.Data type: String

Maximum length: 40

</td></tr><tr><td>

closed\_by

</td><td id="d2279e270">

Sys\_id of the user that closed the case. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

close\_notes

</td><td id="d2279e281">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cmdb\_ci

</td><td id="d2279e294">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr id="loan_service_case-comments-row"><td>

comments

</td><td id="loan_service_case-comments-entry">

Additional comments about the case.Data type: String \(Journal Input\)

 Maximum length: 4,000

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="d2279e320">

Comments and work notes entered for the case.Data type: String \(Journal List\)

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="d2279e334">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr id="loan_service_case-consumer-row"><td>

consumer

</td><td id="loan_service_case-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regards to this case. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

contact

</td><td id="d2081e574">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

contact\_local\_time

</td><td id="d2081e587">

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

contact\_time\_zone

</td><td id="d2081e601">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="task-contact_type-entry">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="d2279e379">

Sys\_id of the contract associated with the case.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr id="loan_service_case-corrective_action-row"><td>

corrective\_action

</td><td id="loan_service_case-corrective_action-entry">

Action the customer is taking to correct the current loan infraction, such as making a payment or remedial package.Data type: String

 Maximum length: 40

</td></tr><tr><td>

correlation\_display

</td><td id="d2279e392">

Display value for the correlation ID.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="task-correlation_id-entry">

Unique identifier for content pulled from an external system. Used in tracking continued updates for the content as part of integration.Data type: String

Maximum length: 100

</td></tr><tr id="loan_service_case-credit_service-row"><td>

credit\_service

</td><td id="loan_service_case-credit_service-entry">

Sys\_id of the associated credit service case. Located in the Credit Service Case \[sn\_bom\_credit\_asmt\_loan\_service\] table.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-debit_account-row"><td>

debit\_account

</td><td id="loan_service_case-debit_account-entry">

Sys\_id of an associated savings account. Located in the Deposit Account \[sn\_bom\_deposit\_account\] table.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-debit_general_ledger_account-row"><td>

debit\_general\_ledger\_account

</td><td id="loan_service_case-debit_general_ledger_account-entry">

General ledger account where funds are parked if the mode of payment is either cash or check.Data type: String

 Maximum length: 255

</td></tr><tr id="loan_service_case-deferment_option-row"><td>

deferment\_option

</td><td id="loan_service_case-deferment_option-entry">

Payment deferment option, such as stop repayments, interest payments only, and smaller repayments.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-deferment_period-row"><td>

deferment\_period

</td><td id="loan_service_case-deferment_period-entry">

Length of time for the selected deferment option, such as, 30 days, 60 days, 90 days, and so on.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-deferment_reason-row"><td>

deferment\_reason

</td><td id="loan_service_case-deferment_reason-entry">

Reason the deferment is being put in place, such as, financial difficulties, change in employment, medical condition, and others.Data type: String

 Maximum length: 40

</td></tr><tr><td>

delivery\_plan

</td><td id="d2279e418">

Sys\_id of the parent execution plan for this case. Located in the Execution Plan \[sc\_cat\_item\_delivery\_plan\] table.Data type: String

</td></tr><tr><td>

delivery\_task

</td><td id="d2279e430">

Sys\_id of the execution plan task. Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr id="loan_service_case-description-row"><td>

description

</td><td id="loan_service_case-description-entry">

Detailed description of the problem associated with the case. Data type: String

 Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="d2279e458">

Date that the case is due to be closed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="loan_service_case-end_date-row"><td>

end\_date

</td><td id="loan_service_case-end_date-entry">

End date of the loan or an associated activity such as a deferment period.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

entitlement

</td><td id="d2081e764">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

escalation

</td><td id="task-escalation-entry">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Maximum length: 40

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="d2279e502">

Date and time when work is scheduled to begin on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="loan_service_case-fee_amount-row"><td>

fee\_amount

</td><td id="loan_service_case-fee_amount-entry">

Amount of the fee that has been applied to the associated account.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-fee_treatment-row"><td>

fee\_treatment

</td><td id="loan_service_case-fee_treatment-entry">

Treatment of the fee identified in **fee\_amount**, such as waive or collect.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-fee_write_off_amount-row"><td>

fee\_write\_off\_amount

</td><td id="loan_service_case-fee_write_off_amount-entry">

Amount of fees that have been written off for this account.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

first\_response\_time

</td><td id="d2081e818">

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

follow\_the\_sun

</td><td id="d2081e829">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

follow\_up

</td><td id="d2279e515">

Date and time of the next follow up action.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="loan_service_case-fund_source-row"><td>

fund\_source

</td><td id="loan_service_case-fund_source-entry">

Source of the funds for this loan.Data type: String

 Maximum length: 255

</td></tr><tr><td>

group\_list

</td><td id="d2279e529">

List of sys\_ids of the group records associated with the case.Data type: Array \(List\)

Maximum length: 4,000

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="d2279e544">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 3

</td></tr><tr><td>

initiated\_as\_request

</td><td id="d2081e918">

Flag that indicates if this inquiry was initiated as a request by the customer.Possible values:

-   true: Inquiry initiated by customer.
-   false: Inquiry wasn't initiated by customer.

Data type: Boolean

Default: false

</td></tr><tr id="loan_service_case-interest_outstanding-row"><td>

interest\_outstanding

</td><td id="loan_service_case-interest_outstanding-entry">

Amount of interest that has yet to be paid on this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-interest_write_off_amount-row"><td>

interest\_write\_off\_amount

</td><td id="loan_service_case-interest_write_off_amount-entry">

Amount of interest that has been written off on this loanData type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-judgement_date-row"><td>

judgement\_date

</td><td id="loan_service_case-judgement_date-entry">

Date that the legal judgement was decided on this loan.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

knowledge

</td><td id="d2279e572">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article isn't available for this issue

Data type: Boolean

Default: false

</td></tr><tr id="loan_service_case-last_repayment_amount-row"><td>

last\_repayment\_amount

</td><td id="loan_service_case-last_repayment_amount-entry">

Amount of the last payment made on this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-last_repayment_date-row"><td>

last\_repayment\_date

</td><td id="loan_service_case-last_repayment_date-entry">

Date of the most recent payment made on this loan.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="loan_service_case-loan_amount-row"><td>

loan\_amount

</td><td id="loan_service_case-loan_amount-entry">

Amount of the loan that the customer is seeking forgiveness on.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-loan_forgiveness_reason-row"><td>

loan\_forgiveness\_reason

</td><td id="loan_service_case-loan_forgiveness_reason-entry">

Reason for the loan being forgiven, such as financial difficulties, change in employment, medical condition, or others. Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-loan_transaction-row"><td>

loan\_transaction

</td><td id="loan_service_case-loan_transaction-entry">

Sys\_id of the loan forgiveness transaction associated with this loan. Located in the Transaction \[sn\_bom\_loan\_transaction\] table.Data type: String

</td></tr><tr><td>

location

</td><td id="d2279e595">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="d2279e608">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with the SLA.
-   false: Case was not resolved according to the SLA.

Data type: Boolean

Default: true

</td></tr><tr id="loan_service_case-mode_of_payment-row"><td>

mode\_of\_payment

</td><td id="loan_service_case-mode_of_payment-entry">

Method used to make the most recent payment, such as cash, check, debit, customer's own bank account, or debit account held by another bank.Data type: String

 Maximum length: 40

</td></tr><tr><td>

notes\_to\_comments

</td><td id="d2081e1053">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="d2081e1074">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr id="loan_service_case-number-row"><td>

number

</td><td id="loan_service_case-number-entry">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

opened\_at

</td><td id="d2279e645">

Date and time that the case was opened.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

opened\_by

</td><td id="d2279e658">

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="d2279e671">

Defines some ordering/sequencing, whose usage depends upon the specific use cases.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr id="loan_service_case-other_charges-row"><td>

other\_charges

</td><td id="loan_service_case-other_charges-entry">

Amount of any other charges applied to the loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-other_charges_write_off_amount-row"><td>

other\_charges\_write\_off\_amount

</td><td id="loan_service_case-other_charges_write_off_amount-entry">

Amount of other charges that have been written-off for this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-outstanding_fee-row"><td>

outstanding\_fee

</td><td id="loan_service_case-outstanding_fee-entry">

Amount of any outstanding fees charged to this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-parent-row"><td>

parent

</td><td id="loan_service_case-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated. Located in the Task \[task\] table.Data type: String

</td></tr><tr><td>

partner

</td><td id="d2081e1162">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="d2081e1175">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr id="loan_service_case-payment_details-row"><td>

payment\_details

</td><td id="loan_service_case-payment_details-entry">

Sys\_id of the payment details associated with this loan. Located in the Transaction \[sn\_bom\_loan\_transaction\] table.Data type: String

</td></tr><tr id="loan_service_case-payment_status-row"><td>

payment\_status

</td><td id="loan_service_case-payment_status-entry">

Status of the payment that is currently due, such as paid or unpaid. Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-prepayment_amount-row"><td>

prepayment\_amount

</td><td>

Amount to be prepaid on this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-principal_outstanding-row"><td>

principal\_outstanding

</td><td id="loan_service_case-principal_outstanding-entry">

Total amount of principal currently outstanding on the loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-principal_write_off_amount-row"><td>

principal\_write\_off\_amount

</td><td id="loan_service_case-principal_write_off_amount-entry">

Total amount of principal that has been written-off for this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

priority

</td><td id="d2279e697">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 4

</td></tr><tr><td>

proactive

</td><td id="d2081e1220">

Flag that indicates whether the inquiry is being proactively monitored.Possible values:

-   true: Being proactively monitored.
-   false: Not being monitored.

Data type: Boolean

Default:false

</td></tr><tr id="loan_service_case-problem-row"><td>

problem

</td><td id="loan_service_case-problem-entry">

Sys\_id of the issue that the customer is encountering. Located in the Problem \[problem\] table.Data type: String

</td></tr><tr id="loan_service_case-product-row"><td>

product

</td><td id="loan_service_case-product-entry">

Sys\_id of the product model of the asset associated to the case. Located in the Product Model \[cmdb\_model\] table. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

</td></tr><tr><td>

reassignment\_count

</td><td id="d2279e730">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Maximum length: 40

Default: 0

</td></tr><tr><td>

rejection\_goto

</td><td id="d2279e746">

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr id="loan_service_case-remainder_loan_treatment-row"><td>

remainder\_loan\_treatment

</td><td id="loan_service_case-remainder_loan_treatment-entry">

How to handle the outstanding loan balance after a prepayment amount is applied, such as change installment, change loan term, or no change.Data type: String

</td></tr><tr id="loan_service_case-remarks-row"><td>

remarks

</td><td id="loan_service_case-remarks-entry">

Customer remarks based on account activity.Data type: String

 Maximum length: 2,000

</td></tr><tr id="loan_service_case-remedial_service-row"><td>

remedial\_service

</td><td id="loan_service_case-remedial_service-entry">

Sys\_id of the company being used for remedial services for this loan. Located in the Service \[cmdb\_ci\_service\] table.Data type: String

</td></tr><tr id="loan_service_case-repayment_amount-row"><td>

repayment\_amount

</td><td id="loan_service_case-repayment_amount-entry">

Total amount that has been repaid on the loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-repayment_amount_due-row"><td>

repayment\_amount\_due

</td><td id="loan_service_case-repayment_amount_due-entry">

Total loan amount outstanding.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-repayment_due_date-row"><td>

repayment\_due\_date

</td><td id="loan_service_case-repayment_due_date-entry">

Date on which the next payment is due.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="loan_service_case-report_to_credit_bureau-row"><td>

report\_to\_credit\_bureau

</td><td id="loan_service_case-report_to_credit_bureau-entry">

Flag that indicates whether the loan status has to be reported to the credit bureaus.Possible values:

 -   true: Has to be reported.
-   false: Does not have to be reported.

 Data type: Boolean

</td></tr><tr><td>

resolution\_code

</td><td id="d2081e1322">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

resolved\_at

</td><td id="d2081e1335">

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

resolved\_by

</td><td id="d2081e1346">

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

route\_reason

</td><td id="d2279e759">

Reason that the case was routed to a different assignee.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr id="loan_service_case-routing_number-row"><td>

routing\_number

</td><td id="loan_service_case-routing_number-entry">

Routing number of the check used to make a payment on the loan.Data type: String

 Maximum length: 255

</td></tr><tr id="loan_service_case-service_definition-row"><td>

service\_definition

</td><td id="loan_service_case-service_definition-entry">

Sys\_id of the definition of service associated with this account. Located in the Service Definition \[sn\_bom\_service\_definition\] table.Data type: String

</td></tr><tr><td>

service\_offering

</td><td id="d2279e772">

Sys\_id of the service offering associated with the payment inquiry. Service offerings uniquely define the level of service in terms of availability, scope, pricing, and packaging options.Data type: String

Table: Service Offering \[service\_offering\]

</td></tr><tr id="loan_service_case-short_description-row"><td>

short\_description

</td><td id="loan_service_case-short_description-entry">

Concise description of the case. Data type: String

 Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="d2279e799">

Sys\_ids of the skills needed to complete the case.Data type: String

Maximum length: 4,000

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="d2279e814">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile

</td><td id="d2081e1417">

Sys\_id of the social media profile associated with the case.Data type: String

Table: Social Profile \[sn\_app\_cs\_social\_social\_profile\]

</td></tr><tr id="loan_service_case-sold_product-row"><td>

sold\_product

</td><td id="loan_service_case-sold_product-entry">

Sys\_id of the customer loan account. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String

</td></tr><tr id="loan_service_case-stage-row"><td>

stage

</td><td id="loan_service_case-stage-entry">

Stage of the inquiry, such as Closed Complete, Closed Rejected, Document Check, Authorization, and so on.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-start_date-row"><td>

start\_date

</td><td id="loan_service_case-start_date-entry">

Start date of the personal loan.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="loan_service_case-state-row"><td>

state

</td><td id="loan_service_case-state-entry">

Current state of the case. Possible values:

 -   1: New
-   2: Open
-   3: Awaiting Info
-   4: Resolved
-   5: Closed

 Data type: Number \(Integer\)

 Maximum length: 40

 Default: 1

</td></tr><tr><td>

subcategory

</td><td id="d2081e1489">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="d2081e1505">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="d2081e1518">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td id="d2279e862">

Table that contains the case record.Data type: String

Maximum length: 80

</td></tr><tr id="loan_service_case-sys_created_by-row"><td>

sys\_created\_by

</td><td id="loan_service_case-sys_created_by-entry">

Person that initially opened the case.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-sys_created_on-row"><td>

sys\_created\_on

</td><td id="loan_service_case-sys_created_on-entry">

Date and time when the case was initially created.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="loan_service_case-sys_domain-row"><td>

sys\_domain

</td><td id="loan_service_case-sys_domain-entry">

Domain associated with the case.Data type: String

 Maximum length: 32

 Default: global

</td></tr><tr id="loan_service_case-sys_domain_path-row"><td>

sys\_domain\_path

</td><td id="loan_service_case-sys_domain_path-entry">

Domain path.Data type: String

 Maximum length: 255

 Default: /

</td></tr><tr id="loan_service_case-sys_sys_id-row"><td>

sys\_id

</td><td id="loan_service_case-sys_sys_id-entry">

Unique identifier for the case.Data type: String

 Maximum length: 32

</td></tr><tr id="loan_service_case-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="loan_service_case-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="loan_service_case-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="loan_service_case-sys_updated_by-entry">

Person that last updated the case.Data type: String

 Maximum length: 40

</td></tr><tr id="loan_service_case-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="loan_service_case-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

task\_effective\_number

</td><td id="d2279e984">

Identifying number. If the task has a Universal Request associated with it, it's the UR number. Otherwise, it's the current task number.

Data type: String

Maximum length: 40

</td></tr><tr><td>

time\_worked

</td><td id="d2279e999">

Total amount of time worked on the case.Data type: String \(Timer\)

Maximum length: 40

</td></tr><tr id="loan_service_case-total_outstanding_amount-row"><td>

total\_outstanding\_amount

</td><td id="loan_service_case-total_outstanding_amount-entry">

Total amount of the loan, including principal, interest, any fees or dues on the loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr id="loan_service_case-total_write_off_amount-row"><td>

total\_write\_off\_amount

</td><td id="loan_service_case-total_write_off_amount-entry">

Total amount that has been written-off for this loan.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

universal\_request

</td><td id="d2279e1013">

Sys\_id of a universal task that this inquiry is part of.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

upon\_approval

</td><td id="d2279e1026">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="d2279e1051">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="d2279e1076">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="d2279e1104">

Additional user input.Data type: String \(User Input\)

Maximum length: 4,000

</td></tr><tr><td>

variables

</td><td id="d2279e1117">

Name-value pairs of variables associated with the case.Data type: String \(Variables\)

Maximum length: 40

</td></tr><tr id="loan_service_case-watch_list-row"><td>

watch\_list

</td><td id="loan_service_case-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed. Located in the User \[sys\_user\] table. Data type: Array \(List\)

 Maximum length: 4,000

</td></tr><tr><td>

wf\_activity

</td><td id="d2279e1146">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

work\_end

</td><td id="d2279e1159">

Date and time work ended on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="loan_service_case-work_notes-row"><td>

work\_notes

</td><td id="loan_service_case-work_notes-entry">

Information about how to resolve the case, or steps taken to resolve it.Data type: String \(Journal Input\)

 Maximum length: 4,000

</td></tr><tr id="loan_service_case-work_notes_list-row"><td>

work\_notes\_list

</td><td id="loan_service_case-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added. Located in the User \[sys\_user\] table. Data type: Array \(List\)

 Maximum length: 4,000

</td></tr><tr><td>

work\_start

</td><td id="d2279e1200">

Date and time that work started on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="loan_service_case-write_off_option-row"><td>

write\_off\_option

</td><td id="loan_service_case-write_off_option-entry">

Type of write-off of the loan, such as full write-off or partial write-off. Data type: String

 Maximum length: 40

</td></tr></tbody>
</table>## Mortgage \[sn\_bom\_mortgage\] table

<table id="d2416e43"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="d2074e70">

Sys\_id of the account record associated with the case. Located in the Account \[customer\_account\] table. Data type: String

</td></tr><tr id="mortgage-account_number-row"><td>

account\_number

</td><td id="mortgage-account_number-entry">

Customer's account number. By default, this is the display value for the record.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-accrued_interest-row"><td>

accrued\_interest

</td><td id="mortgage-accrued_interest-entry">

Amount of accrued interest of the mortgage as of the date it is being viewed.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr id="mortgage-active-row"><td>

active

</td><td id="mortgage-active-entry">

Flag that indicates whether the account is active.Possible values:

-   true: Account is currently active.
-   false: Account is inactive.

 Data type: Boolean

 Default: true

</td></tr><tr id="mortgage-amount-row"><td>

amount

</td><td id="mortgage-amount-entry">

Sanctioned mortgage amount.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr id="mortgage-application_id-row"><td>

application\_id

</td><td id="mortgage-application_id-entry">

Unique identifier of the application submitted when applying for the mortgage.Data type: String

 Maximum length: 255

</td></tr><tr id="mortgage-apr-row"><td>

apr

</td><td id="mortgage-apr-entry">

Annual percentage rate for the mortgage.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-balance-row"><td>

balance

</td><td id="mortgage-balance-entry">

Balance outstanding on the mortgage.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr id="mortgage-base_currency-row"><td>

base\_currency

</td><td id="mortgage-base_currency-entry">

Sys\_id of the base currency used by the credit card. Located in the Currency \[fx\_currency\] table.Data type: String \(Reference\)

</td></tr><tr id="mortgage-closure_date-row"><td>

closure\_date

</td><td id="mortgage-closure_date-entry">

Date that the mortgage account was closed.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-consumer-row"><td>

consumer

</td><td id="mortgage-consumer-entry">

Sys\_id of the primary consumer record associated with the mortgage. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr id="mortgage-cosigner-row"><td>

cosigner

</td><td id="mortgage-cosigner-entry">

Sys\_id of the cosigner consumer record associated with the mortgage. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr id="mortgage-credit_facility_id-row"><td>

credit\_facility\_id

</td><td id="mortgage-credit_facility_id-entry">

Unique identifier of the facility linked to the mortgage.Data type: String

 Maximum length: 255

</td></tr><tr id="mortgage-customer_class-row"><td>

customer\_class

</td><td id="mortgage-customer_class-entry">

Free-form classification of customer, such as Premier, Standard, or VIP.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-days_past_due-row"><td>

days\_past\_due

</td><td id="mortgage-days_past_due-entry">

Number of days that the current mortgage payment is past due.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-delinquency_status-row"><td>

delinquency\_status

</td><td id="mortgage-delinquency_status-entry">

Flag that indicates whether the account is currently delinquent.Possible values:

-   Yes
-   No

 Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-disbursed_amount-row"><td>

disbursed\_amount

</td><td id="mortgage-disbursed_amount-entry">

Total amount of money that has been borrowed by the associated customer.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr id="mortgage-document_id-row"><td>

document\_id

</td><td id="mortgage-document_id-entry">

Unique identifier of the documents associated with this mortgage in an external document management system.Data type: String

 Maximum length: 255

</td></tr><tr id="mortgage-end_date-row"><td>

end\_date

</td><td id="mortgage-end_date-entry">

Date or the mortgage end.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-external_id-row"><td>

external\_id

</td><td id="mortgage-external_id-entry">

Unique identifier used to cross-reference this mortgage account to a record in an external system, such as a mortgage insurance ID.Data type: String

 Maximum length: 255

</td></tr><tr id="mortgage-federal_backed_load-row"><td>

federal\_backed\_load

</td><td id="mortgage-federal_backed_load-entry">

Flag that indicates whether the associated mortgage is federally backed.Possible values:

-   Yes: Federally backed
-   No: Not federally backed

 Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-grace_period_for_repayment-row"><td>

grace\_period\_for\_repayment

</td><td id="mortgage-grace_period_for_repayment-entry">

Number of days that a customer has after the due date to send in a payment without penalties.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-guarantor-row"><td>

guarantor

</td><td id="mortgage-guarantor-entry">

Sys\_id of the person that is guaranteeing the mortgage. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr id="mortgage-interest_rate-row"><td>

interest\_rate

</td><td id="mortgage-interest_rate-entry">

Current interest rate of the mortgage.Data type: Number \(Floating-point\)

 Maximum length: 40

</td></tr><tr id="mortgage-interest_type-row"><td>

interest\_type

</td><td id="mortgage-interest_type-entry">

Type of interest associated with the mortgage, such as fixed or floating.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-is_lending_insured-row"><td>

is\_lending\_insured

</td><td id="mortgage-is_lending_insured-entry">

Flag that indicates whether the account is insured.Possible values:

-   true: Account is insured.
-   false: Account is not insured.

 Data type: Boolean

</td></tr><tr id="mortgage-last_payment_amount-row"><td>

last\_payment\_amount

</td><td id="mortgage-last_payment_amount-entry">

Amount of the most recent payment made by the customer.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr id="mortgage-last_payment_date-row"><td>

last\_payment\_date

</td><td id="mortgage-last_payment_date-entry">

Date of the most recent payment made by the customer.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-last_reviewed_on-row"><td>

last\_reviewed\_on

</td><td id="mortgage-last_reviewed_on-entry">

Date the mortgage was last reviewed.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-loan_classification-row"><td>

loan\_classification

</td><td id="mortgage-loan_classification-entry">

Classification of the mortgage, such as standard, sub-standard, doubtful, or loss assets.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-maturity_date-row"><td>

maturity\_date

</td><td id="mortgage-maturity_date-entry">

Date on which the mortgage becomes due.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-moratorium_end_date-row"><td>

moratorium\_end\_date

</td><td id="mortgage-moratorium_end_date-entry">

End date of any imposed moratorium \(suspension of payment.\)Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-moratorium_period-row"><td>

moratorium\_period

</td><td id="mortgage-moratorium_period-entry">

Period for which the customer has a suspension of mortgage repayment, such as 6 months, 1 year, 2 years, and so on.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-moratorium_start_date-row"><td>

moratorium\_start\_date

</td><td id="mortgage-moratorium_start_date-entry">

Date on which the customer suspended payments on the mortgage.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-name-row"><td>

name

</td><td id="mortgage-name-entry">

Full name of the primary person responsible for the mortgage.Data type: String

 Maximum length: 255

</td></tr><tr id="mortgage-next_review_on-row"><td>

next\_review\_on

</td><td id="mortgage-next_review_on-entry">

Date on which the mortgage is to be reviewed.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-no_of_installments-row"><td>

no\_of\_installments

</td><td id="mortgage-no_of_installments-entry">

Number of payments due on the mortgage.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-no_of_installment_deferrals_made-row"><td>

no\_of\_installment\_deferrals\_made

</td><td id="mortgage-no_of_installment_deferrals_made-entry">

Number of times the customer deferred their payment on the mortgage.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

number

</td><td id="d2074e105">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-open_date-row"><td>

open\_date

</td><td id="mortgage-open_date-entry">

Date when the mortgage account was first opened.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

parent\_sold\_product

</td><td id="d2074e119">

Sys\_id of the parent product associated with this entity. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String \(Reference\)

</td></tr><tr id="mortgage-pending_installments-row"><td>

pending\_installments

</td><td id="mortgage-pending_installments-entry">

Number of payments remaining on the mortgage.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-prepayment_allowed-row"><td>

prepayment\_allowed

</td><td id="mortgage-prepayment_allowed-entry">

Flag that indicates whether the mortgage allows prepayments.Possible values:

-   Yes: Prepayments allowed
-   No: Prepayments not allowed

 Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-principal_balance-row"><td>

principal\_balance

</td><td id="mortgage-principal_balance-entry">

Amount of the remaining mortgage principal.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr id="mortgage-product-row"><td>

product

</td><td id="mortgage-product-entry">

Sys\_id of the product model of the mortgage. Located in the Product Model \[cmdb\_model\] table.Data type: String \(Reference\)

</td></tr><tr id="mortgage-purpose-row"><td>

purpose

</td><td id="mortgage-purpose-entry">

How the funds of the mortgage will be used by the customer, such as working capital or equipment purchase.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-request_channel-row"><td>

request\_channel

</td><td id="mortgage-request_channel-entry">

Type of communications channel \(digital or banker assisted\) the customer used to make the credit limit request.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-risk_rating-row"><td>

risk\_rating

</td><td id="mortgage-risk_rating-entry">

Risk associated with the credit card account.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-rollover_mode-row"><td>

rollover\_mode

</td><td id="mortgage-rollover_mode-entry">

Method in which a customer can extend the mortgage, such as auto rollover or manual rollover.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-rollover_possible-row"><td>

rollover\_possible

</td><td id="mortgage-rollover_possible-entry">

Flag that indicates whether the amount due on the mortgage can be rolled over in the future. Possible values:

-   Yes: Rollover possible
-   No: Not eligible for rollover

 Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-secondary_consumer-row"><td>

secondary\_consumer

</td><td id="mortgage-secondary_consumer-entry">

Sys\_id of the secondary customer's account. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr id="mortgage-sourced_channel-row"><td>

sourced\_channel

</td><td id="mortgage-sourced_channel-entry">

Source of the customer's business, such as broker or customer referral.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-start_date-row"><td>

start\_date

</td><td id="mortgage-start_date-entry">

Start date of the mortgage.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-statement_frequency-row"><td>

statement\_frequency

</td><td id="mortgage-statement_frequency-entry">

Frequency of statements sent to the customer, such as monthly, quarterly, bi-annually, or annually.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-statement_mode-row"><td>

statement\_mode

</td><td id="mortgage-statement_mode-entry">

Method in which the statement is delivered to the customer, such as physical or online.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-status-row"><td>

status

</td><td id="mortgage-status-entry">

Current status of the account, such as issued, active, blocked, closed, cancelled, and so on.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_class\_name

</td><td id="d2074e142">

Table that contains the case record.Data type: String

 Maximum length: 80

</td></tr><tr id="mortgage-sys_created_by-row"><td>

sys\_created\_by

</td><td id="mortgage-sys_created_by-entry">

Name of the entity that created this record.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-sys_created_on-row"><td>

sys\_created\_on

</td><td id="mortgage-sys_created_on-entry">

Date and time that the record was originally created.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-sys_domain-row"><td>

sys\_domain

</td><td id="mortgage-sys_domain-entry">

Unique identifier of the domain associated with the record.Data type: String

 Maximum length: 32

 Default: global

</td></tr><tr id="mortgage-sys_id-row"><td>

sys\_id

</td><td id="mortgage-sys_id-entry">

Unique identifier of the credit card record.Data type: String

</td></tr><tr id="mortgage-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="mortgage-sys_mod_count-entry">

Number of times the record has been updated.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="mortgage-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="mortgage-sys_updated_by-entry">

Name of the entity that last updated this record.Data type: String

 Maximum length: 40

</td></tr><tr id="mortgage-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="mortgage-sys_updated_on-entry">

Date and time that the record was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="mortgage-term-row"><td>

term

</td><td id="mortgage-term-entry">

Number of terms associated with the mortgage.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr></tbody>
</table>## Payment Inquiry Case \[sn\_bom\_payment\_inquiry\]

<table id="d2277e40"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr id="pay_inquiry_case-account-row"><td>

account

</td><td id="pay_inquiry_case-account-entry">

Sys\_id of the account record associated with the case. Located in the Account \[customer\_account\] table. Data type: String

</td></tr><tr id="pay_inquiry_case-active-row"><td>

active

</td><td id="pay_inquiry_case-active-entry">

Flag that indicates whether the case is open and active.Possible values:

 -   true: Case is active
-   false: Case is closed

 Data type: Boolean

 Default: true

</td></tr><tr><td>

active\_account\_escalation

</td><td id="d2081e106">

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

active\_escalation

</td><td id="d2081e119">

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

activity\_due

</td><td id="d2279e93">

Date for which the associated case is expected to be completed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="d2279e106">

List of the sys\_ids of the additional persons \(other than primary assignee\) that have been assigned to the account.Data type: Array

Maximum length: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

approval

</td><td id="d2279e121">

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not requested
-   not required
-   rejected
-   requested

Data type: String

Maximum length: 40

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="d2279e162">

List of all approvals associated with the case.Data type: String \(Journal\)

Maximum length: 4,000

</td></tr><tr><td>

approval\_set

</td><td id="d2279e176">

Date and time that the associated action was approved.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr id="pay_inquiry_case-asset-row"><td>

asset

</td><td id="pay_inquiry_case-asset-entry">

Sys\_id of the asset record associated with the case. Located in the Asset \[alm\_asset\] table.Data type: String

</td></tr><tr><td>

assigned\_on

</td><td>

Date and time that the case was assigned to the person identified in the **assigned\_to** parameter.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-assigned_to-row"><td>

assigned\_to

</td><td id="pay_inquiry_case-assigned_to-entry">

 Data type: String

</td></tr><tr id="pay_inquiry_case-assignment_group-row"><td>

assignment\_group

</td><td id="pay_inquiry_case-aassignment_group-entry">

Sys\_id of the customer service agent group assigned to the case. Located in the Group \[sys\_user\_group\] table.Data type: String

</td></tr><tr id="pay_inquiry_case-auto_created_case-row"><td>

auto\_close

</td><td id="pay_inquiry_case-auto_created_case-entry">

Flag that indicates whether the case was automatically closed.Possible values:

-   true: Case was auto closed
-   false: Case was not auto closed

 Data type: Boolean

 Default: false

</td></tr><tr><td>

business\_duration

</td><td id="d2279e217">

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String \(Duration\)

Maximum length: 40

</td></tr><tr><td>

business\_service

</td><td id="d2279e230">

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

calendar\_duration

</td><td>

Length in calendar hours, days, and weeks that it took to complete the case.Data type: String \(Duration\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-case-row"><td>

case

</td><td id="pay_inquiry_case-case-entry">

Case short description and case number.Data type: String

 Maximum length: 300

</td></tr><tr><td>

case\_report

</td><td id="d2081e371">

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr><td>

category

</td><td id="casetable-category-entry">

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cause

</td><td id="d2081e410">

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr id="pay_inquiry_case-caused_by-row"><td>

caused\_by

</td><td id="pay_inquiry_case-caused_by-entry">

Sys\_id of the change request that caused the case to be created. Located in the Change Request \[change\_request\] table.Data type: String

</td></tr><tr><td>

change

</td><td id="d2081e437">

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr id="pay_inquiry_case-closed_at-row"><td>

closed\_at

</td><td id="pay_inquiry_case-closed_at-entry">

Date and time that the case was closed.Data type: String

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-closed_by-row"><td>

closed\_by

</td><td id="pay_inquiry_case-closed_by-entry">

Sys\_id of the user that closed the case. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

close\_notes

</td><td id="d2279e281">

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cmdb\_ci

</td><td id="d2279e294">

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr id="pay_inquiry_case-comments-row"><td>

comments

</td><td id="pay_inquiry_case-comments-entry">

Additional comments about the case.Data type: String \(Journal Input\)

 Maximum length: 4,000

</td></tr><tr id="pay_inquiry_case-comments_and_work_notes-row"><td>

comments\_and\_work\_notes

</td><td id="pay_inquiry_case-comments_and_work_notes-entry">

Comments and work notes entered for the case.Data type: String \(Journal List\)

 Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="d2279e334">

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr id="pay_inquiry_case-consumer-row"><td>

consumer

</td><td id="pay_inquiry_case-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regards to this case. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr id="pay_inquiry_case-contact-row"><td>

contact

</td><td id="pay_inquiry_case-contact-entry">

Business-to-business based cases only. Sys\_id of the person to contact regarding this case. Located in the Contact \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

contact\_local\_time

</td><td id="d2081e587">

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

contact\_time\_zone

</td><td id="d2081e601">

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

contact\_type

</td><td id="d2279e347">

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

contract

</td><td id="d2279e379">

Sys\_id of the contract associated with the case.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correct\_account

</td><td>

Account number to which the payment should have been sent.Data type: String

 Maximum length: 250

</td></tr><tr><td>

correct\_beneficiary

</td><td>

Corrected name of the beneficiary to whom the payment should have been sent.Data type: String

 Maximum length: 250

</td></tr><tr><td>

correct\_routing

</td><td>

Corrected routing number of the account to apply the payment to.Data type: String

 Maximum length: 250

</td></tr><tr><td>

correlation\_display

</td><td id="d2279e392">

Display value for the correlation ID.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="d2279e405">

Unique identifier for content pulled from an external system. Used in tracking continued updates for the content as part of integration.Data type: String

Maximum length: 100

</td></tr><tr><td>

customer\_reason

</td><td>

Reason that the customer is making the payment inquiry, such as wrong account number, wrong sort code, incorrect amount, recurring payment not cancelled and such.Data type: String

 Maximum length: 40

</td></tr><tr><td>

delivery\_plan

</td><td id="d2279e418">

Sys\_id of the parent execution plan for this case. Located in the Execution Plan \[sc\_cat\_item\_delivery\_plan\] table.Data type: String

</td></tr><tr><td>

delivery\_task

</td><td id="d2279e430">

Sys\_id of the execution plan task. Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr id="pay_inquiry_case-description-row"><td>

description

</td><td id="pay_inquiry_case-description-entry">

Detailed description of the problem associated with the case. Data type: String

 Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td id="d2279e458">

Date that the case is due to be closed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

entitlement

</td><td id="d2081e764">

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

error\_type

</td><td>

Type of error that was made, such as customer error or bank error.Data type: String

 Maximum length: 40

</td></tr><tr><td>

escalation

</td><td id="d2279e471">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Maximum length: 40

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="d2279e502">

Date and time when work is scheduled to begin on the case.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

external\_id

</td><td>

Unique identifier used to cross-reference this payment inquiry to a record in an external system.Data type: String

 Maximum length: 255

</td></tr><tr id="pay_inquiry_case-first_response_time-row"><td>

first\_response\_time

</td><td id="pay_inquiry_case-first_response_time-entry">

Date and time when the first action was taken on the case.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

follow\_the\_sun

</td><td id="d2081e829">

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

follow\_up

</td><td id="d2279e515">

Date and time of the next follow up action.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

group\_list

</td><td id="d2279e529">

List of sys\_ids of the group records associated with the case.Data type: Array \(List\)

Maximum length: 4,000

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

impact

</td><td id="d2279e544">

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 3

</td></tr><tr><td>

initiated\_as\_request

</td><td id="d2081e918">

Flag that indicates if this inquiry was initiated as a request by the customer.Possible values:

-   true: Inquiry initiated by customer.
-   false: Inquiry wasn't initiated by customer.

Data type: Boolean

Default: false

</td></tr><tr><td>

is\_attempted\_recovery

</td><td>

Flag that indicates whether the customer tried to get misappropriated funds returned to them by reaching out to the beneficiary to whom the funds were incorrectly credited. Possible values:

 -   true: Recovery attempt
-   false: Not a recovery attempt

 Data type: Boolean

</td></tr><tr><td>

is\_international

</td><td>

Flag that indicates whether this inquiry was made for an international payment transaction.Possible values:

 -   true: International account
-   false: Domestic account

 Data type: Boolean

</td></tr><tr><td>

is\_recurring

</td><td>

Flag that indicates whether this inquiry was for a recurring payment.Possible values:

 -   true: Recurring payment
-   false: Manual payment

 Data type: Boolean

</td></tr><tr><td>

is\_valid\_claim

</td><td>

Flag that indicates whether this is a valid inquiry claim.Possible values:

 -   true: Valid claim
-   false: Invalid claim

 Data type: Boolean

</td></tr><tr><td>

knowledge

</td><td id="d2279e572">

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article isn't available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

location

</td><td id="d2279e595">

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="d2279e608">

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with the SLA.
-   false: Case was not resolved according to the SLA.

Data type: Boolean

Default: true

</td></tr><tr id="pay_inquiry_case-notes_to_comments-row"><td>

notes\_to\_comments

</td><td id="pay_inquiry_case-notes_to_comments-entry">

Flag that indicates whether to add the resolution notes to the comments.Possible values:

 -   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments are not required

 Data type: Boolean

</td></tr><tr><td>

notify

</td><td id="d2081e1074">

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr id="pay_inquiry_case-number-row"><td>

number

</td><td id="pay_inquiry_case-number-entry">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-opened_at-row"><td>

opened\_at

</td><td id="pay_inquiry_case-opened_at-entry">

Date and time that the case was opened.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-opened_by-row"><td>

opened\_by

</td><td id="pay_inquiry_case-opened_by-entry">

Sys\_id of the person that initially opened the case. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

order

</td><td id="d2279e671">

Defines some ordering/sequencing, whose usage depends upon the specific use cases.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

other\_reason

</td><td>

Information entered in the **Other Reason** text box.Data type: String

 Maximum length: 4,000

</td></tr><tr id="pay_inquiry_case-parent-row"><td>

parent

</td><td id="pay_inquiry_case-parent-entry">

Sys\_id of the parent case to which this case \(child\) is associated. Located in the Task \[task\] table.Data type: String

</td></tr><tr><td>

partner

</td><td id="d2081e1162">

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

partner\_contact

</td><td id="d2081e1175">

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

payment\_processor

</td><td>

Processor used to handle the associated payment, such as BACS, CHAP, Wire, and SWIFT.Data type: String

 Maximum length: 40

</td></tr><tr><td>

priority

</td><td id="d2279e697">

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 4

</td></tr><tr><td>

proactive

</td><td id="d2081e1220">

Flag that indicates whether the inquiry is being proactively monitored.Possible values:

-   true: Being proactively monitored.
-   false: Not being monitored.

Data type: Boolean

Default:false

</td></tr><tr><td>

problem

</td><td id="d2081e1256">

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr id="pay_inquiry_case-product-row"><td>

product

</td><td id="pay_inquiry_case-product-entry">

Sys\_id of the product model of the asset associated to the case. Located in the Product Model \[cmdb\_model\] table. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

</td></tr><tr id="pay_inquiry_case-reassignment_count-row"><td>

reassignment\_count

</td><td id="pay_inquiry_case-reassignment_count-entry">

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

 Maximum length: 40

 Default: 0

</td></tr><tr><td>

receiving\_account

</td><td>

Sys\_id of the account record to which funds were erroneously credited. Located in the Account \[customer\_account\] table.Data type: String

</td></tr><tr><td>

receiving\_contact

</td><td>

Business-to-business based cases only. Sys\_id of the contact associated with the account receiving. Located in the Contact \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

receiving\_customer

</td><td>

Business-to-consumer cases only. Sys\_id of the person associated with the receiving account. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

receiving\_financial\_account

</td><td>

Sys\_id of the financial account to which funds were erroneously sent. Located in the Financial Account \[sn\_bom\_financial\_account\] table.Data type: String

</td></tr><tr><td>

receiving\_transactions

</td><td>

List of sys\_ids of transactions in the financial account to which the funds were erroneously sent. Located in the Financial Transaction \[sn\_bom\_transaction\] table.Data type: String

 Maximum length: 40,000

</td></tr><tr><td>

recipient\_bank

</td><td>

Sys\_id of the bank that incorrectly received funds. Located in the Financial Institution \[sn\_bom\_financial\_institution\] table.Data type: String

</td></tr><tr><td>

recipient\_type

</td><td>

Type of recipient, such as internal \(bank customer\) or external \(not a bank customer\), who incorrectly received funds. Data type: String

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-rejection_goto-row"><td>

rejection\_goto

</td><td id="pay_inquiry_case-rejection_goto-entry">

Sys\_id of the task to execute if the case is rejected. Located in the Task \[task\] table.Data type: String

</td></tr><tr><td>

remitter\_bank

</td><td>

Sys\_id of the bank that incorrectly remitted the funds. Located in the Financial Institution \[sn\_bom\_financial\_institution\] table.Data type: String

</td></tr><tr id="pay_inquiry_case-resolution_code-row"><td>

resolution\_code

</td><td id="pay_inquiry_case-resolution_code-entry">

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-resolved_at-row"><td>

resolved\_at

</td><td id="pay_inquiry_case-resolved_at-entry">

Date and time that the case was resolved.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-resolved_by-row"><td>

resolved\_by

</td><td id="pay_inquiry_case-resolved_by-entry">

Sys\_id of the person that resolved the case. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

route\_reason

</td><td>

Reason that the case was routed to a different assignee.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

sender\_transactions

</td><td>

List of sys\_ids of the transactions from the senders's financial account that were remitted incorrectly. Located in the Financial Transaction \[sn\_bom\_transaction\] table.Data type: String \(List\)

 Maximum length: 40,000

</td></tr><tr><td>

sent\_to\_account

</td><td>

Account number to which the funds were erroneously sent.Data type: String

 Maximum length: 250

</td></tr><tr><td>

sent\_to\_beneficiary

</td><td>

Name of the beneficiary to whom the funds were erroneously sent.Data type: String

 Maximum length: 250

</td></tr><tr><td>

sent\_to\_routing

</td><td>

Routing number or sort code of the bank to which the funds were erroneously sent.Data type: String

 Maximum length: 250

</td></tr><tr><td>

service\_definition

</td><td>

Sys\_id of the definition of service associated with this account. Located in the Service Definition \[sn\_bom\_service\_definition\] table.Data type: String

</td></tr><tr><td>

service\_offering

</td><td id="d2279e772">

Sys\_id of the service offering associated with the payment inquiry. Service offerings uniquely define the level of service in terms of availability, scope, pricing, and packaging options.Data type: String

Table: Service Offering \[service\_offering\]

</td></tr><tr id="pay_inquiry_case-short_description-row"><td>

short\_description

</td><td id="pay_inquiry_case-short_description-entry">

Concise description of the case. Data type: String

 Maximum length: 160

</td></tr><tr><td>

skills

</td><td id="d2279e799">

Sys\_ids of the skills needed to complete the case.Data type: String

Maximum length: 4,000

Table: Skill \[cmn\_skill\]

</td></tr><tr id="pay_inquiry_case-sla_due-row"><td>

sla\_due

</td><td id="pay_inquiry_case-sla_due-entry">

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sn\_app\_cs\_social\_social\_profile

</td><td id="d2081e1417">

Sys\_id of the social media profile associated with the case.Data type: String

Table: Social Profile \[sn\_app\_cs\_social\_social\_profile\]

</td></tr><tr><td>

sold\_product

</td><td>

Sys\_id of the financial account of the customer from where the payment was sent in error. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String

</td></tr><tr><td>

stage

</td><td id="casetable-stage-entry">

Stage of the inquiry, such as Closed Complete, Closed Rejected, Document Check, Authorization, and so on.Data type: String

Maximum length: 40

</td></tr><tr id="pay_inquiry_case-state-row"><td>

state

</td><td id="pay_inquiry_case-state-entry">

Current state of the case. Possible values:

 -   1: New
-   2: Open
-   3: Awaiting Info
-   4: Resolved
-   5: Closed

 Data type: Number \(Integer\)

 Maximum length: 40

 Default: 1

</td></tr><tr><td>

subcategory

</td><td id="d2081e1489">

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

support\_manager

</td><td id="d2081e1505">

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

sync\_driver

</td><td id="d2081e1518">

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr id="pay_inquiry_case-sys_class_name-row"><td>

sys\_class\_name

</td><td id="pay_inquiry_case-sys_class_name-entry">

Table that contains the case record.Data type: String

 Maximum length: 80

</td></tr><tr id="pay_inquiry_case-sys_created_by-row"><td>

sys\_created\_by

</td><td id="pay_inquiry_case-sys_created_by-entry">

Person that initially opened the case.Data type: String

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-sys_created_on-row"><td>

sys\_created\_on

</td><td id="pay_inquiry_case-sys_created_on-entry">

Date and time when the case was initially created.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-sys_domain-row"><td>

sys\_domain

</td><td id="pay_inquiry_case-sys_domain-entry">

Domain associated with the case.Data type: String

 Maximum length: 32

 Default: global

</td></tr><tr id="pay_inquiry_case-sys_domain_path-row"><td>

sys\_domain\_path

</td><td id="pay_inquiry_case-sys_domain_path-entry">

Domain path.Data type: String

 Maximum length: 255

 Default: /

</td></tr><tr id="pay_inquiry_case-sys_sys_id-row"><td>

sys\_id

</td><td id="pay_inquiry_case-sys_sys_id-entry">

Unique identifier for the case.Data type: String

 Maximum length: 32

</td></tr><tr id="pay_inquiry_case-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="pay_inquiry_case-sys_mod_count-entry">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="pay_inquiry_case-sys_updated_by-entry">

Person that last updated the case.Data type: String

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="pay_inquiry_case-sys_updated_on-entry">

Date and time when the case was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

task\_effective\_number

</td><td id="d2279e984">

Identifying number. If the task has a Universal Request associated with it, it's the UR number. Otherwise, it's the current task number.

Data type: String

Maximum length: 40

</td></tr><tr><td>

time\_worked

</td><td id="d2279e999">

Total amount of time worked on the case.Data type: String \(Timer\)

Maximum length: 40

</td></tr><tr><td>

total\_amount

</td><td>

Total currency amount of the payments that were made in error under this inquiry case.Data type: String \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

transaction\_id

</td><td>

Unique transaction identifier for this payment inquiry.Data type: String

 Maximum length: 150

</td></tr><tr><td>

universal\_request

</td><td id="d2279e1013">

Sys\_id of a universal task that this inquiry is part of.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

upon\_approval

</td><td id="d2279e1026">

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

upon\_reject

</td><td id="d2279e1051">

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

urgency

</td><td id="d2279e1076">

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Maximum length: 40

Default: 3

</td></tr><tr><td>

user\_input

</td><td id="d2279e1104">

Additional user input.Data type: String \(User Input\)

Maximum length: 4,000

</td></tr><tr><td>

variables

</td><td id="d2279e1117">

Name-value pairs of variables associated with the case.Data type: String \(Variables\)

Maximum length: 40

</td></tr><tr id="pay_inquiry_case-watch_list-row"><td>

watch\_list

</td><td id="pay_inquiry_case-watch_list-entry">

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed. Located in the User \[sys\_user\] table. Data type: Array \(List\)

 Maximum length: 4,000

</td></tr><tr><td>

wf\_activity

</td><td id="d2279e1146">

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr id="pay_inquiry_case-work_end-row"><td>

work\_end

</td><td id="pay_inquiry_case-work_end-entry">

Date and time work ended on the case.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr id="pay_inquiry_case-work_notes-row"><td>

work\_notes

</td><td id="pay_inquiry_case-work_notes-entry">

Information about how to resolve the case, or steps taken to resolve it.Data type: String \(Journal Input\)

 Maximum length: 4,000

</td></tr><tr id="pay_inquiry_case-work_notes_list-row"><td>

work\_notes\_list

</td><td id="pay_inquiry_case-work_notes_list-entry">

List of sys\_ids of the internal users who receive notifications about this case when work notes are added. Located in the User \[sys\_user\] table. Data type: Array \(List\)

 Maximum length: 4,000

</td></tr><tr id="pay_inquiry_case-work_start-row"><td>

work\_start

</td><td id="pay_inquiry_case-work_start-entry">

Date and time that work started on the case.Data type: String \(Date\)

 Maximum length: 40

</td></tr></tbody>
</table>## Personal Checking Account \[sn\_bom\_checking\_account\] table

<table id="d2116e43"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="d2074e70">

Sys\_id of the account record associated with the case. Located in the Account \[customer\_account\] table. Data type: String

</td></tr><tr><td>

account\_number

</td><td>

Customer's account number. By default, this is the display value for the record.Data type: String

 Maximum length: 40

</td></tr><tr><td>

accrued\_interest

</td><td>

Amount of accrued interest as of the date it is being viewed.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

active

</td><td>

Flag that indicates whether the account is active.Possible values:

-   true: Account is currently active.
-   false: Account is inactive.

 Data type: Boolean

 Default: true

</td></tr><tr><td>

application\_id

</td><td>

Unique identifier of the application submitted when applying for the checking account.Data type: String

 Maximum length: 255

</td></tr><tr><td>

balance

</td><td>

Amount currently in the checking account.Data type: Number \(Currency\)

 Maximum length: 20

</td></tr><tr><td>

base\_currency

</td><td>

Sys\_id of the base currency used by the credit card. Located in the Currency \[fx\_currency\] table.Data type: String \(Reference\)

</td></tr><tr><td>

closure\_date

</td><td>

Date that the checking account account was closed.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

consumer

</td><td id="sold_product-consumer-entry">

Business-to-consumer cases only. Sys\_id of the person to contact with regards to this case. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

customer\_class

</td><td>

Free-form classification of customer, such as Premier, Standard, or VIP.Data type: String

 Maximum length: 40

</td></tr><tr><td>

end\_date

</td><td>

Date the checking account ends.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

external\_id

</td><td id="financial_account-external_id-entry">

Unique identifier used to cross-reference this credit card account to a record in an external system, such as a credit card insurance ID.Data type: String

 Maximum length: 255

</td></tr><tr><td>

interest\_credit\_account

</td><td>

Sys\_id of the deposit account associated with this checking account. Located in the Deposit Account \[sn\_bom\_deposit\_account\] table.Data type: String

</td></tr><tr><td>

interest\_rate\_apy

</td><td>

Annual percentage yield for the checking account.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

interest\_rate\_end\_date

</td><td>

End date of the current interest rate.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

interest\_rate\_start\_date

</td><td>

Start date of the current interest rate.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

name

</td><td>

Full name of the primary person associated with the checking account.Data type: String

 Maximum length: 255

</td></tr><tr><td>

number

</td><td id="d2074e105">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

open\_date

</td><td>

Date when the checking account was first opened.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

other\_margin

</td><td>

Preferential discounts that are applicable to a category of customers, such as minors or senior citizens.Data type: String

 Maximum length: 40

</td></tr><tr><td>

parent\_sold\_product

</td><td id="d2074e119">

Sys\_id of the parent product associated with this entity. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String \(Reference\)

</td></tr><tr><td>

product

</td><td>

Sys\_id of the of the customer checking account. Located in the Product Model \[cmdb\_model\] table.Data type: String \(Reference\)

</td></tr><tr><td>

request\_channel

</td><td>

Type of communications channel \(digital or banker assisted\) the customer used to make the credit limit request.Data type: String

 Maximum length: 40

</td></tr><tr><td>

secondary\_consumer

</td><td id="financial_account-secondary_consumer-entry">

Sys\_id of the secondary customer's account. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

sourced\_channel

</td><td id="financial_account-sourced_channel-entry">

Source of the customer's business, such as broker or customer referral.Data type: String

 Maximum length: 40

</td></tr><tr><td>

start\_date

</td><td>

Date when the checking account was opened.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

statement\_frequency

</td><td id="financial_account-statement_frequency-entry">

Frequency of statements sent to the customer, such as monthly, quarterly, bi-annually, or annually.Data type: String

 Maximum length: 40

</td></tr><tr><td>

statement\_mode

</td><td id="financial_account-statement_mode-entry">

Method in which the statement is delivered to the customer, such as physical or online.Data type: String

 Maximum length: 40

</td></tr><tr><td>

status

</td><td>

Current status of the account, such as active, blocked, closed, cancelled, and so on.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_class\_name

</td><td id="d2074e142">

Table that contains the case record.Data type: String

 Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td id="d2074e156">

Person that initially opened the case.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="d2074e170">

Date and time when the case was initially created.Data type: String \(Date\)

 Maximum length: 40

</td></tr><tr><td>

sys\_domain

</td><td id="d2074e184">

Domain associated with the case.Data type: String

 Maximum length: 32

 Default: global

</td></tr><tr><td>

sys\_id

</td><td>

Unique identifier of the credit card record.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td id="d2074e216">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

 Maximum length: 40

</td></tr><tr><td>

sys\_updated\_by

</td><td id="d2074e230">

Person that last updated the case.Data type: String

 Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td id="d2074e244">

Date and time when the case was last updated.Data type: String \(Date\)

 Maximum length: 40

</td></tr></tbody>
</table>## Personal Loan \[sn\_bom\_personal\_loan\] table

<table id="d2079e43"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="d2081e65">

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

account\_number

</td><td>

Customer's account number. By default, this is the display value for the record.Data type: String

Maximum length: 40

</td></tr><tr><td>

accrued\_interest

</td><td>

Amount of accrued interest as of the date it is being viewed.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

active

</td><td>

Flag that indicates whether the account is active.Possible values:

-   true: Account is currently active.
-   false: Account is inactive.

Data type: Boolean

Default: true

</td></tr><tr><td>

amount

</td><td>

Sanctioned loan amount.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

application\_id

</td><td>

Unique identifier of the application submitted when applying for the personal loan.Data type: String

Maximum length: 255

</td></tr><tr><td>

apr

</td><td>

Annual percentage rate for the personal loan.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

balance

</td><td>

Outstanding balance on the loan.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

base\_currency

</td><td>

Sys\_id of the base currency used by the loan. Located in the Currency \[fx\_currency\] table.Data type: String \(Reference\)

</td></tr><tr><td>

closure\_date

</td><td>

Date that the personal loan account was closed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

consumer

</td><td>

Sys\_id of the primary consumer record associated with the loan. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr><td>

cosigner

</td><td>

Sys\_id of the cosigner consumer record associated with the loan. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr><td>

credit\_facility\_id

</td><td>

Unique identifier of the credit facility linked to the loan.Data type: String

Maximum length: 255

</td></tr><tr><td>

customer\_class

</td><td>

Free-form classification of customers, such as Premier, Standard, or VIP.Data type: String

Maximum length: 40

</td></tr><tr><td>

days\_past\_due

</td><td>

Number of days that the current loan payment is past due.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

delinquency\_status

</td><td>

Flag that indicates whether the account is currently delinquent.Possible values:

-   Yes: Account is delinquent
-   No: Account is not delinquent

Data type: String

Maximum length: 40

</td></tr><tr><td>

disbursed\_amout

</td><td>

Total amount of money that has been borrowed by the associated customer.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

document\_id

</td><td>

Unique identifier of the documents associated with this mortgage in an external document management system.Data type: String

Maximum length: 255

</td></tr><tr><td>

end\_date

</td><td>

End date of the personal loan.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

external\_id

</td><td>

Unique identifier used to cross-reference this loan account to a record in an external system.Data type: String

Maximum length: 255

</td></tr><tr><td>

federal\_backed\_load

</td><td>

Flag that indicates whether the associated loan is federally backed.Possible values:

-   Yes: Federally backed loan
-   No: Not a federally backed loan

Data type: String

Maximum length: 40

</td></tr><tr><td>

grace\_period\_for repayment

</td><td>

Number of days that a customer has after the due date to send in a payment without penalties.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

guarantor

</td><td>

Sys\_id of the person that is guaranteeing the loan. Located in the Consumer \[csm\_consumer\] table.Data type: String \(Reference\)

</td></tr><tr><td>

interest\_rate

</td><td>

Current interest rate of the loan.Data type: Number \(Floating-point\)

Maximum length: 40

</td></tr><tr><td>

interest\_type

</td><td>

Type of interest associated with the loan, such as fixed or floating.Data type: String

Maximum length: 40

</td></tr><tr><td>

is\_lending\_insured

</td><td>

Flag that indicates whether the account is insured.Possible values:

-   true: Account is insured.
-   false: Account isn't insured.

 Data type: Boolean

</td></tr><tr><td>

last\_payment\_amount

</td><td>

Amount of the most recent payment made on the loan.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

last\_payment\_date

</td><td>

Date of the most recent payment made on the loan.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

last\_reviewed\_on

</td><td>

Date the loan was last reviewed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

loan\_classification

</td><td>

Classification of the loan, such as standard, sub-standard, doubtful, or loss assets.Data type: String

Maximum length: 40

</td></tr><tr><td>

maturity\_date

</td><td>

Date on which the loan becomes due.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

moratorium\_end\_date

</td><td>

End date of any imposed moratorium \(suspension of payment.\)Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

moratorium\_period

</td><td>

Period for which the customer has a suspension of loan repayment, such as 6 months, 1 year, 2 years, and so on.Data type: String

Maximum length: 40

</td></tr><tr><td>

moratorium\_start\_date

</td><td>

Date on which the customer suspended payments on the loan.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

name

</td><td>

Full name of the primary person responsible for the loan.Data type: String

Maximum length: 255

</td></tr><tr><td>

next\_review\_on

</td><td>

Date on which the loan is to be reviewed.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

no\_of\_installments

</td><td>

Number of payments due on the loan.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

no\_of\_installment\_deferrals\_made

</td><td>

Number of times the customer deferred their payment on the loan.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

number

</td><td id="d2074e105">

Case number.Data type: String

 Maximum length: 40

</td></tr><tr><td>

open\_date

</td><td>

Date when the personal loan account was first opened.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

parent\_sold\_product

</td><td id="d2074e119">

Sys\_id of the parent product associated with this entity. Located in the Sold Product \[sn\_install\_base\_sold\_product\] table.Data type: String \(Reference\)

</td></tr><tr><td>

pending\_installments

</td><td>

Number of payments remaining on the loan.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

prepayment\_allowed

</td><td>

Flag that indicates whether the loan allows prepayments.Possible values:

-   Yes: Prepayments allowed
-   No: Prepayments not allowed

Data type: String

Maximum length: 40

</td></tr><tr><td>

principal\_balance

</td><td>

Amount of the remaining loan principal.Data type: Number \(Currency\)

Maximum length: 20

</td></tr><tr><td>

product

</td><td>

Sys\_id of the product model of the asset associated to the case. Located in the Product Model \[cmdb\_model\] table.Data type: String \(Reference\)

</td></tr><tr><td>

purpose

</td><td>

How the funds of the loan will be used by the customer, such as working capital or equipment purchase.Data type: String

Maximum length: 40

</td></tr><tr><td>

request\_channel

</td><td>

Type of communications channel \(digital or banker assisted\) the customer used to make the credit limit request.Data type: String

Maximum length: 40

</td></tr><tr><td>

risk\_rating

</td><td>

Risk associated with this loan account.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

rollover\_mode

</td><td>

Method in which a customer can extend the loan, such as auto rollover or manual rollover.Data type: String

Maximum length: 40

</td></tr><tr><td>

rollover\_possible

</td><td>

Flag that indicates whether the balance due on the loan can be rolled over in the future.Possible values:

-   Yes: Rollover is available
-   No: Rollover isn't available

Data type: String

Maximum length: 40

</td></tr><tr><td>

secondary\_consumer

</td><td>

Sys\_id of the secondary customer's account. Located in the Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

sourced\_channel

</td><td>

Source of the customer's business, such as broker or customer referral.Data type: String

Maximum length: 40

</td></tr><tr><td>

start\_date

</td><td>

Start date of the personal loan.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

statement\_frequency

</td><td>

Frequency of statements sent to the customer, such as monthly, quarterly, bi-annually, or annually.Data type: String

Maximum length: 40

</td></tr><tr><td>

statement\_mode

</td><td>

Method in which the statement is delivered to the customer, such as physical or online.Data type: String

Maximum length: 40

</td></tr><tr><td>

status

</td><td>

Current status of the account, such as issued, active, blocked, closed, cancelled, and so on.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_class\_name

</td><td id="d2074e142">

Table that contains the case record.Data type: String

 Maximum length: 80

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the entity that created this record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time that the record was originally created.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

sys\_domain

</td><td>

Unique identifier of the domain associated with the record.Data type: String

Maximum length: 32

Default: global

</td></tr><tr><td>

sys\_id

</td><td>

Unique identifier of the personal loan record.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td>

Number of times the record has been updated.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the entity that last updated this record.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time that the record was last updated.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

term

</td><td>

Number of terms associated with the loan.Data type: Number \(Integer\)

Maximum length: 40

</td></tr></tbody>
</table>