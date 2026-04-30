---
title: Example custom scripts for Password Reset
description: The example scripts perform a user account lookup and processes an identification form, define a credential store, and create an identification type.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Password Reset script includes, Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Example custom scripts for Password Reset

The example scripts perform a user account lookup and processes an identification form, define a credential store, and create an identification type.

## Perform a user account lookup and process an identification form

The main script calls two extension scripts, one to perform the user account lookup, and the other to process the identification form.

```
// User account lookup 
var lookupExtensionSysId = getExtensionScriptSysId('SampleUserAccountLookupExtension', 'user_account_lookup');
var lookupExtension = new SNC.PwdExtensionPoint(lookupExtensionSysId);
 
// Setup parameters required for this extension type - userId
var params = new SNC.PwdExtensionPointParameter() ;
params.userId= 'joe.employee';
 
// Invoke the extension 
var answer = lookupExtension.process(params);
gs.print('user: ' + answer);
 
//Form processor sample - Identification form processor
var identExtensionSysId = getExtensionScriptSysId('SampleIdentificationProcessorExtension', 'identification_form_processor');
var identificationExtension = new SNC.PwdExtensionPoint(identExtensionSysId); 
 
// Setup parameters required for this extension type - processId
var params = new SNC.PwdExtensionPointParameter() ;
params.processId = 'pwdreq1234';
 
// Simulate the posted form parameter for the indentification processor
var request = new SNC.PwdExtensionPointParameter() ; // A real life case will inject it's own request object
request.setParameter('sysparm_user_id', 'joe.employee'); 
 
var userIdentity = identificationExtension.processForm(params, request);
gs.print('identity: ' + userIdentity);
 
// Simple helper to return the sys-id for a given extension script
function getExtensionScriptSysId(scriptName, category) {
   var result;
   var now_GR = new GlideRecord('sys_script_include');
   gr.addQuery('name', scriptName);
   gr.addQuery('script', 'CONTAINS', 'category: \'password_reset.extension.' + category + '\'');
   gr.query();
 
   if (gr.next() ) {
     result = gr.getValue('sys_id');
   }
   return result;
}
```

## Define a credential store

The following is an example of an extended process function in the User Account Lookup category used to define a credential store. To create this extension script, go to **Password Reset** &gt; **Extensions** &gt; **New extension script** and create a new script as described in [Create an Extension Script](../task/t_CreateAnExtensionScript.md). To configure the User Lookup in a Password Reset process, see [Credential Stores](../concept/c_CredentialStores.md).

```

<?xml version="1.0" encoding="UTF-8"?>
<record_update table="sys_script_include">
  <sys_script_include action="INSERT_OR_UPDATE">
    <active>true</active>
    <client_callable>false</client_callable>
    <description>Simple account lookup that returns the supplied user id</description>
    <name>SampleUserAccountLookupExtension</name>
    <script><![CDATA[var SampleUserAccountLookupExtension = Class.create();
SampleUserAccountLookupExtension.prototype = {
  category: 'password_reset.extension.user_account_lookup',	// DO NOT REMOVE THIS LINE!
 
  /**********
   * Returns the credential-store account id for a given user
   * 
   * @param params.userId  The sys-id of the user being checked (table: sys_user)
   * @return               The credential-store account-id (string) for a given user
   **********/
  process: function(params) {
    return params.userId;
  },
 
  type: 'SampleUserAccountLookupExtension'
 
};]]></script>
    <sys_created_by>admin</sys_created_by>
    <sys_created_on>2013-07-30 16:44:55</sys_created_on>
    <sys_id>2df5a103d73201002bb9af728e610333</sys_id>
    <sys_mod_count>1</sys_mod_count>
    <sys_updated_by>admin</sys_updated_by>
    <sys_updated_on>2013-07-30 16:46:00</sys_updated_on>
  </sys_script_include>
  <sys_app_file action="INSERT_OR_UPDATE">
    <customer_update>false</customer_update>
    <publish_override/>
    <replace_on_upgrade>false</replace_on_upgrade>
    <restore/>
    <sys_app/>
    <sys_code>!!1W4/</sys_code>
    <sys_created_by>admin</sys_created_by>
    <sys_created_on>2013-07-30 16:44:55</sys_created_on>
    <sys_id>8306e143d73201002bb9af728e6103d3</sys_id>
    <sys_mod_count>0</sys_mod_count>
    <sys_name>SampleUserAccountLookupExtension</sys_name>
    <sys_parent/>
    <sys_path>!!1W4/</sys_path>
    <sys_policy/>
    <sys_source_deleted>false</sys_source_deleted>
    <sys_source_id>2df5a103d73201002bb9af728e610333</sys_source_id>
    <sys_source_table>sys_script_include</sys_source_table>
    <sys_type>code</sys_type>
    <sys_update_name>sys_script_include_2df5a103d73201002bb9af728e610333</sys_update_name>
    <sys_updated_by>admin</sys_updated_by>
    <sys_updated_on>2013-07-30 16:46:00</sys_updated_on>
  </sys_app_file>
</record_update>        
      
```

## Create an identification type

The following is an example of an extended processForm function in the Identification Form Processor category that can be used to create an identification type. To create this extension script, go to **Password Reset** &gt; **Extensions** &gt; **New extension script** and create a new script as described in [Create an Extension Script](../task/t_CreateAnExtensionScript.md).

```
<?xml version="1.0" encoding="UTF-8"?>
<record_update table="sys_script_include">
  <sys_script_include action="INSERT_OR_UPDATE">
    <active>true</active>
    <client_callable>false</client_callable>
    <description>Script that processes an identification form.&#13;
Returns the sys-id of the user that corresponds to the requested input; if no user was found, null should be returned.&#13;
</description>
    <name>SampleIdentificationProcessorExtension</name>
    <script><![CDATA[var SampleIdentificationProcessorExtension = Class.create();
SampleIdentificationProcessorExtension.prototype = {
  category: 'password_reset.extension.identification_form_processor',	// DO NOT REMOVE THIS LINE!
 
  /**********
   * Process the identification form request, and returns the user's sys_id.  if user was not identified return null.
   *
   * @param params.processId   The sys-id of the calling password-reset process (table: pwd_process)
   * @param request            The form request object. fields in the form can be accessed using: request.getParameter('<element-id>')
   *                           Supported request paramters:
   *                               sysparm_user_id - the user identifier value entered in the form.                        
   * @return The sys-id of the user that corresponds to the requested input; if no user was found, null should be returned.
   **********/
  processForm: function(params, request) {
    return request.getParameter('sysparm_user_id') + '_' + params.processId;
  },
 
  type: 'SampleIdentificationProcessorExtension'
 
};]]></script>
    <sys_created_by>admin</sys_created_by>
    <sys_created_on>2013-07-30 17:00:28</sys_created_on>
    <sys_id>3a79a503d73201002bb9af728e610349</sys_id>
    <sys_mod_count>1</sys_mod_count>
    <sys_updated_by>admin</sys_updated_by>
    <sys_updated_on>2013-07-30 17:08:41</sys_updated_on>
  </sys_script_include>
  <sys_app_file action="INSERT_OR_UPDATE">
    <customer_update>false</customer_update>
    <publish_override/>
    <replace_on_upgrade>false</replace_on_upgrade>
    <restore/>
    <sys_app/>
    <sys_code>!!1W5/</sys_code>
    <sys_created_by>admin</sys_created_by>
    <sys_created_on>2013-07-30 17:00:28</sys_created_on>
    <sys_id>4799ed03d73201002bb9af728e610333</sys_id>
    <sys_mod_count>0</sys_mod_count>
    <sys_name>SampleIdentificationProcessorExtension</sys_name>
    <sys_parent/>
    <sys_path>!!1W5/</sys_path>
    <sys_policy/>
    <sys_source_deleted>false</sys_source_deleted>
    <sys_source_id>3a79a503d73201002bb9af728e610349</sys_source_id>
    <sys_source_table>sys_script_include</sys_source_table>
    <sys_type>code</sys_type>
    <sys_update_name>sys_script_include_3a79a503d73201002bb9af728e610349</sys_update_name>
    <sys_updated_by>admin</sys_updated_by>
    <sys_updated_on>2013-07-30 17:08:41</sys_updated_on>
  </sys_app_file>
</record_update>
```

## Use the process and processForm extensions

This example shows a script that uses two sample extensions, one process extension and one processForm extension.

```
// User account lookup 
var lookupExtensionSysId = getExtensionScriptSysId('SampleUserAccountLookupExtension','user_account_lookup');
var lookupExtension =new SNC.PwdExtensionPoint(lookupExtensionSysId);
 
// Setup parameters required for this extension type - userId
var params =new SNC.PwdExtensionPointParameter();
params.userId='joe.employee';
 
// Invoke the extension 
var answer = lookupExtension.process(params);
gs.print('user: '+ answer);
 
 
//Form processor sample - Identification form processor
var identExtensionSysId = getExtensionScriptSysId('SampleIdentificationProcessorExtension','identification_form_processor');
var identificationExtension =new SNC.PwdExtensionPoint(identExtensionSysId); 
 
// Setup parameters required for this extension type - processId
var params =new SNC.PwdExtensionPointParameter();
params.processId='pwdreq1234';
 
// Simulate the posted form parameter for the indentification processor
var request =new SNC.PwdExtensionPointParameter();// A real life case will inject it's own request object
request.setParameter('sysparm_user_id','joe.employee'); 
 
var userIdentity = identificationExtension.processForm(params, request);
gs.print('identity: '+ userIdentity);
 
// Simple helper to return the sys-id for a given extension scriptfunction 
getExtensionScriptSysId(scriptName, category){
var result;
var now_GR =new GlideRecord('sys_script_include');
   gr.addQuery('name', scriptName);
   gr.addQuery('script','CONTAINS','category: \'password_reset.extension.'+ category +'\'');
   gr.query();
 
   if(gr.next()){
     result = gr.getValue('sys_id');}return result;}
```

process function:

```
<?xml version="1.0" encoding="UTF-8"?><record_update table="sys_script_include"><sys_script_include action="INSERT_OR_UPDATE"><active>true</active><client_callable>false</client_callable><description>Simple account lookup that returns the supplied user id</description><name>SampleUserAccountLookupExtension</name><script><![CDATA[var SampleUserAccountLookupExtension =Class.create();
SampleUserAccountLookupExtension.prototype={
  category:'password_reset.extension.user_account_lookup',// DO NOT REMOVE THIS LINE!
 
  /**********
   * Returns the credential-store account id for a given user
   * 
   * @param params.userId  The sys-id of the user being checked (table: sys_user)
   * @return               The credential-store account-id (string) for a given user
   **********/
  process:function(params){return params.userId;},
 
  type:'SampleUserAccountLookupExtension'
 
};]]></script><sys_created_by>admin</sys_created_by><sys_created_on>2013-07-3016:44:55</sys_created_on><sys_id>2df5a103d73201002bb9af728e610333</sys_id><sys_mod_count>1</sys_mod_count><sys_updated_by>admin</sys_updated_by><sys_updated_on>2013-07-3016:46:00</sys_updated_on></sys_script_include><sys_app_file action="INSERT_OR_UPDATE"><customer_update>false</customer_update><publish_override/><replace_on_upgrade>false</replace_on_upgrade><restore/><sys_app/><sys_code>!!1W4/</sys_code><sys_created_by>admin</sys_created_by><sys_created_on>2013-07-3016:44:55</sys_created_on><sys_id>8306e143d73201002bb9af728e6103d3</sys_id><sys_mod_count>0</sys_mod_count><sys_name>SampleUserAccountLookupExtension</sys_name><sys_parent/><sys_path>!!1W4/</sys_path><sys_policy/><sys_source_deleted>false</sys_source_deleted><sys_source_id>2df5a103d73201002bb9af728e610333</sys_source_id><sys_source_table>sys_script_include</sys_source_table><sys_type>code</sys_type><sys_update_name>sys_script_include_2df5a103d73201002bb9af728e610333</sys_update_name><sys_updated_by>admin</sys_updated_by><sys_updated_on>2013-07-3016:46:00</sys_updated_on></sys_app_file></record_update>
```

processForm function:

```
<?xml version="1.0" encoding="UTF-8"?><record_update table="sys_script_include"><sys_script_include action="INSERT_OR_UPDATE"><active>true</active><client_callable>false</client_callable><description>Script that processes an identification form.&#13;
Returns the sys-id of the user that corresponds to the requested input;if no user was found,null should be returned.&#13;</description><name>SampleIdentificationProcessorExtension</name><script><![CDATA[var SampleIdentificationProcessorExtension =Class.create();
SampleIdentificationProcessorExtension.prototype={
  category:'password_reset.extension.identification_form_processor',// DO NOT REMOVE THIS LINE!
 
  /**********
   * Process the identification form request, and returns the user's sys_id.  if user was not identified return null.
   *
   * @param params.processId   The sys-id of the calling password-reset process (table: pwd_process)
   * @param request            The form request object. fields in the form can be accessed using: request.getParameter('<element-id>')
   *                           Supported request paramters:
   *                               sysparm_user_id - the user identifier value entered in the form.                        
   * @return The sys-id of the user that corresponds to the requested input; if no user was found, null should be returned.
   **********/
  processForm:function(params, request){return request.getParameter('sysparm_user_id')+'_'+ params.processId;},
 
  type:'SampleIdentificationProcessorExtension'
 
};]]></script><sys_created_by>admin</sys_created_by><sys_created_on>2013-07-3017:00:28</sys_created_on><sys_id>3a79a503d73201002bb9af728e610349</sys_id><sys_mod_count>1</sys_mod_count><sys_updated_by>admin</sys_updated_by><sys_updated_on>2013-07-3017:08:41</sys_updated_on></sys_script_include><sys_app_file action="INSERT_OR_UPDATE"><customer_update>false</customer_update><publish_override/><replace_on_upgrade>false</replace_on_upgrade><restore/><sys_app/><sys_code>!!1W5/</sys_code><sys_created_by>admin</sys_created_by><sys_created_on>2013-07-3017:00:28</sys_created_on><sys_id>4799ed03d73201002bb9af728e610333</sys_id><sys_mod_count>0</sys_mod_count><sys_name>SampleIdentificationProcessorExtension</sys_name><sys_parent/><sys_path>!!1W5/</sys_path><sys_policy/><sys_source_deleted>false</sys_source_deleted><sys_source_id>3a79a503d73201002bb9af728e610349</sys_source_id><sys_source_table>sys_script_include</sys_source_table><sys_type>code</sys_type><sys_update_name>sys_script_include_3a79a503d73201002bb9af728e610349</sys_update_name><sys_updated_by>admin</sys_updated_by><sys_updated_on>2013-07-3017:08:41</sys_updated_on></sys_app_file></record_update>
```

