--------

This guide is for the Snowball \(50 TB or 80 TB of storage space\)\. If you are looking for documentation for the Snowball Edge, see the [AWS Snowball Edge Developer Guide](http://docs.aws.amazon.com/snowball/latest/developer-guide/whatisedge.html)\.

--------

# Options for the Amazon S3 Adapter for Snowball<a name="using-adapter-options"></a>

Following, you can find information on Amazon S3 Adapter for Snowball options that help you configure how the adapter communicates with a Snowball\.

**Note**  
Before transferring data into Amazon S3 using Snowball, make sure that the files and directories that you're going to transfer are named according to the [Object Key Naming Guidelines](http://docs.aws.amazon.com/AmazonS3/latest/dev/UsingMetadata.html#object-key-guidelines)\.


| Option | Description | Usage and Example | 
| --- | --- | --- | 
|  `-a` `--aws-profile-name`  | The AWS profile name that you want to use to sign requests to the Snowball\. By default, the adapter uses the credentials specified in the home directory/\.aws/credentials file, under the \[default\] profile\. To specify a different profile, use this option followed by the profile name\. |  `snowball-adapter -a` 

```
snowball-adapter -a Lauren
```  | 
|  `-s` `--aws-secret-key`  | The AWS secret key that you want to use to sign requests to the Snowball\. By default, the adapter uses the key present in the default profile specified in the home directory/\.aws/credentials file, under the \[default\] profile\. To specify a different profile, use this option, followed by a secret key\. The \-\-aws\-profile\-name option takes precedence if both options are specified\. |  `snowball-adapter -s` 

```
snowball-adapter -s wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
```  | 
|  `-h` `--help` | Usage information for the adapter\. | `snowball-adapter -h`  | 
|  `-i` `--ip`  | The Snowball's IP address, which can be found on the Snowball's E Ink display\. |  `snowball-adapter -i` 

```
snowball-adapter -i 192.0.2.0
```  | 
|  `-m` `--manifest`  | The path to the manifest file for this job\. You can get the manifest file from the AWS Snowball Management Console, or programmatically from the job management API\. |  `snowball-adapter -m` 

```
snowball-adapter -m ~/Downloads/manifest.bin
```  | 
|  `-u` `--unlockcode`  | The unlock code for this job\. You can get the unlock code from the AWS Snowball Management Console, or programmatically from the job management API\. |  `snowball-adapter -u` 

```
snowball-adapter -u 01234-abcde-01234-ABCDE-01234
```  | 
| `-ssl` `--ssl-enabled`  | A value that specifies whether or not the Secure Socket Layer \(SSL\) protocol is used for communicating with the adapter\. If no additional certification path or private key is provided, then a self\-signed certificate and key are generated in the home directory/\.aws/snowball/config directory\. |  `snowball-adapter -ssl` 

```
snowball-adapter -ssl
```  | 
|  `-c` `--ssl-certificate-path`  | The path to the certificate to use for the SSL protocol when communicating with the adapter\. |  `snowball-adapter -c` 

```
~/.aws/snowball/myssl/certs
```  | 
|  `-k` `--ssl-private-key-path`  | The path to the private key to use for the SSL protocol when communicating with the adapter\. |  `snowball-adapter -k` 

```
~/.aws/snowball/myssl/keys
```  | 