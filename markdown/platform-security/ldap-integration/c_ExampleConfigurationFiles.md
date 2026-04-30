---
title: Example ADAM configuration files
description: All of the configurations for ADAMSync are stored in xml files.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the ADAM configuration file, Use ADAMSync to populate ADAM, Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Example ADAM configuration files

All of the configurations for ADAMSync are stored in xml files.

## Default configuration file with comments

There is a default configuration file called MS-AdamSyncConf.xml included with the ADAMSync install. Make a copy of this file so you have a base example to refer to in the future. This example is the default configuration file with comments added.

```
<?xml version="1.0"?>
<doc>	
 <configuration>		
<!-- Sync File Description --> 
<description>MyCompany ADAMSync Configuration</description>		
  <security-mode>object</security-mode>;	        
<!-- source-ad-name = fqdn of the domain controller -->;
  <source-ad-name>;fully.qualified.domain.name.of.domain.controller</source-ad-name>;		
<!-- source-ad-partition = root AD domain partition -->;
  <source-ad-partition>;dc=myCompany,dc=com</source-ad-partition>;
<!-- source-ad-account = use this to specify an account to connect to AD -->;
<!-- if not used, the current user will be used  -->;
  <source-ad-account>;</source-ad-account>;                
  <account-domain>;</account-domain>;
<!-- target-dn = target ADAM OU -->;
  <target-dn>;ou=servicenow users,dc=myCompany,dc=adam</target-dn>;		
  <query>;			
<!-- base-dn = should be the root AD partition if you want all users -->;
   <base-dn>;dc=myCompany,dc=com</base-dn>;
<!-- object-filter = standard ldap query format, this will grab all users -->;
<!-- need to review results to see if you should modify this filter -->;
   <object-filter>;(objectCategory=person)</object-filter>;			
   <attributes>;			
<!-- include=userproxy requires objectSID to link back to the AD account -->;	
    <include>;objectSID</include>;
    <include>;givenName</include>;
    <include>;sn</include>;
    <include>;description</include>;
    <include>;title</include>;
    <include>;company</include>;
    <include>;department</include>;
    <include>;mail</include>;
    <include>;physicalDeliveryOfficeName</include>;
    <include>;telephoneNumber</include>;
    <include>;sAMAccountName</include>;
   </attributes>;		
  </query>;	
<!-- map for user-to-userproxy object types -->;
  <user-proxy>;
    <source-object-class>;user</source-object-class>;
    <target-object-class>;userProxy</target-object-class>;
  </user-proxy>; 
  <schedule>;			
   <aging>;				
    <frequency>;0</frequency>;				
    <num-objects>;0</num-objects>;			
   </aging>;			
   <schtasks-cmd>;</schtasks-cmd>;		
  </schedule>;	
 </configuration>;	
 <synchronizer-state>;		
  <dirsync-cookie>;</dirsync-cookie>;		
  <status>;</status>;		
  <authoritative-adam-instance>;</authoritative-adam-instance>;		
  <configuration-file-guid>;</configuration-file-guid>;		
  <last-sync-attempt-time>;</last-sync-attempt-time>;		
  <last-sync-success-time>;</last-sync-success-time>;		
  <last-sync-error-time>;</last-sync-error-time>;		
  <last-sync-error-string>;</last-sync-error-string>;		
  <consecutive-sync-failures>;</consecutive-sync-failures>;		
  <user-credentials>;</user-credentials>;		
  <runs-since-last-object-update>;</runs-since-last-object-update>;		
  <runs-since-last-full-sync>;</runs-since-last-full-sync>;	
 </synchronizer-state>;
</doc>;
```

## LDAP filters configuration file

You can provide any level of filtering in the object-filter value in the configuration file. Use standard LDAP query syntax with the following xml escape characters in place of the standard operators.

-   AND = "&amp;" replace with &amp;\#38;
-   OR = "\|" \(vertical line\) replace with &amp;\#124;
-   NOT = "!" replace with &amp;\#33;

## Reference configuration file

Here's an actual configuration file that can be referenced as a sample.

```
<?xml version="1.0"?>;
<doc>;	
 <configuration>;		
<description>;SNCTest ADAMSync Configuration</description>;		
  <security-mode>;object</security-mode>;	        
  <source-ad-name>;domaincontroller.service-now.com</source-ad-name>;		
  <source-ad-partition>;dc=service-now,dc=com</source-ad-partition>;
  <source-ad-account>;</source-ad-account>;                
  <account-domain>;</account-domain>;
  <target-dn>;ou=servicenow users,dc=service-now,dc=adam</target-dn>;		
  <query>;			
   <base-dn>;dc=service-now,dc=com</base-dn>;
   <object-filter>;(objectCategory=person)</object-filter>;			
   <attributes>;			
    <include>;objectSID</include>;
    <include>;givenName</include>;
    <include>;sn</include>;
    <include>;description</include>;
    <include>;title</include>;
    <include>;company</include>;
    <include>;department</include>;
    <include>;mail</include>;
    <include>;physicalDeliveryOfficeName</include>;
    <include>;telephoneNumber</include>;
    <include>;userAccountControl</include>;
   </attributes>;		
  </query>;	
  <user-proxy>;
    <source-object-class>;user</source-object-class>;
    <target-object-class>;userProxy</target-object-class>;
  </user-proxy>; 
  <schedule>;			
   <aging>;				
    <frequency>;0</frequency>;				
    <num-objects>;0</num-objects>;			
   </aging>;			
   <schtasks-cmd>;</schtasks-cmd>;		
  </schedule>;	
 </configuration>;	
 <synchronizer-state>;		
  <dirsync-cookie>;</dirsync-cookie>;		
  <status>;</status>;		
  <authoritative-adam-instance>;</authoritative-adam-instance>;		
  <configuration-file-guid>;</configuration-file-guid>;		
  <last-sync-attempt-time>;</last-sync-attempt-time>;		
  <last-sync-success-time>;</last-sync-success-time>;		
  <last-sync-error-time>;</last-sync-error-time>;		
  <last-sync-error-string>;</last-sync-error-string>;		
  <consecutive-sync-failures>;</consecutive-sync-failures>;		
  <user-credentials>;</user-credentials>;		
  <runs-since-last-object-update>;</runs-since-last-object-update>;		
  <runs-since-last-full-sync>;</runs-since-last-full-sync>;	
 </synchronizer-state>;
</doc>;

```

