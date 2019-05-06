### HelpDeskZ Arbitrary File Upload Exploit

This exploit was originally posted on ExploitDB, but the version found there had quite a few syntax errors and other issues. I needed to use it during an excersize and wanted to store the corrected version.

This version of the script has been corrected and a few minor updates have been made to ensure that it works without issues.

HelpDeskZ will allow you to attach a `.php` file to a ticket before submission using the file upload option. Due to an oversight in the helpdesk application the file is uploaded to the server before it is verified. Even though you are told that the file type is not allowed, it will still be accessible on the server.

The method that this application uses to name uploaded files makes them easy to reproduce, as it is based on upload time. This script will make requests to 300 of the most likely possibilities and return a successful URL if one is found.

###### Note:
Make sure that you are running this script shortly after submitting a ticket to HelpDeskZ with your PHP shell. The name that HelpDeskZ gives each uploaded file is based on the time of the upload, making this time-sensitive.

#### Usage:
`python exploit.py [BASE URL OF HELPDESKZ] [NAME OF PHP SHELL SCRIPT].php`
