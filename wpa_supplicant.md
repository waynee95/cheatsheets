# WPA Supplicant

## Start WPA Supplicant

```bash
$ systemctl restart wpa_supplicant.service
$ wpa_supplicant -i wlp3s0 -c /etc/wpa_supplicant.conf
```

## Config

The config file is stored at `/etc/wpa_supplicant.conf`.

```
network={
  ssid="MyRouter123"
  psk="abcdf"
  id_str="home"
}
```

```
network={
  ssid="eduroam"
  scan_ssid=1
  key_mgmt=WPA-EAP
  eap=PEAP
  identity="user [at] example.com"
  password="password"
  phase1="peaplabel=0"
  phase2="auth=MSCHAPV2"
  id_str="uni"
}
```

When using `wpa_cli` include this:

```
ctrl_interface=/var/run/wpa_supplicant GROUP=wheel
ctrl_interface_group=wheel
```

## Cannot initialize driver

Use `wpa_supplicant -D wext ...` instead.
