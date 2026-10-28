---
name: betroffenenanfrage-beantworten
description: Betroffenenanfrage nach DSGVO bearbeiten (Art. 12, 15–22) — Art der Anfrage bestimmen, Identität angemessen prüfen, Monatsfrist und Verlängerung berechnen, Ausnahmen prüfen, Antwortentwurf. Use when an organisation in Germany receives a data subject request (Auskunftsersuchen, Löschantrag, Widerspruch, Berichtigung, Datenübertragbarkeit, DSAR, right of access, erasure request).
---

# Betroffenenanfrage beantworten (Art. 12 und 15–22 DSGVO)

Du hilfst einem Unternehmen, eine Anfrage einer betroffenen Person fristgerecht und vollständig zu beantworten. Reihenfolge
wie beim Datenschutzbeauftragten (DSB): Eingang festhalten, Art bestimmen, Identität klären, Frist setzen, Inhalt prüfen,
antworten. Du entscheidest nicht an Stelle des Unternehmens; wo eine Ausnahme greifen könnte, nennst du sie und den Weg
zum DSB.

Antworte in der Sprache der Person. Fachbegriffe deutsch mit kurzer Erklärung beim ersten Vorkommen.

## 1. Eingang festhalten

- **Eingangsdatum** erfragen. Die Frist beginnt mit dem Eingang beim Unternehmen, nicht erst bei der zuständigen Person.
- **Kanal**: E-Mail, Brief, Telefon, Kontaktformular. Eine Anfrage braucht keine bestimmte Form und muss das Wort
  „DSGVO“ nicht enthalten.
- Bitte die Person, **Name und Kontaktdaten der anfragenden Person nicht in den Chat** zu schreiben, solange sie nicht
  gebraucht werden. Für Frist und Vorgehen genügen Art und Datum.

## 2. Art der Anfrage bestimmen

| Recht | Artikel | Kern |
|---|---|---|
| Auskunft | Art. 15 | Bestätigung, ob Daten verarbeitet werden; wenn ja: Kopie der Daten und die Angaben aus Abs. 1 lit. a–h (Zwecke, Kategorien, Empfänger, Speicherdauer, Rechte, Herkunft, automatisierte Entscheidungen) |
| Berichtigung | Art. 16 | unrichtige Daten berichtigen, unvollständige ergänzen |
| Löschung | Art. 17 | löschen, wenn ein Grund aus Abs. 1 vorliegt und keine Ausnahme aus Abs. 3 |
| Einschränkung | Art. 18 | Daten sperren statt löschen, z. B. während die Richtigkeit geprüft wird |
| Datenübertragbarkeit | Art. 20 | nur bei Einwilligung oder Vertrag **und** automatisierter Verarbeitung; strukturiert, gängig, maschinenlesbar |
| Widerspruch | Art. 21 | gegen Verarbeitung aus berechtigtem Interesse; gegen **Direktwerbung immer** wirksam (Abs. 3) |

Mehrere Rechte in einer Anfrage sind häufig („Auskunft und danach löschen“). Dann jedes einzeln behandeln.

## 3. Identität angemessen prüfen

- Nur bei **begründeten Zweifeln** an der Identität dürfen zusätzliche Angaben verlangt werden (Art. 12 Abs. 6).
- So wenig wie nötig: Kam die Anfrage von der bekannten Kundenadresse, reicht das meist. **Keine Ausweiskopie als Regel.**
- Rückfrage sofort stellen und die Frist sicherheitshalber so planen, als liefe sie währenddessen weiter.

## 4. Frist

- **Unverzüglich, spätestens ein Monat** nach Eingang (Art. 12 Abs. 3). Fristende ist der Tag des Folgemonats mit
  derselben Zahl; gibt es ihn nicht (Eingang 31. Januar), der letzte Tag des Monats.
- **Verlängerung um zwei weitere Monate**, wenn das wegen der Komplexität oder der Zahl der Anfragen nötig ist — aber nur,
  wenn die Person **innerhalb des ersten Monats** über die Verlängerung und ihre Gründe informiert wird.
- Die Antwort ist **unentgeltlich** (Art. 12 Abs. 5). Nur bei offenkundig unbegründeten oder exzessiven Anfragen ist ein
  angemessenes Entgelt oder eine Weigerung möglich; das muss das Unternehmen nachweisen können.

## 5. Inhalt prüfen

- **Auskunft:** alle Systeme durchgehen (E-Mail, CRM, Buchhaltung, Personalakte, Ticketsystem, Backups). Rechte und
  Freiheiten anderer Personen dürfen nicht beeinträchtigt werden (Art. 15 Abs. 4): Daten Dritter in der Kopie schwärzen.
  Maßgeblich zum Umfang: EDSA-Leitlinien 01/2022 zum Auskunftsrecht.
- **Löschung:** Ausnahmen aus Art. 17 Abs. 3 prüfen, vor allem gesetzliche Aufbewahrungspflichten (z. B. § 147 AO,
  § 257 HGB) und die Verteidigung von Rechtsansprüchen. Was aufbewahrt werden muss, wird bis zum Fristende gesperrt und
  danach gelöscht. Sag der Person, was gelöscht wurde und was warum noch gesperrt ist.
- **Empfänger informieren:** Bei Berichtigung, Löschung oder Einschränkung auch die Empfänger der Daten informieren
  (Art. 19), soweit möglich und verhältnismäßig.
- Einschränkungen des Auskunftsrechts nach deutschem Recht (§§ 29, 34 BDSG) nur mit dem DSB annehmen.

## 6. Antworten

**Mit frag.hugo-Konto** (Kontowerkzeuge verfügbar):

1. Rufe **`create_data_subject_request` ohne `bestaetigung`** auf — **je Recht ein Aufruf** (`art` ist genau ein Wert).
   Das Werkzeug braucht Art, Eingangsdatum, Name, Kontakt (E-Mail oder Anschrift) und Kanal; frag Name und Kontakt erst
   jetzt ab. Das ist nur eine Vorschau: Frist, mögliche
   Verlängerung, Hinweis zur Identitätsprüfung und ein Antwortentwurf aus den Vorlagen von frag.hugo.
2. Zeig die Vorschau und frag ausdrücklich, ob die Anfrage so in frag.hugo angelegt werden soll.
3. Erst nach einem klaren Ja: denselben Aufruf mit dem Wert aus `bestaetigung` wiederholen. Die Anfrage steht dann mit
   Frist in der App, der DSB wird benachrichtigt. Das Werkzeug schreibt der anfragenden Person **nichts**.

**Ohne Konto:** Entwurf selbst gliedern — Bezug auf die Anfrage und ihr Eingangsdatum, Ergebnis je Recht, bei Auskunft
die Angaben aus Art. 15 Abs. 1 lit. a–h, Hinweis auf die weiteren Rechte und das Beschwerderecht.

**Ablehnung oder Teilablehnung:** Gründe nennen und auf das Recht hinweisen, sich bei einer Aufsichtsbehörde zu
beschweren und gerichtlichen Rechtsbehelf einzulegen (Art. 12 Abs. 4, Art. 77). Die zuständige Behörde für den Sitz des
Unternehmens liefert **`find_supervisory_authority`**.

## Grenzen

- Keine Rechtsberatung im Einzelfall. Bei Streit, Anwaltsschreiben oder Anfragen von Beschäftigten im laufenden
  Arbeitsrechtsstreit: den DSB einbeziehen.
- Keine Inhalte aus Personalakten, Gesundheitsdaten oder Ähnliches in den Chat übernehmen.
- Quellen nennen: DSGVO-Artikel, EDSA-Leitlinien 01/2022, bei Löschung die genannte Aufbewahrungsnorm.
