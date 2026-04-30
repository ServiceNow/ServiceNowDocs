---
title: Sample C
description: This C class illustrates creating a digest token from three input parameters.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Digest token authentication, Token based authentication \(User logins\), Authentication, Access Management]
---

# Sample C

This C class illustrates creating a digest token from three input parameters.

-   strEncryptionMethod – lists the hash computation method \(SHA1, SHA256 or MD5\)
-   message – lists the value to be converted into a digest token
-   sharedKey – lists the secret key

**Note:** Use stronger secure hash algorithm like SHA256 for digest token generation.

This sample assumes:

-   The web server supports C
-   Other code calls this class and passes the expected parameters

## Sample Code

```
  private stringdigestData(string strEncryptionMethod , string message , string sharedKey ) {
            UnicodeEncoding myUnicodeEncoding  = new UnicodeEncoding ( ) ;
 
            byte [ ] messageBytes  = System. Text. Encoding. ASCII. GetBytes (message ) ;
            byte [ ] sharedKeyBytes  = System. Text. Encoding. ASCII. GetBytes (sharedKey ) ;
            byte [ ] hashedMessage ;
 
            string b64SHA1Message ;
 
             if (this. DEBUG ) {
                TextBoxMessage. Text = message ;
                TextBoxSecret. Text = sharedKey ; }
 
             switch ( (strEncryptionMethod ) )
 
             { case "SHA1" :
 
                    HMACSHA1 hmacsha1  = new HMACSHA1 ( ) ;
                    hmacsha1. Key = sharedKeyBytes ;
                    hashedMessage  = hmacsha1. ComputeHash (messageBytes ) ;
                    b64SHA1Message  = Convert. ToBase64String (hashedMessage ) ; if (this. DEBUG ) TextBoxDigest. Text = Convert. ToString (hashedMessage ) ; break ;
 
                 case "MD5" :
 
                    HMACMD5 hmacmd5  = new HMACMD5 (sharedKeyBytes ) ;
                    hashedMessage  = hmacmd5. ComputeHash (messageBytes ) ;
                    b64SHA1Message  = Convert. ToBase64String (hashedMessage ) ; if (this. DEBUG ) TextBoxDigest. Text = Convert. ToString (hashedMessage ) ; break ;
 
                 default :
 
                    b64SHA1Message  = "Unknown Encryption Method" ; break ;
 
             }
 
 
            TextBoxBase64. Text = b64SHA1Message ; return b64SHA1Message ;
 
         }
```

