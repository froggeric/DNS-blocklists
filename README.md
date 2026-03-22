# DNS blocklists in adblock format

Two types of blocklists are provided for each service:

| Suffix | Type | Use Case |
|--------|------|----------|
| (none) | Full syntax | Browser extensions (uBlock Origin, AdGuard browser extension, etc.) |
| DNS | DNS-level only | AdGuard Home, Pi-hole, or other DNS-level blockers |

---

## NoAppleAds

Block Apple advertising on Apple devices.

- **Full syntax:** `https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/NoAppleAds`
- **DNS-only:** `https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/NoAppleAdsDNS`

**Updated:** 22 March 2026 (v20260322.1)

**Sources:**
- Subject alternative names for SSL certificate iadsdk.apple.com: https://certificatedetails.com/8f0e2165a72e13498d6b8de78605cccf19a0c15122d064d3f9af0e32ef8f7873/iadsdk.apple.com
- HaGeZi DNS Blocklists, NextDNS native tracking domains, v2fly domain lists
- Reddit discussions: [1](https://www.reddit.com/r/pihole/comments/dk3sv9/apple_news_ads/) [2](https://www.reddit.com/r/pihole/comments/dbkcg6/couple_sneakies_to_block/) [3](https://www.reddit.com/r/apple/comments/8o0rx0/i_just_want_to_drop_in_and_say_that_apples_news/)
- Netgate forum: https://forum.netgate.com/topic/149750/how-to-block-ads-in-apple-news/22

---

## NoYouTubeAds

Block YouTube advertising (banners, overlays, tracking). Note: DNS-level blocking cannot block video ads served from the same CDN as content.

- **Full syntax:** `https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/NoYouTubeAds`
- **DNS-only:** `https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/NoYouTubeAdsDNS`

**Updated:** 22 March 2026 (v20260322.1)

**Sources:**
- GoodbyeAds, OISD Blocklist, StevenBlack Hosts
- uBlock Origin uAssets, EasyList

---

## BlockYouTube

Completely blocks access to YouTube.

`https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/BlockYouTube`

---

## BlockParallels

Blocks Parallels software activation and licensing servers.

`https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/BlockParallels`

---

## BlockSpotifyUpdates

Blocks Spotify update servers.

`https://raw.githubusercontent.com/froggeric/DNS-blocklists/main/BlockSpotifyUpdates`

---

## Changelog

### 2026-03-22
- Split NoAppleAds and NoYouTubeAds into two versions each:
  - Full syntax versions (browser extensions) retain original names
  - New DNS-only versions with `*DNS` suffix for AdGuard Home/Pi-hole
- Updated domain lists with current verified domains
- Added new Apple advertising domains: `api-adservices.apple.com`, `searchads.apple.com`, `books-analytics-events.apple.com`, etc.
- Added new YouTube ad domains: DoubleClick variants, 2MDN, third-party ad platforms
- Fixed syntax errors in original files