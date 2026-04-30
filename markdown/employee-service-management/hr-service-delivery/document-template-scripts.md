---
title: Document template scripts
description: With document template scripts, you can dynamically change the text in the body of the HTML template. Document template scripts allow you to perform simple tasks, such as displaying HR data, and complex ones, such as making advanced database queries.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Document Templates of type HTML, Configure, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Document template scripts

With document template scripts, you can dynamically change the text in the body of the HTML template. Document template scripts allow you to perform simple tasks, such as displaying HR data, and complex ones, such as making advanced database queries.

You can add a `${template_script:script name}` embedded script tag to the body of the HTML template, replacing script name with the name of the script you created. This makes it easy to use the same scripts in multiple document templates. You can create a script by navigating to**Document Templates** &gt; **Document Templates Script**.

## Example of how to create and use a document template script in an HTML template

1.  The employee\_emergency\_contacts script populates the emergency contacts list in an Employee Profile document.

    ```
    (function runTemplateScript(target /*GlideRecord for target task*/ ) {
    	var getHeaderCell = function(label) {
    		return '<th style="border: 1px solid #dddddd; text-align: left; padding: 8px;">' + label + '</th>';
    	};	
    	var getDataCell = function(value) {
    		return '<td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">' + value + '</td>';
    	};
    	
    	var html = '';
    	var hrTaskGr = new GlideRecord('sn_hr_core_contact');
    	hrTaskGr.addQuery('user', target.getValue('subject_person'));
    	hrTaskGr.query();
    	while(hrTaskGr.next()) {
    		html = html + '<tr>';
    		html = html + getDataCell(hrTaskGr.getDisplayValue('name'));
    		html = html + getDataCell(hrTaskGr.getDisplayValue('mobile_phone'));
    		html = html + getDataCell(hrTaskGr.getDisplayValue('relation_to_employee'));
    		html = html + '</tr>';
    	}
    	
    	if(!gs.nil(html))
    		html = '<h4>Emergency Contact Information</h4><table width="500px;"><tr>' + getHeaderCell('Name') + getHeaderCell('Mobile phone') + getHeaderCell('Relationship') + html + '</table>';
    	
    	return html;
    })(target);
    ```

2.  The employee\_emergency\_contacts script is called in an HTML document template by typing **$ \{template\_script:employee\_emergency\_contacts\}** in the body of the Employee Profile HTML document template.

    ![A template showing fields, including a script input area that has basic editing controls.](document-template-scripts.png)

3.  The Employee Profile HTML document template is selected on a case and the document template is generated with emergency contacts list as follows:

    ![The HR Case form where you can enter "Employee Profile" in the Document template field.](document-template-scripts-case.png)

    ![A preview of the Employee Profile document.](document-template-scripts-preview.png)


## Example of how document template script translates text in an HTML template

Following is an employee\_emergency\_contacts script that populates the emergency contacts list in an Employee Profile document.

`docTemplate` in this script references to the document template record, which helps in identifying the language and date format that are selected on the document template. `getDisplayValueLang` is an API that helps in changing the language of dynamic tokens to the display language set in the **Template language** field in a document template. `getByFormat` is an API that helps in displaying the date in the format set in the **Template date format** field in a document template.

```
(function runTemplateScript(target /*GlideRecord for target task*/, docTemplate /*GlideRecord for doc template*/) {

    //Add your code here to return the dynamic content for template
    var getHeaderCell = function(label) {
        return '<th style="border: 1px solid #dddddd; text-align: left; padding: 8px;">' + label + '</th>';
    };  
    var getDataCell = function(value) {
        return '<td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">' + value + '</td>';
    };
    
    var html = '';
    var templateLang = docTemplate.getValue('language');
    var templateDateFormat = docTemplate.getValue('template_date_format');
    var hrTaskGr = new GlideRecord('sn_hr_core_contact');
    hrTaskGr.addQuery('user', target.getValue('subject_person'));
    hrTaskGr.query();
    while(hrTaskGr.next()) {
        var dob = hrTaskGr.getDisplayValue('date_of_birth');
        var grDOB = new GlideDateTime(dob);
        html = html + '<tr>';
        html = html + getDataCell(hrTaskGr.getDisplayValue('name'));
        html = html + getDataCell(hrTaskGr.getDisplayValue('mobile_phone'));
        html = html + getDataCell(hrTaskGr.getElement('relation_to_employee').getDisplayValueLang(templateLang));
        html = html + getDataCell(hrTaskGr.getElement('priority').getDisplayValueLang(templateLang));
        html = html + getDataCell(grDOB.getLocalDate().getByFormat(templateDateFormat)
        );
        html = html + '</tr>';
    }
    
    if(!gs.nil(html))
        html = '<h4>Emergency Contact Information</h4><table width="500px;"><tr>' + getHeaderCell('Name') + getHeaderCell('Mobile phone') + getHeaderCell('Relationship') + getHeaderCell('Priority') + getHeaderCell('Date of birth') + html + '</table>';
    
    return html;

})(target, docTemplate);
```

Following is an example of how dynamic tokens are translated in an HTML doc template.

1.  While configuring an HTML template, the template language is selected as German and date format is set to dd/MM/yyyy.![The HR Case Employment Verification Letter template. It displays all the fields and the body text that is used for the letter.](../image/config-lang.png)
2.  The HTML document template is referenced in an HR case.
3.  When the agent previews the document, generates the attachment, or initiates document tasks for participants, priority and relationship fields are translated into the German language, and dates appear in the dd/MM/yyyy format.

    ![The translated preview of the document template. I is translated to German.](../image/preview-output.png)


