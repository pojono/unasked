# Network data — sources

Generated 2026-09-26T11:31:36.606Z by `scripts/net/` (build e67ecac75bc7). The page reads these files same-origin after the
IP lookup, so the snapshot lookups send the visitor's address to no new third party.

| id | Source | Kind | Entries | As of | This build | Terms |
|---|---|---|---|---|---|---|
| `tor-exit` | [Tor Project — exit list (TorBulkExitList)](https://check.torproject.org/torbulkexitlist) | tor, determined (exits/) | 1382 | 2026-09-26T10:56:09.000Z | fresh | Tor Metrics data, CC0 1.0. Cross-checked on every run against the running exit relays Onionoo reports (normally about 99% of their IPv4 addresses are on the list). |
| `tor-relay-v6` | [Tor Project — Onionoo running exit relays (IPv6 relay addresses of exits that allow IPv6 exit)](https://onionoo.torproject.org/details?type=relay&running=true&flag=Exit) | tor, inferred (exits/) | 620 | 2026-09-26T10:00:00.000Z | fresh | Tor Metrics data, CC0 1.0. Heuristic: the actual IPv6 exit address can differ from the relay address. Label as "probably". |
| `apple-relay` | [Apple — iCloud Private Relay egress IP ranges](https://mask-api.icloud.com/egress-ip-ranges.csv) | relay, determined | 52259 | 2026-09-26T11:31:18.775Z | fresh | Published by Apple so that sites can recognise Private Relay traffic; no licence text |
| `google-vpn` | [Google — VPN by Google geofeed](https://www.gstatic.com/vpn/geofeed) | vpn, determined | 12885 | 2026-09-26T10:26:33.000Z | fresh | Self-published RFC 8805 geofeed; no licence text |
| `cloudflare-egress` | [Cloudflare — egress IP geofeed (local-ip-ranges.csv: WARP, Zero Trust and other Cloudflare egress)](https://api.cloudflare.com/local-ip-ranges.csv) | vpn, determined | 76039 | 2026-09-26T05:09:10.000Z | fresh | Published by Cloudflare; no licence text. Also contains iCloud Private Relay egress operated by Cloudflare: check apple-relay first. |
| `mullvad` | [Mullvad VPN — relay list](https://api.mullvad.net/www/relays/all/) | vpn, determined | 1122 | 2026-09-24T11:26:10.000Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Entry (server) addresses. Exits usually match for WireGuard servers but not always; a miss means nothing. |
| `ivpn` | [IVPN — server list](https://api.ivpn.net/v5/servers.json) | vpn, determined | 178 | 2026-09-26T11:31:22.803Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Entry (server) addresses. Exits usually match for WireGuard servers but not always; a miss means nothing. |
| `nordvpn` | [NordVPN — server list (undocumented public API)](https://api.nordvpn.com/v1/servers) | vpn, determined | 7667 | 2026-09-26T11:31:23.000Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Entry (server) addresses. Exits usually match for WireGuard servers but not always; a miss means nothing. |
| `pia` | [Private Internet Access — server list](https://serverlist.piaservers.net/vpninfo/servers/v6) | vpn, determined | 1586 | 2026-09-26T11:31:22.000Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Entry (server) addresses. Exits usually match for WireGuard servers but not always; a miss means nothing. |
| `zscaler` | [Zscaler — cloud egress ranges (cenr, all Zscaler clouds)](https://config.zscaler.com/zscaler.net/cenr) | corporate-proxy, determined | 941 | 2026-09-26T11:31:26.719Z | fresh | Published by Zscaler for customer firewall configuration; no licence text |
| `aws` | [Amazon Web Services — ip-ranges.json](https://ip-ranges.amazonaws.com/ip-ranges.json) | datacenter, determined | 12344 | 2026-09-26T09:17:06.000Z | fresh | Published by AWS for public use; no licence text. AMAZON is a superset of the service ranges; prefer the most specific service. Categories: EC2, WorkSpaces, CodeBuild, Cloud9 and unspecified AMAZON space are rentable compute (datacenter); every other service is one of Amazon's own services (cdn). |
| `gcp-cloud` | [Google Cloud — customer IP ranges (cloud.json)](https://www.gstatic.com/ipranges/cloud.json) | datacenter, determined | 1103 | 2026-09-26T01:06:52.658Z | fresh | Published by Google; no licence text |
| `google-own` | [Google — own services and infrastructure (goog.json minus cloud.json)](https://www.gstatic.com/ipranges/goog.json) | cdn, determined | 402 | 2026-09-26T01:06:52.658Z | fresh | Published by Google; no licence text. goog.json lists all of Google's addresses; the Google Cloud customer ranges (cloud.json) are subtracted. |
| `github` | [GitHub — meta API (Actions runners, Codespaces and GitHub services)](https://api.github.com/meta) | datacenter, determined | 7786 | 2026-09-26T11:31:27.542Z | fresh | GitHub API terms. actions, actions_macos and codespaces are rentable CI / development machines (a bot, not a person); the Actions ranges sit inside Azure. The other keys are GitHub's own services (cdn). |
| `azure` | [Microsoft Azure — Service Tags (public cloud), AzureCloud.<region> tags](https://www.microsoft.com/en-us/download/details.aspx?id=56519) | datacenter, determined | 15253 | 2026-09-21T00:00:00.000Z | fresh | Published by Microsoft for firewall configuration; no licence text |
| `oracle` | [Oracle Cloud Infrastructure — public_ip_ranges.json](https://docs.oracle.com/en-us/iaas/tools/public_ip_ranges.json) | datacenter, determined | 1107 | 2026-08-25T08:06:24.590Z | fresh | Published by Oracle; no licence text. OCI ranges are rentable compute (datacenter); OSN and OBJECT_STORAGE are Oracle's own services (cdn). |
| `digitalocean` | [DigitalOcean — geofeed](https://www.digitalocean.com/geo/google.csv) | datacenter, determined | 764 | 2026-09-26T11:31:28.594Z | fresh | Self-published RFC 8805 geofeed; no licence text |
| `linode` | [Linode (Akamai Cloud) — geofeed](https://geoip.linode.com/) | datacenter, determined | 522 | 2026-09-26T10:00:05.000Z | fresh | Self-published RFC 8805 geofeed; no licence text |
| `vultr` | [Vultr (Constant) — geofeed](https://geofeed.constant.com/) | datacenter, determined | 466 | 2026-09-26T11:31:29.124Z | fresh | Self-published RFC 8805 geofeed; no licence text |
| `starlink` | [SpaceX Starlink — geofeed](https://geoip.starlinkisp.net/feed.csv) | satellite, determined | 2117 | 2026-09-17T00:02:42.000Z | fresh | Self-published RFC 8805 geofeed; no licence text. The city is the Starlink point of presence the operator presents, not the user's location. IPv4 is carrier-grade NAT (shared). |
| `cloudflare` | [Cloudflare — CDN / reverse-proxy edge ranges (ips-v4, ips-v6)](https://www.cloudflare.com/ips/) | cdn, determined | 22 | 2026-09-26T11:19:01.000Z | fresh | Published by Cloudflare; no licence text |
| `fastly` | [Fastly — public IP list (CDN edge)](https://api.fastly.com/public-ip-list) | cdn, determined | 21 | 2026-09-26T11:31:29.540Z | fresh | Published by Fastly; no licence text |
| `mullvad-net` | [Mullvad VPN — networks around its servers (/24, /64)](https://api.mullvad.net/www/relays/all/) | vpn, claimed | 698 | 2026-09-24T11:26:10.000Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Widened from mullvad: "in the network of a Mullvad VPN server". Exits often use nearby addresses. |
| `ivpn-net` | [IVPN — networks around its servers (/24, /64)](https://api.ivpn.net/v5/servers.json) | vpn, claimed | 92 | 2026-09-26T11:31:22.803Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Widened from ivpn: "in the network of a IVPN server". Exits often use nearby addresses. |
| `nordvpn-net` | [NordVPN — networks around its servers (/24, /64)](https://api.nordvpn.com/v1/servers) | vpn, claimed | 785 | 2026-09-26T11:31:23.000Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Widened from nordvpn: "in the network of a NordVPN server". Exits often use nearby addresses. |
| `pia-net` | [Private Internet Access — networks around its servers (/24, /64)](https://serverlist.piaservers.net/vpninfo/servers/v6) | vpn, claimed | 195 | 2026-09-26T11:31:22.000Z | fresh | Operator's public server list (app API; no published terms); only the derived address → operator map is shipped. Widened from pia: "in the network of a Private Internet Access server". Exits often use nearby addresses. |
| `iptoasn` | [iptoasn.com — IP to ASN (BGP origin) table](https://iptoasn.com/) | network metadata | 500197 | 2026-09-23T23:46:10.000Z | reused (within refresh interval) | Public domain (PDDL v1.0) |
| `ipverse` | [ipverse/as-metadata — network names, category, role and routing statistics](https://github.com/ipverse/as-metadata) | network metadata | 124915 | 2026-09-23T02:02:07.000Z | reused (within refresh interval) | CC0 1.0 |
| `nro` | [NRO — combined RIR delegated statistics (registry, country, date, holder)](https://ftp.ripe.net/pub/stats/ripencc/nro-stats/latest/nro-delegated-stats) | network metadata | 122508 | 2026-09-23T00:00:00.000Z | reused (within refresh interval) | Public RIR statistics (RIR Statistics Exchange Format) |
| `linnaeus` | [Linnaeus AS classification (Northwestern AquaLab), sub-level labels](https://github.com/NU-AquaLab/linnaeus) | network metadata | 119381 | 2025-06-01T00:00:00.000Z | reused (within refresh interval) | MIT License (code and released data; the upstream notice is reproduced in LICENSE); paper CC BY 4.0 |
| `x4b` | [X4BNet lists_vpn — data-centre and VPN network lists (ASN inputs)](https://github.com/X4BNet/lists_vpn) | network metadata | 947 | 2026-09-13T06:26:35.000Z | reused (within refresh interval) | MIT License as stated in the project README (the repository has no LICENSE file; the README's licence section is reproduced in LICENSE); ASN lists only, with attribution |
| `bgptools` | [bgp.tools — network class (asns.csv) and tags](https://bgp.tools/kb/api) | network metadata | 19656 | 2026-09-26T05:06:05.048Z | reused (within refresh interval) | No licence published; included for this prototype while the owner asks bgp.tools for permission |
| `asdb` | [Stanford ASdb — organisation industry categories (NAICSlite)](https://asdb.stanford.edu/) | network metadata | 115490 | 2026-03-01T00:00:00.000Z | reused (within refresh interval) | No licence published; included for this prototype while the owner asks the ASdb team for permission. Cite: Ziv et al., "ASdb: A System for Classifying Owners of Autonomous Systems", ACM IMC 2021 |
| `iplocate` | [IPLocate.io — free IP to ASN database (network website domain)](https://www.iplocate.io/) | network metadata | 75922 | 2026-09-24T01:13:10.000Z | reused (within refresh interval) | CC BY-SA 4.0 (IPLocate.io); the derived asn-domain/ files are CC BY-SA 4.0 and must be credited with a link to https://www.iplocate.io/ |
| `iana-rdap` | [IANA — RDAP bootstrap registries (ipv4, ipv6, asn)](https://data.iana.org/rdap/) | network metadata | 5 | 2026-06-01T20:00:01Z | reused (within refresh interval) | Public IANA registry data |

Statuses: *fresh* = downloaded for this build; *reused* = the previous copy is still within its refresh interval
(network-number datasets refresh weekly or monthly, bgp.tools daily); *kept* = the fresh download failed or was
refused by a safety gate (shrank by more than 30%, fell below its floor, failed a known answer or a cross-check), so
the last good copy and its old date are shipped; *missing* = no copy at all. Sources marked `keep: false` never
ship a kept copy or one older than their maximum age.

Evidence tiers: *determined* = the operator's own published list (an exact fact about the range, dated);
*claimed* = a third party's classification or a widened operator list; *inferred* = our heuristic.

## Files

- `meta.json` — build id, a content version per file family, per-source dates and status, chunk index,
  known-answer results (fetch with `cache: 'no-cache'`; each chunk is fetched with `?v=<its family's version>`).
- `ranges/v4|v6/*.json` — published list ranges (329 files, 1112 KB gzip).
- `exits/v4|v6/*.json` — single addresses from the lists that change on every run: Tor exits and Tor exit relays'
  IPv6 addresses (21 files, 10 KB gzip). (The public open-proxy exit list is off by default — NET_OPEN_PROXY=1 —
  because most of its addresses are dynamic home connections of people who may not know about it.)
- `ip2asn/v4|v6/*.json` — BGP origin network per address range, from iptoasn.com (350 files, 1753 KB gzip).
- `asn/<first>-<last>.json` — per-network metadata by network-number range: ipverse, NRO, Linnaeus, X4BNet, bgp.tools, ASdb (347 files, 3720 KB gzip).
- `asn-domain/<first>-<last>.json` — network website domains from IPLocate.io's free IP to ASN database, **CC BY-SA 4.0**; credit IPLocate.io with a link to https://www.iplocate.io/ wherever a domain is shown (347 files, 680 KB gzip).
- `rdap-bootstrap.json` — IANA RDAP bootstrap (ipv4, ipv6, asn) for the live registry lookup.

Formats are documented in `scripts/net/lib/format.mjs` and read by `src/collectors/netData.ts`.

Network label keys in `asn/` (`meta.json` `asnLabels`):

- `ipverse`: ipverse category (isp, hosting, business, education_research, government_admin)
- `ipverse-role`: ipverse network role (tier1_transit, major_transit, midsize_transit, access_provider, content_network, stub)
- `linnaeus`: Linnaeus sub-level classes (e.g. Access_LargeISP, Mobile, Satellite, ContentProvider_Cloud, VPNs)
- `x4b`: X4BNet list membership (datacenter, vpn)
- `bgptools`: bgp.tools tags (dsl, mobile, satnet, biznet, corp, vpsh, vpn, tor, cdn, uni, gov, anycast, perso, ddosm, icrit)
- `bgptools-class`: bgp.tools class (Eyeball, Content, Carrier, T1)
- `asdb`: Stanford ASdb categories ("Layer 1: Layer 2")

## Citations

- Linnaeus: E. Carisimo et al., Northwestern AquaLab, arXiv 2603.13649 (MIT).
- ASdb: M. Ziv, L. Izhikevich, K. Ruth, K. Izhikevich, Z. Durumeric, "ASdb: A System for Classifying Owners of Autonomous Systems", ACM IMC 2021.
- bgp.tools and ASdb publish no licence; they are included in this prototype while the site owner asks both for permission.
