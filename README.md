# AWS-CLI-Credentials-Setup  
This is setup for configuration and credentials used by the AWS CLI to access your AWS account.  

1. To see if the AWS CLI is installed:<br>
```
$ aws --version
```
`aws-cli/2.16.9 Python/3.11.8 Darwin/23.5.0 exe/x86_64`

If you instead got `command not found`, then you need to install `awscli`. Refer to the link below to install `awscli`.<br>
<https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html>

2. Run `aws configure` and provide the following values:<br>
```
$ aws configure --profile master-programmatic-admin
```
`AWS Access Key ID [*************xxxx]:` -> Your AWS Access Key ID<br>
`AWS Secret Access Key [**************xxxx]:` -> Your AWS Secret Access Key<br>
`Default region name: [us-east-2]: ap-northeast-1`<br>
`Default output format [None]: json`

3. Check current profile and credenital<br>
```
$ cat ~/.aws/config
```
`[profile programmatic-admin]`<br>
`region = ap-northeast-1`<br>
`output = json`<br>  

```
$ cat ~/.aws/credentials
```
`[programmatic-admin]`<br>
`aws_access_key_id = *************xxxx`<br>
`aws_secret_access_key = **************xxxx`<br>

5. To see if credentail works  
```
$ aws iam list-users --profile programmatic-admin
```
