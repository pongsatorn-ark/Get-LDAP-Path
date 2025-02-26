Import-Module .\ldap_path.ps1

**Example enumeration with all users in domain**

LDAPSearch -LDAPQuery "(samAccountType=805306368)"

**Example enumeration with all groups in domain**

LDAPSearch -LDAPQuery "(objectclass=group)"
