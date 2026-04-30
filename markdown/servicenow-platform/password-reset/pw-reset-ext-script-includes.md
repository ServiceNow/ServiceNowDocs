---
title: Password Reset extension scripts
description: Extension scripts allow you to extend Password Reset functionality in credential store, verification, or identification types.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Password Reset script includes, Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset extension scripts

Extension scripts allow you to extend Password Reset functionality in credential store, verification, or identification types.

## Password Reset extension script includes

Each script include is associated with a specific category, which is available in the appropriate field of a Password Reset form.

**Note:** Create extension scripts only from the Password Reset Extension Script form \(**Password Reset** &gt; **Extensions** &gt; **New extension script**\). Extension scripts are special purpose script includes that are not created in the **System Definition** &gt; **Script Includes** interface. To use a script include as an extension script, you must set it to **Active** status.

## 'Enrollment Check' script include category

<table><thead><tr><th>

Script include category

</th><th>

Description

</th><th>

Method signature

</th><th>

Input fields

</th><th>

Output fields

</th></tr></thead><tbody><tr><td>

Enrollment Check

</td><td>

Checks whether a user is enrolled for a given verification.

</td><td>

process\(params\)

</td><td>

Parameters:-   params.userId - The sys\_id of the user to check \(table: sys\_user\).
-   params.verificationId - The sys\_id of the verification to check \(table: pwd\_verification\).

</td><td>

Returns: \(boolean\) true, if the user is enrolled in the specified verification; otherwise, false.

</td></tr></tbody>
</table>This Enrollment Check example signals that the user is enrolled if both expected parameters are supplied. The code would be contained in the **Script** field of an extension script named SampleEnrollmentCheck:

```
var SampleEnrollmentCheck = Class.create ();
SampleEnrollmentCheck. prototype = {
  category:'password_reset.extension.enrollment_check', // DO NOT REMOVE THIS LINE!
 
   /**********
   * Returns boolean telling whether the user is enrolled.
   * This sample returns true if both parameters are supplied, false otherwise 
   *
   * @param params.userId         The sys-id of the user being checked (table: sys_user)
   * @param params.verificationId The sys-id of the verification being checked (table: pwd_verification)
   * @return Boolean indicating whether the user is enrolled into the specified verification
   **********/
  process:function (params) {return (params.userId && params.verificationId)? true:false; },
 
  type:'SampleEnrollmentCheck'};
```

## 'Enrollment Form Processor' script include category

<table><thead><tr><th>

Script include category

</th><th>

Description

</th><th>

Method signature

</th><th>

Input fields

</th><th>

Output fields

</th></tr></thead><tbody><tr><td>

Enrollment Form Processor

</td><td>

Checks whether all necessary information has been collected from the user. Stores the information so it can be used for verification when the user resets their password.

</td><td>

process\(params\)

</td><td>

Parameters:-   params.resetRequestId - The sys\_id of the current Password Reset request \(table: pwd\_reset\_request\).
-   params.userId - The sys\_id of the user to be verified \(table: sys\_user\).
-   params.verificationId - The sys\_id of the verification to be processed \(table: pwd\_verification\).
-   request - The form request object. Fields in the form can be accessed with request.getParameter\('&lt;element-id&gt;'\).

 The following information should be added to the state of the enrollment process:

-   gs.getSession\(\).putProperty\("result.status",status\) - Whether the user was successfully enrolled.
-   gs.getSession\(\).putProperty\("result.message",message\) - An associated message to be returned to the UI, such as a detailed error message.
-   gs.getSession\(\).putProperty\("result.value",value\) - A custom value associated with the enrollment.

</td><td>

Returns: \(boolean\) true, if the user is enrolled in the specified verification; otherwise, false.

</td></tr></tbody>
</table>This example processes an enrollment form submission successfully if the user-submitted response was success. The code would be contained in the **Script** field of an extension script named SampleEnrollmentProcessor:

```
var SampleEnrollmentProcessor = Class.create ();
SampleEnrollmentProcessor.prototype = {
    category: 'password_reset.extension.enrollment_form_processor', // DO NOT REMOVE THIS LINE!
 
     /**********
    * Process the enrollment form request, and return whether the user was successfully enrolled.
    * 
    * @param params.userId         The sys_id of the user trying to enroll (table: sys_user)
    * @param params.verificationId The sys_id of the verification to be enrolled into (table: pwd_verification)
    * @param params.enrollmentId   The sys_id of this enrollment process
    * @param request               The form request object. Felds in the form can be accessed with
    *                                           request.getParameter('<element-id>')
    * @return boolean telling whether the user was successfully enrolled
    * The following information should be added to the state of the enrollment process
    *     gs.getSession().putProperty("result.status",status) - whether the user was successfully enrolled
    *     gs.getSession().putProperty("result.message",message) - an associated message to be returned 
    *             to the UI. Eg. a detailed error message
    *     gs.getSession().putProperty("result.value",value) - custom value associated with the enrollment
    **********/
    processForm:function (params, request) {var verificationId = params.verificationId; var sampleInput = request.getParameter ('sample_input');
 
	 if (gs.nil (verificationId) || (sampleInput!= 'success')) { return false; }
 
	 var now_GR = new GlideRecord ('sys_user');
	now_GR.get (params. userId);
	now_GR.print ('User:' + now_GR.getValue ('user_name') + ' successfully enrolled'); return true; },
    type: 'SampleEnrollmentProcessor' };
```

## 'Identification Form Processor' script include category

<table><thead><tr><th>

Script include category

</th><th>

Description

</th><th>

Method signature

</th><th>

Input fields

</th><th>

Output fields

</th></tr></thead><tbody><tr><td>

Identification Form Processor

</td><td>

Processes an identification form request.

</td><td>

processForm\(params, request\)

</td><td>

Parameters:-   params.processId - The sys\_id of the calling Password Reset process \(table: pwd\_process\).
-   request - The form request object. Fields in the form can be accessed with `request.getParameter('<element-id>')`. Use `request.getParameter('sysparm_user_id')` to get the user ID that was entered into the form.

</td><td>

Returns: the sys\_id of the user that corresponds to the requested input. Returns null, if no user was found.

</td></tr></tbody>
</table>This example attempts to identify the user within the sys\_user table given a user name submitted from the identification form. The code would be contained in the **Script** field of an extension script named PwdIdentifyViaUsername:

```
var PwdIdentifyViaUsername = Class.create ();
PwdIdentifyViaUsername. prototype = {
    category: 'password_reset.extension.identification_form_processor', // DO NOT REMOVE THIS LINE!
 
    initialize: function () { },
 
   /**********
   * Process the identification form request, and returns the user's sys_id. If user was not identified return null.
   *
   * @param params.processId   The sys_id of the calling Password Reset process (table: pwd_process)
   * @param request            The form request object. fields in the form can be accessed with
   *  request.getParameter('<element-id>')
   *  Supported request parameters: sysparm_user_id - the user identifier value entered in the form                       
   * @return The sys_id of the user that corresponds to the requested input; 
   *  if no user was found, null should be returned
   **********/
   processForm: function (params, request) {var processId = params. processId; var sysparm_user_id = request.getParameter ('sysparm_user_id');
      now_GR = new GlideRecord ('sys_user') ;
      now_GR.addQuery ('user_name', sysparm_user_id) ;
      now_GR.query (); if (!now_GR.next ()) {return null; } return now_GR.sys_id;},
 
    type:'PwdIdentifyViaUsername' }
```

## 'Password Generator' script include category

|Script include category|Description|Method signature|Input fields|Output fields|
|-----------------------|-----------|----------------|------------|-------------|
|Password Generator|Returns an auto-generated password.|process\(params\)|Parameters:params.processId - The sys\_id of the calling Password Reset process \(table: pwd\_process\).|Returns: \(String\) an auto-generated password.|

This example randomly generates a password from a base word and numbers. The base word is selected depending on the credential store. The code would be contained in the **Script** field of an extension script named SamplePasswordGenerator:

```
var SamplePasswordGenerator = Class.create ();
SamplePasswordGenerator. prototype = {
  category: 'password_reset.extension.password_generator', // DO NOT REMOVE THIS LINE!
 
   /**********
   * Returns an auto-generated string password.
   * This sample randomly generates 4 digits to add to the password.
   * 
   * @param params.credentialStoreId The sys_id of the target Password Reset credential store to generate 
   *  a password for (table: pwd_cred_store)
   * @return An auto-generated string password
   **********/
  process:function (params) { var basePassword ;
 
	 var now_GR = new GlideRecord ('pwd_cred_store');
	now_GR.addQuery ('name', 'Local ServiceNow Instance');
	now_GR.query (); if (now_GR.next ()) { if (params.credentialStoreId = now_GR.getValue ('sys_id'))
			basePassword = "Password"; else
			basePassword = "Dorwssap"; } return this. generateSimple (basePassword); },
 
  generateSimple:function (base) {var pwd = base; var numbers = '0123456789'; var length = 4;
 
     for (var i  = 0 , n  = numbers. length ; i  < length ; i ++) {
        pwd += numbers.charAt (Math.floor (Math.random () * n) + 1); } return pwd;}, 
 
  type:'SamplePasswordGenerator'} ;
```

## 'Post Reset' script include category

<table><thead><tr><th>

Script include category

</th><th>

Description

</th><th>

Method signature

</th><th>

Input fields

</th><th>

Output fields

</th></tr></thead><tbody><tr><td>

Post Reset

</td><td>

Performs additional operations after the completion of the Password Reset process.

</td><td>

process\(params\)

</td><td>

Parameters:-   params.resetRequestId - The sys\_id of the calling Password Reset process \(table: pwd\_process\).
-   params.wfSuccess - A flag indicating whether the workflow completed successfully. True if, and only if, successful.

</td><td>

Returns: void

</td></tr></tbody>
</table>This example adds failed reset requests to the system log. The code would be contained in the **Script** field for an extension script named PwdPostProcessor':

```
var PwdPostProcessor = Class.create ();
 
PwdPostProcessor. prototype = {
    category: 'password_reset.extension.post_reset_script', // DO NOT REMOVE THIS LINE!
 
    initialize:function () { },
 
     /**********
     * Execute custom actions after the Password Reset process has completed.
    * 
    * @param params.resetRequestId The sys_id of the current Password Reset request (table: pwd_reset_request)
    * @param params.wfSuccess      A flag indicating if the workflow completed sucessfully. 
    *  True if (and only if) successful.
    * @return no return value
    **********/
    process: function (params) {if (!params. wfSuccess) {
           now_GS.log ('[PwdPostProcessor.process] failure post processing for request [' + params. resetRequestId + ']'); }
 
         // We could place actions here that we always want executed return; },
 
    type:'PwdPostProcessor' }
```

## 'User Account Lookup' script include category

|Script include category|Description|Method signature|Input fields|Output fields|
|-----------------------|-----------|----------------|------------|-------------|
|User Account Lookup|Gets the credential store account ID for a given user.|process\(params\)|Parameters:params.userId - The sys\_id of the user being checked \(table: sys\_user\).|Returns: \(String\) the credential store account ID for the given user.|

This example gets the credential store account for a user. This code would be contained in the **Script** field of an extension script named SampleUserAccountLookupExtension:

```
var SampleUserAccountLookupExtension = Class.create ();
SampleUserAccountLookupExtension. prototype = {
  category:'password_reset.extension.user_account_lookup', // DO NOT REMOVE THIS LINE!
 
   /**********
  * Returns the credential store account id for a given user.
  * This sample echoes the user_id supplied as the credential store account id for that user.
  * 
  * @param params.userId  The sys_id of the user being checked (table: sys_user)
  * @return               The credential store account id (string) for a given user
  **********/
  process:function (params) {return params.userId;},
 
  type:'SampleUserAccountLookupExtension' }
```

## 'Verification Form Processor' script include category

<table><thead><tr><th>

Script include category

</th><th>

Description

</th><th>

Method signature

</th><th>

Input fields

</th><th>

Output fields

</th></tr></thead><tbody><tr><td>

Verification Form Processor

</td><td>

Processes a verification form request and indicates whether the user was verified or not.

</td><td>

processForm\(params, request\)

</td><td>

Parameters:-   params.resetRequestId - The sys\_id of the current Password Reset request \(table: pwd\_reset\_request\).
-   params.userId - The sys\_id of the user to be verified \(table: sys\_user\).
-   params.verificationId - The sys\_id of the verification to be processed \(table: pwd\_verification\).
-   request - The form request object. Fields in the form can be accessed with request.getParameter\('&lt;element-id&gt;'\).

</td><td>

Returns: \(boolean\) true, if the user is verified; otherwise, false.

</td></tr></tbody>
</table>This example shows a verification processor that returns true only if the user sent **ok** in the input field; otherwise, it returns false. The code would be contained in the Script field of an extension script named SampleVerificationFormProcessor:

```
var SampleVerificationFormProcessor = Class.create ();
SampleVerificationFormProcessor.prototype = {
  category:'password_reset.extension.verification_form_processor', // DO NOT REMOVE THIS LINE!
 
   /**********
   * Process the verification form request, and return whether the user was successfully verified.
   * This is a sample verification processor returns true only if the user sent "ok" in the input field; 
   * otherwise, it returns false.
   * 
   * @param params.resetRequestId The sys_id of the current Password Reset request (table: pwd_reset_request)
   * @param params.userId         The sys_id of the user trying to be verified (table: sys_user)
   * @param params.verificationId The sys_id of the verification to be processed (table: pwd_verification)
   * @param request               The form request object. Fields in the form can be accessed with
   * request.getParameter('<element-id>')
   * @return Boolean indicating whether the user is successfully verified
   **********/
  processForm:function (params, request) {if (request.getParameter ("sysparm_simple_input") == "ok") return true; else return false; },
 
  type:'SampleVerificationFormProcessor'};
```

**Related topics**  


[Extension points](https://www.servicenow.com/docs/access?context=extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

