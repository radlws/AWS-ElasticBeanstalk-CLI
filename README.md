Eb Command Line Interface Updated
===============

This package contains an updated command line interface (CLI), called eb, for AWS Elastic Beanstalk. 
This revision is based on the original EB CLI 2.6.4 from Amazon with many small improvements and bug fixes. 
AWS Elastic Beanstalk provides easy application deployment and management utilizing various Amazon 
Web Services resources that are created on your behalf. Eb helps you create and deploy your application 
in minutes.

Requirements
-----

* An AWS account with access to AWS Elastic Beanstalk
* boto python
* git

Installation
-----

Once you have downloaded the CLI package:

1) Unzip this archive to a location of your choosing. Eb is located in the "eb" directory. The complete CLI reference 
for more advanced scenarios can be found in the "api" directory.
To add eb files to your path:

Linux/Mac OS X (Bash shell):

    export PATH=$PATH:<path to eb>

Windows:

    set PATH=<path to eb>;%PATH%

Usage
-----

For instructions on how to use eb, see the AWS Elastic Beanstalk documentation at 
http://docs.amazonwebservices.com/elasticbeanstalk/latest/dg/command-reference-get-started.html.

This package contains the following:
* Eb - a command line interface for easy application management and deployment. Can be found in the "eb" directory.
* API command line interface - a command line interface for advanced scenarios that can be used to interact with the service. Can be found in the "api" directory.
* AWS DevTools - a Git client extension for AWS Elastic Beanstalk. Can be found in the "AWSDevTools" directory.

### Available eb commands
* eb init - initializes eb by creating scripts for aws.config and aws.push that live in .git/. Run at root of repo.
* eb status –verbose - view the environment status in detail
* git aws.config - allows you to change the environment. If you clone an existing project and maintain it, run the following command and follow the prompt steps to configure your git in your project folder
* git aws.push - (not git push) - deploys the code to the environment, push to -e env, -c commit, with optional -t tag for version label
* eb start - starts the Beanstalk environment
* eb logs - dumps all logs
* eb update - Update your environment configuration

See eb –help. More info

Troubleshooting
-----

ERROR: git aws.config / aws.push not found

SOLUTION: Run this:

    bash ~/.bin/ebcli/AWSDevTools/Linux/AWSDevTools-RepositorySetup.sh 
