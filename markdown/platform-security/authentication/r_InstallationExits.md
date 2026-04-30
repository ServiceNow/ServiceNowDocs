---
title: Installation exits
description: Installation exits are customizations that exit from Java to call a script before returning back to Java.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Authentication, Access Management]
---

# Installation exits

Installation exits are customizations that exit from Java to call a script before returning back to Java.

**Note:** Functionality described here requires the **Admin** role.

## Available installation exits

Navigate to **System Definition** &gt; **Installation Exits**. Some installation exit names \(Login, Logout, ValidatePassword, ExternalAuthentication\) are reserved and cannot be changed. Other installation exits can override these with custom script that replaces the script in the default installation exit.

The following installation exits are available in the base system:

|Installation Exit|Description|
|-----------------|-----------|
|Login|Takes a username and password pair and authenticates with the user object|
|Logout|Takes the user to the welcome page upon signing out; can be overridden by LogoutRedirect|
|LogoutRedirect|Takes the user to a specified URL upon signing out|
|ExternalAuthentication|Authenticates using header, parameter, or cookie; can be overridden by DigestSingleSignOn and PGPSingleSignOn|
|DigestSingleSignOn|Authenticates using header, parameter, or cookie and decrypts Digest encryption|
|PGPSingleSignOn|Authenticates using header, parameter, or cookie and decrypts PGP encryption|
|ValidatePassword|Active by default, starting with the Helsinki release; allows customers to define their own password validation; can be overridden by ValidatePasswordStronger|
|ValidatePasswordStronger|Requires passwords be at least 8 characters long and contain a digit, an uppercase letter, and a lowercase letter|
|GetIntegrationSessionTimeout|Implements the default integration session timeout behavior.|

## Login modifications

The following modification to the **Login** installation exit sets each user's session timeout value as the user is logging in. In this particular example, if the user name is admin, the session is set to timeout in 30 seconds.

```
gs.include("PrototypeServer");
 
var Login = Class.create();
Login.prototype = {
	initialize : function() {
	},
 
        process : function() {
          // the request is passed in as a global
          var userName = request.getParameter("user_name");
          var userPassword = request.getParameter("user_password");
 
          var authed = GlideUser.authenticate(userName, userPassword);
          if (authed) {
             // ***********************************************************        
             // customization - if the userName == admin, set the session
             // timeout to be 30 seconds. You can implement your own  
             // session timeout algorithm here by checking to see if a user
             // belongs to a certain group or has a certain role.
             // Values of setMaxInactiveInterval exceeding 1440 minutes are
             // treated as one day (1440 minutes).
  
           if (userName == "admin") {
               request.getSession().setMaxInactiveInterval(30);
             }
             // ************************************************************
             return GlideUser.getUser(userName);
          }
 
          this.loginFailed();
 
          return "login.failed";
        },
 
        loginFailed : function() {
          var message = GlideSysMessage.format("login_invalid");
          var gSession = GlideSession.get();
          gSession.addErrorMessage(message);
 
          var userName = request.getParameter("user_name");
          EventManager.queue("login.failed", "", userName, "");
       }
 
}
```

Session timeout can also be set according to IP address.

```
gs.include("PrototypeServer");
 
var Login = Class.create();
Login.prototype = {
	initialize : function() {
	},
 
        process : function() {
          // the request is passed in as a global
          var userName = request.getParameter("user_name");
          var userPassword = request.getParameter("user_password");
 
          var authed = GlideUser.authenticate(userName, userPassword);
          if (authed) {
 
          // **************************************************************
          // customization - if the user is logging in from a particular IP
          // range starting with XXX.XXX you can implement your own
          // session timeout algorithm here by checking the login IP
          // 
          // Values of setMaxInactiveInterval exceeding 1440 minutes are
          // treated as one day (1440 minutes).
 
          var clientIP = gs.getSession().getClientIP().toString();

          // if client IP starts with specified range
          if (clientIP.indexOf('XXX.XXX') == 0) {  
             // set to 10 hours
             request.getSession().setMaxInactiveInterval(60 * 60 * 10); 
          }
          // ***************************************************************
 
             return GlideUser.getUser(userName);
          }
 
          this.loginFailed();
 
          return "login.failed";
        },
 
        loginFailed : function() {
          var message = GlideSysMessage.format("login_invalid");
          var gSession = GlideSession.get();
          gSession.addErrorMessage(message);
 
          var userName = request.getParameter("user_name");
          EventManager.queue("login.failed", "", userName, "");
       }
 
}

```

**Related topics**  


[Authentication](../../../administer/security-center/reference/sc-authentication.md)

