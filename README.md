# Free Proxy List

[![WeProxy — Free proxy list](./assets/banner.png)](https://weproxy.io/en/tools/free-proxy-list?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)

[![Live list](https://img.shields.io/badge/Live%20tool-Free%20Proxy%20List-111111?style=for-the-badge)](https://weproxy.io/en/tools/free-proxy-list?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)
[![Checker](https://img.shields.io/badge/Tool-Proxy%20Checker-2563eb?style=for-the-badge)](https://weproxy.io/en/tools/proxy-checker?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)
[![Upgrade](https://img.shields.io/badge/Paid-WeProxy%20plans-16a34a?style=for-the-badge)](https://weproxy.io/en/pricing?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)

How to use a **public free proxy list** safely — and when to stop relying on it.

[WeProxy](https://weproxy.io) hosts a live, filterable free proxy table for exploration. This repository documents the workflow; it does **not** vendor a giant static dump that goes stale overnight.

**Open the live list →** [weproxy.io/en/tools/free-proxy-list](https://weproxy.io/en/tools/free-proxy-list?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list)

---

## What the live tool includes

- HTTP / HTTPS and SOCKS entries in a table  
- Location and protocol filters  
- Download for local experiments  
- Hand-off to [Proxy Checker](https://weproxy.io/en/tools/proxy-checker) for liveness tests  

Free proxies help with prototyping. **They are not a production network.**

## Honest limitations

| Expectation | Reality on free lists |
| --- | --- |
| “Always online” | Most exits die or throttle quickly |
| “Private / safe” | Operators are unknown; traffic may be watched |
| “Good for logins” | Session stability is poor |
| “Drop-in for residential” | Reputation and geo control differ completely |

Never send passwords, cookies, or payment flows through free public proxies.

## Recommended workflow

1. Open [Free Proxy List](https://weproxy.io/en/tools/free-proxy-list)  
2. Filter protocol (HTTP vs SOCKS) and location  
3. Copy a small batch into [Proxy Checker](https://weproxy.io/en/tools/proxy-checker)  
4. Keep only lines that respond within your timeout  
5. Discard the rest — churn is normal  
6. For real workloads, move to [WeProxy Pricing](https://weproxy.io/en/pricing)

## Quick cURL checks

**Free line (replace host/port from the live table):**

```bash
curl -x http://HOST:PORT https://api.ipify.org --connect-timeout 10 --max-time 20
```

**WeProxy paid gateway (production path):**

```bash
curl -x http://USER:PASSWORD@gw.weproxy.com.tr:8989 https://api.ipify.org
```

Gateway details and product lines: [paid-proxy-servers](https://github.com/weproxy-io/paid-proxy-servers) · [residential-proxies](https://github.com/weproxy-io/residential-proxies)

## Free vs WeProxy paid

| | Free public list | WeProxy |
| --- | --- | --- |
| Access | Open IP:PORT from public sources | Panel user/pass → `gw.weproxy.com.tr:8989` |
| Support | None | [support@weproxy.io](mailto:support@weproxy.io) |
| Best for | Learning, one-off tests | Scraping, ads QA, geo, production |
| Products | Mixed unknown pools | Residential, DC, mobile, ISP |

## When to upgrade

Upgrade when you need any of:

- Repeatable uptime or bandwidth plans  
- Geo / package control  
- Documented auth for CI and servers  
- Support and acceptable-use clarity  

Start here: [Pricing](https://weproxy.io/en/pricing?utm_source=github&utm_medium=referral&utm_campaign=free-proxy-list) · [Rotating residential](https://weproxy.io/en/proxies/rotating-ipv4-residential)

## FAQ

**Are these proxies safe?**  
No. Treat free proxies as untrusted. Use WeProxy for sensitive work.

**Why is the list empty after filters?**  
Public pools fluctuate; broaden filters or refresh later.

**Can I commit the full list into git?**  
Not recommended — it goes stale fast. Use the live tool instead.

**Language examples for paid gateway?**  
[nodejs-proxy](https://github.com/weproxy-io/nodejs-proxy) · [php-proxy](https://github.com/weproxy-io/php-proxy) · [python-proxy](https://github.com/weproxy-io/python-proxy)

## Links

- [Live Free Proxy List](https://weproxy.io/en/tools/free-proxy-list)  
- [Proxy Checker](https://weproxy.io/en/tools/proxy-checker)  
- [WeProxy](https://weproxy.io)  
- [All tools](https://weproxy.io/en/tools)  

## License

MIT — see [LICENSE](./LICENSE).
