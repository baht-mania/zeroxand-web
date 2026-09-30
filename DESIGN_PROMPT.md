# ZEROXAND 사이트 사양 (디자인 의뢰용)

외부 AI나 디자이너에게 작업을 맡길 때 아래 블록을 그대로 붙여넣는다. 현재 `index.html` 기준이며 확정 사항이 바뀌면 이 파일부터 고친다.

```
You are refining an existing one-page corporate website for ZEROXAND, a game developer and publisher. The attached index.html is the current build. Keep its structure, content and brand system; improve craft only where asked. Do not revert any of the fixed facts below.

## Fixed facts (do not change)
- Brand: ZEROXAND. Legal name: ZERO X AND PTE. LTD. Singapore, incorporated 02 Nov 2021.
- Primary activity: Publishing of games software/applications (SSIC 58201)
- Contact: baht@0xand.com
- Office: 38 Beach Road, #17-12, South Beach Tower, Singapore 189767
- Domain: https://zeroxand.com (static site on Vercel)
- Do NOT show: UEN, company type, registered office in the Company block, UEN in the footer.
- English only. No invented numbers, player counts, awards, partners, store links, Discord or trailers.

## Brand system (CI)
- Logo: "ZEROXAND" geometric wordmark with a red X (assets/brand/zeroxand-logo.png, transparent). No pixel "0x&" mark.
- Colors: Carbon #0A0A0B, Ivory #F1EFE8, Ash #B7B3AA, Signal Red #D54A3A (sparingly), Gunmetal #242427
- Type: Archivo Black (display), Inter (body), IBM Plex Mono (labels / metadata)
- Mood: "Black File" — cinematic, restrained, credible. No neon glow, no particles, no glassmorphism, no purple/blue gradients.

## Sections (in order)
1. Hero: the ZEROXAND logo, revealed once with a left-to-right wipe, then one scan line. Line: "We develop and publish games for players around the world." Meta: Singapore / Est. 2021 / Independent Studio. Link: Next title — Project X — Q4 2027.
2. Project X (disclosed): anime-style side-scrolling defense game; Mobile, PC, H5; launch Q4 2027; Access: Restricted. World background art + 5-character showcase (click a thumbnail to switch):
   - 01 Sera — Medic / Researcher (default)
   - 02 Izuna — Wandering Swordswoman / Leader
   - 03 Roha — Scrap Hunter
   - 04 Nut — Mechanic / Hacker
   - 05 Sion — Sniper / Scout
   Then a full-width "Classified" project archive file (stamp, restricted-access tag, spec rows, one redacted "Internal notes" row).
3. Track Record: Ragnarok Monster World — developed & published in-house, global service 2024–2025. Artwork dominates; carousel controls stay quiet. Legal line: "Ragnarok and related marks are trademarks of their respective owners."
4. Company: editorial profile — "ZERO X AND / PTE. LTD." headline, Singapore / Est. 2021, one-line description, registry rows (Legal name, Incorporated, Primary activity only).
5. Contact: large "LET'S TALK." with a red arrow (mailto), email and Singapore office.
6. Footer: © ZERO X AND PTE. LTD. · Singapore

## Principles
Project X = anticipation, Ragnarok Monster World = proof, Company = trust, ZERO X AND = brand.
One strong hero animation only; other motion is subtle. Respect prefers-reduced-motion, WCAG AA contrast, visible focus, no horizontal overflow at 360px. Mobile is composed as a vertical poster, not a shrunk desktop.
```
