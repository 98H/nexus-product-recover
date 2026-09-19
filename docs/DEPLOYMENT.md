# Deployment & Operations Guide: Product Recover

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-recover-667f9f/](/preview/prod-product-recover-667f9f/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T19:04:59.390723+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product Recover Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-13/test_orphaned_in_progress_stor0/workspaces/prod-product-recover-667f9f
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-13/test_orphaned_in_progress_stor0/workspaces/prod-product-recover-667f9f/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
