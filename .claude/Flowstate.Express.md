# Flowstate Express Made In Germany
## Inhaltsverzeichnis
Gehe zu
- [Flowstate Express Made In Germany](#flowstate-express-made-in-germany)
  - [Inhaltsverzeichnis](#inhaltsverzeichnis)
- [Brand-Vision](#brand-vision)
  - [Werteprinzipien](#werteprinzipien)
  - [Werteleitlinie](#werteleitlinie)
  - [Raum](#raum)
  - [Konzept](#konzept)
  - [Grund](#grund)
  - [Fonts](#fonts)
  - [Colours](#colours)
- [Tech Infrastructure](#tech-infrastructure)
  - [Deployment, Data](#deployment-data)
  - [Software Tools](#software-tools)
- [Pages](#pages)
  - [Header](#header)
  - [Footer](#footer)
    - [\[MVP\] Impressum](#mvp-impressum)
  - [React Tabs](#react-tabs)
  - [Landingpage-Specs](#landingpage-specs)
  - [Experience-Specs](#experience-specs)
    - [Online-Event-Module-Specs](#online-event-module-specs)
    - [Personal-Event-Module-Specs \[SCOPE\]](#personal-event-module-specs-scope)
    - [Event-Component](#event-component)
      - [Kunstobjekte-Referenzen:](#kunstobjekte-referenzen)
  - [Observe-Specs](#observe-specs)
    - [Observe-Settings](#observe-settings)
    - [Observe-Rules](#observe-rules)
  - [Profile-Specs](#profile-specs)
  - [Profile-Specs-Login](#profile-specs-login)
    - [Profile-Login-Art-Instances](#profile-login-art-instances)
    - [Profile-Login-Art-Instances-Sample-Explanation](#profile-login-art-instances-sample-explanation)
    - [Art-Instances-Datenlogik](#art-instances-datenlogik)
    - [Profile-Login-Art-Instances-Explanation](#profile-login-art-instances-explanation)
    - [Profile-Subscriptions](#profile-subscriptions)
    - [Profile-Events](#profile-events)
    - [Profile-Collection-Export](#profile-collection-export)
    - [Profile-Settings](#profile-settings)
- [Workflows \[SCOPE\]](#workflows-scope)
  - [Artist-Upload-Manual](#artist-upload-manual)
  - [Artist-Upload-Workflow-Agent](#artist-upload-workflow-agent)
  - [Eventbuchungen](#eventbuchungen)
- [Plattform-Subscription-Specs \[SCOPE\]](#plattform-subscription-specs-scope)
- [Texts](#texts)
  - [Landingpage-Texts](#landingpage-texts)
    - [Hero-Text](#hero-text)
    - [Vision-Section](#vision-section)
    - [Zahlen, Daten, Fakten](#zahlen-daten-fakten)
      - [Der digitale Mangel](#der-digitale-mangel)
      - [Die Folgen](#die-folgen)
      - [Der Gegenentwurf: Ausdruck heilt](#der-gegenentwurf-ausdruck-heilt)
  - [Experience-Texts](#experience-texts)
    - [Hero-Text](#hero-text-1)
    - [Online-Event-Module-Text](#online-event-module-text)
    - [Personal-Event-Module-Text](#personal-event-module-text)
    - [Community-Chat-Text](#community-chat-text)
  - [Observe-Texts](#observe-texts)
    - [Hero-Text](#hero-text-2)
- [Allgemein](#allgemein)


# Brand-Vision

## Werteprinzipien
1. Verbindung
2. Sinnlichkeit
3. Faszination

## Werteleitlinie
1. Vom Konsum ins Erschaffen
2. Basiert auf Empowerment
3. Erfahren von Zeitlosigkeit

## Raum
- Erwartungslos
- Verletzlich
- Echt
- Fühlend

## Konzept
- Vom Kopf ins Herz

## Grund
Derzeit digitaler Überfluss
  - Ziel ist es Bewusst Dinge zu erfahren, weshalb Werke nur einmal betrachtet werden können
  
## Fonts
Headline - Fraunces
Body - DM Sans
Accent - Caveat

## Colours
Gradient:
- 4DD2F6
- FF7A2E
- FB343B

Background: FAF1E6
Dark Mode: 1C1130
Empty Space: FFFFFF
Text: 111827
Secondary Labels: 6B7280



# Tech Infrastructure
- [MVP] NextJs
- [MVP] Tailwind
- [MVP] CSV Datenstruktur (nachher mit Supabase ersetzt)
- [SCOPE] i18n
## Deployment, Data
- [MVP] Hosting auf VPS, Docker, Caddy 
- [SCOPE] Supabase (PosgreSQL)
- [SCOPE] Hetzner Object Storage (für Binärdaten)
- [SCOPE] Nextcloud als WebDAV
## Software Tools
- [MVP]Zoom (wöchentlich wiederkehrend) 
- [SCOPE] cal.com 



# Pages
- [MVP] Jede Section innerhalb der Tabs wird Modular erstellt,...
- [SCOPE] sodass man Sections nicht nur Coding technisch verschieben kann, sondern der User, Künstler, sein eigenes Interface erstellen kann und interessenbasiert in Profileinstellungen einrichten kann 
- Ziel: User Ermächtigung

## Header
- [MVP] Flowstate Express Logo - 
- [MVP] Login (vorausgefüllt)
- [SCOPE] i18n lanuage service
## Footer 
- [MVP] Logo
- [MVP] Datenschutz (siehe Datenschutz.tsx und füge Zoom.us als Service hinzu)
### [MVP] Impressum
  - Angaben gemäß § 5 TMG
Nils Tenkotte
Gertrudisstraße 7
50859 Köln

Kontakt:
E-Mail: nils@flowstate.foundation

Steuer:
Kleinunternehmer gemäß § 19 UStG

Steuernummer: 223/5296/5078

Verantwortlich für den Inhalt nach § 55 Abs. 2 RStV:
Nils Tenkotte
Gertrudisstraße 7, 50859 Köln

Streitschlichtung
Die Europäische Kommission stellt eine Plattform zur Online-Streitbeilegung (OS) bereit: https://ec.europa.eu/consumers/odr/
Wir sind nicht bereit oder verpflichtet, an Streitbeilegungsverfahren vor einer Verbraucherschlichtungsstelle teilzunehmen.

Haftung für Inhalte
Als Diensteanbieter sind wir gemäß § 7 Abs.1 TMG für eigene Inhalte auf diesen Seiten nach den allgemeinen Gesetzen verantwortlich.

## React Tabs
- [MVP] Landingpage (Home Icon) 
  GoTo: [Texts](#landingpage-specs)
  GoTo: [Texts](#landingpage-texts)
- [MVP] Experience (Community Icon) 
  GoTo: [Texts](#experience-specs)
  GoTo: [Texts](#experience-texts)
- [MVP] Observe (Eye Icon) 
  GoTo: [Texts](#observe-specs)
  GoTo: [Texts](#observe-texts)
- [MVP] Profile (Profile Icon) 
  GoTo: [Specs](#profile-specs) - GoTo: [Specs Login](#profile-specs-login)
  Hinweis: Keine eigene "Profile-Texts"-Sektion — Texte werden vom Künstler selbst im Profil gepflegt (siehe Profile-Specs: "Was ist meine Essenz?")

## Landingpage-Specs
1. Hero (ein Bild) - clickable und vergrößerbar (da man sonst Gedichte nicht lesen konnte) ([MVP] Statisch)
1.1 Buttons: zum Profil des Künstlers der Woche ([MVP] zum einzig existierenden Profil derzeit)
GoTo: [Profile](#profile-specs)
1.2 Button: Experience 
GoTo: [Experience](#experience-specs)

2. Sections + Erklärung:
2.1 Core Vision
2.2 Page Experience
2.3 Page Observe
2.4 Page Profile
2.5 Zahlen Daten Fakten [ZDF-Text](#zahlen-daten-fakten)
2.6 Verweis auf Flowstate Foundation





## Experience-Specs
1. [MVP] Eventauflistung (Filter: Online, Persönlich)
### Online-Event-Module-Specs
  Zoom: 20 min Selbstausdruck, 10 min Sharing

  Zoom Events sind über folgenden Google Kalender-Freigabelink angelegt: https://calendar.google.com/calendar/u/0?cid=Y185MmEwYmFiYmViOTc0NTMzZWNkMDhjNDAyYTY5NGJmNmEwNjk2NzMzY2NjZDZhYjc2N2FlNGI4MzVjZmJjZTgwQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20

  [MVP] Zoomevents auf der Website in eigener Komponente
  [SCOPE] Eventkomponente mit folgenden Filtern (Online und Persönlich zwei Tabellen)
   1. Online
   2. Persönlich
   3. Kunst Arten, Tags

### Personal-Event-Module-Specs [SCOPE]
1. Eventpartner (Kategorisch): Events über Plattform buchbar [Workflow](#eventbuchungen)
2. Eigene Events

2. [MVP] Community Chat mit Austausch
   1. Gedichte
   2. Zeichnen
   3. Philosophie
   4. Skulpturen
  - [SCOPE] Reihenfolge der Community Chats im Künstlerprofil frei bestimmbar (bei login) 
  - [SCOPE] Auch die Reihenfolge von Events und Chat kann im Künsterprofil angepasst werden (Makrotechnisch und Mikrotechnisch (Chats))

3. [SCOPE] Kooperations Ateliers und Eventanbieter Partner können Events anlegen (Suchfunktion & Filter wie Zeit und Ort, durch Eventtags und Kategorie, zB ich möchte Töpfern) 
  
### Event-Component
[MVP] Komponente mit:
- Meetingname | Eventname
- Zeit
- Ort (wenn persönlich)
- Datum
- Online oder Persönlich
  - Wenn Online Zoom Icon
  - Wenn persönlich Personen Icon
- Teilnehmerzahl
- Meetingkategorie (erstmal leer)
- Meetinglink zum einwählen
- Binärarray an Kunstobjekten [Erklärung](#Kunstobjekte-Referenzen)
- Meetingpartner
- Mitwirkende Künstler
- Follower, die dort auch sind (sichtbare)
- erweiterbar...

#### Kunstobjekte-Referenzen: 
- Werke, Serien oder Collections, die auf diesem Event ausgestellt wurden
  - [SCOPE] Markierbar als "Exklusiver Release dieses Events"
- [SCOPE] Event-Atmosphäre-Fotos (z.B. Scale des Events, Menschen vor Ort)
  - Ausnahme vom allgemeinen Prinzip "kein Fokus auf Gesichter/Personen" — bei Events explizit erlaubt, da es hier um das gemeinschaftliche Erleben geht, nicht um Einzelpersonen-Content

## Observe-Specs
- Hier werden Bilder gefolgter Künstler gepostet
- Alle Bilder sind nur einmal sichtbar (kommentierbar, wenn erlaubt)
- Künstler Kategorie und Tags sichtbar 
	- Profil und Kategorie (führt zur Community) wählbar

- [MVP] Vier Beispielwerke im Feed
  - draw-04.webp
  - poem-03.webp
  - sculpture-01.webp
  - draw-03.webp
Profil des Künstlers wählbar GoTo: [Profil](#profile-specs)

### Observe-Settings
- [SCOPE] Über eigenes Profil einstellbar Wie viele Künstler pro 100 Beiträge neu | unbekannt sind und ob überhaupt neue angezeigt werden sollen. 
- [SCOPE] Letztes Event oder zukünftiges Event auf dem der Künstler ist wird angezeigt und ist wählbar (Einstellbar im eigenen Künstlerprofil)

### Observe-Rules
- Alle Bilder sind nur einmal sichtbar
- [MVP] Werke sind nicht öffentlich kommentierbar
  - Grund: Eine öffentliche Kommentarbox senkt die Hemmschwelle für Hass-Kommentare. Interaktion mit dem Künstler soll stattdessen direkt erfolgen (nicht anonym-öffentlich)

## Profile-Specs
Profil des Künstlers (als User ohne Login) 
- [MVP] Titel: Was ist meine Essenz? 
- [MVP] Beschreibung: Was prägt(e) meinen Ausdruck? 
- [MVP] Ein Ausstellungswerk jeder Kategorie nach Wahl des Künstlers
  - draw-01.webp, philosophie-01.webp, poem-05.webp, sculpture-01.webp
- [MVP] Rampenlicht: Derzeitiger Stand eines aktuellen Projektes nach Wahl des Künstlers (in Prozent)
  - draw-02-02 (true false, ob vorher (erstes Bild) nachher hinzugefügt werden soll)
- [SCOPE] 5 Collaboriations mit anderen Künstlern nach Wahl
- [SCOPE] Eine Serie oder Collection im Rampenlicht (oder EP bei Musik) = ein Datenarray aus Kunstobjekten, zeigt die ersten drei Objekte an, beim clicken öffnet sich mit fließender Vergrößerungsanimation die Serie oder Collection mit allen Inhalten
- [SCOPE] Ausgewähltes Event im Rampenlicht
  - zB Einstellbar, dass neue Serien die alten Darstellungstechnisch auf Profil ersetzen
- [SCOPE] Eventübersicht (vergangene Events & kommende Events)

Reihenfolge auf Profil frei bestimmbar (auch Beschreibung nur Titel und Profilbild ist fest)

## Profile-Specs-Login
- [MVP] Basic Auth

1. [MVP] Visuelle Oberfläche was andere auf dem Profil sehen
   1. [MVP] Drag and Drop Module
   2. [MVP] Editier Icon für jeden Bereich
      1. Werk | Serie | [SCOPE] Collaboriations | aktuelles Projekt
      2. Werk | Serie  [SCOPE] Collaboriations | aktuelles Projekt
      - Modulreihenfolge Drag und Drop oben links 
      - EditierIcon: Serie, Werk oder Collaboration ersetzen
  

### Profile-Login-Art-Instances
- [MVP] Werkemanagement - Suche und Filter: Tags und Kategorie
- [MVP] Werkeliste - Create, Update, Delete-Icons
- [MVP] Collectionliste - Create, Update, Delete-Icons
- [MVP] Serienliste - Create, Update, Delete-Icons
  - [MVP] Update funktionsfähig (außer Werk durch Upload austauschen)
  - [MVP-Frontend] Create (Upload), Delete - nur Frontend
- [SCOPE] Ökosystem

### Profile-Login-Art-Instances-Sample-Explanation
  1. [MVP] Werkesammlung des Künstlers Filterbar nach Serien, Kategorien und Tags (zB Standort, Zeitdaten oder Event)
     1. [MVP] Kategorien Zeichnen, Dichten, Philosiphieren, Skulpturen
     2. [MVP] Serien: 
        Beispieldatensätze
        1. Serienname: English [poem-02, poem-03, poem-04, poem-06] (auf Profil dargestellt false)
        2. Seriename: Deutsch [poem-01, poem-05] (auf Profil dargestellt true)
        - [SCOPE] Man kann Werke zu Serien bzw EPs (bei Musik) zuordnen.
     3. [SCOPE] Hauptkategorien: Worte (Kurzgeschichten, Gedichte, Geschichten, Bücher, Philosophie), Acoustik (Instrumental | Gesang | Instrumente & Gesang: Musikkomposition, Lyrics, Beats, Mantras etc.), Sehen (Gemälde, Zeichnen, Acryl etc.), Skulpturen (Lichtkunst, Ton, Stein etc.)...
        1. [SCOPE] Spüren (Stricken, Häkeln)
     4. [SCOPE] Plattform-Subscription: eigenes Ökosystem (wie Pokemon oder Happy Potter)
  2. [MVP] Auflistung von Versionierungen aktueller Projektes (status von Projekten und Prozent der Fertigstellung) - nur aktiv (in Prozent: Hier 67 %), beendet derzeit
     1. zugriff auf Versionen im Profilinterface durch Dropdown (draw-02-02 (aktuell), draw-02-01) 
     2. [Workflow](#artist-upload-workflow-agent)
     3. [Workflow](#artist-upload-manual)

Werke: Uploadseite im von Werken im Profil [MVP-Frontend]: Hauptkategorie, Unterkategorie, Tags, Homepage, Preis, Upload
- Name (Pflicht)
- Beschreibung (Optional)
     1. Tags
     2. Veröffentlichungsdatum
     3. Veröffentlichungsort, wenn Event
     4. Zeitraum
     5. Inspiraton
        1. Künstler (Verlinkung möglich)
        2. Epoche
        3. Gefühl
    - Buttons: Cancel, Reihenfolge anpassen, Erschaffen
  
### Art-Instances-Datenlogik
- [MVP] Jedes Werk besitzt eine stabile Basis-ID (z.B. `draw-02`) und eine Versionsnummer (Integer)
- [MVP] Ein "Update" erzeugt einen neuen CSV-Eintrag mit derselben Basis-ID und hochgezählter Versionsnummer — der alte Eintrag bleibt erhalten
- [MVP] Drei CSV-Dateien: `artworks.csv`, `series.csv`, `collections.csv`
- [MVP] `artworks.csv` Spalten: `id`, `base_id`, `version`, `name` (Pflicht), `beschreibung` (optional), `hauptkategorie`, `unterkategorie`, `tags`, `homepage`, `preis`, `veroeffentlichungsdatum`, `zeitraum`, `veroeffentlichungsort`, `event_id`, `event_exclusive_release`, `inspiration_kuenstler`, `inspiration_epoche`, `inspiration_gefuehl`, `filename`, `collection_id`, `series_id`, `is_rampenlicht`, `rampenlicht_percent`, `created_at`
- [MVP] `collections.csv` / `series.csv` Spalten: `id`, `name`, `beschreibung`, `tags`, `show_in_profile` (siehe Toggle-Snippet, keine Exklusivitäts-Logik in dieser Phase)
- [MVP] **Unterschied Collection vs. Serie:** Eine **Collection** darf Werke aus mehreren Kategorien enthalten (kategorienübergreifend). Eine **Serie** enthält ausschließlich Werke derselben Kategorie.
- [MVP] Rampenlicht ist exklusiv: nur ein Werk pro Künstler kann `is_rampenlicht = true` haben — bei Neuwahl wird das alte auf `false` gesetzt. Gilt auf `base_id`-Ebene: nur die jeweils neueste Version einer `base_id` trägt den Rampenlicht-Status.
- [SCOPE] Vorher/Nachher-Vergleich (`filename_before`) — Phase 1 nur `filename`

### Profile-Login-Art-Instances-Explanation
[MVP] Collections: CRUD - Delete wird für Prototyp verhindert
- [Frontend-MVP] Create: Objekte frei wählbar (Zahlenreihenfolge oben Links), Toggle Button für Präsentation auf Profil, Suche nach Tags, Kategorien und Namen
- MVP-Frontend] Toggle Button für Präsentation auf Profil: rein visuell, keine Exklusivitäts-Logik in dieser Phase
  - Mehrere Collections/Serien können gleichzeitig "true" sein, keine Backend-Validierung nötig
  - [SCOPE] Exklusivität (nur eine aktiv, wie Radio-Button) erst in späterer Phase
  - Beschreibung (optional)
     1. Tags
     2. Veröffentlichungsdatum
     3. Veröffentlichungsort, wenn Event
     4. Zeitraum
     5. Inspiraton
        1. Künstler (Verlinkung möglich)
        2. Epoche
        3. Gefühl
    - Buttons: Cancel, Reihenfolge anpassen, Erschaffen

- [MVP] Update: Objekte frei anpassbar (Haken bei derzeit ausgewählten Objekten)
  - Create: Objekte nach Kategorie frei wählbar (Zahlenreihenfolge oben Links), Toggle Button für Präsentation auf Profil, Suche nach Tags, Kategorien und Namen
  - Name (Pflicht)
  - Beschreibung (optional) 
     1. Tags
     2. Veröffentlichungsdatum
     3. Veröffentlichungsort, wenn Event
     4. Zeitraum
     5. Inspiraton
         1. Künstler (Verlinkung möglich)
         2. Epoche
         3. Gefühl
  - Buttons: Cancel, Reihenfolge anpassen, Erschaffen

- Update: Objekte frei anpassbar (Haken bei derzeit ausgewählten Objekten)

### Profile-Subscriptions
1. [SCOPE] Künstler können Subscriptions frei anlegen bezüglich Preis und Umfang
   1. Preview anderer aktiver Projekte für Subscriber 
   2. Zugang zum Kauf seiner Kunst 
   3. Rechtekauf seiner Kunst (kategorisch von Künstler selbst wählbar zB Musik beats oder Bildrechte) 
2.  [SCOPE] Button Zugang zu Atelier (Kategorien, Serien, Tags die dargestellt werden sollen wählbar) - individueller Zeitstrahl Werdegang
  
### Profile-Events
1.  [SCOPE] Fotos und Videos zu einem Event können dem Event beigefügt werden als Referenz
   
### Profile-Collection-Export
- [SCOPE] Export des eigenen Ausdruck in ein Atelier (Farbkunst) oder Studio (Musikkunst) mit Zugangskey für Eventorganisatoren (wie DJ Events, Kunstausstellungen) oder Manager (Verläge von Buch oder Musiklabels)

    - Darstellungform für Betrachter flexibel
    - atelier.flowstate.express/artistName

### Profile-Settings
- [SCOPE] Künstlerprofil Einstellungen
    1.  Mail, Passwort, Sicherheit
    2.  Standard Sichtbarkeitseinstellungen
    3.  Module verschieben

# Workflows [SCOPE]
## Artist-Upload-Manual
- Über das Profileinterface über ein "Werk hochladen" "Werk updaten" Button auf der Hauptseite des Profils

## Artist-Upload-Workflow-Agent
- Der Künstler fotografiert seinen derzeitigen Stand eines Projektes
  - Agent erkennt, ob ein Werk erweitert wurde 
    - "Möchtest du es als Update erfassen?"
    - "Dein alter stand war 34 % fertig. Gib deinen neuen Stand schätzungsweise ein:"
- Informationen werden über Agent erfasst (Bild, Text, Einordnung welches Projekt, welche Tags und Kategorie (falls neues Projekt))
- Wenn abgeschlossen fragt er, ob der Fortschritt behalten werden soll (Verfügbarkeitsrechte für Subscriber des Künstlers möglich)

- Bild wird bei Experience für Follower und Interessenten von Kategorien oder Tags angezeigt (Follower First Prinzip)

## Eventbuchungen
- So wenig Steps wie möglich zum Kauf oder kostenfreie Teilnahme
- Kalenderintegration mit Ort, Datum, Uhrzeit, Anfahrt etc. 
 
# Plattform-Subscription-Specs [SCOPE]
- Zugang für das persönlichen Export (zB Atelier oder Musikstudio (Phase 4))
  - Zeitstrahl Resumé
- Eventhinterlegung von Bildern und Videos
- Vergünstigung von Live Events (Kooperationen mit Ateliers, Yogafestivals etc.)
- Zugang zu exklusiven live Events
- Eventhistorie mit Bldern und Videos im Profil (Resumé)
Subscription Künstler & Plattform
- Export Funktion + Zeitstrahl werdegang der eigenen Kunst
- Zugriff auf die Ökosystem Funktion zB eigenes Kunst oder Geschichtsökosystem (wie Pokémon oder OnePiece mit Charakteren (Identitäten)) 
- Bei jedem Vergangenen Event können die Werke beigefügt werden 
  
# Texts 
[MVP]
## Landingpage-Texts
### Hero-Text
Text: Spüre deinen Ausdruck
Buttons: [Erlebe](#experience-texts) -  [Spüre](#observe-texts)
### Vision-Section
**Der Raum**
Flowstate ist der Wunsch einen Raum für jeden zu schaffen, in der jede Emotion getragen wird um im Ausdruck des Selbst Raum findet.

**Der Ausdruck** Das was uns alle miteinander verbindet ist das Gefühl. Flowstate Express schafft ein Raum des Erkennens im Ausdruck des anderen. Das betrachten des Ausdrucks und des anderen ohne Filter.

**Die Relevanz** KI Übernimmt die Welt der Gedanken, kann aber nie fühlen oder wahnehmen wie wir Menschen. Dies unterscheidet uns von der Maschine. Genau aus diesem Grund ist der Ausdruck durch das Gefühl wichtiger denn je. Vom Kopf ins Herz.

**Kultur** Das Ziel ist es die Menschen in ein gemeinschaftliches harmonisches Erleben zu führen. Voller Akzeptanz und Wertschätzung einander.

### Zahlen, Daten, Fakten

Diese Fakten gehören auf die Landingpage – als emotionaler Anker direkt unter den Events, um Menschen „ins Fühlen" zu bringen.

#### Der digitale Mangel
- **Bis zu 95 %** der 13- bis 17-Jährigen nutzen Social Media; rund **ein Drittel** nutzt es „fast ständig". ~ Pew Research 2022, Yale Medicine 
- Teenager kamen zwischen 2015–2021 auf durchschnittlich **8 Std. 39 Min.** Mediennutzung pro Tag. ~ Research: Common Sense Media Census 2021
- Etwa die **Hälfte** der 12- bis 17-Jährigen hat **4+ Stunden** tägliche Bildschirmzeit. ~CDC NCHS-Teen-Survey (Juli 2021–Dez 2023)

#### Die Folgen
- Bei **4+ Stunden** Bildschirmzeit berichten rund **1 von 4** Teenagern von Angst- (27 %) bzw. Depressionssymptomen (26 %) – bei unter 4 Stunden sinkt das auf 12 % bzw. 10 %. ~ CDC NCHS Data Brief Nr. 513 (Okt 2024)
- Der **US Surgeon General erklärte Einsamkeit 2023 zur Public-Health-Epidemie**. Einsamkeit verdoppelt das Depressionsrisiko und erhöht das Risiko für Herzkrankheit, Schlaganfall und vorzeitigen Tod.
- Soziale Medien bauen strukturell auf **Vergleich** auf („mehr, mehr, mehr") – genau das Gegenteil von Selbstwert.

#### Der Gegenentwurf: Ausdruck heilt
- **45 Minuten künstlerisches Gestalten senken nachweislich den Cortisolspiegel** (Stresshormon) – unabhängig von Vorerfahrung. ~ Studie (Kaimal, Ray & Muniz 2016, Art Therapy Journal)
- **Expressives Schreiben** ist mit langfristig besserer Gesundheit und niedrigerem Stress verbunden; Studien zeigen Wirkung bei Depression, Trauma und sogar suizidalen Gedanken.
- Systematische Reviews: Kunsttherapie steigert emotionales Wohlbefinden, Selbstwert und Lebenszufriedenheit.

**Die Botschaft:** Glück kommt nicht durch das Außen. Es kommt durch das Fühlen, das Hinschauen, das Loslassen – durch den Ausdruck in uns. Genau dafür ist Flowstate.express ein Raum.

## Experience-Texts
### Hero-Text
Text: Spüre dich selbst und verleihe dem Ausdruck
Button: [Online](#Online-Event-Module-Text), [Persönlich](#Personal-Event-Module-Text)

### Online-Event-Module-Text
Text: Finde deinen Ausdruck Ortsungebunden in Gemeinschaft

### Personal-Event-Module-Text
Text: Spüre die Resonanz mit anderen im gemeinschaftlichen Erleben 

### Community-Chat-Text
Text: Teile deine Freude am Ausdruck mit Gleichgesinnten und lass dich von ihnen verzaubern

## Observe-Texts
### Hero-Text
Text: Spüre den Ausdruck anderer und lass ihn auf dich Wirken

# Allgemein
- Man kann sich folgen
  - Im Profil Einstellbar, ob der Künstler sichbar sein möchte als Follower
- Man kann zusammen mit mehreren Personen etwas erschaffen
- Grundprinzip: Inhalte zeigen Kunst, nicht Gesichter/Personen (kein Portrait- oder Personenfokus)
- Ausnahme: Event-Atmosphäre-Fotos (siehe Event-Component)