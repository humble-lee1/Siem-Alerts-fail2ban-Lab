# SIEM Alerts + Fail2ban + Email Alerting Lab

## Attack Simulation Results

| Attempt | Result | IP |
|---------|--------|-----|
| 1-5 | ❌ Failed | 192.168.122.109 |
| 6 | ✅ SUCCESS | 192.168.122.109 |

## Key Findings

1. Brute force detected - 5 failed attempts
2. Successful login after failures - Credential found
3. Fail2ban response - IP banned after 5 failures
4. Email alerts triggered - Real-time notification

## Splunk Alerts Created (WITH EMAIL)

| Alert | Trigger | Email Sent |
|-------|---------|------------|
| High SSH Failure Rate | >4 failures in 5 min | ✅ Yes |
| Success After Failure | Success within 5 min of failures | ✅ Yes |
| Invalid User Detection | Any invalid username | ✅ Yes |

## Recommendations

1. Reduce maxretry to 3
2. Require MFA for SSH
3. Monitor email alerts for immediate response
