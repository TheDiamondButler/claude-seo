# Schema / Structured Data — rings.anjain.in

**Score: 0 / 100** (unverifiable, page not indexed)

## Required Schema for a Rings Landing/Category Page

### Organization (required for brand entity)
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "A.N. JAIN",
  "url": "https://www.anjain.in",
  "logo": "https://www.anjain.in/logo.png",
  "sameAs": [
    "https://www.instagram.com/anjain.in/"
  ],
  "description": "Lab grown diamond jewellery made with recycled gold"
}
```

### ItemList (for category pages listing multiple rings)
```json
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "name": "Lab Grown Diamond Rings",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "url": "https://www.anjain.in/shop/p/samantha",
      "name": "Samantha Ring"
    }
  ]
}
```

### Product (on individual ring listings, if present)
Must include: name, image, description, offers.price, offers.priceCurrency, offers.availability, material, brand.

## Critical Missing
- No BreadcrumbList schema (navigation context for subdomain)
- No WebPage schema with `isPartOf` pointing to main site
- No canonical breadcrumb trail from subdomain to main brand
