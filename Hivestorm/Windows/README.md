### Local User Auditing
Make sure to run in PowerShell
This will show what user accounts are enabled/disabled
also shows waht groups said users belong too

```
Get-LocalUser
``` 

### Enable/Disable User
In this example im disabling the guest account

```
net user guest /active no
```
