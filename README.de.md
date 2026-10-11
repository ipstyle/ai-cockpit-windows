# AI-Cockpit für Windows — Downloads

*[English](README.md)*

Alle KI-Limits an einem Ort, im Infobereich der Taskleiste — Claude,
ChatGPT/Codex, die OpenAI- und Anthropic-Schnittstellen, Kimi K3, OpenRouter,
Grok (xAI), GitHub Copilot, DeepSeek und die laufenden Claude-Code-Sitzungen.
Neun Dienste, bis zu elf Karten — Claude zählt doppelt, wenn ein zweites Konto eingerichtet ist.

Das ist die Windows-Fassung von [AI-Cockpit für macOS](https://apps.apple.com/app/id6802014255).
Sie ist **gratis**.

**Dieses Repo trägt die Downloads und sonst nichts.** Quellcode steht hier
keiner: Er ist derselbe wie bei der macOS-Fassung und bleibt
geschlossen.

## Herunterladen

**[→ Neueste Fassung](../../releases/latest)**

| Datei | Wofür |
|---|---|
| `AI-Cockpit-<Fassung>-win-x64.exe` | gewöhnliche Windows-PCs |
| `AI-Cockpit-<Fassung>-win-arm64.exe` | Windows on ARM — Snapdragon-Geräte und Windows-VMs auf Apple-Silicon-Macs |

Jede Datei ist in sich vollständig; .NET muss nicht installiert sein.

### Windows warnt

Die Dateien sind nicht mit einem Code-Signing-Zertifikat signiert. Ein solches
kostet mehrere hundert Franken im Jahr — bei einer kostenlosen App trage ich das
nicht. SmartScreen zeigt deshalb **«Der Computer wurde durch Windows
geschützt»**.

So starten Sie sie trotzdem: **Weitere Informationen** → **Trotzdem ausführen**.

Wer lieber vorher prüft: Zu jeder Fassung liegt eine `.sha256`-Datei neben der
Anwendung.

```
certutil -hashfile AI-Cockpit-1.8.1-win-arm64.exe SHA256
```

Die Warnung sagt nichts über den Inhalt aus, nur über die Verbreitung, und
verschwindet von selbst, sobald die Datei oft genug heruntergeladen wurde.
Manche verwalteten Firmenrechner blockieren unsignierte Anwendungen allerdings
hart — da hilft kein Klick.

## Neu in 1.8

**1.8.1 (11.10.2026):** Die OpenAI-Karte geht wieder. OpenAI liefert Kosten nur noch ein Jahr zurück und lehnte die alte Abfrage über drei Jahre mit HTTP 400 ab; die App liest jetzt ein Jahr und zeigt den Grund, wenn ein Dienst eine Abfrage ablehnt.

Die ganze Liste steht in den Release-Notizen; das Wichtigste (die Funktionen der Mac-App 7.5 – «Dein Geld und deine Zeit im Griff»):

- **Abo-Kalender** — Verlängerungsdatum und Rhythmus je Abo (Claude, zweites
  Claude-Konto, ChatGPT/Codex). Eine Mitteilung 1–7 Tage vorher (Standard 3)
  um 09:00, auf Wunsch mit dem Abo-Check («Max 5× würde wohl reichen»), und
  auf der Karte «Verlängert in 5 Tagen».
- **Reset-Wecker** — die Glocke an einem Fenster: eine einzige Mitteilung, wenn
  es wieder geht, auch beim Sonder-Reset. Kommt auch in der Ruhezeit.
- **Tagesration** — «Heute noch 9 % frei, damit die Woche reicht» unter den
  Wochenfenstern; abschaltbar.
- **Ruhezeiten** — von–bis ohne Mitteilungen (Standard 22–07, aus), der
  Kosten-Alarm darf auf Wunsch durch; «Pause bis morgen» im Menü des
  Infobereichs.
- **Dein KI-Monat** — am 1. ein Rückblick auf den Vormonat: Summe, Abos und API,
  je Dienst, Vergleich mit dem Monat davor. Als PNG teilbar, ohne Kontonamen.

## Frühe Fassungen

Die aktuelle Fassung **wurde nie ausgeführt.** Sie ist auf einem Mac gebaut und
übersetzt worden; WPF läuft dort nicht. Geprüft ist, was sich ohne laufendes
Programm prüfen lässt: Die gesamte Projektmappe übersetzt samt XAML, 1606 Tests
des Kerns laufen durch, und ein Vergleichswerkzeug beweist, dass der
Windows-Kern Byte für Byte dasselbe rechnet wie der macOS-Kern.

**Alles Sichtbare ist ungeprüft.** Die Release-Notizen listen auf, was das
konkret heisst — bitte vor dem Start lesen.

Der schnellste Weg zu einem Eindruck: starten, dann im Assistenten «Demo
ansehen» — oder später Einstellungen → Konten → Demomodus. Alle Karten füllen
sich mit Beispielzahlen, ohne einen einzigen Zugang.

Bleibt etwas leer: Einstellungen → Diagnose → **Bericht erzeugen**. Der Text
sagt je Karte, was ihr Zustand ist, und enthält keinen einzigen Schlüssel.

## Was sie braucht

- Windows 11, x64 oder arm64. Windows 10 ist ungeprüft.
- Keine Systemfreigaben: kein Sandbox, kein Bedienungshilfen-Zugriff.
- Zugangsdaten liegen in der Windows-Anmeldeinformationsverwaltung,
  verschlüsselt mit dem Benutzerkonto und nur auf diesem Rechner. Es gibt keinen
  Server, kein Konto beim Herausgeber und keine Messung.

## Hilfe und Rückmeldung

Fragen, Probleme oder Wünsche: **[aicockpit.info](https://aicockpit.info/de/)**
— die Heimat des Projekts für alle vier Plattformen (Mac, iPhone/iPad/Apple
Watch und Windows), mit einem Rückmeldeformular. Fehler in dieser Fassung
lassen sich auch über die Issues dieses Repos melden.

## Keine Verbindung

AI-Cockpit ist ein unabhängiges Programm und steht in keiner Verbindung zu
Anthropic, OpenAI, Moonshot AI, OpenRouter, xAI, GitHub oder DeepSeek. Die genannten Namen dienen
ausschliesslich der Beschreibung, welche Dienste die App auslesen kann.
