# Flåklypa Grand Prix (2000-2002) Preservation Project
Flåklypa Grand Prix Gullutgave (2002) Windows 11 installasjons guide.

Spillet i både original versjon (2000) og Gullutgaven (2002) kan [lastes ned med arkiv lenkene nedenfor!](#-tilgang-til-spillet)

---

Digital preservation and compatibility project for the original PC releases of *Flåklypa Grand Prix* (2000-2002). (English: *Pinchcliffe Grand Prix*).

These games have not been commercially available for many years.

---

## Legal Notice
*Flåklypa Grand Prix / Pinchcliffe Grand Prix* and related intellectual property remain the property of their respective rights holders.

This is an unofficial preservation project and is not affiliated with, endorsed by, or sponsored by any rights holder.

Users are responsible for ensuring they have the legal right to use any software referenced by this project.

The repository does **not include the original game, installation media, or copyrighted game assets.** Links to third-party sources are provided for preservation purposes only. Availability and legality of third-party sources may vary by jurisdiction.

---

### Tilgang til spillet
De originale spillene har aldri blitt utgitt digitalt og er ikke lenger kommersielt tilgjengelige. For å bevare vår kulturarv finnes det fellesskapsarkiverte kopier på Archive.org.

* [Gullutgave (2002)](https://archive.org/details/flaklypagullutgave) Guiden er for denne.
* [Originalen (2000)](https://archive.org/details/flaklypa-grand-prix-cracket) Guide følger med.
* [Andre akriverte versjoner og nye opplastinger](https://archive.org/search?query=Fl%C3%A5klypa+Grand+Prix&and%5B%5D=mediatype%3A%22software%22)
* [Stem på GOG Dreamlist for nyutgivelse!](https://www.gog.com/dreamlist/game/pinchcliffe-grand-prix-2000)
* Uten Windows: [Linux guide av tjerandb](https://github.com/tjerandb/Flaklypa_Grand_Prix_2000-2002_Preservation_Project/blob/main/linux.md) - [Linux gjennom Lutris](https://lutris.net/games/pinchcliffe-grand-prix/) - [Mac guide](https://hals.app/blog/fgp-modern/)

### Installasjonsguide: Gullutgave (2002)
1. Monter CD-filene med [WinCDEmu](https://wincdemu.sysprogs.org/) (eller pakk dem ut med [Universal Extractor](https://github.com/bioruebe/uniextract2)) og installer i denne rekkefølgen:
    * FGPGULL1.mdf (CD1 Hvit)
    * FGPGULL2.mdf (CD2 Svart)
    * FGPGULL1.mdf (CD1 Hvit) igjen.
2. Oppdater med `FGPGOLD_UPD12.exe` - Andre oppdateringer akrivert på [FlåklypaFix](https://sites.google.com/view/flaklypafix/)
3. Erstatt `FGP.exe` i `C:\Program Files (x86)\Flåklypa Grand Prix` med den moderne kompatibilitetsversjonen: [replacement executable](https://github.com/Hawkling/Flaklypa-Grand-Prix_2000-2002_Preservation-Project/releases). (samme filen er i arkiv mappen)

> **Grunnleggende installasjon fullført. Du kan spille nå.** Lag gjerne en snarvei til skrivebordet. 
>
> Hvis spillet ikke starter, bruk Windows XP [kompatibilitetsmodus](https://imgur.com/pPUNzuL) på `.exe`-filen.

#### Anbefalt: Borderless fullscreen med dgVoodoo2
4. [Last ned dgVoodoo2](https://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/)
5. Kopier `dgVoodooCpl.exe`, `dgVoodoo.conf` og filer fra `MS\x86` (inkl. `DDraw.dll`) til spillmappen. (Sammen med FGP.exe)
6. Åpne `dgVoodooCpl.exe`:
    * **General:** Scaling mode: *Unspecified* (16:9) eller *Keep aspect ratio* (4:3). (bilde strekkes i 16:9)
    * **[DirectX](https://imgur.com/BzplWw1):** Velg ønsket oppløsning og slå av "dgVoodoo Watermark".
    * [Høyreklikk, velg "Show all sections of the configuration"](https://imgur.com/mnglcos)
    * **[GeneralExt](https://imgur.com/a/74R3CFy):** ", aktiver *Borderless*, *Fullscreen size* og *Fake*.

Anbefalt oppsett er nå fullført. **Kos deg :)**

---

## Bevaring av norsk spillhistorie og digital kulturarv
Mange eldre norske PC-spill blir ikke lenger solgt og risikerer å gå tapt, til tross for at de er 100 % digitale. De er en viktig del av Norges digitale spillhistorie.

Spill som ikke lenger selges bør bevares og bli offentlig arkivert av Nasjonalbiblioteket eller lignende offentlige institusjoner, fremfor å være avhengige av frivillige og Archive.org for langsiktig bevaring.

Hvis offisielle nyutgivelser eller remastere blir tilgjengelige på GOG eller Steam, er den beste måten å støtte rettighetshaverne på å kjøpe disse. Bedre tilgjengelighet av eldre versjoner kan også skape økt interesse for nyere utgivelser, som *[Flåklypa Grand Prix (2021)](https://store.steampowered.com/app/3352670)*. Interesse for offisielle nyutgivelser kan også vises ved å stemme på [GOG Dreamlist](https://www.gog.com/dreamlist/game/pinchcliffe-grand-prix-2000).

Offisielle nyutgivelser, remastere, offentlig og frivillig arkivering, blant annet gjennom Archive.org, spiller alle en viktig rolle i bevaringen av Norges digitale spillhistorie.

---

## Troubleshooting
* **Alt-Tabbing:** Uten dgVoodoo2 kjører spillet som eksklusiv "Fullscreen mode" som kan gi flere problemer på moderne windows. Inkludert: svart skjerm i flere sekunder når spillet åpnes og lukkes, endringer i skjermoppsettet, feil farger når man tabber tilbake til spillet, og mer.
* **Flere skjermer:** Bruk dgVoodoo2 for og tvinge spillet inn i "borderless windowed mode".
* **Steam Overlay/Controllers:** vis du legger til spillet som et "non-steam game" for å kunne bruke kontrollerkonfigurasjoner, vil kompatibilitetsinnstillingen for Windows XP føre til at `.exe`-filen kjøres som administrator. Dette krever at **også Steam kjøres som administrator** for at Overlay og kontroller skal registreres.
* **[PCGamingWiki](https://www.pcgamingwiki.com/wiki/Pinchcliffe_Grand_Prix)** - For andre problemer skjekk "glossary pages".

---

## Håper og få arkivert
* English (Pinchcliffe Grand Prix)
* Danish (Bjergkøbing Grand Prix)
* Swedish

---

## Eksterne lenker
* [Wikipedia](https://no.wikipedia.org/wiki/Fl%C3%A5klypa_Grand_Prix_(PC-spill)) - [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Pinchcliffe_Grand_Prix) (shortcuts, savegame location, cheats.) Oppdatert av meg :)
* [FlåklypaFix](https://sites.google.com/view/flaklypafix/): Kilde for offisielle oppdateringer - [Caprino.no arkiv alternativ](https://web.archive.org/web/20260000000000*/http://www.caprino.no/pages/oppdateringer.html)
* [Guide for å finne minigames](https://imgur.com/gallery/Hi9UwkT)
* [Arkivert Caprino.no](https://web.archive.org/web/*/http://www.caprino.no/pages/*)
* [Norsk Dub Wiki](https://norske-dubber.fandom.com/no/wiki/Fl%C3%A5klypa_Grand_Prix_(Spill))

### Andre prosjekter
* [Liste over PC Spill med norsk tale og skrift](https://www.reddit.com/r/norge/comments/1tctxoi/) (Project/Report form: [Link](https://docs.google.com/forms/d/e/1FAIpQLSf8JcEtqf-u4Zv1LU3e7uycHVuK311ZcRte9n_gU3zFocXjMg/viewform))
* [List of PC games with Norwegian support (English)](https://www.reddit.com/r/Norway/comments/1tcpetk/huge_list_of_video_games_available_in_norwegian/)
* [List of Norwegian-developed games](https://www.reddit.com/r/Norway/comments/1tbbiv4/saw_the_games_of_norway_event_decided_to_look_for/) (Including non-Norwegian language titles)
* [Steam Search Filters Proposal](https://steamcommunity.com/discussions/forum/10/571552997743547079/) ("No Language Required" initiative)



---

## Credits and Contributions
Takk Til mullemekk på Archive.org for den nåværende opplastingen av gullutgaven.

Takk til alle som hjelper å arkivere norske spill, eller oppdaterer guider og info på nett! 

## License
* **Documentation & Preservation:** Released under **[The Unlicense](https://unlicense.org/)**.
* **Third-party software and tools:** Remain subject to their respective licenses.
* **Replacement or modified executables:** Provided solely for interoperability and preservation purposes and are not affiliated with the original rights holders.
