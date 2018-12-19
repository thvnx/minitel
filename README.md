# minitel

## hardware

* PL2303HX
* 5-pin plug
* 10K, 22K, 220K resistors
* 2N2222 transistor


## software

### systemd

```sh
cp systemd/serial-getty-minitel@.service /etc/systemd/system/
ln -s /etc/systemd/system/serial-getty-minitel@.service /etc/systemd/system/getty.target.wants/serial-getty-minitel@ttyUSB0.service
systemctl daemon-reload
systemctl start serial-getty-minitel@ttyUSB0.service
```

### minicom

```sh
cp minicom/minirc.minitel /etc/
minicom minitel
```

## references

[Pila's Blog (french)](http://pila.fr/wordpress/?p=361)
