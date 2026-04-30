---
title: Implement a nonce
description: Add a cryptographic nonce to the authentication header to ensure that it can only be used once.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Implement a nonce, Local authentication, Authentication, Access Management]
---

# Implement a nonce

Add a cryptographic nonce to the authentication header to ensure that it can only be used once.

-   Create a system property called **glide.authenticate.header.nonce\_key** and set its value to whatever variable name you're using for the nonce, such as NONCE or NCE.
-   Create a new table called `u_authentication_nonce`. Add a field to the table called `u_nonce`.
-   Go to **System Properties** &gt; **Installation Exits** and create an item called `DigestSingleSignOnNonce` which overrides ExternalAuthentication \(**glide.authenticate.external\_property**\).
-   Add the following code to the script portion of the newly created DigestSingleSignOnNonce.

    ```
    
    gs.include("PrototypeServer");
    
    var DigestSingleSignOnNonce = Class.create();
    DigestSingleSignOnNonce.prototype = {
    	
    	process : function() {
    		
    		var headerKey = GlideProperties.get("glide.authenticate.header.key", "SM_USER");
    		var headerDigestKey = GlideProperties.get("glide.authenticate.header.encrypted_key", "DIGEST");
    		var headerNonceKey = GlideProperties.get("glide.authenticate.header.nonce_key", "NCE");
    		var fieldName = GlideProperties.get("glide.authenticate.header.value", "user_name");
    		var fkey = GlideProperties.get("glide.authenticate.secret_key");
    		
    		// Look in the Headers
    		var data = request.getHeader(headerKey);
    		var encdata = request.getHeader(headerDigestKey);
    		var nonce = request.getHeader(headerNonceKey);
    		
    		// If not, then check the URL Parameters
    		if (data == null || encdata == null || nonce == null) {
    			data = request.getParameter(headerKey);
    			encdata = request.getParameter(headerDigestKey);
    			nonce = request.getParameter(headerNonceKey);
    		}
    		
    		// then maybe its a cookie
    		if (data == null || encdata == null || nonce == null) {
    			var cookies = request.getCookies();
    			data = GlideCookieMan.getCookieValue(cookies, headerKey);
    			encdata = GlideCookieMan.getCookieValue(cookies, headerDigestKey);
    			nonce = GlideCookieMan.getCookieValue(cookies, headerNonceKey);
    		}
    		
    		// if found run encryption
    		if (data != null && encdata != null && nonce != null) {
    			try {
    				
    				// Replace all spaces with plus(+)'s, converted in url
    				encdata = encdata.replaceAll(' ', '+');
    				
    				// ----- Encrypt the username|nonce
    				var key = this.getDigest( data + "|" + nonce, fkey);
    				
    				// Check for match of received encoded data
    				// and your encoding of user name
    				if (encdata == key) {
    					var ugr = new GlideRecord("sys_user");
    					ugr.initialize();
    					if (!ugr.isValidField(fieldName)) {
    						GlideLog.warn("External authorization is set to use field: '"+ fieldName + "' which doesn't exist");
    						return "failed_missing_requirement";
    					}
    					ugr.addQuery(fieldName, data);
    					ugr.query();
    					if (!ugr.next()) {
    						var userLoad = GlideUser.getUser(data);
    						if (userLoad == null)
    							return "failed_authentication";
    						
    						ugr.initialize();
    						ugr.addQuery(fieldName, data);
    						ugr.query();
    						if (!ugr.next())
    							return "failed_authentication";
    						
    					}
    					
    					if (this.processNonce(nonce)){
    						var userName = ugr.getValue("user_name");
    						return userName;
    					}
    					else return "failed_missing_requirement";
    					}
    				else {
    					
    					return "failed_authentication";
    				}
    			} catch(e) {
    				gs.log(e);
    				return "failed_authentication";
    			}
    			// Encoded data didn't match recieved Encoded data
    		} else {
    			
    			return "failed_missing_requirement";
    		}
    	},
    	
    	getDigest : function( data, fkey ) {
    		try {
    			// default to something JDK 1.4 has
    			var MAC_ALG = "HmacSHA1";
    			return SncAuthentication.encode(data, fkey, MAC_ALG);
    			
    		} catch (e) {
    			gs.log(e.toString());
    			throw 'failed_missing_requirement';
    		}
    	} ,
    	
    	processNonce : function( sentNonce ) {
    		var ngr = new GlideRecord("u_authentication_nonce");
    		
    		ngr.addQuery("u_nonce", sentNonce);
    		ngr.query();
    		if (ngr.next()) {
    			gs.log("This SSO entry has already been processed! (Nonce: " + sentNonce + ")");
    			return false;
    		}
    		var ngrNew = new GlideRecord("u_authentication_nonce");
    		ngrNew.initialize();
    		ngrNew.u_nonce = sentNonce;
    		ngrNew.insert();
    		gs.log("Inserted new nonce: " + sentNonce);
    		return true;
    	}
    };      
         
    ```

-   Once you've saved your new installation exit, go to the DigestSingleSignOn installation exit and make sure that it is set Active=false.

Your instance should now be configured to implement a nonce.

