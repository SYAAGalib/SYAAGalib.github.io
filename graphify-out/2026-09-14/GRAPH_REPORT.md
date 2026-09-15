# Graph Report - dotcv-main  (2026-09-14)

## Corpus Check
- cluster-only mode — file stats not available

## Summary
- 107 nodes · 162 edges · 11 communities
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- i18n/index.ts
- pages/index.astro
- package.json
- tsconfig.json
- cvSchema.ts
- registry.ts
- dependencies
- generate-comparison.mjs
- generate-screenshots.mjs

## God Nodes (most connected - your core abstractions)
1. `getTranslations()` - 8 edges
2. `resolveAsset()` - 7 edges
3. `scripts` - 7 edges
4. `loadConfig()` - 6 edges
5. `DotcvConfig` - 5 edges
6. `resolveTheme()` - 5 edges
7. `parseJson()` - 3 edges
8. `compilerOptions` - 3 edges
9. `include` - 3 edges
10. `ThemeName` - 2 edges

## Surprising Connections (you probably didn't know these)
- `loadData()` --calls--> `parseJson()`  [EXTRACTED]
  src/lib/parser/index.ts → src/lib/parser/jsonParser.ts

## Import Cycles
- None detected.

## Communities (11 total, 0 thin omitted)

### Community 0 - "i18n/index.ts"
Cohesion: 0.20
Nodes (6): resolveAsset(), DotcvConfig, getTranslations(), SupportedLocale, TranslationKey, translations

### Community 1 - "pages/index.astro"
Cohesion: 0.15
Nodes (11): dotcvConfigSchema, cvSchema, loadConfig(), loadData(), parseJson(), jsonLd, nameParts, resolvedTheme (+3 more)

### Community 2 - "package.json"
Cohesion: 0.12
Nodes (15): devDependencies, @types/node, engines, node, name, scripts, astro, build (+7 more)

### Community 3 - "tsconfig.json"
Cohesion: 0.17
Nodes (11): **/*, astro/tsconfigs/strict, .astro/types.d.ts, dist, node, compilerOptions, strict, types (+3 more)

### Community 4 - "cvSchema.ts"
Cohesion: 0.20
Nodes (9): certificationsSchema, CVData, educationItemSchema, experienceSchema, languageItemSchema, profileSchema, projectItemSchema, skillCategorySchema (+1 more)

### Community 5 - "registry.ts"
Cohesion: 0.29
Nodes (7): resolvedTheme, getTheme(), ResolvedTheme, resolveTheme(), ThemeDefinition, ThemeName, themes

### Community 6 - "dependencies"
Cohesion: 0.29
Nodes (7): astro, dependencies, astro, puppeteer, zod, puppeteer, zod

### Community 7 - "generate-comparison.mjs"
Cohesion: 0.67
Nodes (3): checkServer(), main(), OUTPUT_DIR

### Community 8 - "generate-screenshots.mjs"
Cohesion: 0.67
Nodes (3): checkServer(), main(), OUTPUT_DIR

## Knowledge Gaps
- **44 isolated node(s):** `SupportedLocale`, `TranslationKey`, `CVData`, `ResolvedTheme`, `ThemeDefinition` (+39 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 55 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `dependencies` connect `dependencies` to `package.json`?**
  _High betweenness centrality (0.019) - this node is a cross-community bridge._
- **What connects `SupportedLocale`, `TranslationKey`, `CVData` to the rest of the system?**
  _44 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `package.json` be split into smaller, more focused modules?**
  _Cohesion score 0.125 - nodes in this community are weakly interconnected._