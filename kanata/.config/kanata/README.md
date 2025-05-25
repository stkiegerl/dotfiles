# Kanata Windows Config

Homerow-Mod config & remap Capslock to CRTL (long press) & ESC (short press)

## Autostart kanata with systemd

Add this to: `~/.config/systemd/user/kanata.service`:

```
[Unit]
Description=Kanata keyboard remapper
Documentation=https://github.com/jtroo/kanata

[Service]
Environment=PATH=/usr/local/bin:/usr/local/sbin:/usr/bin:/bin:$HOME/.cargo/bin
Environment=DISPLAY=:0
Type=simple
ExecStart=/usr/bin/sh -c 'exec $$(which kanata) --cfg $${HOME}/.config/kanata/config.kbd'
Restart=no

[Install]
WantedBy=default.target
```

Then run

```
systemctl --user daemon-reload
systemctl --user enable kanata.service
systemctl --user start kanata.service
systemctl --user status kanata.service   # check whether the service is running
```
