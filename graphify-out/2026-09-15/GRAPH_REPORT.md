# Graph Report - dotcv-main  (2026-09-14)

## Corpus Check
- 32 files · ~127,944 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 133 nodes · 185 edges · 14 communities (10 shown, 2 thin omitted)
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- i18n/index.ts
- configParser.ts
- package.json
- tsconfig.json
- cvSchema.ts
- registry.ts
- dependencies
- generate-comparison.mjs
- generate-screenshots.mjs
- dotcv
- rules/graphify.md
- workflows/graphify.md

## God Nodes (most connected - your core abstractions)
1. `dotcv` - 10 edges
2. `getTranslations()` - 8 edges
3. `scripts` - 7 edges
4. `resolveAsset()` - 7 edges
5. `loadConfig()` - 6 edges
6. `DotcvConfig` - 5 edges
7. `resolveTheme()` - 5 edges
8. `Available Themes` - 4 edges
9. `Quick Start` - 4 edges
10. `parseJson()` - 3 edges

## Surprising Connections (you probably didn't know these)
- `loadData()` --calls--> `parseJson()`  [EXTRACTED]
  src/lib/parser/index.ts → src/lib/parser/jsonParser.ts

## Import Cycles
- None detected.

## Communities (14 total, 2 thin omitted)

### Community 0 - "i18n/index.ts"
Cohesion: 0.22
Nodes (5): resolveAsset(), getTranslations(), SupportedLocale, TranslationKey, translations

### Community 1 - "configParser.ts"
Cohesion: 0.29
Nodes (3): DotcvConfig, dotcvConfigSchema, loadConfig()

### Community 2 - "package.json"
Cohesion: 0.12
Nodes (15): devDependencies, @types/node, engines, node, name, scripts, astro, build (+7 more)

### Community 3 - "tsconfig.json"
Cohesion: 0.17
Nodes (11): **/*, astro/tsconfigs/strict, .astro/types.d.ts, dist, node, compilerOptions, strict, types (+3 more)

### Community 4 - "cvSchema.ts"
Cohesion: 0.16
Nodes (12): certificationsSchema, CVData, cvSchema, educationItemSchema, experienceSchema, languageItemSchema, profileSchema, projectItemSchema (+4 more)

### Community 5 - "registry.ts"
Cohesion: 0.15
Nodes (13): jsonLd, nameParts, resolvedTheme, skillKeywords, twitterSocial, resolvedTheme, resolvedTheme, getTheme() (+5 more)

### Community 6 - "dependencies"
Cohesion: 0.29
Nodes (7): astro, dependencies, astro, puppeteer, zod, puppeteer, zod

### Community 7 - "generate-comparison.mjs"
Cohesion: 0.67
Nodes (3): checkServer(), main(), OUTPUT_DIR

### Community 8 - "generate-screenshots.mjs"
Cohesion: 0.67
Nodes (3): checkServer(), main(), OUTPUT_DIR

### Community 11 - "dotcv"
Cohesion: 0.09
Nodes (21): 1. Classic Theme (`classic`), 1. Clone the repository & install dependencies, 1. Configure site URL (`astro.config.mjs`), 1. `dotcv.config.json` (Settings), 2. Add your CV data, 2. Choose your hosting provider, 2. `cv.json` (Resume Data), 2. Sidebar Theme (`sidebar`) (+13 more)

## Knowledge Gaps
- **61 isolated node(s):** `name`, `type`, `version`, `node`, `dev` (+56 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 75 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **2 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `dependencies` connect `dependencies` to `package.json`?**
  _High betweenness centrality (0.012) - this node is a cross-community bridge._
- **What connects `name`, `type`, `version` to the rest of the system?**
  _61 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `package.json` be split into smaller, more focused modules?**
  _Cohesion score 0.125 - nodes in this community are weakly interconnected._
- **Should `dotcv` be split into smaller, more focused modules?**
  _Cohesion score 0.09090909090909091 - nodes in this community are weakly interconnected._