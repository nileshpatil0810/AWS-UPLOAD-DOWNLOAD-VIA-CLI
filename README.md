# AWS-UPLOAD-DOWNLOAD-VIA-CLI
AWS S3 UPLOADING AND DOWNLOADING FROM LINUX COMMAND LINE

----------------------
#1 INSTALL PYTHON PIP 

$ sudo apt-get update

$ sudo apt-get install python-pip

#2 INSTALL AWS CLI

$ pip install --upgrade --user awscli

#3 CHECK INSTALLATION

$ aws --version

#4 CONFIGURATION

a. Log in the the AWS console web site.
b. Go to the IAM Management Console > Users > Add user
c. Type in a user name and select Programmatic access to get an access key ID and secret access key, instead of a password.
d. Set up the user’s permissions.
e. Apply the user credentials to AWS CLI on the Linux machine.

$ aws configure

AWS Access Key ID [None]: XXXXXXXXXXX
AWS Secret Access Key [None]: XXXXXXXXXXX
Default region name [None]: US West (Oregon)
Default output format [None]:

#5 Some example of s3 operation

a. LIST THE CONTENTS OF AN S3 BUCKET

$ aws s3 ls s3://my-bucket

b. LIST THE CONTENTS OF AN S3 BUCKET DIRECTORY

$ aws s3 ls s3://my-bucket/some/directory/

c. UPLOAD A FILE TO S3

$ aws s3 cp /opt/inbound/ s3://abc/attachment/ --recursive     --exclude "*" --include "*.pdf" --include "*.tif"

d. DELETE A FILE FROM S3

$ aws s3 rm s3://my-bucket/some/directory/profile.txt
