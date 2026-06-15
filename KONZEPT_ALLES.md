# Produktkonzept: Alles. (Alles Punkt)

## 1. Produktvision
**"Alles."** ist eine intelligente, persistente Overlay-Schnittstelle, die als zentraler Ankerpunkt ("ALLES PUNKT") über dem gesamten Betriebssystem liegt. Sie dient als universeller Werkzeugkasten, der durch ein modulares **ArbeitsBOX-System** und ein mehrschichtiges **Layersystem** komplexe Systeminteraktionen (OCR, Automatisierung, Sprachsteuerung) in einer minimalistischen, cyberpunk-inspirierten Ästhetik vereinfacht.

---

## 2. Kernkonzepte

### 2.1 Der ALLES PUNKT (`.`)
Der Punkt ist nicht nur ein Icon, sondern das Interface-Prinzip. Er verkörpert die Balance zwischen maximaler Funktionalität und minimaler Ablenkung.

*   **Atomisierung (Split):** Bei Interaktion zerteilt sich der Punkt organisch in Sub-Funktionen (Module).
*   **Synthese (Group):** Inaktive oder zusammengehörige Funktionen verschmelzen wieder zu einem einzigen, ruhigen Punkt.
*   **Visuelles Feedback:** Nutzung von `view-transitions` und `cubic-bezier` Animationen für flüssige, organische Bewegungen (Cyberpunk-Stil: Cyan & Magenta).

### 2.2 Die ArbeitsBOX
Ein modulares System, in dem Funktionen wie Bausteine angeordnet werden.
*   **Modularität:** Funktionen (OCR, Player, Suche, Automation) sind unabhängige Module.
*   **Kombinatorik:** Module können per Drag & Drop verbunden werden (gestrichelte Linien).
*   **Persistenz:** Layouts der ArbeitsBOX können gespeichert und kontextabhängig geladen werden.

### 2.3 Das Layersystem
Die App arbeitet in Ebenen, die den Bildschirm kontextuell überlagern:
*   **Base Layer:** Der ALLES PUNKT und die Grundsteuerung.
*   **Interaction Layer:** Aktive Module der ArbeitsBOX.
*   **Data Layer:** Visualisierte Informationen (z.B. OCR-Ergebnisse, Benachrichtigungen).
*   **System Layer:** Direkte Interaktion mit dem OS (Accessibility Service).

---

## 3. Feature-Spezifikation

| Feature | Beschreibung | User Story |
| :--- | :--- | :--- |
| **Intelligentes Overlay** | Ein schwebender Punkt, der über allen Apps sichtbar bleibt. | "Als Power-User möchte ich jederzeit Zugriff auf meine Tools haben, ohne die aktuelle App zu verlassen." |
| **Kontextuelle OCR** | Erkennt Text und Objekte auf dem Bildschirm in Echtzeit. | "Als Rechercheur möchte ich Text aus Bildern kopieren oder direkt übersetzen können." |
| **Sprachassistenz (Claude)** | Integrierte KI-Steuerung via Sprache und Text. | "Als vielbeschäftigter Nutzer möchte ich komplexe Befehle per Sprache ausführen lassen." |
| **Modulare ArbeitsBOX** | Ein Werkzeugkasten zum freien Kombinieren von Funktionen. | "Als Designer möchte ich mir meine eigene Palette aus Tools zusammenstellen, die miteinander kommunizieren." |

---

## 4. Technische Referenz (basierend auf fooView)
*   **Kern:** `BIND_ACCESSIBILITY_SERVICE` für Bildschirm-Interaktion.
*   **UI:** `SYSTEM_ALERT_WINDOW` für das Overlay-System.
*   **KI:** Integration von Claude (Cloud-basiert) für Sprachassistenz und Logik.
*   **OCR:** Tesseract/PaddlePaddle für On-Device Erkennung.
*   **Scripting:** QuickJS für benutzerdefinierte Automatisierungen.

---

## 5. UI/UX-Details & Design
*   **Farbschema:** Cyberpunk (Cyan `#00fff7`, Magenta `#ff00c8`).
*   **Animationen:** Hochdynamisch, 0.25s Dauer, `cubic-bezier(0.19, 1, 0.22, 1)`.
*   **Gesten:** Wischen zum Splitten, Halten zum Gruppieren.

---

## 6. Nächste Schritte für Claude Code
1.  Implementierung des **Base Overlay Service** (Android).
2.  Entwicklung des **Split/Group-Animationsprototyps**.
3.  Aufbau der **ArbeitsBOX-Logik** (Drag & Drop Framework).
4.  Integration der **Claude API** für die Sprachassistenz.
