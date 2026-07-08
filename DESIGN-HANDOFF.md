# 927fc7e4-07cc-4c21-a4ec-1c7f0085e87a implementation handoff

This archive is the source of truth for turning the design into production code. Start from `index.html`, then preserve the visual system, responsive behavior, and interactions found in the exported files.

## Implementation target
- Build production UI from the exported design, not a loose reinterpretation.
- Preserve typography scale, spacing rhythm, color tokens, border radii, shadows, motion timing, and component states.
- Replace static placeholders only when the target app has real data or functional equivalents.
- Keep generated product UI free of Open Design chrome, preview labels, or design-process annotations.
- Treat this handoff as a visual contract: if implementation choices conflict, match the exported pixels and behavior first, then refactor internals.

## Source map
- Primary entry: `index.html`
- HTML screens detected: 2
- Stylesheets detected: 0
- Script/component files detected: 0
- Supporting assets detected: 102

## Responsive contract
Validate the implementation across this 2025–2026 viewport matrix:
- Mobile compact: 360×800
- Mobile standard: 390×844
- Mobile large: 430×932
- Foldable / small tablet: 600×960
- Tablet portrait: 820×1180
- Tablet landscape: 1024×768
- Laptop: 1366×768
- Desktop: 1440×900
- Wide desktop: 1920×1080

For responsive web exports, treat these as a modern breakpoint system for one adaptive web experience, not three fixed screenshots. Do not split responsive web into unrelated native app screens unless the project explicitly includes native targets. Use semantic layout thresholds, fluid `clamp()` type/spacing, and container queries where component width matters more than viewport width. Preserve any CSS media queries, container queries, fluid `clamp()` scales, and layout changes already present in the exported files.

## Design fidelity contract
- Extract reusable tokens before writing components: background, surface, foreground, muted text, border, accent, radius, shadow, spacing, type scale, and motion duration/easing.
- Map product screens, in-app modules/components, optional landing page, and optional OS widget surfaces before coding. Keep these surfaces separate in the target architecture.
- Match layout geometry: max-widths, gutters, grid columns, card proportions, sticky/fixed elements, and viewport-specific navigation.
- Preserve real copy, labels, and data shown in the export. Do not replace specific text with generic marketing filler.
- Preserve interactive affordances: hover, focus, pressed, disabled, loading, validation, copy/share, tab/accordion, modal/sheet, and keyboard states where present.
- Preserve accessibility semantics when converting: headings stay hierarchical, controls remain buttons/links/inputs, focus states stay visible.
- Do not keep prototype-only annotations, frame labels, or Open Design chrome in the production UI.

## CJX-ready UX contract
- Use `DESIGN-MANIFEST.json` as the machine-readable map for screens, app modules, OS widgets, landing pages, tokens, interactions, and viewport checks.
- Screen-file-first: when multiple user-facing surfaces exist, implement each HTML screen as its own route/file. Treat `index.html` as a launcher/overview when the manifest marks it that way, not as a combined final UI.
- If `landing.html`, app screens, platform screens, or OS widget files exist, preserve those boundaries in the target app instead of merging them into one page.
- A single self-contained `index.html` is acceptable only when the export truly contains one user-facing screen and its CSS/JS are structured enough to extract tokens, components, states, and behavior.
- If separate `css/` or `js/` files exist, treat them as source of truth for token/component/interactions before porting to React, Vue, SwiftUI, Compose, or another target stack.
- In-app modules/components are product UI blocks inside the app. OS widgets are home-screen/lock-screen/quick-access surfaces outside the app. Do not merge those concepts.

## Color and brand contract
- Use the exported design tokens and product/domain context as the color source of truth.
- Do not introduce warm beige / cream / peach / pink / orange-brown background washes unless they are already explicit brand/reference colors in the export.
- No obvious token stylesheet was detected; sample colors from the entry file and convert them into named tokens before coding.

## Implementation sequence for AI coding tools
1. Open `index.html` and `DESIGN-MANIFEST.json`; identify every screen file, launcher/overview file, app module, and interaction before coding.
2. If multiple HTML screens exist, map them to separate routes/surfaces first; do not merge `landing.html`, product app screens, platform screens, or OS widgets into one route.
3. Extract a token table from CSS/root styles and inline styles before building framework components.
4. Build product screens and domain-specific in-app modules from largest layout regions down to controls; avoid starting with isolated atoms that lose spatial intent.
5. Port responsive behavior across the modern viewport matrix and test each semantic breakpoint before cleanup.
6. Port interactions and states, then replace static placeholders only with real app data or functional equivalents.
7. Keep optional landing page and OS widget surfaces as separate surfaces if present.
8. Compare final screenshots against the export at 360×800, 390×844, 430×932, 820×1180, 1024×768, 1366×768, 1440×900, and 1920×1080 before declaring done.

## Entry points
- `index.html`
- `santtini-catalog.html`

## Styles
- None detected

## Scripts/components
- None detected

## Assets and supporting files
- `mq75cp6e-logo.svg`
- `mq75mko9-image.png`
- `mq77143m-image.png`
- `mq776ev7-image.png`
- `mq77s6en-image.png`
- `mq77wxjy-image.png`
- `mq780yfu-image.png`
- `mq785w5x-image.png`
- `mq78egt3-image.png`
- `mq7ea3wn-image.png`
- `mq7fpzo0-image.png`
- `mqaei8bc-mini-kibe.png`
- `mqaei8d2-mini-risoles.png`
- `mqaei8e5-mini-bolinha-de-queijo.png`
- `mqaei8fb-mini-coxinha.png`
- `mqaeryrd-mini-coxinha-de-carne.png`
- `mqaeryt2-mini-kibe-2.png`
- `mqaeryu6-mini-bolinha-de-queijo-2.png`
- `mqaeryvp-mini-risole-2.png`
- `mqaeryww-mini-coxinha-de-frango_.png`
- `mqaf0ahp-coxinha-de-carne_.png`
- `mqaf0ajp-coxinha-de-frango.png`
- `mqaf0alp-risole-de-carne.png`
- `mqaf0amv-risole-de-presunto-e-queijo.png`
- `mqaf0aoq-enroladinho.png`
- `mqaf0apw-kibe_.png`
- `mqaf2n9s-image.png`
- `mqahcens-assado-de-frango.png`
- `mqahceq9-assado-de-frango-com-bacon.png`
- `mqahces3-pão-de-batata.png`
- `mqahcet4-Pranchpão-de-batata-presunto.png`
- `mqahceup-pão-de-batata-frango.png`
- `mqahcew1-hamburguer.png`
- `mqahcexs-dog-americano.png`
- `mqahcez2-esfiha-1.png`
- `mqahcf0e-esfiha-2.png`
- `mqahcf1e-sfiha-de-frango.png`
- `mqahcf3z-dog.png`
- `mqahcf60-pão-pizza.png`
- `mqahcfdw-assado-de-calabresa.png`
- `mqahhnl4-sfiha-de-carne.png`
- `mqahkncp-sfiha-de-carne.png`
- `mqahtth4-site-item.png`
- `mqahyimc-site-item.png`
- `mqaimaeu-Bolacha-de-Nata-Super-480x270.png`
- `mqaimrb0-receita-de-suspiro.jpeg`
- `mqaizuya-2.png`
- `mqaizv19-3.png`
- `mqaizv2y-1.png`
- `mqaj7ly4-image.png`
- `mqajfyqx-image.png`
- `mqajk3st-image.png`
- `mqajqkgf-3.png`
- `mqajqkju-1.png`
- `mqajqklj-2.png`
- `mqlpb072-magnific_melhore-a-qualidade-da-im_xgfYbvyjfW.png`
- `mqlpb1lk-magnific_melhore-a-qualidade-da-im_CHp4tMcEEy.png`
- `mqlpb2yr-magnific_melhore-a-qualidade-da-im_kLhGQRK16B.png`
- `mqsdcbst-magnific_melhore-a-qualidade-da-im_CHdQfUDEEy.png`
- `mqsdr92h-magnific_melhore-a-qualidade-da-im_CHdQfUDEEy.png`
- `mqsemq1t-magnific_melhore-a-qualidade-da-im_CHdQfUDEEy.png`
- `mqsv2cca-magnific_recrie-melhorando-a-quali_Te38vdpVNR.png`
- `mqsv5cct-magnific_melhore-a-qualidade-da-im_ubBq10yQLD.png`
- `mqsvd7lp-magnific_melhore-a-qualidade-da-im_MXZtQ47DCm.png`
- `mqsvg6yl-magnific_melhore-a-qualidade-da-im_5xh1b2GKxe.png`
- `mqsvhmfe-magnific_melhore-a-qualidade-da-im_fFeuaGlCDY.png`
- `mqsvj3n5-magnific_melhore-a-qualidade-da-im_LUQyAddswO.png`
- `mqsvk30j-magnific_melhore-a-qualidade-da-im_CHdQf2CEEy.png`
- `mqsvqf9h-magnific_melhore-a-qualidade-da-im_l7HUsmegv9.png`
- `mqsvzww3-magnific_melhore-a-qualidade-da-im_jSug97SLD0.png`
- `mqsvzxzg-magnific_melhore-a-qualidade-da-im_l7HwiyQgv9.png`
- `mqsvzz4s-magnific_melhore-a-qualidade-da-im_DB2XfoRpcl.png`
- `mqsw3pi8-magnific_melhore-a-qualidade-da-im_DB2XfoRpcl-_1_.png`
- `mqsw4k0n-magnific_melhore-a-qualidade-da-im_l7HwiyQgv9-_1_.png`
- `mqsw6fcu-magnific_melhore-a-qualidade-da-im_DB2XfoRpcl-_1_.png`
- `mqsw6yv0-magnific_melhore-a-qualidade-da-im_jSug97SLD0-_1_.png`
- `mqsw866x-magnific_melhore-a-qualidade-da-im_l7HwiyQgv9-_2_.png`
- `mqsw9h46-magnific_melhore-a-qualidade-da-im_y6x281SPW9-_1_.png`
- `mqsw9jl5-magnific_melhore-a-qualidade-da-im_swFPVuCl8e-_1_.png`
- `mqsw9lkv-magnific_melhore-a-qualidade-da-im_l7HwiyQgv9-_2_.png`
- `mqswd5qq-2.png`
- `mqswd5si-3.png`
- `mqswd5uc-1.png`
- `mqswdxmc-3.png`
- `mqswfucc-3.png`
- `mqswhfr4-magnific_melhore-a-qualidade-da-im_aQp5JrSfSh.png`
- `mqtp5v5d-magnific_melhore-a-qualidade-da-im_brmZV895Y2.png`
- `mqtp6nko-magnific_melhore-a-qualidade-da-im_jSuWBpTLD0.png`
- `mqtp6yvb-magnific_melhore-a-qualidade-da-im_mCV7472hJQ.png`
- `mqtp7k8u-magnific_melhore-a-qualidade-da-im_EqX9XPAuuO.png`
- `mqtpd7iz-magnific_melhore-a-qualidade-da-im_xgEYqKAjfW.png`
- `mqtpkezs-magnific_melhore-a-qualidade-da-im_xgEYqKAjfW-_1_.png`
- `mqtpl5vj-magnific_melhore-a-qualidade-da-im_brmZV895Y2-_1_.png`
- `mqtplo97-magnific_melhore-a-qualidade-da-im_mCV7472hJQ-_1_.png`
- `mqtpoco0-magnific_melhore-a-qualidade-da-im_jSuWBpTLD0-_1_.png`
- `mqtpslzx-magnific_melhore-a-qualidade-da-im_LUQcfdcswO.png`
- `mqtpt7o9-magnific_melhore-a-qualidade-da-im_l7HTIXLgv9.png`
- `mqtq08yy-magnific_melhore-a-qualidade-da-im_l7HVZJKgv9.png`
- `mqv8xin6-magnific_melhore-a-qualidade-da-im_BmYcDfRoQR.png`
- `mqv8y5uw-magnific_melhore-a-qualidade-da-im_1sfEqSYr4r.png`
- `mqv8z44q-magnific_melhore-a-qualidade-da-im_BmYcDfRoQR.png`
- `mqv95dz1-magnific_melhore-a-qualidade-da-im_NZlURAh6D9.png`

## Coding checklist for AI tools
1. Inspect `index.html` and `DESIGN-MANIFEST.json` first and identify reusable components before coding.
2. Implement each user-facing screen file as its own route/surface; keep launcher, landing, app, platform, and OS widget files separate.
3. Extract design tokens into the target stack: colors, type scale, spacing, radius, shadows, and motion.
4. Implement layout with real 2025–2026 responsive breakpoints, fluid type/spacing, and container-query-aware component behavior; test with no horizontal overflow.
5. Preserve interactive controls, hover/focus/pressed states, form behavior, validation, and copy actions where present.
6. Implement domain-specific in-app modules with real states; do not flatten them into generic cards.
7. Keep landing page, product screens, and OS widget/quick-access surfaces separate when present.
8. Confirm the production result visually matches the exported design before refactoring internals.
9. Reject implementation shortcuts that flatten the design into generic cards, generic gradients, placeholder stats, or framework-default typography.
10. If a detail is ambiguous, keep the exported HTML/CSS/JS behavior rather than inventing a new pattern.
