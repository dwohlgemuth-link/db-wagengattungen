## db-wagengattungen

Interaktive, klick- und tastaturgesteuerte Präsentation zu DB-Wagengattungen. Enthält Intro-/Outro-Video, elf Slides zu Syntax und Beispielen sowie einen Abschluss-Lock-Screen.

### Inhalt
- Startscreen mit Logo und CTA, Intro-Video, 11 Slides (Hero, Team, Syntax, Section, Grid, Analyze), Outro-Video, Lock-Screen.
- Navigation: Keyboard (Space/Enter/Right, Left), Klick rechts/links, Vollbild-Toggle mit F.

### Schnellstart
1. Öffne index.html direkt im Browser oder nutze VS Code Live Server.
2. Klicke auf den Startscreen oder den CTA, das Intro-Video läuft an und wechselt danach automatisch in die Slides.
3. Navigiere mit Space/Enter/Rechtspfeil oder Klick rechts weiter, mit Linkspfeil oder Klick links zurück. F toggelt Vollbild.

### Projektstruktur
- index.html: Enthält Styles, Daten (Slides-Array) und Logik, kein Build-Schritt nötig.
- assets/: Logos/SVGs und db-soundlogo.mp4 (Intro/Outro-Clip).

### Bedienung im Detail
- Progress-Bar am unteren Rand zeigt den Fortschritt über alle Slides.
- Letzte Slide triggert automatisch das Outro-Video und blendet anschließend den Lock-Screen ein (Navigation danach gesperrt).
- Startscreen nimmt Klicks überall an; CTA besitzt eigenen Listener.

### Anpassungen
- Slides bearbeiten: Im `slides`-Array in index.html Einträge anpassen oder neue hinzufügen. Unterstützte Typen: hero, team, syntax, section, grid, analyze.
- Farben/Branding: Design-Tokens in `:root` (DB-Rot, Schwarz, Graustufen) ändern.
- Übergänge: `--transition-layer` (Layer-Fades) und `--transition-slide` (Slide-Animation) anpassen.
- Videos: Quelle im `<source>`-Tag von `#video-player` ändern, Laufzeit bestimmt die Intro-/Outro-Dauer.

### Hinweise für Betrieb/Hosting
- Lokal genügt ein statischer Server oder file://; Videos sollten aus demselben Pfad laden.
- Für Präsentationsmodus empfiehlt sich Start im Vollbild (Taste F nach Laden drücken).
- Mediengröße klein halten, damit Intro/Outro ohne Delay starten.

### Troubleshooting
- Video startet nicht: Prüfe Pfad assets/db-soundlogo.mp4 und Browser-Autoplay-Policy (mancher Browser blockiert Autoplay ohne User-Interaktion; der Klick auf Startscreen/CTA erfüllt die Policy).
- Keine Navigation: Sicherstellen, dass Layer „App“ aktiv ist (Intro muss beendet sein). Tastaturfokus liegt auf der Seite, nicht im Browser-UI.
- Vollbild klappt nicht: Einige Browser blockieren Fullscreen außerhalb von User-Events; F direkt nach einem Klick drücken.

### Lizenz / Nutzung
Interner Präsentationsgebrauch. Alle Marken, Logos und Medien verbleiben bei den jeweiligen Rechteinhabern.
