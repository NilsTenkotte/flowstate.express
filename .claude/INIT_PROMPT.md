# Init Prompt — Flowstate Express MVP (Entwurf, bitte manuell anpassen)

Du baust das MVP von **Flowstate Express**. Die vollständige Produktspezifikation ist
`.claude/Flowstate.Express.md` — lies sie **vollständig**, bevor du irgendetwas anlegst.
Sie ist die Quelle der Wahrheit. Du editierst sie nicht.

## Vorgehen (in dieser Reihenfolge)

1. Lies `.claude/Flowstate.Express.md` komplett.
2. Lies `.claude/design-tokens.md` (Farben, Fonts, Logo-Regeln) — halte dich strikt daran, erfinde keine eigenen Farben/Fonts.
3. Erstelle `.claude/plan/IMPLEMENTATION_PLAN.md`: eine aus der Spec abstrahierte Task-Liste, **nur `[MVP]`-markierte Punkte**, `[SCOPE]`-Punkte ignorierst du für diese Phase komplett. Jeder Task bekommt einen Status (offen / in Arbeit / fertig). Diese Datei pflegst du selbst weiter, während du arbeitest.
4. Pflege `.claude/context/QUESTIONS.md`. Immer wenn die Spec an einer Stelle mehrdeutig ist oder du eine Annahme triffst, die nicht eindeutig aus dem Text folgt: Eintrag hier, statt zu raten. Arbeite mit der naheliegendsten Annahme weiter, aber dokumentiere sie.
5. Erst danach: Code.

## Tech-Stack (Phase 1)
- Next.js, Tailwind
- CSV als Datenstruktur (kein Supabase in dieser Phase)
- CSV-Spalten so anlegen, dass sie wie Fremdschlüssel funktionieren (`collection_id`, `series_id`, `version_of` o.ä.) — Ziel: spätere Migration nach Supabase ohne Redesign
- Schema leitest du selbst aus der Spec ab (siehe `### Art-Instances-Datenlogik` in der Spec für die Update/Versionierungs-Logik)

## Feste Prinzipien (nicht verhandelbar, unabhängig von Formulierung einzelner Sections)
- Kunst ist **nicht öffentlich kommentierbar**. Grund: öffentliche Kommentarboxen senken die Hemmschwelle für Hass; Interaktion mit dem Künstler soll direkt erfolgen.
- Inhalte zeigen **Kunst, nicht Gesichter/Personen**. Einzige Ausnahme: Event-Atmosphäre-Fotos (Scale/Stimmung eines Events).
- Jedes Werk-Update erzeugt einen **neuen versionierten Eintrag**, überschreibt nicht den alten (Versionshistorie bleibt erhalten, siehe Dropdown-Logik in der Spec).

## Beispieldaten
Nutze die vorhandenen Dateien in `/.claude/context/sample-images/` (draw-01 bis draw-04, poem-01 bis poem-06, sculpture-01, philosophie-01) als Seed-Daten für die CSV, exakt wie in der Spec unter „Beispieldatensätze" referenziert.

## Wenn du unsicher bist
Nicht raten und stillschweigend weiterbauen. Eintrag in `/.claude/context/QUESTIONS.md`, plausibelste Annahme wählen, weiterarbeiten, am Ende Zusammenfassung der offenen Fragen.

---
*Hinweis für Nils: Dieser Entwurf geht davon aus, dass ein zweiter Agent (Reviewer) `.claude/plan/IMPLEMENTATION_PLAN.md` + `.claude/context/QUESTIONS.md` + den Code-Stand gegen `.claude/Flowstate.Express.md` gegenprüft, in einer separaten/frischen Session ohne geerbten Reasoning-Trail. Passe Formulierung/Reihenfolge gern an, bevor du ihn an Claude Code gibst.*
