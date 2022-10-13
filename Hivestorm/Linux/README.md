### Finding bad packages

Read all currently installed packages, compare to os default packages, and list the differences

For Ubuntu 16.04 example

```
wget https://releases.ubuntu.com/xenial/ubuntu-16.04.6-desktop-i386.manifest

cat ubuntu-16.04.6-desktop-i386.manifest | cut -d$'\t' -f 1| set 's/-16.04//g > default'

apt list --installed | cut -f 1 -d '/' > current

for x in $(cat current) ; do if ! $(grep -q $x default); then echo $x ; fi ; done
```