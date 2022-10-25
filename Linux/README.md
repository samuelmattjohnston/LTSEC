### Finding bad packages

Read all currently installed packages, compare to os default packages, and list the differences

For Ubuntu 16.04 example

```
wget https://releases.ubuntu.com/xenial/ubuntu-16.04.6-desktop-i386.manifest

cat ubuntu-16.04.6-desktop-i386.manifest | cut -d$'\t' -f 1| set 's/-16.04//g > default'

apt list --installed | cut -f 1 -d '/' > current

for x in $(cat current) ; do if ! $(grep -q $x default); then echo $x ; fi ; done
```

### Check binaries checksums packages

Debian based:

```
sudo debsums -a | grep -v OK$
```

### CCDC Blueman Manual

https://github.com/C0nd4/CCDC-Blueteam-Manual#linux

### check sudo/wheel users

```
getent group {sudo,wheel} | cut -d: -f4
```

### Check sudoers and sudoers.d

```
sudo grep -v ^# /etc/{sudoers.d/*,sudoers}
```

### Basic pamd config
```
password requisite pam_cracklib.so try_first_pass retry=3 minlength=16lcredit=-1 ucredit=-1 dcredit=-1 ocredit=-1 difok=4 reject_username
```

### Audit Logs script

https://gist.github.com/Neo23x0/9fe88c0c5979e017a389b90fd19ddfee