---
title: Setup Transcript for Amazon Connect
description: Configure Conversational IVR with Amazon Connect application to store the conversation between the Agent and the User over Softphone as a transcript.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring your AWS account for use with Conversational IVR, Integrating Virtual Agent with Conversational IVR, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Setup Transcript for Amazon Connect

Configure Conversational IVR with Amazon Connect application to store the conversation between the Agent and the User over Softphone as a transcript.

## Before you begin

Role required: admin

## About this task

-   The voice transcript is stored by Amazon Connect, a third-party provider, post the voice conversation in the \[sys\_cs\_message\] table.
-   Messages between the User and the Agent are fetched by transcript API and attached to the Conversation. Also, the sentiment score from Amazon for each message is considered to derive overall Sentiment of User and Agent Conversation.
-   From Utah, the voice transcription is available real-time with the APIs that persist transcribed messages of an on-going phone call in real time. The messages are displayed in the Agent workspace chat panel along with previous conversation history \(if enabled\) and allows the Agent to leverage features like agent assist and search while actively talking to the caller. For more information about using Transcript API for real-time transcription, see [Voice Interaction Resource API](https://www.servicenow.com/docs/access?context=voice-interaction-resource-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

    To date, we ensure that performance is acceptable for the volume of transactions, about 5 million utterances/day/customer.

    We have also updated the system to store all details associated to a voice call in standard CI tables \(e.g., conversation and interaction tables\) instead of the sn\_openframe\_phone\_log table.


## Procedure

1.  Open your Amazon Connect instance page in AWS Console.

2.  Navigate to **Analytics tools** page and click **Enable contact lens**.

3.  Click **Save**.

4.  Navigate to **Data storage** &gt; **Call recordings** and click **Edit**.

5.  On the Call recordings page, select **Enable call recording**.

    To enable Call recordings, you can either create a new S3 bucket by selecting **Create a new S3 bucket \(recommended\)** or use an existing s3 bucket by selecting **Select an existing S3 bucket**.

    **Note:** This procedure explains creating a transcript using an existing S3 bucket.

6.  Select the **Name** of the existing S3 bucket from the drop-down and click **Save**.

7.  Copy the S3 bucket name from the Data storage page, under the Call recordings section.![The Amazon S3 bucket name from the Data storage page.](../images/copy-s3-bucket.png)

8.  Navigate to **AWS Lambda** &gt; **Functions** and select the**SN\_CI\_CC\_ProcessRequest** Function name.

9.  Click **Add trigger** and select **S3** from the Select a source drop-down.

10. In the **Bucket** drop-down, paste the copied bucket name.

11. Select the acknowledgement check box and click **Add**.

12. Configure Google Sentiment Analysis.

    1.  Log in to your ServiceNow instance and navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Find the Sentiment Analysis \(com.glide.cs.sentiment\) application using the filter criteria and search bar and click **Install**.

    3.  Select the **Enable Sentiment Analysis** check box on the Amazon Connect's messaging channel record to enable Sentiment Analysis in your ServiceNow instance.![Amazon Connect messaging channel window, with Enable Sentiment Analysis option highlighted.](../images/amz-sentiment-analysis.png)

    4.  Create a connection for the Google Sentiment Analysis API.

        -   Create a service account on Google Cloud and the Cloud Natural Language API. For more information, see [https://cloud.google.com/natural-language/docs/sentiment-analysis-gcloud](https://cloud.google.com/natural-language/docs/sentiment-analysis-gcloud).
        -   Download JSON file and create a JAVA Key Store Certificate. For more information, see [Create a Java KeyStore certificate](https://www.servicenow.com/docs/access?context=create-jks-google&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
        -   Navigate to **Workflow Studio** &gt; **Connections** &gt; **Google Sentiment Analysis**.
        -   Set the following fields using the JSON and generated `.jks` file.
        -   Click **Get Auth Token**.
        **Note:** The Connection details shared previously are related to the personal google service account. To set up a new account and get the JSON key file, use see [Google Documentation](https://cloud.google.com/natural-language/docs/sentiment-analysis-gcloud).

        After you get that JSON Key file, the `.jks` file can be generated using the following code:

        ```
        createJKS() { 
        
          cd $(dirname $1)  
        
          cat $1 | jq -r .private_key > GCPNaturalLanguage_pk.pem;
        
          kid=$(cat $1 | jq -r .private_key_id); 
        
          cert_url=$(cat $1 | jq -r .client_x509_cert_url); 
        
          curl ${cert_url} | jq -r --arg jq_kid "$kid" '.[$jq_kid]' > GCPNaturalLanguage_cert.pem; 
        
          openssl pkcs12 -export -in GCPNaturalLanguage_cert.pem -inkey GCPNaturalLanguage_pk.pem -certfile GCPNaturalLanguage_cert.pem -out GCPNaturalLanguage_pkcs12.p12; 
        
          keytool -importkeystore -srckeystore GCPNaturalLanguage_pkcs12.p12 -srcstoretype pkcs12 -destkeystore GCPNaturalLanguage.jks -deststoretype JKS 
        
        } 
        
        createJKS /Users/firstname.lastname/git/ServiceAccountKey/core-period-341405-9e1ed1673139.json (Path of JSON Key)
        ```


