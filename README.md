# Overview
This role provides centralized account management for various services to use.
The goal for this role is to provide the infrastructure for a user to use a single
set of credentials across a variety of services.

Only local access is permitted for authentication with the LDAP server at this time.
Passwords are stored as SHA256 hashes.

OpenLDAP is an open source project and more information is available at
http://www.openldap.org. The license for OpenLDAP is available here
http://www.openldap.org/software/release/license.html.

# Dependencies
None

# Variables
```yaml
- vars:
  domain: domain.com
  ldapadminpassword: change_this_password
  ldap_org_name: your name
  emailusers:
    - username: name
      lastname: lastname
      firstname: firstname
      password: change_this_password
      uidnumber: 10001 # increase this number for any additional users
      gidnumber: 5000 # keep this number the same for any additional users
      fullname: firstname lastname
```
