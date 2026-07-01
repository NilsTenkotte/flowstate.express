# IMPLEMENTATION_PLAN.md
Quelle der Wahrheit: `Flowstate.Express.md` · Design: `design-tokens.md`
Scope: **nur [MVP]-Tasks, Phase 1 (Website)**. Langfristige Roadmap (Phasen 2-4) siehe `ROADMAP.md` — nicht Teil dieses Plans.

Status-Werte: `offen` / `in Arbeit` / `fertig`. Diese Datei wird vom Builder-Agent laufend aktualisiert.
Offene Design-Fragen gehören nicht hierher, sondern in `QUESTIONS.md`.

---

## 0. Setup
- [ ] **Next.js + Tailwind Grundgerüst** — Status: offen
  - Tailwind-Config strikt aus `design-tokens.md` ableiten (Farben, Fonts) — keine eigenen Werte erfinden
- [ ] **CSV-Datenmodell anlegen** — Status: offen
  - 3 Dateien: `artworks.csv`, `series.csv`, `collections.csv`
  - `artworks.csv` Spalten: `id`, `base_id`, `version` (Integer), `name` (Pflicht), `beschreibung` (optional), `hauptkategorie`, `unterkategorie`, `tags`, `homepage`, `preis`, `veroeffentlichungsdatum`, `zeitraum`, `veroeffentlichungsort`, `event_id`, `event_exclusive_release`, `inspiration_kuenstler`, `inspiration_epoche`, `inspiration_gefuehl`, `filename`, `filename_before`, `collection_id`, `series_id`, `is_rampenlicht`, `rampenlicht_percent`, `created_at`
  - `series.csv` / `collections.csv` Spalten: `id`, `name`, `beschreibung`, `tags`, `show_in_profile`
  - Versionierung: neues Update = neuer Eintrag mit gleicher `base_id`, hochgezählter `version` — kein Überschreiben, kein separates `version_of`-Feld
  - **Rampenlicht ist unabhängig pro Werk** — mehrere Werke können gleichzeitig `is_rampenlicht = true` sein, jedes mit eigenem `rampenlicht_percent`. Keine Exklusivitäts-Logik nötig.
  - Spalten so anlegen, dass sie wie Fremdschlüssel funktionieren (`collection_id`, `series_id`) — spätere Supabase-Migration ohne Redesign

## 1. Header & Footer
- [ ] **Header**: Logo + Login (vorausgefüllt) — Status: offen
- [ ] **Footer**: Logo + Impressum (Spec Z. 95–119, unverändert übernehmen) — Status: offen
- [ ] **Datenschutzerklärung um Zoom erweitern** — Status: offen
  - Zoom als Auftragsverarbeiter ergänzen (SCC-Hinweis, Verweis auf Zoom.us Datenschutzhinweise)
  - Text noch nicht final formuliert — vor Umsetzung mit Nils abstimmen oder als Platzhalter-Absatz mit TODO markieren

## 2. React Tabs

### 2.1 Landingpage — Status: offen
- Hero: ein Bild, clickable/vergrößerbar
- 6 Sections (Core Vision, Experience, Observe, Profile, ZDF-Text, Verweis Flowstate Foundation)
- ZDF-Text Inhalt: internationale Zahlen (Pew/CDC) + mindestens eine bestätigte deutsche Dissertation (Oepen 2015, Kunsttherapie/Wohlbefinden) als "Made in Germany"-Anker
  - Optional/offen: zusätzliche deutsche Kontext-Studie (z.B. HBSC 2022) — noch nicht final entschieden, siehe `QUESTIONS.md`

### 2.2 Experience — Status: offen
- Eventauflistung (Filter: Online, Persönlich)
- Zoom-Event-Komponente: Meetingname, Zeit, Ort, Datum, Online/Persönlich-Icon, Teilnehmerzahl, Meetinglink, Kunstobjekte-Referenz-Array (Werke/Serien/Collections, die dort ausgestellt wurden), `event_exclusive_release`-Markierung, Meetingpartner, mitwirkende Künstler
- Event-Atmosphäre-Fotos: Ausnahme vom allgemeinen "keine Gesichter/Personen"-Prinzip
- Community Chat: 4 Kategorien (Gedichte, Zeichnen, Philosophie, Skulpturen)

### 2.3 Observe — Status: offen
- 4 Beispielwerke im Feed (draw-04, poem-03, sculpture-01, draw-03)
- **Keine öffentliche Kommentarfunktion** — Begründung im Code/Kommentar festhalten: öffentliche Kommentarboxen senken die Hemmschwelle für Hass; Interaktion mit dem Künstler soll direkt erfolgen, nicht anonym-öffentlich

### 2.4 Profile (ohne Login) — Status: offen
- Titel "Was ist meine Essenz?", Beschreibung "Was prägt(e) meinen Ausdruck?" — beides nutzerdefiniert, keine separate Profile-Texts-Sektion nötig
- Ein Ausstellungswerk je Kategorie
- Rampenlicht-Anzeige (Prozent-Fortschritt)

## 3. Profile-Login — Status: offen
- Basic Auth
- CRUD Art-Instances (Werke, Collections, Serien) inkl. Suche/Filter nach Tags/Kategorie
- Drag & Drop Modulreihenfolge
- Collection-/Serien-Toggle "Präsentation auf Profil": **rein visuell/frontend, keine Exklusivitäts-Logik in dieser Phase** — mehrere können gleichzeitig `show_in_profile = true` sein
- Werke-Upload-Formular mit allen Spec-Feldern (siehe CSV-Schema oben)

## 4. Seed-Daten — Status: offen
- `artworks.csv`, `series.csv`, `collections.csv` befüllen mit vorhandenen Dateien aus `images/` gemäß Spec-Beispieldatensätzen (Serie "English": poem-02/03/04/06 nicht dargestellt, Serie "Deutsch": poem-01/05 dargestellt)

## Grundprinzipien (gelten über alle Punkte hinweg)
- Inhalte zeigen Kunst, nicht Gesichter/Personen — Ausnahme: Event-Atmosphäre-Fotos
- Kein öffentliches Kommentieren von Werken
- CSV-Spalten als Fremdschlüssel-Äquivalent anlegen (spätere Supabase-Migration)
- Bei Mehrdeutigkeit: Eintrag in `QUESTIONS.md`, plausibelste Annahme wählen, weiterarbeiten

## Referenzen
- `Flowstate.Express.md` — Produktspezifikation
- `design-tokens.md` — Farben/Fonts
- `ROADMAP.md` — langfristige Phasen (nicht Teil dieses Plans)
- `QUESTIONS.md` — offene Punkte, die Rückfrage an Nils brauchen
