# Marius Comper - Portfolio Site

A bilingual (English/Romanian) portfolio website for International Editor and digital strategist Marius Comper, combining editorial sophistication with technical polish.

## Overview

Single-page portfolio site showcasing a career spanning Romanian digital media to international news aggregation at NewsNow, London. The design balances journalistic gravitas with modern web aesthetics, reflecting the intersection of editorial judgment and algorithmic systems.

## Features

- **Bilingual Interface**: Seamless EN/RO language switching with fade transitions
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Dark Editorial Theme**: Near-black (#050505) background with blue/gold accents
- **Animated Elements**: Subtle marquee ticker, scroll-reveal animations, hover effects
- **Content Sections**:
  - Hero with personal motto "Nunquam Dormio"
  - Core editorial values (Algorithmic Neutrality, Cultural Diversity, Vigilance)
  - Career timeline from GSP.ro (2003) to NewsNow International Editor (2020+)
  - Curated writings portfolio with links to published articles
  - Civic engagement (Superscrieri jury member)

## Tech Stack

- **HTML5** with semantic markup
- **Tailwind CSS** (via CDN) for utility-first styling
- **Vanilla JavaScript** for interactivity
- **Google Fonts**: 
  - Playfair Display (editorial serif)
  - JetBrains Mono (technical credibility)
  - Inter (UI readability)
- **Font Awesome** for icons

## Design Philosophy

The site employs what might be called "editorial brutalism" - sharp edges (1px border-radius), restrained color palette, sophisticated typography, and subtle texture (SVG noise overlay at 3.5% opacity). The aesthetic choices reflect the subject's professional identity: precision, neutrality, and the tension between algorithmic systems and human curation.

**Key Design Decisions:**
- **Typography Hierarchy**: Playfair for gravitas, JetBrains Mono for technical contexts, Inter for body text
- **Color System**: `news-black` (#050505), `accent-blue` (#3b82f6) for trust/tech, `accent-gold` (#d4af37) for editorial prestige
- **Minimal Animation**: Purposeful restraint to avoid undermining serious content
- **Sharp Borders**: Editorial sharpness over rounded modern UI trends

## Structure

```
├── Hero Section
│   ├── Name & Title
│   ├── Location Badge (London, UK)
│   └── Bio + Quote
├── Ticker (Breaking News Style)
├── Ethos Cards (3 Core Values)
├── Main Content Bento Grid
│   ├── Current Role Card
│   ├── Origins Card (Previous Roles)
│   └── Civic Engagement Card
├── Career Timeline (2003-Present)
└── Selected Writings (4 Featured Articles)
```

## Customization

### Updating Content

All translatable content lives in the `translations` object (lines 574-664):

```javascript
const translations = {
    en: {
        "nav.ethos": "Values",
        "hero.quote": "\"Information must be neutral...\"",
        // ... etc
    },
    ro: {
        // Romanian translations
    }
};
```

### Modifying Colors

Adjust the Tailwind config (lines 27-35):

```javascript
colors: {
    'news-black': '#050505',
    'accent-blue': '#3b82f6',
    'accent-gold': '#d4af37',
    // ...
}
```

### Animation Speed

Ticker speed is controlled in keyframes (line 42):
```javascript
'marquee': 'marquee 45s linear infinite',
```
Reduce to 25-30s for faster breaking-news feel.

## Deployment

### GitHub Pages
1. Push to repository
2. Settings → Pages → Source: main branch
3. Site will be live at `https://[username].github.io/[repo-name]`

### Netlify
1. Connect repository
2. Build command: (none needed - static HTML)
3. Publish directory: `/`
4. Deploy

### Vercel
```bash
vercel --prod
```

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile: iOS Safari 14+, Chrome Android 90+

Note: Uses modern CSS (custom properties, Grid, Flexbox) and ES6+ JavaScript. IE11 not supported.

## Performance Considerations

**Current Setup:**
- CDN-hosted Tailwind (~500KB uncompressed)
- Google Fonts preconnect
- Font Awesome CDN

**Production Optimization:**
- Build Tailwind with PurgeCSS (reduce to ~10-20KB)
- Self-host fonts for GDPR compliance
- Replace Font Awesome with inline SVGs (reduce HTTP requests)
- Add service worker for offline capability

## Known Issues

- Language switcher placement could be more integrated (consider nav bar icons)
- Orbit animation system (if prominent) may feel gimmicky for editorial context
- No analytics/tracking (add Google Analytics or privacy-focused alternative if needed)

## Credits

**Design & Development:**
- Research: ChatGPT (biographical content compilation)
- Implementation: Google Gemini (HTML/CSS/JS generation)
- Content Subject: Marius Comper

**Fonts:**
- Playfair Display by Claus Eggers Sørensen
- JetBrains Mono by JetBrains
- Inter by Rasmus Andersson

## License

Personal portfolio site. All biographical content relates to Marius Comper. Code structure and design patterns may be adapted with attribution.

## Contact

- **Facebook**: [facebook.com/marius.comper](https://www.facebook.com/marius.comper)
- **Professional**: International Editor at NewsNow.co.uk
- **Location**: London, UK

---

*"Nunquam Dormio" - Never Sleeping, Always Vigilant*
