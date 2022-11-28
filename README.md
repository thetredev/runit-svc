# svc - runit service management script

A bash script to simplify the usage of `runit`'s `sv` command:
```shell
sudo svc enable <service>
sudo svc disable <service>
sudo svc start <service>
sudo svc stop <service>
sudo svc restart <service>
sudo svc reload <service>
sudo svc status <service>
```

# Installation

## system-wide
```shell
RUNIT_SVC_INSTALL_DIR=/usr/local/bin
sudo mkdir -p $RUNIT_SVC_INSTALL_DIR
curl -fsSL --output /tmp/runit-svc https://raw.githubusercontent.com/thetredev/runit-svc/main/svc
sudo mv /tmp/runit-svc $RUNIT_SVC_INSTALL_DIR/svc
sudo chmod +x $RUNIT_SVC_INSTALL_DIR/svc
```

## user-specific
```shell
RUNIT_SVC_INSTALL_DIR=$HOME/.bin
mkdir -p $RUNIT_SVC_INSTALL_DIR
curl -fsSL --output /tmp/runit-svc https://raw.githubusercontent.com/thetredev/runit-svc/main/svc
mv /tmp/runit-svc $RUNIT_SVC_INSTALL_DIR/svc
chmod +x $RUNIT_SVC_INSTALL_DIR/svc
```

Make sure `$RUNIT_SVC_INSTALL_DIR` is in your `$PATH`, no matter which method you're using!

# Removal
```shell
RUNIT_SVC_INSTALL_DIR=/usr/local/bin
sudo rm -f $RUNIT_SVC_INSTALL_DIR
```
