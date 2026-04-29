---
title: Use Java/C\#/PHP code to fetch the XML data using basic authentication
description: If a local data store is not an option, another way to get the data is to call the CSV/XML processor directly and then parse the results.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Strategies, Record retrieval limitations, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Use Java/C\#/PHP code to fetch the XML data using basic authentication

If a local data store is not an option, another way to get the data is to call the CSV/XML processor directly and then parse the results.

Use the resulting data in a similar manner as you would a direct SOAP call. An example of this in PHP:

```
<?php
//This example is in PHP 
 
	$user = "itil";
	$pass = "itil";
        $userPass = $user.':'.$pass;
 
 
        $ch = curl_init();
        curl_setopt($ch, CURLOPT_URL, 'https://<instance name>.service-now.com/incident_list.do?CSV');
        curl_setopt($ch, CURLOPT_HEADER, 0);
        curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
        curl_setopt($ch, CURLOPT_FOLLOWLOCATION, true);
        curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
        curl_setopt($ch, CURLOPT_USERPWD, $userPass);
 
        $data = curl_exec($ch);
        $info = curl_getinfo($ch);
 
        if ($output === false) {
          $output = "No cURL data returned for $addr [". $info['http_code']. "]";
          if (curl_error($ch))
              $output .= "\n". curl_error($ch);
          print $output;
        }
        else{
          echo $data;
        }
        curl_close($ch);
?>
```

**Parent Topic:**[SOAP strategies](../concept/c_SOAPStrategies.md)

