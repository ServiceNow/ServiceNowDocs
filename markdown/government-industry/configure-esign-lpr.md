---
title: Configure E-sign in License and Permit Playbook
description: E-Signature enables users to sign their applications from Government Service Portal with a typed or drawn e-signature that implies an acknowledgement to the application.​ This functionality can be optionally configured by an admin upon upgrade.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [License and Permit Playbook, Playbooks, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure E-sign in License and Permit Playbook

E-Signature enables users to sign their applications from Government Service Portal with a typed or drawn e-signature that implies an acknowledgement to the application.​ This functionality can be optionally configured by an admin upon upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Record Producers**.

2.  Select the **Request License** record producer.

3.  Under the Variables tab, select **New**.

4.  Under Type, select **Custom**.

5.  In the **Questions** tab, enter **Esignature for Record Producers** in the Question field, and `esignature_for_record_producers` in the Name field.

6.  In the **Type Specifications** tab, enter **Esignature for License Permit in Portal** in the Widget field.

7.  Select **Submit**.

8.  Under the Variables tab, select **New**.

9.  Under Type, select **Multi Line Text**.

10. Select the checkbox for **Hidden**.

11. In the **Questions** tab, enter **Esignature Variable** in the Question field, and `esignature_variable` in the Name field.

12. If an eligibility checklist is configured for License and Permit Playbook, navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Catalog UI Policies** to create a Catalog UI Policy for the record producer catalog item.

    Switch to the Public Sector Digital Services Core application if prompted.

13. Add a show/hide logic to the script of the record producer for the `esignature_for_record_producers` widget.

14. Append the following code block in the server script of the **Request license** record producer in the **What it will contain** tab.​

    Switch to the Public Sector Digital Services Core application if prompted.

    ```
    if (gs.nil (producer.esignature_variable) || producer. esignature_variable == "") {
    gs. addErrorMessage(gs. getMessage ('Please do the E-signature and click on Accept. '));
    current.setAbortAction(true);
    var caseTable = sn_gsm. GovernmentServicesConstants. LICENSE_PERMIT_CASE;
    var attachment = new GlideSysAttachment();
    var caseRecord = new GlideRecord (caseTable);
    caseRecord.get (current.sys_id) ;
    var fileName = 'applicantESign.png';
    var contentType = "image/png';
    attachment.writeBase64(caseRecord, fileName, contentType, producer.esignature_variable);
    var sigRec = new GlideRecord( 'signature image');
    sigRec.signed_on = new GlideDateTime ().getDisplayValue();
    sigRec.user = gs.getUserID();
    sigRec.table = caseTable;
    sigRec.document = current.sys_id;
    sigRec.is_drawing = true;
    sigRec.active = true;
    sigRec.acknowledgment_text = "This constitutes your electronic signature and has the same legal impact as signing a printed version of this document.";
    var signSysId = sigRec.insert();
    var signRecord = new GlideRecord('signature image');
    signRecord.get (signSysId);
    attachment.writeBase64(signRecord, fileName, contentType, producer.esignature_variable);
    ```

15. Select **Update**


## Result

The **Draw Signature**tab is now be displayed alongside the **Type Signature** tab. When a constituent creates a License and Permit case, the option to type draw a signature is shown. When an application is submitted with an E-Signature, an image is created containing E-Signature of the user, which is then mapped and attached to the corresponding application.​

