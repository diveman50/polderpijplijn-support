# Changelog — Grim Reader

All notable changes per release. Newest first.
Versions match the `vX.Y` tags and `CFBundleShortVersionString`.

## 1.85 — 2026-06-26

- **Downloaden van eigen OPDS-catalogi werkt nu:** boeken van een zelf-gehoste OPDS-bron
  (bijvoorbeeld Calibre-Web) die over http draait, gaven een beveiligingsfout. De app
  staat nu verbindingen met je eigen opgegeven servers toe, net als bij je NAS.
- **OPDS-catalogi bij je servers:** je eigen OPDS-bronnen voeg je nu toe onder Instellingen
  → Servers, samen met je Grimmory- en WebDAV-servers, via één "Server toevoegen"-knop.
- **"Ontdek" heet nu "Internet boeken":** duidelijker waar je gratis boeken van het
  internet vindt.

## 1.84 — 2026-06-26

- **Je blijft langer ingelogd op je Grimmory-server:** een tijdelijke serverhapering
  (bijvoorbeeld als de NAS net even herstart) meldt je niet meer onnodig af. Pas als je
  aanmelding echt is verlopen, kom je terug op het inlogscherm.
- **Vertalen (proef) werkt nu echt:** koos je een taal die je nog niet had, dan bleef het
  bij een tollend wieltje. iOS vraagt nu netjes om het taalpakket te downloaden, en de
  brontaal wordt uit de boekgegevens gehaald (of anders automatisch herkend).

## 1.83 — 2026-06-26

- **Eigen OPDS-catalogi:** voeg in Instellingen je eigen OPDS-bron toe (bijvoorbeeld een
  Calibre-Web-server of een andere OPDS-feed). Die verschijnen onder Ontdek naast de
  ingebouwde bronnen, met bladeren, zoeken en downloaden.
- **VoiceOver houdt je leespositie beter vast:** schakel je VoiceOver in tijdens het lezen,
  dan blijft de lezer nu staan waar je was in plaats van naar het begin van het hoofdstuk te
  springen.
- **Vertalen (proef):** op iOS 18 en nieuwer kun je een hoofdstuk on-device laten vertalen
  via een nieuwe knop in de leesbalk. Dit is een eerste experiment — de tekst wordt zonder
  opmaak getoond.

## 1.82 — 2026-06-26

- **Swipen om te bladeren:** veeg in de EPUB-lezer naar links voor de volgende pagina en
  naar rechts voor de vorige — naast het bestaande tikken links/rechts. De veegbeweging
  werkte voorheen niet doordat de tekstweergave hem opslokte; dat is nu verholpen.

## 1.81 — 2026-06-25

- **VoiceOver houdt je leespositie vast:** zet je VoiceOver aan (of weer uit) terwijl je
  een EPUB leest, dan blijft de lezer nu staan waar je was, in plaats van terug te springen
  naar het begin van het hoofdstuk. De positie wordt bij het wisselen tussen kolom- en
  doorlopende voorleesweergave bewaard.

## 1.80 — 2026-06-25

- **Uitloggen houdt je in de app:** log je uit van je Grimmory-server, dan kom je nu
  netjes terug in het hoofdmenu (met Mijn boeken, Ontdek en je WebDAV-servers) in plaats
  van vast te lopen op het accountscherm. En na een herstart word je niet meer naar het
  Grimmory-inlogscherm gedwongen zodra je de app eenmaal hebt gebruikt — opnieuw inloggen
  kan altijd via Instellingen.

## 1.79 — 2026-06-25

- **De app werkt nu ook zonder Grimmory-server:** wil je alleen boeken van een
  WebDAV-server (NAS, Nextcloud e.d.) lezen, dan kun je vanaf het inlogscherm meteen
  een WebDAV-server toevoegen zonder eerst op een Grimmory-server in te loggen. De
  Grimmory-specifieke onderdelen (Start, Series, Schrijvers, Bibliotheken, Zoeken,
  Onderhoud …) blijven dan netjes verborgen; je ziet enkel je servers, Mijn boeken en
  Ontdek. Log je later alsnog in op een Grimmory-server, dan verschijnt alles vanzelf.
- **Onderhoud opgeruimd in Instellingen:** de beheerdersfuncties voor je Grimmory-
  bibliotheek (duplicaten, samenvoegen, metadata aanvullen …) staan nu samen onder één
  "Onderhoud"-knop in plaats van los onder elkaar.
- **Geen storende balk meer:** de rode "geen verbinding"-strook onderaan is verdwenen;
  schermen die niet kunnen laden tonen zelf al een melding.

## 1.78 — 2026-06-25

- **Boeken van een WebDAV-server bewerken:** open je een boek van een WebDAV-server,
  dan kun je nu via het potlood titel, auteur, taal en omschrijving aanpassen — net
  als bij je eigen boeken in "Mijn boeken". Je kunt ook de cover vervangen via een
  online zoekopdracht, een foto of een bestand. De wijzigingen worden bewaard in de
  `books.yaml` op de server zelf, zodat ze op al je toestellen verschijnen; heb je het
  boek gedownload, dan worden de gegevens daar meteen mee bijgewerkt.
- **Rustiger overzicht:** het mapicoon ("Bladeren per map") is uit het serverboeken-
  raster gehaald; het scherm toont nu enkel je boeken.

## 1.77 — 2026-06-25

- **Voortgang tijdens het scannen van een WebDAV-server:** loopt de app map voor
  map door de server, dan zie je nu live "X mappen doorzocht · Y boeken" onder de
  spinner, en een balkje bovenaan als je een al gevulde lijst vernieuwt — zodat je
  ziet dat hij nog bezig is in plaats van enkel een tollend wieltje.
- **Bibliotheek laadt direct op een tweede toestel:** na een scan bewaart de app de
  hele boekenstructuur als `books.yaml` op de server zelf (naast `authors.yaml`).
  Open je dezelfde server op een ander toestel, dan verschijnt de bibliotheek meteen
  uit die index in plaats van opnieuw de hele mappenboom te scannen; covers vullen
  daarna vanzelf aan. Op een alleen-lezen share blijft het bij de gewone scan.

## 1.76 — 2026-06-25

- **Schrijversinfo bij WebDAV-boeken:** open je een boek van een WebDAV-server, dan
  zoekt de app de schrijver op (Wikipedia) en toont een portret met een korte bio.
  Die gegevens worden bewaard in een eigen `authors.yaml` op de server zelf, zodat ze
  bij je bibliotheek horen en op al je toestellen beschikbaar zijn — en offline in een
  lokale cache. Op een alleen-lezen share blijft het bij de lokale cache.
- **Overal hetzelfde openen:** tik nu op de cover van een boek om het te openen — bij
  je eigen boeken en WebDAV-boeken net zoals bij de Grimmory-bibliotheek.
- **Sneller scannen van grote WebDAV-bibliotheken:** de app probeert de hele mappenboom
  in één keer op te halen. Staat je server dat niet toe, dan valt hij automatisch terug
  op de vertrouwde map-voor-map-scan.

## 1.75 — 2026-06-25

- **Alle boeken van een server in één overzicht:** elke WebDAV-server toont nu een
  raster met álle boeken uit de hele mappenboom, mét cover en titel/auteur. De lijst
  wordt op je toestel onthouden zodat hij niet elke keer opnieuw hoeft te scannen;
  met "Vernieuwen" zoek je opnieuw, en "Bladeren per map" blijft beschikbaar.
- **Eén plek voor al je servers:** in Instellingen staan je Grimmory-bibliotheek en
  WebDAV-servers nu samen onder "Servers". Naast elke server zie je of hij bereikbaar
  is; bij een WebDAV-server geeft een potlood aan dat de app er een eigen mapje voor
  metadata mag bijhouden. Toevoegen gaat via één knop met de keuze Grimmory of WebDAV.

## 1.74 — 2026-06-25

- **Lees boeken van een WebDAV-server:** voeg in Instellingen één of meer WebDAV-
  servers toe (NAS, Nextcloud e.d.) met gebruikersnaam en wachtwoord, blader door de
  mappen en download EPUB- en PDF-boeken. Het wachtwoord staat veilig in de Keychain,
  en met "Verbinding testen" controleer je de server meteen.
- **Covers uit de bestanden zelf:** voor WebDAV-downloads haalt de app de cover uit
  het EPUB of toont de eerste PDF-pagina. De boeken verschijnen bij "Mijn boeken" en
  blijven offline beschikbaar, net als catalogus-downloads.

## 1.73 — 2026-06-25

- **De tekst springt niet meer als je het paneel opent:** tik je tijdens het lezen
  onderaan om de bediening te tonen, dan blijft de pagina nu staan. Eerder schoof de
  statusbalk mee waardoor het boek opnieuw werd ingedeeld en de tekst versprong.
- **Gewijzigde schrijversfoto verandert direct overal:** pas je een auteur aan
  (foto, naam of een online match), dan ververst de portretfoto meteen op elk scherm,
  ook in de lijst "Schrijvers" — net zoals boekkaften dat al deden. Voorheen zag je
  de nieuwe foto pas na het herstarten van de app.

## 1.72 — 2026-06-25

- **You're back where you stopped reading:** when you leave a book and come back,
  it now reliably reopens on the exact page you left off. Before, it could land a
  page or two earlier — for PDFs the very last page turn wasn't always saved before
  closing, and for EPUBs the restored page could get nudged back while the page was
  still re-laying out.
- **Tap the cover to open a book:** on a book's page you can now tap the cover image
  itself to start reading (or listening, or to download it first) — the same as the
  button below it.

## 1.71 — 2026-06-24

- **A new cover stays put when you go back:** after you change the cover of a book
  from your Grimmory server, the new image now shows immediately on every screen,
  including the library grid one step back. Previously the cover could briefly go
  blank there and only fill in later, because the app re-fetched it from the server
  before the server had finished saving it. It now reuses the image you just picked.

## 1.70 — 2026-06-24

- **A search bar on every book screen:** every screen with books now has a search
  bar pinned at the top that searches within that screen — All books, each
  library, shelf and smart shelf, a series, an author's books, and My books.
- **Search everything from the home screen:** a search field right under the
  Grim Reader logo searches your whole library.
- **Search bar pinned on the Authors screen** so it's always in reach.
- **Faster edit screen:** opening the edit screen from a book's details no longer
  stalls while it re-formats the description.
- **Covers no longer disappear after you change them:** the new cover is uploaded
  directly instead of asking the server to fetch it, which could fail and wipe the
  existing cover. Missing covers in a library grid also retry instead of staying
  blank.

## 1.69 — 2026-06-24

- **Covers from your Grimmory server refresh straight away:** after you replace
  the cover of a server book, the library updates immediately instead of only
  after restarting the app.
- **More cover choices when searching:** the online cover search now also looks
  on Apple Books, alongside Open Library and Google Books — handy for modern
  titles the others don't have.

## 1.68 — 2026-06-24

- **Author and series pages now show their books:** when an author or series had
  stray spaces in its stored name, the page showed a book count but no books.
  It now falls back to searching, so the books appear just like they do when you
  search for them.
- **Covers refresh straight away:** after you edit a book and change its cover,
  "My books" now updates immediately instead of only after restarting the app.

## 1.67 — 2026-06-24

- **Pick the language from a list:** when editing a book you now choose the
  language from a searchable list of languages instead of typing free text, so
  it's always stored consistently.
- **Edit Grimmory books too:** administrators can now edit the title, author,
  language and description of books from your Grimmory server — including the
  online "search the whole book" auto-fill and online cover search — just like
  for your own local books.
- **Read-aloud now scrolls and highlights:** starting read-aloud switches the
  reader to scroll mode and highlights the sentence being spoken; the highlight
  is now visible in every theme.

## 1.66 — 2026-06-24

- **Edit metadata for your own books:** for books that don't come from your
  Grimmory server you can now edit the title, author, language and description
  from a pencil button on the book screen.
- **Auto-fill book details online:** search Open Library and Google Books for the
  whole book and fill in the title, author, language, description and cover in one
  go — you can still tweak everything by hand afterwards.
- **Change the cover three ways:** an online cover search, a photo from your
  library, or an image file.

## 1.65 — 2026-06-24

- **"Open with …" for EPUB/PDF:** open an EPUB or PDF file from Files or the
  share sheet straight into Grim Reader. The file is saved to your local
  library and opened right away — even when you're not signed in to the server.
- **"Downloaded" becomes "My books":** server downloads and locally added or
  catalogue-downloaded books now sit together in a single grid. Books from your
  own Grimmory server carry a NAS badge on the cover.
- The Discover tab now shows only the catalogues; the downloads section moved
  to "My books".

## 1.64 — 2026-06-23

- **New Discover tab with DRM-free catalogues (Project Gutenberg):** browse
  over 70,000 free public-domain books, download them and read them offline in
  the app. Works independently of your Grimmory server.

## 1.62 — 2026-06-23

- The iPad sidebar no longer jumps back to Favourites: the selected shelf or
  library now stays put.
- The connection check no longer refreshes the view unnecessarily.

## 1.61 — 2026-06-23

- Improvements to the offline demo.

## 1.60 — 2026-06-23

- Renamed the demo button to "Offline demo".
- Polished, code-drawn covers for the demo books.
