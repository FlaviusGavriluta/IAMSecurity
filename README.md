# IAM security

## Story

You now have to secure your own AWS account and have stricter password policies for your AWS users. Using IAM you have to assign and request individual and temporary credentials via IAM roles to provide users with access to AWS services and resources.

## What are you going to learn?

- How to secure your AWS account
- How to enable and use MFA
- How to increase password complexity

## Tasks

1. - Enable Multi-factor authentication, MFA, on your root account and use Google Authenticator
- Set a password policy with a set of rules for complexity
    - Verify access to AWS Management console requires MFA code on each log-in.
    - Passwords should require at least one uppercase, lowercase, number, special character and is minimum 20-char length

2. You have a custom application hosted on an EC2 instance. This app needs to interact with objects in an S3 bucket. Create an IAM role to pass temporary security credentials as part of an instance profile. The application would use the identity assumed by the instance to access the S3 bucket
    - Verify that an EC2 instance is capable of accessing S3 bucket objects

3. You have an IAM user that has restricted access to S3 buckets. The user may _sometimes_ have to perform tasks that require administrative privileges
    - Create a new IAM admin policy, create a new role and attach the policy to the role
    - When required the user can be allowed to __assume__ the IAM Admin role and gain administrative access achieving the so-called `Wear a different hat`

## General requirements

None

## Hints

- Extra password policies (password expiration, prevent password reuse, etc.) may be burdensome for your users but add an extra layer of protection.
- An `IAM role` is similar to a user in that it is an IAM identity with permissions of what can and cannot do.
- If a user is assigned to a role, access keys are created dynamically and provided to the user temporarily.
- IAM policies can be assigned to an `IAM role`.
- Use `AmazonS3FullAccess` in your role.

## Background materials

- <i class="far fa-exclamation"></i> [IAM Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html)
- <i class="far fa-video"></i> [AWS IAM Overview](https://www.youtube.com/watch?v=y8cbKJAo3B4)
