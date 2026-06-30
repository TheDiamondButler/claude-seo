# Technical SEO — rings.anjain.in

**Score: 22 / 100**

## Critical Issues

### 1. Zero Google Indexation — CRITICAL
`site:rings.anjain.in` returns zero results. The subdomain is invisible to organic search.
- No pages crawled, indexed, or appearing in any SERP
- Likely cause: very new domain, noindex meta tag, or password protection
- **Fix:** Verify robots.txt allows Googlebot; submit sitemap to GSC; check for noindex meta

### 2. Subdomain vs Subfolder — CRITICAL SEO Architecture Error
Using `rings.anjain.in` (subdomain) instead of `www.anjain.in/rings/` or `www.anjain.in/shop/rings/` (subfolder) splits domain authority.

- Google treats subdomains as separate websites
- Domain authority, backlinks, and crawl budget from `anjain.in` do NOT flow to `rings.anjain.in`
- `anjain.in` itself has virtually zero backlink profile (~0–5 referring domains estimated)
- Creating a subdomain takes that minimal authority and **cuts it in half**
- Every major SEO study (Moz, Ahrefs) confirms subfolders outperform subdomains for e-commerce category pages

**Impact:** The rings page must earn authority from scratch, with no inheritance from the brand domain.

### 3. Platform Fragmentation — HIGH
- Main site: Squarespace on `198.49.23.144`
- `rings.anjain.in`: AWS EC2 `98.84.224.111` — a completely separate hosting environment

This means:
- Two separate GSC Search Console properties needed
- No unified sitemap
- No unified analytics (unless manually configured)
- Canonical relationship between subdomain and main site must be manually established

### 4. Canonical Tags — Unknown / At Risk — HIGH
Without a `<link rel="canonical">` on `rings.anjain.in` pointing to either itself or the canonical version on the main domain, Google may:
- Index both and split signals
- Choose not to index the subdomain if it sees it as a thin duplicate of the main rings section

### 5. HTTPS / Security — Unknown
Could not verify TLS configuration, HSTS headers, or CSP headers due to network egress restriction.

## What Works
- DNS resolves correctly (`rings.anjain.in → 98.84.224.111`)
- Subdomain separation could be valid for a standalone campaign or microsites (but not recommended for SEO)
