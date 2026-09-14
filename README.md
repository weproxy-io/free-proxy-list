# Free Proxy List

[![WeProxy — Free proxy list](./assets/banner.png)](https://weproxy.io/en/tools/free-proxy-list?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)

[![Live list](https://img.shields.io/badge/Live%20list-weproxy.io-111111?style=for-the-badge)](https://weproxy.io/en/tools/free-proxy-list?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list) [![Proxy Checker](https://img.shields.io/badge/Tool-Proxy%20Checker-2563eb?style=for-the-badge)](https://weproxy.io/en/tools/proxy-checker?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)

Browse and download a **public free proxy list** — HTTP and SOCKS addresses for testing and exploration.

Maintained by [WeProxy](https://weproxy.io). The live table lives on the site tool page (not as a static dump in this repo):

**→ [Free Proxy List on weproxy.io](https://weproxy.io/en/tools/free-proxy-list?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)**

## What you get on the live tool

- Public HTTP / HTTPS and SOCKS proxies in a filterable table
- Location and protocol filters
- One-click download for exploration
- Easy hand-off to [Proxy Checker](https://weproxy.io/en/tools/proxy-checker) to verify live lines

Free proxies are useful for quick prototyping. **Speed, security, and uptime are not guaranteed.** For production, use managed [WeProxy](https://weproxy.io) residential or datacenter lines.

## Risks of free proxies

Public free proxy lists often include:

- Short-lived or already-blocked exits
- Overloaded / slow hosts
- Unknown operators (traffic may be inspected)
- No support or SLA

Do **not** send passwords, sessions, or sensitive data through free public proxies.

## Free vs paid (quick compare)

| | Free public list | WeProxy paid lines |
| --- | --- | --- |
| Source | Third-party public pools | Managed gateway + product packages |
| Auth | Usually open IP:PORT | Username/password on `gw.weproxy.com.tr:8989` |
| Best for | Experiments, learning | Scraping, ads QA, geo checks, production |
| Support | None | [support@weproxy.io](mailto:support@weproxy.io) / panel |

Explore paid options: [Pricing](https://weproxy.io/en/pricing) · [Residential](https://weproxy.io/en/proxies/rotating-ipv4-residential) · [Datacenter](https://weproxy.io/en/proxies/rotating-ipv4-datacenter)

## How to use the free list

1. Open the [live Free Proxy List](https://weproxy.io/en/tools/free-proxy-list)
2. Filter by protocol (HTTP/HTTPS or SOCKS) and location
3. Copy candidates into [Proxy Checker](https://weproxy.io/en/tools/proxy-checker)
4. Discard dead lines immediately — free pools churn fast
5. For anything beyond a quick test, switch to a WeProxy package

## Example: test a single free proxy with cURL

Replace host/port with a line from the live list (many free proxies die quickly):

```bash
curl -x http://HOST:PORT https://api.ipify.org --connect-timeout 10 --max-time 20
```

For a production-style check against WeProxy instead:

```bash
curl -x http://USER:PASSWORD@gw.weproxy.com.tr:8989 https://api.ipify.org
```

## FAQ

### Are free proxies safe?

No guarantee. Treat them as untrusted infrastructure. Use WeProxy for sensitive or authenticated workflows.

### How often is the list updated?

The site refreshes periodically, but individual free proxies still go offline quickly. Always re-test before use.

### Why do so many free proxies fail?

They are shared, rate-limited, and frequently blocked. That is normal for public lists.

### What should I use in production?

[WeProxy residential](https://weproxy.io/en/proxies/rotating-ipv4-residential) or other managed products on [Pricing](https://weproxy.io/en/pricing). Free lists are for exploration only.

## Related repos

- [paid-proxy-servers](https://github.com/we1town-dev/paid-proxy-servers)
- [residential-proxies](https://github.com/we1town-dev/residential-proxies)
- [nodejs-proxy](https://github.com/we1town-dev/nodejs-proxy) · [php-proxy](https://github.com/we1town-dev/php-proxy) · [python-proxy](https://github.com/we1town-dev/python-proxy)

## Suggested GitHub topics

`free-proxy` · `free-proxy-list` · `proxy` · `proxies` · `http-proxy` · `socks5` · `web-scraping` · `proxy-list`

## License

MIT — see [LICENSE](./LICENSE).
