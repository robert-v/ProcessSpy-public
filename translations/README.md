# ProcessSpy Translations

[ProcessSpy](https://process-spy.app) is a macOS process monitoring utility. This folder contains localization files for the app.

Community translations are welcome and appreciated. If you'd like to contribute, follow the steps below.

---

## Current Languages

| Language | Code | Status |
|---|---|---|
| English | `en` | ✅ Base language |
| Chinese Simplified | `zh-Hans` | ✅ |
| German | `de` | 🔄 In progress |
| Russian | `ru` | 🔄 In progress |
| Ukrainian | `ua` | 🔄 In progress |

---

## Contributing a New Language

Ideally you should be a native speaker with familiarity with technical 
and macOS terminology — ProcessSpy is aimed at developers and power users, 
so translations should reflect that.

Before you start, open an issue to let me know which language you'd 
like to translate. I'll add the `.xcloc` file for your language to this 
folder so you have the correct file to work with.

Once the translation is complete and the PR is merged, I'll send you 
a lifetime license for ProcessSpy as a thank you. One license per language.

## How New Strings Are Handled

When new features are added, new strings appear marked as untranslated. 
Until translated, the app displays them in English — nothing breaks for 
users. If you've translated a language, you'll occasionally receive a 
ping when new strings need attention.

---

## How to Contribute

### 1. Download the translation file

1. Go to the [ProcessSpy-public repository](https://github.com/robert-v/ProcessSpy-public)
2. Click the green **Code** button → **Download ZIP**
3. Unzip the downloaded file
4. Open the `translations` folder — you'll find `.xcloc` files, one per language

### 2. Open your language file in Xcode

Double-click the `.xcloc` file for your language. Xcode opens it in a 
dedicated translation editor showing English on the left and your language 
on the right. No project setup needed.

### 3. Translate

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

**Keep the same tone.** ProcessSpy is a technical utility aimed at developers and power users. Translations should be precise and professional rather than casual.

**macOS terminology.** Use Apple's official terminology for your language where it exists. When in doubt, check what macOS itself uses for the same concept in your language.

### 4. Submit your translation

1. Go to the [translations folder](https://github.com/robert-v/ProcessSpy-public/tree/main/translations) on GitHub
2. Click **Add file → Upload files**
3. Drag your translated `.xcloc` file into the upload area
4. Scroll down, leave the branch name as the default, and select 
   **Create a new branch and start a pull request**
5. Click **Propose changes**
6. On the next screen, update the title to something like 
   `Add German translation` and add a short description if any 
   strings were unclear or skipped
7. Click **Create pull request**t

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
