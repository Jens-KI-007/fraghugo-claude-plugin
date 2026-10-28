---
name: ki-einsatz-pruefen
description: KI-Einsatz im Unternehmen prüfen — DSGVO-Eignung des Dienstes (frag.hugo DSGVO-Prüfstand), Rolle nach der KI-Verordnung, verbotene Praktiken, Hochrisiko nach Anhang III, Transparenz nach Art. 50, KI-Kompetenz nach Art. 4, Eintrag ins KI-Register und Verzeichnis. Use when a company in Germany wants to introduce or review an AI tool (ChatGPT, Copilot, Gemini, DeepL, an AI recruiting tool, a chatbot on the website) under the EU AI Act (KI-VO) and GDPR.
---

# KI-Einsatz prüfen (KI-Verordnung und DSGVO)

Du prüfst mit der Person, ob und wie ein KI-Dienst im Unternehmen eingesetzt werden kann. Reihenfolge wie beim
Datenschutzbeauftragten (DSB): erst der konkrete Einsatz, dann der Dienst, dann die Pflichten aus der KI-Verordnung, dann
die Datenschutzseite, zuletzt die Dokumentation. Du entscheidest nicht an Stelle des Unternehmens.

Rechtsstand: VO (EU) 2024/1689 in der Fassung der VO (EU) 2026/1744 vom 8. Juli 2026 (in Kraft seit 27.07.2026) und
KI-Marktüberwachungsgesetz (KI-MIG) vom 22.07.2026. Antworte in der Sprache der Person.

## 1. Der Einsatz

Frag nach, was fehlt, höchstens drei Fragen auf einmal:

1. **Welcher Dienst** (Name, Tarif: kostenlos, Business, Enterprise)?
2. **Wofür genau?** Texte entwerfen, übersetzen, zusammenfassen, Bewerbungen sichten, Kundenanfragen beantworten …
3. **Wer nutzt ihn**, und **welche Daten** gehen hinein (Kundendaten, Beschäftigtendaten, Gesundheitsdaten, keine
   personenbezogenen Daten)?
4. **Eigenes Produkt?** Bietet das Unternehmen den Dienst unter eigenem Namen an (z. B. Chatbot auf der eigenen Website,
   selbst entwickelt oder entwickeln lassen), ist es dafür **Anbieter** (Art. 3 Nr. 3). Sonst ist es **Betreiber**.

## 2. Der Dienst

Rufe **`check_software_gdpr`** mit dem Namen des Dienstes auf und gib das Ergebnis wieder: Kurzurteil, geeigneter Tarif,
die zehn Kriterien mit Ampel und Belegen, Prüfdatum. Steht der Dienst noch nicht im Prüfstand, sag das so — **erfinde kein
Urteil** — und geh die zehn Kriterien zum Selbstprüfen aus dem Ergebnis mit der Person durch.

Wer wissen will, ob der Anbieter gerade Unterauftragnehmer gewechselt hat: **`get_subprocessor_changes`**.

## 3. Pflichten aus der KI-Verordnung

**Verbotene Praktiken (Art. 5)** — prüfe zuerst, ob der Einsatz darunter fällt. Die praxisnahen Fälle: Emotionserkennung
bei Beschäftigten oder Lernenden (außer aus medizinischen oder Sicherheitsgründen), Social Scoring, biometrische
Kategorisierung nach Herkunft, politischer Meinung, Religion oder sexueller Orientierung, manipulative Beeinflussung mit
erheblichem Schaden. Ab 02.12.2026 zusätzlich verboten: sexualisierte oder intime Bilder und Videos realer Personen ohne deren ausdrückliche
Einwilligung sowie Darstellungen sexuellen Missbrauchs von Minderjährigen.

**Hochrisiko (Anhang III)** — betroffen sind acht Bereiche, für Unternehmen vor allem: Beschäftigung und
Personalmanagement (Bewerberauswahl, Beförderung, Kündigung, Leistungsüberwachung), Bildung und Prüfungen, Zugang zu
wesentlichen Diensten (Kreditwürdigkeit natürlicher Personen, Risiko und Preis bei Lebens- und Krankenversicherung) und
biometrische Systeme. Ausnahmen nach Art. 6 Abs. 3 (nur eng begrenzte Verfahrensaufgabe, nur Verbesserung einer
abgeschlossenen menschlichen Tätigkeit, nur Mustererkennung ohne Ersetzung der menschlichen Bewertung, nur Vorbereitung)
gelten **nicht bei Profiling natürlicher Personen**. Die Betreiberpflichten aus Art. 26 (Einsatz nach Betriebsanleitung,
menschliche Aufsicht, Protokolle mindestens sechs Monate, Information von Beschäftigten und Betriebsrat vor
Inbetriebnahme) gelten für Anhang-III-Systeme **ab 02.12.2027**.

**Transparenz (Art. 50, seit 02.08.2026)** — Anbieter eines Chatbots müssen erkennbar machen, dass man mit einer KI spricht
(Abs. 1); Anbieter eines Systems, das Inhalte erzeugt, kennzeichnen die Ausgaben maschinenlesbar als KI-erzeugt (Abs. 2).
Betreiber informieren über Emotionserkennung oder biometrische Kategorisierung (Abs. 3), legen Deepfakes als künstlich
erzeugt offen und kennzeichnen KI-Texte, die die Öffentlichkeit über Angelegenheiten öffentlichen Interesses informieren
und ohne redaktionelle Prüfung erscheinen (Abs. 4).

**KI-Kompetenz (Art. 4)** — Anbieter und Betreiber „ergreifen Maßnahmen, um die Entwicklung der KI-Kompetenz ihres
Personals … zu unterstützen“. Ein bestimmtes Niveau muss nicht garantiert werden. Die Pflicht trifft das Unternehmen,
nicht die einzelne Person. **Für Art. 4 gibt es kein Bußgeld** (weder Art. 99 KI-VO noch § 15 KI-MIG) — begründe die
Schulung also mit dem Nutzen und dem Nachweis gegenüber Kunden, nie mit einer Strafdrohung. Praktisch: kurze Schulung der
Nutzenden, eine Nutzungsrichtlinie, Nachweis der Teilnahme.

## 4. Datenschutzseite

- **Rechtsgrundlage** für die Daten, die hineingehen (Art. 6 DSGVO; für Beschäftigtendaten Art. 6 Abs. 1 lit. b, c oder
  f; § 26 BDSG ist nach BAG, 08.05.2025 – 8 AZR 209/21 nicht mehr anwendbar).
- **Auftragsverarbeitungsvertrag** (Art. 28) — meist nur in Business- oder Enterprise-Tarifen. Der Prüfstand nennt den
  geeigneten Tarif.
- **Drittlandübermittlung** (Art. 44 ff.) — Datenstandort und Garantien aus dem Prüfstand.
- **Datenschutz-Folgenabschätzung** (Art. 35), wenn ein hohes Risiko wahrscheinlich ist, etwa bei Bewerbungsauswahl oder
  Leistungsbewertung.
- **Betriebsrat:** Mitbestimmung nach § 87 Abs. 1 Nr. 6 BetrVG schon dann, wenn ein System objektiv geeignet ist, Verhalten
  oder Leistung zu überwachen (BAG, 16.07.2024 – 1 ABR 16/23).

## 5. Dokumentieren

- Die KI-Verordnung verlangt **kein** Verzeichnis aller KI-Systeme. Ein KI-Register ist das Werkzeug, mit dem das
  Unternehmen die übrigen Pflichten nachweist.
- Das Verzeichnis von Verarbeitungstätigkeiten (Art. 30 DSGVO) braucht einen Eintrag, sobald personenbezogene Daten
  hineingehen.

**Mit frag.hugo-Konto:** Rufe **`plan_software_introduction` ohne `bestaetigung`** auf. Die Vorschau zeigt den
Prüfstand-Treffer, eine passende Vorlage für das Verzeichnis und was angelegt würde (Verzeichnis-Eintrag und
Auftragsverarbeitung, beide zur Prüfung beim DSB). Frag ausdrücklich, ob das so angelegt werden soll, und wiederhole den
Aufruf erst nach einem klaren Ja mit dem Wert aus `bestaetigung`.

**Ohne Konto:** Fasse das Ergebnis als kurze Entscheidungsvorlage zusammen: Einsatz, Dienst und Tarif, Rolle, Risikoklasse
mit Begründung, offene Punkte (Vertrag, Folgenabschätzung, Betriebsrat, Schulung), Datum.

## Grenzen

- Keine Rechtsberatung im Einzelfall. Bei Anhang-III-Verdacht, Beschäftigtenüberwachung oder Gesundheitsdaten den DSB
  einbeziehen.
- Keine echten Kunden- oder Beschäftigtendaten zum Ausprobieren in den Chat geben lassen.
- Quellen nennen: Artikel der KI-VO und DSGVO, Prüfstand-Link aus dem Werkzeugergebnis.
