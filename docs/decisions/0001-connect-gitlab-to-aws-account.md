# connect gitlab to aws account

* Status: accepted
* Deciders: David
* Date: 2023-05-03

Technical Story: considering to use AWS  Security Token service over aws cognito to authorize secure

## Context and Problem Statement

secured connection between gitlabs and aws account, run Ci CD ops easly, without access to aws account

## Decision Drivers

* easy of use.
* aws best practices
* cloud guru forum discussion

## Considered Options

* STS
* Cognito

## Decision Outcome

Chosen option: "STS", because enables you to let users sign in using a third party identity provider. we can exchange the credentials from that provider for temporary permissions to use resources in your AWS account. This is known as the web identity federation approach to temporary access and helps you keep your AWS account secure,you don’t have to distribute long-term security credentials, such as IAM user access keys, with your application.

### Positive Consequences

* cognito fits to mobile sdk
* maintainble

## Links

* https://acloudguru.com/forums/aws-certified-security-specialty/sts-vs-cognito-gy
