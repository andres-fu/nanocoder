---
"@nanocollective/nanocoder": patch
---

Fix Windows treating differently cased spellings of the same folder as different folders. A directory you already trusted as `C:\Work\Proj` no longer prompts for trust again when the working directory is spelled `c:\work\proj`, editor sessions still load that project's plugins, and file tools no longer throw `Invalid file path` for a valid absolute path that only differs in case. Paths are compared in a normalized form while the saved trust entry keeps your original spelling.
