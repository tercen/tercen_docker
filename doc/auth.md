# Session

## Token

A token contains the following elements : 
 - userId
 - the expiration date
 - signature
 
Token validity period can be change in tercen config file.

```yaml
tercen.token.validity: '15' #15 days
```
The token signature is generate using a secret key.

The secret key can be change in tercen config file.
```yaml
tercen.secret: "3ab70b11-d7bd-4097-958f-01b7ac4e955f"
```

# ldap

To use ldap for authentication set the following in ./config/tercen.config.yaml file.

```yaml
tercen.user.service: 'ldap'
tercen.user.service.ldap.host: '127.0.0.1'
tercen.user.service.ldap.port: '389'
# TLS
# tercen.user.service.ldap.protocol: 'ssl'
# tercen.user.service.ldap.port: '636'

tercen.user.service.ldap.bind: 'dc=example,dc=org'
```

When a new session is created,a bind operation is perform
 on the configure ldap server with
 the following arguments

```bash
BindCN = "cn=&{username},${tercen_user_service_ldap_bind}"
Password = "given_password"
```

if the bind operation succeed a Token is generated,
 and a session is created based on that token.
  
 
