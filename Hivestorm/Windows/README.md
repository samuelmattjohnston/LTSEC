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

###  Windows Privilege Escalation Awesome Scripts (WinPEAS)

https://github.com/carlospolop/PEASS-ng/tree/master/winPEAS


### Get services currently stopped or running (equivalent to PS command in Linux) 

'''
Get-Service
'''

# List current running processes
'''
Get-Process
'''

### stop a process based on process ID or program name
'''
Stop-Process
'''




