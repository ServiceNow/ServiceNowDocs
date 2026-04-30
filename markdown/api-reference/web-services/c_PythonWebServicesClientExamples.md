---
title: Python web services client examples
description: Examples demonstrating an integration with a Python web services client.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Inbound web service examples, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Python web services client examples

Examples demonstrating an integration with a Python web services client.

## Requirements

The following examples require the installation of the following Python modules:

-   fpconst [http://pypi.python.org/pypi/fpconst/0.7.2](http://pypi.python.org/pypi/fpconst/0.7.2)
-   PyXML [http://pyxml.sourceforge.net/topics/](http://pyxml.sourceforge.net/topics/)
-   SOAPpy [http://pywebsvcs.sourceforge.net/](http://pywebsvcs.sourceforge.net/)

## insert

This is an example of inserting an incident.

```
#!/usr/bin/python
 
 from SOAPpy  import SOAPProxy
 import sys
 
 def createincident (params_dict ):
 
         # instance to send to
        instance = 'demo'
 
         # username/password
        username = 'itil'
        password = 'itil'
 
 
         # proxy - NOTE: ALWAYS use https://INSTANCE.service-now.com, not https://www.service-now.com/INSTANCE for web services URL from now on!
        proxy  = 'https://%s:%s@%s.service-now.com/incident.do?SOAP' %  (username , password , instance )
        namespace  = 'http://www.service-now.com/'
        server  = SOAPProxy (proxy , namespace )
 
         # uncomment these for LOTS of debugging output #server.config.dumpHeadersIn = 1 #server.config.dumpHeadersOut = 1 #server.config.dumpSOAPOut = 1 #server.config.dumpSOAPIn = 1
 
        response  = server. insert (impact = int (params_dict [ 'impact' ] ) , urgency = int (params_dict [ 'urgency' ] ) , priority = int (params_dict [ 'priority' ] ) , category =params_dict [ 'category' ] , location =params_dict [ 'location' ] , caller_id =params_dict [ 'user' ] , assignment_group =params_dict [ 'assignment_group' ] , assigned_to =params_dict [ 'assigned_to' ] , short_description =params_dict [ 'short_description' ] , comments =params_dict [ 'comments' ] )
 
         return response
 
values  = { 'impact':  '1' , 'urgency':  '1' , 'priority':  '1' , 'category':  'High' , 'location':  'San Diego' , 'user':  'fred.luddy@yourcompany.com' , 'assignment_group':  'Technical Support' , 'assigned_to':  'David Loo' , 'short_description':  'An incident created using python, SOAPpy, and web services.' , 'comments':  'This a test making an incident with python.\n Isn \' t life wonderful?' }
 
new_incident_sysid =createincident (values )
 
 print "Returned sysid: "+ repr (new_incident_sysid )
```

## getKeys

This is an example of executing getKeys on the demo instance using basic authentication.

```
#!/bin/env python
 
 # use the SOAPpy module from SOAPpy  import SOAPProxy
 
username , password , instance  = 'admin' , 'admin' , 'demo'
proxy , namespace  = 'https://username:password@www.service-now.com/'+instance+ '/incident.do?SOAP' , 'http://www.service-now.com/'
 
server  = SOAPProxy (proxy ,namespace )
response  = server. getKeys (category  = 'Network' )
 
 print response. sys_id. split ( ',' )
```

## getRecords

In this example, we get an incident, querying for category == "Network" \(with basic authentication\).

```
#!/bin/env python
 
 # use the SOAPpy module from SOAPpy  import SOAPProxy
 
username , password , instance  = 'admin' , 'admin' , 'demo'
proxy , namespace  = 'https://username:password@www.service-now.com/'+instance+ '/incident.do?SOAP' , 'http://www.service-now.com/'
 
server  = SOAPProxy (proxy ,namespace )
response  = server. getRecords (category  = 'Network' )
 
 for record  in response:
	 for item  in record:
		 print item
```

## get

In this example, we get an incident record by `sys_id` \(with basic authentication\).

```
#!/bin/env python
 
 # use the SOAPpy module from SOAPpy  import SOAPProxy
 
username , password , instance  = 'admin' , 'admin' , 'demo'
proxy , namespace  = 'https://username:password@www.service-now.com/'+instance+ '/incident.do?SOAP' , 'http://www.service-now.com/'
 
server  = SOAPProxy (proxy ,namespace )
response  = server. get (sys_id  = '9c573169c611228700193229fff72400' )
 
 for each  in response:
	 print each
```

## Advanced

This is an example of advanced Python script that reads a log file for a keyword invalid spi and creates an ECC Queue record where the payload is set to an alert of XML format.

```
#!/bin/env python
 
 # kevin.pickard@service-now.com			2008.07.03		initial creation
 
 from SOAPpy  import SOAPProxy
 from xml. dom. minidom import getDOMImplementation
 import sys , os , socket , pickle , re
 
 # instance to send to
instance = 'demo'
 
 # username/pass
username = 'admin'
password = 'admin'
 
 # log file to watch
syslogfile = '/var/log/cisco.log.ksp'
 
 # state file
statefile = '/tmp/syslog_ecc.state-test'
 
 # ECC queue values
soapagent = 'SOAPpy'
ecctopic = 'PIX Error: '
eccname = 'Invalid SPI: '
eccsource = 'Syslog'
 
 # regex string to match
matchstring = 'invalid spi'
 
 try:
	state = open (statefile , 'r' )
	lastbyte = pickle. load (state )
	state. close ( ) except:
	lastbyte = 0
 
 #print 'DEBUG: lastbyte = '+str(lastbyte)
 
 try:
	log = open (syslogfile , 'ro' ) except:
	errortopic = 'Script Error'
	errorname = 'Unable to open log file '+syslogfile+ '.'
	errorpayload = 'This message was generated due to an error condition encountered in a script.  The name of the script is '+ os. path. basename ( sys. argv [ 0 ] )+ ' on server '+ socket. gethostname ( )+ '.'
 
	proxy  = 'https://'+username+ ':'+password+ '@'+instance+ '.service-now.com/ecc_queue.do?SOAP'
	namespace  = 'http://www.service-now.com/'
	server  = SOAPProxy (proxy , namespace )
	server. config. dumpSOAPOut = 1 
	server. config. dumpSOAPIn = 1 
        response  = server. insert (agent =soapagent , topic =errortopic , name =errorname , source = sys. argv [ 0 ] , payload =errorpayload )
 
	 sys. exit ( 1 )
 
 if lastbyte  != 0:
	 try:
		log. seek (lastbyte ) except IOError:
		 pass
 
loglines =log. readlines ( )
 
lastbyte =log. tell ( )
 
log. close ( )
 
state = open (statefile , 'w' ) pickle. dump (lastbyte , state )
state. close ( )
 
 # regex out the line
matchedlines = [ ] for line  in loglines:
	 if re. search (matchstring , line ) != None:
		matchedlines. append (line )
 
 #print 'DEBUG: len->loglines = '+str(len(loglines)) #print 'DEBUG: lastbyte = '+str(lastbyte) #print 'DEBUG: matchedlines = '+str(matchedlines)
 
 if len (matchedlines ) == 0:
	 sys. exit ( 0 )
 
proxy  = 'https://'+username+ ':'+password+ '@'+instance+ '.service-now.com/ecc_queue.do?SOAP'
namespace  = 'http://www.service-now.com/'
 
server  = SOAPProxy (proxy , namespace ) #server.config.dumpSOAPOut = 1 #server.config.dumpSOAPIn = 1
 
entriestosend = { } for line  in matchedlines:
	device =line. split ( ) [ 3 ]
	sourceip =line. split ( ) [- 1 ]
	entriestosend [sourceip ] = [device , line ]
 
 for key ,value  in entriestosend. iteritems ( ):
	 #impl=getDOMImplementation() #newdoc = impl.createDocument(None, "log_line", None) #top_element = newdoc.documentElement #text = newdoc.createTextNode(value[1]) #top_element.appendChild(text)
 
	response  = server. insert (agent =soapagent , topic =ecctopic+value [ 0 ] , name =eccname+key , source =eccsource , payload =value [ 1 ] )
```

**Parent Topic:**[Inbound web service examples](c_InboundWebServiceExamples.md)

