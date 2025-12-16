# SPL Queries

## Brute Force Attempts by Source IP + User
```spl
index=auth_logs action=failure
| stats count as failures by src_ip, user
| where failures > 5
| sort - failures
```

## Successful Logins After Multiple Failures (Same User + IP)
```spl
index=auth_logs (action=failure OR action=success)
| stats count(eval(action="failure")) as failures, count(eval(action="success")) as successes by src_ip, user
| where failures > 5 AND successes > 0
| sort - failures
```

## Users Logging In From Many Different IPs
```spl
index=auth_logs action=success
| stats dc(src_ip) as unique_ips values(src_ip) as ip_list by user
| where unique_ips >= 3
| sort - unique_ips
```
