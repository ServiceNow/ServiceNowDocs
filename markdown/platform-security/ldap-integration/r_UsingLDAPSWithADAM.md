---
title: Use LDAPS with ADAM
description: The default configuration for userProxy object authentication is to enforce LDAPS \(secure LDAP\) communications. LDAPS requires SSL certificates to secure the network traffic.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Use LDAPS with ADAM

The default configuration for userProxy object authentication is to enforce LDAPS \(secure LDAP\) communications. LDAPS requires SSL certificates to secure the network traffic.

To remove this requirement make the following change using the ADSIEdit console connected to the configuration partition.

```
Object: CN=Directory Service, CN=Windows NT, CN=Services, CN=Configuration
Attribute: msDS-Other-Setings
Value: change RequiresSecureProxyBind from 1 (enforced) to 0 (disabled)
```

Restart the ADAM service to use the new setting.

To support secure binds and encrypt the user and password information being transmitted, a SSL certificate must be installed on the server and any LDAP client. Since there is limited and controlled uses to the ADAM service, it is feasible to use a self-signed certificate which would meet the needs without incurring certificate costs or building a Certificate Authority \(CA\) infrastructure. If you already have a CA, you can issue a certificate. Otherwise, create a self-signed certificate.

## Creating a Self-Signed Certificate

To use the selfssl utility, Internet Information Services \(IIS\) must be installed. This service can be removed after you generate the certificate. You can get the selfssl.exe utility from the IIS Resource Kit. If IIS is already installed, create a new website so that the current sites will not be impacted during the certificate generation. Selfssl needs to temporarily attach the new self-issued certificate to a valid web site.

Selfssl is a command-line tool and has the following common parameters.

|Parameter|Description|
|---------|-----------|
|/T|Adds the cert to ‘Trusted Certificates’ on the local machine|
|/N:cn|Set the common name of the certificate. This must match the fully qualified domain name of the server running the web service using the certificate|
|/K|Sets the strength of the key size in bits|
|/V|Number of days the cert is valid|
|/S|Web site ID to attach the certificate to|
|/P|IP port of the web service|

The common name attribute should match the external name or address that the instance will use to connect to your ADAM computer. You will need to get the IIS Website site id unless you are using the default website which is 1 and does not need to be defined in the selfssl command. A sample command to generate a certificate for myCompany would be:

```
selfssl /N:CN=myCompany.externaldomain.com /K:1024 /V:3650 /S:12345 /P:50001 /T
```

This statement creates a certificate that is valid for 10 years. Set the value to any duration, but be aware the new certificate must be generated and submitted to the instance before the old one expires. We recommend making a note of the expiration date on the certificate.

Once the certificate is generated you can remove it from the website, or delete the entire web site if you created a temporary site.

**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

