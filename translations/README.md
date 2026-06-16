# ProcessSpy Translations

[ProcessSpy](https://process-spy.app) is a macOS process monitoring utility. This folder contains localization files for the app.

Community translations are welcome and appreciated. If you'd like to contribute, follow the steps below.

---

## Current Languages

| Language | Code | Status |
|---|---|---|
| English | `en` | ✅ Base language |
| German | `de` | 🔄 In progress |
| Chinese Simplified | `zh-Hans` | 🔄 In progress |

---

## Contributing a New Language

Ideally you should be a native speaker with familiarity with technical 
and macOS terminology — ProcessSpy is aimed at developers and power users, 
so translations should reflect that.

Before you start, open an issue to let me know which language you'd 
like to translate. I'll add the language column to `Localizable.xcstrings` 
and push the updated file so you have the correct structure to work with.

Once the translation is complete and the PR is merged, I'll send you 
a lifetime license for ProcessSpy as a thank you. One license per language.

## How New Strings Are Handled

When new features are added, new strings appear in `Localizable.xcstrings` 
marked as untranslated. Until translated, the app displays them in English 
— nothing breaks for users. If you've translated a language, you'll 
occasionally receive a ping when new strings need attention.

## How to Contribute

### 1. Fork and clone the repository

```bash
git clone https://github.com/robert-v/ProcessSpy-public.git
```

### 2. Open `Localizable.xcstrings`

The file is a standard JSON file and can be edited in:
- **Xcode** — open it for a visual table editor with all languages side by side (recommended)
- **Any text editor** — edit the JSON directly if you prefer

### 3. Find your language column

Each string has slots for every language. Find the column for your language and fill in the translations. Leave the English column untouched.

### 4. Translate

A few important rules:

**Preserve placeholders exactly.** Placeholders are variables the app fills in at runtime. They must appear in your translation unchanged:

| Placeholder | Meaning |
|---|---|
| `%@` | A string value (e.g. process name) |
| `%lld` | An integer number |
| `%d` | An integer number |
| `%.1f` | A decimal number |
| `%1$@`, `%2$@` | Ordered values — order matters |

❌ Wrong: `进程 %A 正在运行`  
✅ Correct: `进程 %@ 正在运行`

**Do not translate keys.** The key is the identifier on the left side of each entry — only translate the value.

**Keep the same tone.** ProcessSpy is a technical utility aimed at developers and power users. Translations should be precise and professional rather than casual.

**macOS terminology.** Use Apple's official terminology for your language where it exists. Apple publishes localized HIG and system UI terms — when in doubt, check what macOS itself uses for the same concept.

### 5. Submit a Pull Request

Once done, submit a PR with a title like `Add Chinese Simplified translation` or `Update German translation`. Include a brief note if any strings were unclear or skipped.

---

## Tips for Chinese Simplified

- Use Simplified Chinese (`zh-Hans`), not Traditional (`zh-Hant`)
- Refer to macOS Chinese system UI for standard terminology (e.g. how macOS itself labels CPU, memory, processes)
- No spaces needed between Chinese characters and placeholders in most cases: `进程 %@ 已退出` is fine

## Tips for German

- Strings in German are typically 30–40% longer than English. Where a 
  literal translation feels too long, prefer a shorter idiomatic alternative 
  over a word-for-word translation — natural German is more important than 
  mirroring the English exactly.
- All nouns must be capitalized (`Prozess`, `Speicher`, `Filter`).
- Use `du` (informal), not `Sie` — consistent with Apple's own German macOS UI.
- Merge compound terms rather than leaving them as separate words: 
  `Prozessmonitor` not `Prozess Monitor`.
- Refer to macOS German system UI for standard terminology.

---

## Questions

If a string is ambiguous or you're unsure of context, open an issue and reference the string key. Screenshots can be provided on request.
