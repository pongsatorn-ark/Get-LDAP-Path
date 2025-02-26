Import-Module .\ldap_path.ps1

**Example enumeration with all users in domain**

LDAPSearch -LDAPQuery "(samAccountType=805306368)"

**Example enumeration with all groups in domain**

LDAPSearch -LDAPQuery "(objectclass=group)"

**Example enumerate every group available in the domain and display the user members**

```sh
foreach ($groups in $(LDAPSearch -LDAPQuery "(objectCategory=group)")) {$group.properties | select {$_.cn}, {$_.member}}
```
