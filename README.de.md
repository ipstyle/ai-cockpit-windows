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
certutil -hashfile AI-Cockpit-1.7.0-win-arm64.exe SHA256
```

Die Warnung sagt nichts über den Inhalt aus, nur über die Verbreitung, und
verschwindet von selbst, sobald die Datei oft genug heruntergeladen wurde.
Manche verwalteten Firmenrechner blockieren unsignierte Anwendungen allerdings
hart — da hilft kein Klick.

## Neu in 1.7

Die ganze Liste steht in den Release-Notizen; das Wichtigste (die Funktionen der Mac-App 7.3 und 7.4):

- **Keine Überraschungen** — eine Mitteilung, wenn ein Fenster früher als
  geplant zurückgesetzt wird, und ein Kosten-Alarm, wenn das Guthaben bei
  OpenRouter, DeepSeek oder Kimi schnell sinkt oder die Tageskosten bei
  OpenAI/Anthropic springen.
- **Abo-Check** — der API-Gegenwert deiner Claude-Code-Nutzung gegen den
  Abopreis, dazu ein Blick auf die Wochenspitzen («Max 5× würde wohl reichen»).
- **Für Entwickler** — auf Wunsch der Stand für die Statuszeile von Claude Code
  (`stand.json` + `statusline.ps1`, standardmässig aus, ohne Schlüssel und
  Kontonamen) und die Mitteilung «Claude ist fertig».
- **Klarheit** — ein Satz zur Lage oben im Panel, ein Tipp, welches Konto oder
  welcher Dienst noch Luft hat, und (i)-Knöpfe, die die Begriffe erklären.
- **Dein Aussehen** — Farbschemata Graphit (neuer Standard), Tiefblau und
  Klassisch, eine Farbe je Abo und «Als Bild teilen» ohne Kontonamen.

## Frühe Fassungen

Die aktuelle Fassung **wurde nie ausgeführt.** Sie ist auf einem Mac gebaut und
übersetzt worden; WPF läuft dort nicht. Geprüft ist, was sich ohne laufendes
Programm prüfen lässt: Die gesamte Projektmappe übersetzt samt XAML, 1506 Tests
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
