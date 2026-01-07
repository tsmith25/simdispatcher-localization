# SIM Dispatcher Localization

Community-driven localization repository for the SIM Dispatcher platform.

- Language and locale resources
- Region-specific formatting and conventions
- Simulation-specific localization assets
- Name pools for realistic dialog generation

This repository is planned to be extended to cover additional localization resources for SIM Dispatcher beyond personal names. The goal is to progressively support broader region- and locale-specific assets required for accurate simulation localization, while maintaining the same strict structure, validation rules, and locale constraints defined in this repository. All extensions will remain data-only and locale-scoped.

**Important: Commit messages must follow Conventional Commits and use the locale as the scope (example: `feat(en-US): add family names`).**

## Supported Locales

Only the following language and region combinations are accepted. Submissions outside this list are rejected.

| Region | ISO Country | Phone Code | Locale (used in Files) |
|------|------------|------------|------------------------|
| Germany | DE / DEU | 49 | `de-DE`                |
| Austria | AT / AUT | 43 | `de-AT`                |
| Switzerland | CH / CHE | 41 | `de-CH`                |
| Netherlands | NL / NLD | 31 | `nl-NL`                |
| United Kingdom | GB / GBR | 44 | `en-GB`                |
| United States | US / USA | 1 | `en-US`                |
| France | FR / FRA | 33 | `fr-FR`                |
| Poland | PL / POL | 48 | `pl-PL`                |
| Italy | IT / ITA | 39 | `it-IT`                |
| Spain | ES / ESP | 34 | `es-ES`                |
| Luxembourg | LU / LUX | 352 | `lb-LU`                |
| Czech Republic | CZ / CZE | 420 | `cs-CZ`                |
| Denmark | DK / DNK | 45 | `da-DK`                |
| Sweden | SE / SWE | 46 | `sv-SE`                |
| Finland | FI / FIN | 358 | `fi-FI`                |
| Norway | NO / NOR | 47 | `nb-NO`                |

[See Reference ...](https://docs.resqueserve.com/reference/XENBIT.ResQueServe.Abstractions.DataStructures.Country.html)

## Repository Structure

```
resources/
├── PersonNames/
│ ├── Firstname.Female.<locale>.txt
│ ├── Firstname.Male.<locale>.txt
│ └── Lastname.<locale>.txt
```

### Name Localization

Path: `resources/PersonNames`

**Purpose:** 

SIM Dispatcher generates dialogs by randomly selecting personal names appropriate to the active locale.

Rules:

- One name per line
- UTF-8 encoding
- No numbering, no punctuation
- Culturally accurate names only
- Locale suffix must match exactly

Current examples:

- `Firstname.Female.de-DE.txt`
- `Firstname.Male.de-DE.txt`
- `Lastname.de-DE.txt`

SIM Dispatcher selects names at runtime using uniform random distribution.

## Contribution

Contributions are welcome.

* Submit all changes via pull requests only
* Content must be locale-correct and culturally appropriate
* Existing file structure, naming, and formatting must be followed exactly
* Each pull request must contain changes for one locale only
* Review `docs/conventional-commits-cheatsheet.md` before submitting
* Commit messages must follow Conventional Commits and use the locale as the scope (example: `feat(en-US): add family names`)

All submissions are reviewed for structural correctness and consistency before being merged.