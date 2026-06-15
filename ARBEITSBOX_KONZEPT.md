# Konzept: Die ArbeitsBOX — "Alles."

## 1. Vision & Kernkonzept
Die **ArbeitsBOX** ist das Herzstück der App "Alles.". Sie ist ein modulares, hochflexibles Interface, das die Komplexität von über 1000 Funktionen (basierend auf fooView) in ein intuitives, schichtbasiertes System übersetzt. Das Ziel ist es, die "21+ verborgenen Funktionen", die bisher zu kompliziert waren, durch eine transparente Interaktionsebene und KI-Unterstützung (Claude) jedem zugänglich zu machen.

---

## 2. Das Layer-System (Die Ebenen)

### 2.1 Der "Gläserne" Interaktions-Layer (Transparent Layer)
Dies ist eine permanente, unsichtbare Ebene über dem gesamten System.
*   **Funktion:** Sie fängt Gesten und Klicks ab, bevor sie das System erreichen (falls aktiviert).
*   **Interaktions-Modi:**
    *   **Normaler Touch:** Geht durch an das System (Pass-through).
    *   **Long Press / Force Touch:** Aktiviert den "ALLES PUNKT" oder öffnet die ArbeitsBOX.
    *   **Gesten-Shorthands:** Zeichnen von Symbolen (z.B. ein "S" für Suche) direkt auf dem Layer.
    *   **Maus-Hover (Desktop):** Zeigt kontextbezogene Informationen an, ohne zu klicken.

### 2.2 Der Funktions-Layer (Action Layer)
Hier werden die Module der ArbeitsBOX "gebastelt".
*   **Baukasten-Prinzip:** Funktionen wie OCR, Datei-Explorer, Automatisierungsskripte oder die Sprachassistenz werden als Kacheln/Module platziert.
*   **Kombinatorik:** Ein OCR-Modul kann mit einem Übersetzungs-Modul verbunden werden. Das Ergebnis fließt automatisch weiter.
*   **Splitting:** Die Box kann sich in mehrere kleine Bubbles aufteilen, die an verschiedenen Bildschirmrändern "parken".

---

## 3. Die "21+ Verborgenen Funktionen" (Power-User Integration)
Viele Funktionen von fooView sind mächtig, aber schwer zu finden. In "Alles." werden diese durch die ArbeitsBOX "atomisiert":
1.  **Regelbasierte Automatisierung:** Wenn App X startet, aktiviere Layer Y.
2.  **Globaler Clipboard-Manager:** Mit Filterfunktionen.
3.  **Netzwerk-Sniffer / API-Logger:** Für Entwickler.
4.  **Batch-Bildverarbeitung:** Direkt aus dem Overlay.
5.  **Remote-Control via WebDAV/FTP:** Integriert in den Datei-Layer.
6.  **Custom Scripting (JS):** Direkter Zugriff auf die QuickJS-Engine.
7.  *... (und weitere 15 spezialisierte System-Tools, die nun modular ansprechbar sind).*

---

## 4. Tech-Stack & Architektur

### 4.1 Android
*   **Einstellungen UI:** Vollbild-Ansicht mit Reitern (Tabs) für eine klare Trennung der Kategorien (z.B. Allgemein, Module, Interaktion, Claude, System). Dies ermöglicht eine desktopähnliche Benutzererfahrung für die Konfiguration, während die App im aktiven Betrieb auf den minimalistischen "ALLES PUNKT" reduziert bleibt.

*   **Sprache:** Kotlin / Java (für Legacy-Kompatibilität mit fooView-Architektur).
*   **Kern:** `AccessibilityService` + `MediaProjection` (für Screen Capture).
*   **UI:** Jetpack Compose für die ArbeitsBOX-Module (flexibel & performant).
*   **Engine:** QuickJS für Skripting, PaddlePaddle/Tesseract für OCR.
*   **Kommunikation:** Shizuku für Root-Funktionen ohne echten Root.

### 4.2 Windows / Linux (Desktop)
*   **Einstellungen UI:** Ebenfalls Vollbild mit Reitern, um Konsistenz über die Plattformen hinweg zu gewährleisten und eine umfassende Konfiguration zu ermöglichen.

*   **Framework:** **Electron** oder **Tauri** (Tauri bevorzugt wegen Performance und nativer Systemnähe).
*   **Sprache:** Rust (Backend) + React/TypeScript (Frontend).
*   **Overlay-Technik:** Transparent Borderless Windows mit `always-on-top` Flag.
*   **System-Integration:** `enigo` oder `robotjs` für Maus-/Tastatur-Simulation.

---

## 5. Roadmap

### Phase 1: Fundament (Monat 1-2)
*   Entwicklung des persistenten Overlay-Dienstes (Android).
*   Erstellung des transparenten Interaktions-Layers.
*   Implementierung des "ALLES PUNKT" Basis-Designs.

### Phase 2: Die ArbeitsBOX (Monat 3-4)
*   Entwicklung des modularen UI-Frameworks.
*   Integration der ersten 10 Kernfunktionen (OCR, Suche, Navigation).
*   Drag & Drop Logik für Modul-Verbindungen.

### Phase 3: Power-Features & Desktop (Monat 5-6)
*   Freischaltung der "21+ Funktionen" als Module.
*   Beta-Release der Windows/Linux Desktop-App.
*   Synchronisation der ArbeitsBOX-Layouts zwischen Geräten.

---

## 6. Bedienungsanleitung der Zukunft

1.  **Aktivierung:** Ein kurzer Wisch vom Bildschirmrand zur Mitte ruft den Punkt.
2.  **Basteln:** Ziehen Sie den Punkt in die Mitte, um die ArbeitsBOX zu öffnen. Wählen Sie "Module hinzufügen".
3.  **Kombinieren:** Verbinden Sie das "Kamera"-Modul mit dem "KI-Analyse"-Modul.
4.  **Benutzen:** Tippen Sie auf den transparenten Layer, um die aktive Kette auszuführen.
5.  **Sprache:** Sagen Sie "Claude, analysiere diesen Bereich", während Sie mit dem Finger ein Rechteck zeichnen.

---

## 7. Logo & Design-Integration
Das Logo (basierend auf der Cyberpunk-Ästhetik) wird als zentraler Ankerpunkt im "ALLES PUNKT" verwendet. Bei Interaktion pulsiert es in Cyan und Magenta und zerfällt in die einzelnen Funktionsmodule der ArbeitsBOX.

### 4.1.1 Informationsarchitektur der Einstellungen (Android & Desktop)
Um eine übersichtliche und intuitive Konfiguration zu gewährleisten, wird das Vollbild-Einstellungsfenster in logische Reiter (Tabs) unterteilt. Diese Struktur ermöglicht es dem Benutzer, schnell zu den gewünschten Einstellungen zu navigieren und die Komplexität der App effektiv zu verwalten.

| Reiter (Tab) | Beschreibung | Wichtige Einstellungsbereiche |
| :------------ | :------------ | :----------------------------- |
| **Allgemein** | Grundlegende App-Einstellungen, Erscheinungsbild und Verhaltensweisen. | Sprache, Design (Cyberpunk-Farben), Startverhalten, Benachrichtigungen, Backup & Wiederherstellung. |
| **Module** | Verwaltung der ArbeitsBOX-Module und deren Funktionen. | Aktivierung/Deaktivierung von Modulen (OCR, Dateimanager, etc.), Modul-spezifische Einstellungen, Import/Export von Modul-Konfigurationen. |
| **Interaktion** | Konfiguration des transparenten Interaktions-Layers und der Gestensteuerung. | Gesten-Definition (Wischen, Long Press, Force Touch), Maus-Interaktionen (Desktop), Feedback-Optionen (Haptik, Sound). |
| **Claude** | Einstellungen für die integrierte Sprachassistenz. | Sprachmodell-Auswahl, Aktivierungswort, Sprachausgabe (TTS), Datenschutz & Datenverarbeitung, API-Schlüssel-Verwaltung. |
| **System** | Erweiterte Systemintegrationen und Berechtigungen. | Accessibility Service-Einstellungen, Overlay-Berechtigungen, Root/Shizuku-Integration, Benachrichtigungszugriff, Energieoptimierung. |
| **Profil & Sync** | Benutzerprofil, Cloud-Synchronisation und Lizenzverwaltung. | Anmeldeinformationen, Synchronisations-Einstellungen (ArbeitsBOX-Layouts, Module), Lizenzstatus, Abonnements. |
