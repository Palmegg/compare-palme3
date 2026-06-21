# compare.palme3.dk

Statisk HTML-side hostet på CTID `116` (`websites`).

## Filer

- Webroot: `/var/www/sites/compare-palme3`
- HTML: `/var/www/sites/compare-palme3/index.html`
- Nginx server block: `/etc/nginx/sites-available/compare.palme3.dk`

## NPM

Proxy Host:

```text
Domain Names: compare.palme3.dk
Scheme: http
Forward Hostname / IP: 10.10.20.27
Forward Port: 80
```

## Test

Inde i containeren:

```bash
curl -H "Host: compare.palme3.dk" http://127.0.0.1
```

Fra Proxmox hosten:

```bash
curl -H "Host: compare.palme3.dk" http://10.10.20.27
curl -H "Host: compare.palme3.dk" http://10.10.20.16
```
