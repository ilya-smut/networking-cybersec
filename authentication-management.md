# Authentication Management

## Identification

User claims or professes and identity, such as with username, email address, or biomentrics

## Authentication

Entity provides a proof of a claimed identity, such as
1. Something you know
2. Something you have
3. Something you are
Second entity is an authenticator who verifies the authentication

## Authorisation

Access to resources is provided based on a proven identity

## Authentication factors:
- Something you are (e.g. Biomentrics)
- Something you have (e.g. Smartphone)
- Something you know (e.g. Password)

## Authentication Attributes:
- Something you are (MAC num, Geo position)
- Something you can do (gestures on a touch screen)
- Something you exhibit (ID badge)
- Someone you know (Someone who vouches for you)

## PAM - Rrivileged Access management

Allows stringent control over privileged accounts, such as root or administrator account. Implements possibility for users to access administrative accounts with their own password for a period of time. All activity is logged (e.g. Linux sudo command)

## Measures to implement strong authorisation
- Users should not have shared accounts
- Guest account should be disabled
- Administrators should have 2 accounts (Regular and Administrative)
- Time based logins may be used (e.g. 7AM - 7PM)
- Location based policies (e.g. block IP's from Russia or some other country)
- Account audits (Meaning revision of accounts' rights and permissions)

# Single Sign On

Single Sign On allows users to authenticate with a single user account and access multiple resources on a network without authenticating again

## Kerberos

Uses KDC and TGT tickets. If ticket granting ticket expires - user may not have access to resources (Microsot Active Directory domains and Unix realms use Kerberos for SSO authentication)

## Federated Identity

Central authentication with a federated database. Federation treats credentials from different networks as one entity

## SAML 

Security Assertion Markup Language - extensive markup language based standard used to exchange authentication and authorisation information between different parties. Is used within web apps

## OAuth

Open standard used for authentication, which allows users to log on with another account, such as PayPal or Google. It uses API calls to exchange information and a token to show that access is authorised

## Open ID

Authentication Standard by Open ID foundation. Is old

## OIDC - Open ID Connect

Builds on Open ID for authentication and uses OAth for authorisation. Instead of token it uses JSON web token (JWT). Like Oath user can log on with Google etc.

# Acces Control Schemes

## Role based

Uses roles to grant permissions. Users get access based on their assigned jobs

## Group based

Users should be put in a group with specific permissions. All group members have same permissions

## Rule Based

Set of approved instructions, such as ACL lists on Firewals 

## Discretionary

Every object has a discretionary control list. Every object has an owner who decides permissions. Used in Linux and Windows systems

## MAC - Mandatory Access Control

Uses security labels such as secret, top secret, etc. for both users and objects. Based on need-to-know basis

## Attribute based

Access is granted to users with specific attributes
