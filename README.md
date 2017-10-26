# openhab-arm-server-doc
openHAB2 ARM ArchLinux Docs

## Install Oracle Java

1. Download
2. Extract to ``/opt/jdk1.8.0_xxx``
3. Create symlink to ``/opt/jdk``
4. Create symlink from ``ln -s /opt/jdk/bin/java /usr/bin/java``

## Install openHAB2

__ Use the zip file!__

## Privileged Ports for Java

Used for bindings ``SNMP`` and ``Network ``

Use real path, not sym link path!

```bash
setcap cap_net_bind_service=+epi /opt/jdk1.8.0_152/bin/java 
echo "/opt/jdk1.8.0_152/lib/arm/jli" > /etc/ld.so.conf.d/java-libjli.conf
ldconfig -v
```
