# Flåklypa Grand Prix (2000-2002) Preservation Project

Digital preservation and compatibility project for the original PC releases of *Flåklypa Grand Prix* (2000-2002). (English: *Pinchcliffe Grand Prix*).

Covers only the original release (2000), Anniversary Edition (2001), and Gold Edition (2002).

These games have not been commercially available for many years.

This repository does not contain the original game data.

---

## Legal Notice

*Flåklypa Grand Prix / Pinchcliffe Grand Prix* and related intellectual property remain the property of their respective rights holders.

This is an unofficial preservation project and is not affiliated with, endorsed by, or sponsored by any rights holder.

The repository does **not** include the original game, installation media, or copyrighted game assets. Links to third-party sources are provided for preservation purposes only. Availability and legality of third-party sources may vary by jurisdiction.

Users are responsible for ensuring they have the legal right to use any software referenced by this project.

---
## 🇳🇴 Prosjektoversikt (English below)

Dette prosjektet har som mål å bevare og gjøre en viktig del av norsk spillhistorie tilgjengelig gjennom:

- Installasjonsveiledning for moderne Windows.
- Arkiverte offisielle oppdateringer.
- Erstatningsfil (`FGP.exe`) for moderne Windows-kompatibilitet.
- dgVoodoo2-konfigurasjon for  "widescreen" og "borderless fullscreen".
- Forbedring av [Wikipedia](https://no.wikipedia.org/wiki/Fl%C3%A5klypa_Grand_Prix_(PC-spill)) og [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Pinchcliffe_Grand_Prix) artikler.
- Lenker til eksterne arkiveringsressurser, inkludert Archive.org.
- Lenker til mine andre prosjekter om bevaring og synliggjøring av norske dataspill.

---

###  Bevaring av norsk spillhistorie og digital kulturarv

Mange eldre norske PC-spill blir ikke lenger solgt og risikerer å gå tapt, til tross for at de er 100 % digitale. De er en viktig del av Norges digitale spillhistorie.

Spill som ikke lenger selges bør bevares og bli offentlig arkivert av Nasjonalbiblioteket eller lignende offentlige institusjoner, fremfor å være avhengige av frivillige og Archive.org for langsiktig bevaring.

Hvis offisielle nyutgivelser eller remastere blir tilgjengelige på GOG eller Steam, er den beste måten å støtte rettighetshaverne på å kjøpe disse. Bedre tilgjengelighet av eldre versjoner kan også skape økt interesse for nyere utgivelser, som *[Flåklypa Grand Prix (2021)](https://store.steampowered.com/app/3352670)*. Interesse for offisielle nyutgivelser kan også vises ved å stemme på [GOG Dreamlist](https://www.gog.com/dreamlist/game/pinchcliffe-grand-prix-2000).

Offisielle nyutgivelser, remastere, offentlig og frivillig arkivering, blant annet gjennom Archive.org, spiller alle en viktig rolle i bevaringen av Norges digitale spillhistorie.

### Tilgang til spillet

De originale spillene har aldri blitt utgitt digitalt og er ikke lenger kommersielt tilgjengelige. For å bevare vår kulturarv finnes det fellesskapsarkiverte kopier på Archive.org.

* [Gullutgave (2002)](https://archive.org/details/flaklypagullutgave) Guiden er for denne.
* [Originalen (2000)](https://archive.org/details/flaklypa-grand-prix-cracket) Guide følger med.
* [Andre versjoner og nye opplastinger](https://archive.org/search?query=Fl%C3%A5klypa+Grand+Prix)
* [Stem på GOG Dreamlist for nyutgivelse!](https://www.gog.com/dreamlist/game/pinchcliffe-grand-prix-2000)

### Installasjonsguide: Gullutgave (2002)

1. Monter CD-filene med [WinCDEmu](https://wincdemu.sysprogs.org/) (eller pakk dem ut med [Universal Extractor](https://github.com/bioruebe/uniextract2)) og installer i denne rekkefølgen:
    * FGPGULL1.mdf (CD1 Hvit)
    * FGPGULL2.mdf (CD2 Svart)
    * FGPGULL1.mdf (CD1 Hvit) igjen.
2. Oppdater med `FGPGOLD_UPD12.exe` - Offisiell oppdatering fra [FlåklypaFix](https://sites.google.com/view/flaklypafix/) (sammen filen er i arkiv mappen)
3. Erstatt `FGP.exe` i `C:\Program Files (x86)\Flåklypa Grand Prix` med den moderne kompatibilitetsversjonen: [replacement executable](https://github.com/Hawkling/Flaklypa-Grand-Prix_2000-2002_Preservation-Project/releases). (sammen filen er i arkiv mappen)

> **Grunnleggende installasjon fullført. Du kan spille nå.** Lag gjerne en snarvei til skrivebordet. 
>
> Hvis spillet ikke starter, bruk Windows XP [kompatibilitetsmodus](https://imgur.com/pPUNzuL) på `.exe`-filen.

#### Anbefalt: Borderless fullscreen med dgVoodoo2

4. [Last ned dgVoodoo2](https://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/)
5. Kopier `dgVoodooCpl.exe`, `dgVoodoo.conf` og filer fra `MS\x86` (inkl. `DDraw.dll`) til spillmappen. (Sammen med FGP.exe)
6. Åpne `dgVoodooCpl.exe`:
    * **General:** Scaling mode: *Unspecified* (16:9) eller *Keep aspect ratio* (4:3).
    * **[DirectX](https://imgur.com/BzplWw1):** Velg ønsket oppløsning og slå av "dgVoodoo Watermark".
    * Høyreklikk, velg "Show all sections of the configuration"
    * **[GeneralExt](https://imgur.com/mnglcos):** ", aktiver *Borderless*, *Fullscreen size* og *Fake*.

Anbefalt oppsett er nå fullført.


### Mer info på bunn av siden.

---

## 🇬🇧 Project Overview

This project aims to preserve and improve access to an important part of Norwegian video game history through:

- Installation guide for modern versions of Windows.
- Archived official updates.
- Replacement FGP.exe for modern Windows compatibility.
- dgVoodoo2 configuration for widescreen and borderless fullscreen.
- Improving the [Wikipedia](https://no.wikipedia.org/wiki/Fl%C3%A5klypa_Grand_Prix_(PC-spill)) and [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Pinchcliffe_Grand_Prix) articles.
- Links to external preservation resources, including Archive.org.
- Links to my other projects focused on preserving and promoting Norwegian video games.

---

### Preserving Norwegian Video Game History and Digital Cultural Heritage

Many older Norwegian PC games are no longer sold and risk being lost, despite being 100% digital. They are an important part of Norway's digital gaming history.

Games that are no longer sold should be preserved in public archives by the National Library of Norway or similar public institutions, rather than relying on volunteers and Archive.org for long-term preservation.

If official re-releases or remasters become available on GOG or Steam, purchasing them is the best way to support the rights holders. Better availability of older versions may also generate renewed interest in newer releases, such as *[Pinchcliffe Grand Prix (2021)](https://store.steampowered.com/app/3352670)*. Interest in official re-releases can also be shown by voting on the [GOG Dreamlist](https://www.gog.com/dreamlist/game/pinchcliffe-grand-prix-2000).

Official re-releases, remasters, public and community archiving, including through Archive.org, all play an important role in preserving Norway's digital gaming history.

---

### Availability of the Game

The original games have never been released digitally and are no longer commercially available. For preservation purposes, community-archived copies are available through Archive.org.

* [Gold edition (2002)](https://archive.org/details/flaklypagullutgave) The guide is for this one.
* [The original (2000)](https://archive.org/details/flaklypagullutgave) A guide is included.
* [Other versions and new uploads](https://archive.org/search?query=Fl%C3%A5klypa+Grand+Prix)
* [Vote on GOG Dreamlist for a rerelease!](https://www.gog.com/dreamlist/game/pinchcliffe-grand-prix-2000)

### Installation Guide: Gold Edition (2002)

1. Mount the CD files with [WinCDEmu](https://wincdemu.sysprogs.org/) (or extract with [Universal Extractor](https://github.com/bioruebe/uniextract2)) and install in this order:
    * FGPGULL1.mdf (CD1 Hvit, white)
    * FGPGULL2.mdf (CD2 Svart, black)
    * FGPGULL1.mdf (CD1 Hvit, white) again.
2. Update with `FGPGOLD_UPD12.exe` - Official update from [FlåklypaFix](https://sites.google.com/view/flaklypafix/). (same file exists in the archived folder)
3. Replace `FGP.exe` in `C:\Program Files (x86)\Flåklypa Grand Prix` with the modern compatibility [replacement executable](https://github.com/Hawkling/Flaklypa-Grand-Prix_2000-2002_Preservation-Project/releases). (same file exists in the archived folder)

> **Basic installation complete. You can play now.** Create a desktop shortcut if desired. 
>
> If the game does not start, enable Windows XP [compatibility mode](https://imgur.com/pPUNzuL) on the executable.

#### Recommended: Borderless Fullscreen with dgVoodoo2

4. [Download dgVoodoo2](https://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/).
5. Copy `dgVoodooCpl.exe`, `dgVoodoo.conf`, and files from the `MS\x86` folder (including `DDraw.dll`) to the game folder. (With FGP.exe)
6. Open `dgVoodooCpl.exe`:
    * **General:** Scaling mode: *Unspecified* (for 16:9) or *Keep aspect ratio* (for 4:3).
    * **[DirectX](https://imgur.com/BzplWw1):** Select your desired resolution and turn off "dgVoodoo Watermark."
    *  Right-click and select "Show all sections of the configuration."
    * **[GeneralExt](https://imgur.com/mnglcos):**" Enable *Borderless*, *Fullscreen size*, and *Fake*.

Recommended setup is now complete.

---

## Troubleshooting & Known Issues

* **[PCGamingWiki](https://www.pcgamingwiki.com/wiki/Pinchcliffe_Grand_Prix)** (for other issues see the glossary pages for potential workarounds. Also includes: shortcuts, [minigame location guide]([url](https://imgur.com/gallery/Y44AtiM)), savegame location, cheats)
* **Alt-Tabbing:** Without dgVoodoo2 the game runs in exclusive fullscreen mode, which can cause numerous issues. These include monitor layouts changing, incorrect colors after returning to the game, and other display problems.
* **Multiple Monitors:** Use dgVoodoo2 to force the game into a borderless windowed mode.
* **Steam Overlay/Controllers:** If you add the game as a non-steam game to use controller configurations, the Windows XP compatibility setting causes the `.exe` to run as administrator. This requires **Steam to also run as administrator** for the overlay and controller input to be detected.

---

## Missing releases wanted for archival preservation

* English (Pinchcliffe Grand Prix)
* Danish (Bjergkøbing Grand Prix)
* Swedish

---

## External resources

* [PCGamingWiki Page](https://www.pcgamingwiki.com/wiki/Pinchcliffe_Grand_Prix)
* [FlåklypaFix](https://sites.google.com/view/flaklypafix/): Primary source for official updates. [Archive alternative](https://web.archive.org/web/20260000000000*/http://www.caprino.no/pages/oppdateringer.html)
* [Norwegian Wikipedia (PC Game)](https://no.wikipedia.org/wiki/Fl%C3%A5klypa_Grand_Prix_(PC-spill))
* [English Wikipedia (Franchise)](https://en.wikipedia.org/wiki/The_Pinchcliffe_Grand_Prix)
* [Guide for minigame locations](https://imgur.com/gallery/Hi9UwkT)
* [Archived Caprino.no](https://web.archive.org/web/*/http://www.caprino.no/pages/*)
* [Norwegian Dub Wiki](https://norske-dubber.fandom.com/no/wiki/Fl%C3%A5klypa_Grand_Prix_(Spill))

### Norwegian Game Preservation and industry exposure Projects

* [List of PC games with Norwegian support](https://www.reddit.com/r/norge/comments/1tctxoi/) (Project/Report form: [Link](https://docs.google.com/forms/d/e/1FAIpQLSf8JcEtqf-u4Zv1LU3e7uycHVuK311ZcRte9n_gU3zFocXjMg/viewform))
* [List of PC games with Norwegian support (English)](https://www.reddit.com/r/Norway/comments/1tcpetk/huge_list_of_video_games_available_in_norwegian/)
* [List of Norwegian-developed games](https://www.reddit.com/r/Norway/comments/1tbbiv4/saw_the_games_of_norway_event_decided_to_look_for/) (Including non-Norwegian language titles)
* [Steam Search Filters Proposal](https://steamcommunity.com/discussions/forum/10/567037313987872927/) ("No Language Required" initiative)

---

## Credits and Contributions

Special thanks to mullemekk on Archive.org for preserving the currently available archival copy.

Thanks to everyone who has contributed information, research, compatibility fixes, and preservation efforts for Norwegian PC games.

Corrections, compatibility reports, and anything else you can think of are welcome.

## License

* **Documentation & Preservation:** Released under **[The Unlicense](https://unlicense.org/)**.
* **Third-party software and tools:** Remain subject to their respective licenses.
* **Replacement or modified executables:** Provided solely for interoperability and preservation purposes and are not affiliated with the original rights holders.
