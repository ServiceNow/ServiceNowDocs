---
title: C Sharp integration source code
description: After defining the source code, insert it.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Call a web service, .NET tutorial, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# C Sharp integration source code

After defining the source code, insert it.

Now we are ready to insert the code. Double-click on the **Send Web Service** button on your form to open the backend code to the form that has been created. Here is the code to insert a record into the demo instance and to read the response.

```
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace ExampleWebServiceForWiki
{
    public partial class FormMain : Form
    {
        public FormMain()
        {
            InitializeComponent();
        }

        private void buttonSend_Click(object sender, EventArgs e)
        {
            /*  SERVICE REFERENCE-SPECIFIC CODE  
            ServiceReference1.ServiceNowSoapClient soapClient = new ServiceReference1.ServiceNowSoapClient();
            soapClient.ClientCredentials.UserName.UserName ="itil";
            soapClient.ClientCredentials.UserName.Password ="itil"; 
            
            ServiceReference1.insert insert = new ExampleWebServiceForWiki.ServiceReference1.insert();
            ServiceReference1.insertResponse response = new ExampleWebServiceForWiki.ServiceReference1.insertResponse();
            //   END OF SERVICE REFERENCE CODE    */

            //   WEB REFERENCE-SPECIFIC CODE
            WebReference1.ServiceNow_incident soapClient = new ExampleWebServiceForWiki.WebReference1.ServiceNow_incident();
            System.Net.ICredentials cred = new System.Net.NetworkCredential("itil", "itil");
            soapClient.Credentials = cred;

            WebReference1.insert insert = new WebReference1.insert();
            WebReference1.insertResponse response = new WebReference1.insertResponse();
            //   END OF WEB REFERENCE CODE

            insert.category = "Category";
            insert.comments = "Comments";
            insert.short_description = "My short description";
           
            try
            {
                response = soapClient.insert(insert);
                this.richTextBoxResult.Text = "Incident Number: " + response.number + "\n";
                this.richTextBoxResult.Text += "Sys_id: " + response.sys_id;
            }
            catch (Exception error)
            {
                this.richTextBoxResult.Text = error.Message;
            }          
        }
    }
 


}


```

**Parent Topic:**[Call a web service in visual studio .NET](c_CallAWebServiceInVisualStudioNET.md)

