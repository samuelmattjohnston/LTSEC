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

### Get services currently stopped or running 
You can also run this with a specific service to get more info on that service
```
Get-Service
```

### List current running processes (equivalent to ps command in Linux)

```
Get-Process
```

### stop a process based on process ID or program name

```
Stop-Process -ID 2668
Stop-Process -Name "process_name"
```

###  Windows Privilege Escalation Awesome Scripts (WinPEAS)

https://github.com/carlospolop/PEASS-ng/tree/master/winPEAS

###  Windows Blue team tips and tricks

https://github.com/C0nd4/CCDC-Blueteam-Manual#windows