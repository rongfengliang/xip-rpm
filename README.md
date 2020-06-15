# xip.name rpm for linux

source code https://github.com/peterhellberg/xip.name

> build with fpm 


## build rpm

```code
fpm -s dir -t rpm -n xip --rpm-os linux -v v1.0 \
  ./xip.linux=/usr/bin/ \
  ./xip.service=/usr/lib/systemd/system/xip.service \
  ./xipconfig/xip=/etc/xipconfig/xip
```

## useage

* install 

```code

yum install -y xip-v1.0-1.x86_64.rpm
```

* config

> /etc/xipconfig/xip

```code
OPTIONS = "-fqdn <xip.name> -ip <127.0.0.1>"
```

change  `<xip.name>` and `<127.0.0.1>` to your well-known domain && ipaddress 