---
title: Posting a CSV file - Perl and Java examples
description: An example using Perl to post a CSV file with basic auth credentials and Java Apache HttpClient class to post a CSV file with basic auth credentials.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Post CSV or Excel files directly to an import set, Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Posting a CSV file - Perl and Java examples

An example using Perl to post a CSV file with basic auth credentials and Java Apache HttpClient class to post a CSV file with basic auth credentials.

For more information, see [Post CSV or Excel files directly to an import set](../task/t_PostCSVOrExcelFilesToImportSet.md).

## Perl example

```
# file: uploadafile.pl
# call me like this:
# uploadafile.pl --url="https://instance.service-now.com/sys_import.do?sysparm_import_set_tablename=dloo_test&sysparm_transform_after_load=true" 
# --uploadfile=/Users/davidloo/Desktop/test_files/test_users.csv
#
# the "sysparm_transform_after_load=true" parameter instructs the import set to transform immediately after loading
#
use strict;
use LWP::UserAgent;
use HTTP::Request::Common;
use Getopt::Long;
use File::Basename;
 
my ( $o_url, $o_fqn );
GetOptions(
    "url=s"        => \$o_url,
    "uploadfile=s" => \$o_fqn,
);
 
# mandatory arguments: url
&usage unless ( $o_url && $o_fqn );
 
my $url   = $o_url;
my $fname = $o_fqn;
 
# put timeouts, proxy etc into the useragent if needed
my $ua  = LWP::UserAgent->new();
 
# setup basic authentication credentials
$ua->credentials(
  'demo.service-now.com:443',
  'Service-now',
  'admin' => 'admin'
);
 
my $req = POST $url, Content_Type => 'form-data',
        Content      => [
                submit => 1,
                upfile =>  [ $fname ]
        ];
my $response = $ua->request($req);
 
 
 
if ($response->is_success()) {
    print "OK: ", $response->content;
} else {
    print $response->as_string;
}
 
exit;
 
sub usage {
        printf "usage:&nbsp;%s --url=%s --uploadfile=%s\\n",
                basename($0),'https://....','c:/data/test.csv';
        exit
}
```

## Java example

**Note:** The Apache HttpClient may limit the amount of data you can import in a single transaction. This example is meant as a starting point and should not be used in production.

```
HttpClient httpclient = new HttpClient();
PostMethod post = new PostMethod("https://instance-name.service-now.com/sys_import.do?sysparm_import_set_tablename=u_test_upload&sysparm_transform_after_load=true");
 
try {
  Credentials defaultcreds = new UsernamePasswordCredentials("admin", "admin");
  httpclient.getState().setCredentials(AuthScope.ANY, defaultcreds); // Prepare HTTP post
  httpclient.getParams().setAuthenticationPreemptive(true);
 
  File targetFile = new File("/Users/davidloo/Desktop/test_files/nodeinfo2736820198834983863.csv");
  Part[] parts = { new FilePart(targetFile.getName(), targetFile) };
 
  post.setRequestEntity(new MultipartRequestEntity(parts, post.getParams()));
 
  int result = httpclient.executeMethod(post);
 
  // Display status code
  System.out.println("Response status code: " + result);
 
  // Display response
  System.out.println("Response body: "+post.getResponseBodyAsString());
} catch(Exception e) {
  System.err.println(e.getMessage());
} finally {
  // Release current connection to the connection pool
  // once you are done
  post.releaseConnection();
}
```

**Parent Topic:**[Post CSV or Excel files directly to an import set](../task/t_PostCSVOrExcelFilesToImportSet.md)

