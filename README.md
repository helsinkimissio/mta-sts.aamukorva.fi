## MTA STS Policy

Aamukorva.fi's SMTP MTA Strict Transport Security Policy adds a security layer between the sending and receiving email server.

| Tag | Value |
| --- | --- |
| version | STSv1 |
| mode | enforce |
| mx | aamukorva-fi.mail.protection.outlook.com |
| max_age | 86400 |

Lines of MX tags should always list the current MX servers for the domain, one server per line. The servers can be queried with the command:

```
% host -t MX aamukorva.fi
aamukorva.fi mail is handled by 50 aamukorva-fi.mail.protection.outlook.com.
```

## MTA STS Record

| Tag | Value |
| --- | --- |
| v | STSv1 |
| id | 202211231428 |

The id tag value should be updated on each policy change. The current value can be resolved using the command:

```
% host -t TXT _mta-sts.aamukorva.fi
_mta-sts.aamukorva.fi descriptive text "v=STSv1; id=202211231428;"
```
