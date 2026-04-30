---
title: Configure key-based MID Web Server authentication
description: Provide added security to your MID Web Server extension by using key-based authentication. Generate an authentication token to be sent in the Authorization header of incoming client requests.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure key-based MID Web Server authentication

Provide added security to your MID Web Server extension by using key-based authentication. Generate an authentication token to be sent in the Authorization header of incoming client requests.

## Before you begin

**Note:** This procedure is only for compatibility with releases prior to Yokohama. For details on the procedure in the Yokohama release for configuring the MID Web Server, see [Configure the MID Web Server extension](configure-mid-web-server-extension.md).

-   Deploy and start a MID Server.
-   Configure a MID Web Server extension and select Keybased as the authentication type. For details, see [Configure the MID Web Server extension](configure-mid-web-server-extension.md).

Role required: agent\_admin

## Procedure

1.  Using a script program, create a token by constructing a string using defined elements of the HTTP/HTTPS request \(HTTP verb, content type header, and request path, received from the client accessing the MID Web Server extension endpoints\).

2.  Create an HMAC \(Hash Message Authentication Code\) of the string by signing the generated string with the auto-generated secret key that is displayed in the **Secret Key**.

    This key is unique per context.

3.  Provide information to send this authentication token in the request Authorization header.

<table id="table_dsc_k3w_nrb"><thead><tr><th>

Item

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Path to a web service API for sending raw data

</td><td>

URL format:`https://<MID Server IP address>:<port number>/api/mid/sa/metrics`

 Use a port number that matches one of the port numbers set up in the Web Server extension.

 Example: `http://10.10.10.10:8097/api/mid/sa/metrics`

</td></tr><tr><td>

Request type

</td><td>

POST

</td></tr><tr><td>

Date format

</td><td>

```
yyyy-MM-dd'T'HH:mm:ss.SSS'Z'
```

For example: 2016-06-08T20:54:58.917Z

</td></tr><tr><td>

Content-Type

</td><td>

application/json

</td></tr></tbody>
</table>    Use the following request elements to generate the required string: HTTP-Verb, Content-Type, Date, and request path. Specify these elements and place them in this order:

    -   HTTP-Verb + "\\n" +
    -   Content-Type + "\\n" +
    -   Date + "\\n" +
    -   Request-Path
    For this example, the request string is:

    `POST\napplication/json\n2016-06-08T20:54:58.917Z\n/api/mid/sa/metrics`

    For the timestamp requirement, a valid timestamp that uses HTTP date header is required for authenticating the request. Ensure that the timestamp is within 15 minutes of the MID Server.


## How to generate the HMAC of the string that uses defined elements of the HTTP/HTTPS request, using Java

```
package sample;
import com.glide.util;
import java.security.SignatureException;

import javax.crypto.Mac;
import javax.crypto.spec.SecretKeySpec;

public class AuthUtil {
	
private static final String HMAC_SHA1_ALGORITHM = "HmacSHA1";

/***
 * Generates base64-encode the HMAC(Hash Message Authentication Code) of input data
 * 
 * @param data
 * @param key
 * @return
 * @throws java.security.SignatureException
 */
public static String signData(String data, String key) throws java.security.SignatureException {
	String result;
	try {
		// get an hmac_sha1 key from the raw key bytes
		SecretKeySpec signingKey = new SecretKeySpec(key.getBytes(), HMAC_SHA1_ALGORITHM);

		// create hmac_sha1 Mac instance and initialize with the signing key
		Mac = Mac.getInstance(HMAC_SHA1_ALGORITHM);
		mac.init(signingKey);

		// compute the hmac on input data bytes
		byte[] rawHmac = mac.doFinal(data.getBytes("UTF-8"));

		// base64-encode the hmac
		result = Base64.encode(rawHmac);

	} catch (Exception e) {
		throw new SignatureException("Failed to generate HMAC : " + e.getMessage());
	}
	return result;
}
}

```

**Parent Topic:**[Configure the MID Web Server extension](configure-mid-web-server-extension.md)

