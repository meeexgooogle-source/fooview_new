# Entwicklungs-Roadmap: Alles. (Alles Punkt)

## 1. Einleitung
Diese Roadmap skizziert die geplanten Entwicklungsphasen für die App "Alles.", die eine innovative Kombination aus minimalistischem UI und mächtigen Funktionen bietet. Sie umfasst die Entwicklung für Android sowie die Desktop-Versionen (Windows/Linux) und integriert die Sprachassistenz Claude.

---

## 2. Strategische Phasen
Die Entwicklung wird in mehrere aufeinander aufbauende Phasen unterteilt, um eine agile und zielgerichtete Umsetzung zu gewährleisten.

### Phase 0: Konzeption & Vorbereitung (Aktuell)
*   **Ziel:** Abschluss der Produktkonzeption, technische Machbarkeitsstudie und Setup der Entwicklungsumgebung.
*   **Dauer:** 1 Monat
*   **Meilensteine:**
    *   Vollständiges Produktkonzept (inkl. ArbeitsBOX, Layer-System, UI/UX).
    *   Definition des Tech-Stacks für Android und Desktop.
    *   Einrichtung der GitHub-Repositories und CI/CD-Pipelines.
    *   Prototyping der grundlegenden UI-Elemente (ALLES PUNKT, Split/Group-Animation).

### Phase 1: Android Core & Basis-UI (Monat 1-3)
*   **Ziel:** Implementierung des Kern-Frameworks der Android-App und der grundlegenden UI-Interaktionen.
*   **Dauer:** 3 Monate
*   **Meilensteine:**
    *   Entwicklung des persistenten `AccessibilityService` und `System Overlay`.
    *   Implementierung des "ALLES PUNKT" mit Split/Group-Animationen (Jetpack Compose).
    *   Basis-Struktur der ArbeitsBOX (Module hinzufügen, verschieben).
    *   Vollbild-Einstellungsfenster mit Reitern (Informationsarchitektur).
    *   Erste Integration von fooView-Kernfunktionen (z.B. einfache OCR, Clipboard-Manager).
    *   Interaktions-Layer mit grundlegenden Gesten (Long Press, Wischgesten).

### Phase 2: Erweiterte Android-Funktionen & Claude-Integration (Monat 4-6)
*   **Ziel:** Integration der erweiterten Funktionen, der Sprachassistenz und Optimierung der Benutzererfahrung.
*   **Dauer:** 3 Monate
*   **Meilensteine:**
    *   Vollständige Integration der "21+ verborgenen Funktionen" als ArbeitsBOX-Module.
    *   Implementierung der Claude-Sprachassistenz (on-device und Cloud-Anbindung).
    *   Erweiterung des Layersystems (z.B. Data Layer Visualisierung).
    *   Feinschliff der Gestensteuerung und Interaktions-Feedback.
    *   Beta-Testphase für Android (geschlossene Gruppe).

### Phase 3: Desktop-App & Cross-Platform Sync (Monat 7-9)
*   **Ziel:** Entwicklung der Desktop-App und Implementierung der geräteübergreifenden Synchronisation.
*   **Dauer:** 3 Monate
*   **Meilensteine:**
    *   Entwicklung der Desktop-App (Tauri/Rust) mit schwebender Kugel und Hintergrund-App.
    *   Implementierung des Desktop-Einstellungsfensters mit Reitern.
    *   Synchronisation von ArbeitsBOX-Layouts und Einstellungen über alle Geräte.
    *   Anpassung der Claude-Integration für Desktop-Umgebung.
    *   Beta-Testphase für Desktop (geschlossene Gruppe).

### Phase 4: Optimierung, Stabilität & Release (Monat 10-12)
*   **Ziel:** Performance-Optimierung, Fehlerbehebung, Sicherheitsaudits und finaler Release.
*   **Dauer:** 3 Monate
*   **Meilensteine:**
    *   Umfassende Performance-Optimierung und Ressourcenmanagement.
    *   Sicherheitsaudits und Datenschutz-Compliance-Prüfung.
    *   Erstellung von Marketingmaterialien und Dokumentation.
    *   Offizieller Release der App "Alles." für Android und Desktop.

---

## 3. Tech-Stack Zusammenfassung

| Plattform | Kernsprache(n) | UI-Framework | Overlay-Technik | KI/OCR | Scripting | System-Integration |
| :-------- | :------------- | :----------- | :-------------- | :----- | :-------- | :----------------- |
| **Android** | Kotlin/Java | Jetpack Compose | AccessibilityService, System Overlay | PaddlePaddle/Tesseract, Claude API | QuickJS | Shizuku |
| **Desktop** | Rust (Backend), TypeScript (Frontend) | Tauri (React) | Transparent Borderless Windows | Claude API | QuickJS | Enigo/RobotJS |

---

## 4. Wichtige Überlegungen
*   **Agile Entwicklung:** Die Roadmap dient als Leitfaden und wird bei Bedarf angepasst.
*   **Community-Feedback:** Frühes Einbeziehen von Beta-Testern ist entscheidend.
*   **Sicherheit & Datenschutz:** Von Anfang an in den Entwicklungsprozess integrieren.
*   **Monetarisierung:** Strategie für App Store und Sideloading definieren.

---

## 5. Nächste Schritte
*   Detaillierte Planung der ersten Sprints für Phase 1 (Android Core).
*   Erstellung von User Stories für die Kernfunktionen.
*   Beginn der Implementierung des "ALLES PUNKT" Prototyps.
