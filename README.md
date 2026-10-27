# aria-panel-deploy

one-file installer for **aria-relay-panel v1.4.0 (build rfix2)**

```bash
curl -fsSL https://raw.githubusercontent.com/hhhgfdxxxccfgff/aria-panel-deploy/main/install.sh -o install.sh && bash install.sh
```

- installs Node.js 20 if needed, deps (`pg`, `ws`), unpacks the panel to `/opt/aria-panel`
- creates `/etc/aria-panel.env` with random `SITE_KEY` / `ADMIN_PASS` (printed at the end)
- runs as a systemd service (`aria-panel`), with a nohup+cron fallback
- panel URL: `http://<server-ip>:8080/stock-manage`

embedded `server.js` is the unmodified rfix2 build:
`md5 234aeaf00e20897cd1e0bc0ba9c81940` (verify after unpack: `md5sum /opt/aria-panel/server.js`)
