# EmptyFolderCleaner

A lightweight, portable single-file Windows HTA application to safely find and delete truly empty directories — including nested empty folder trees — without risking 0-byte files or protected system folders.

No installation, no `.NET` or Python runtime, and no external dependencies required. Just double-click the `.hta` file and run.

## Features

- **Safe Empty Detection:** Checks actual file and subfolder counts instead of folder byte size (`0-byte` marker/lock files like `.gitkeep` stay safe).
- **Nested Empty Trees:** Detects parent folders that only contain empty subdirectories and deletes them safely from the inside out.
- **System & Symlink Protection:** Automatically skips junction points/symlinks (reparse points) and protected Windows directories (`Windows`, `ProgramData`, `$Recycle.Bin`, `System Volume Information`, etc.).
- **Optional Metadata Handling:** Optionally treats folders containing only `desktop.ini` or `Thumbs.db` as empty.
- **Interactive Explorer Integration:** Click any result path to open it directly in Windows Explorer, or jump to its parent directory with the folder pre-selected for manual inspection.
- **Live Filter & Single-File Transparency:** Filter large result lists in real time. Full source code in a single readable file.

## Usage

1. Download `EmptyFolderCleaner.hta`.
2. *(Optional)* If Windows SmartScreen blocks downloaded `.hta` files: Right-click the file → **Properties** → check **Unblock** (*Zulassen*) → **OK**.
3. Double-click `EmptyFolderCleaner.hta`, choose a drive or folder (local or `\\UNC` network path), and click **Scannen**.
4. Review the detected folders and click **Markierte löschen** to remove the selected entries.

## Requirements

- Windows 7 / 8 / 10 / 11 (uses built-in `mshta.exe`).

  
# EmptyFolderCleaner

Eine schlanke, portable Windows-HTA-Anwendung (bestehend aus einer einzigen Datei), mit der Sie tatsächlich leere Verzeichnisse – einschließlich ineinander verschachtelter leerer Ordnerstrukturen – sicher finden und löschen können. Dabei besteht kein Risiko, dass 0-Byte-Dateien oder geschützte Systemordner versehentlich entfernt werden.

Es ist keine Installation erforderlich; zudem werden weder eine .NET- oder Python-Laufzeitumgebung noch externe Abhängigkeiten benötigt. Einfach die `.hta`-Datei per Doppelklick starten – fertig.

## Funktionen

- **Sichere Erkennung leerer Ordner:** Die Anwendung prüft die tatsächliche Anzahl der enthaltenen Dateien und Unterordner, anstatt sich auf die Byte-Größe des Ordners zu verlassen (sogenannte 0-Byte-Platzhalterdateien wie `.gitkeep` bleiben somit erhalten).
- **Verschachtelte leere Strukturen:** Erkennt übergeordnete Ordner, die ausschließlich leere Unterverzeichnisse enthalten, und löscht diese sicher – von innen nach außen.
- **Schutz für Systemordner & Symlinks:** Verzeichnisknoten (Junction Points), symbolische Links (Symlinks) sowie geschützte Windows-Verzeichnisse (wie `Windows`, `ProgramData`, `$Recycle.Bin`, `System Volume Information` usw.) werden automatisch übersprungen.
- **Optionale Behandlung von Metadaten-Dateien:** Auf Wunsch können Ordner, die lediglich Dateien wie `desktop.ini` oder `Thumbs.db` enthalten, ebenfalls als „leer“ betrachtet und gelöscht werden.
- **Interaktive Explorer-Integration:** Klicken Sie auf einen gefundenen Pfad, um ihn direkt im Windows-Explorer zu öffnen, oder springen Sie in das übergeordnete Verzeichnis, wobei der entsprechende Ordner für eine manuelle Überprüfung bereits vorausgewählt ist.
- **Echtzeit-Filter & Transparenz:** Filtern Sie umfangreiche Ergebnislisten in Echtzeit. Der vollständige Quellcode ist in einer einzigen, gut lesbaren Datei enthalten.

## Verwendung

1. Laden Sie `EmptyFolderCleaner.hta` herunter.
2. *(Optional)* Falls Windows SmartScreen den Start der heruntergeladenen `.hta`-Datei blockiert: Rechtsklick auf die Datei → **Eigenschaften** → Option **Zulassen** (Unblock) aktivieren → **OK**.
3. Starten Sie `EmptyFolderCleaner.hta` per Doppelklick, wählen Sie ein Laufwerk oder einen Ordner aus (lokal oder als `\\UNC`-Netzwerkpfad) und klicken Sie auf **Scannen**.
4. Überprüfen Sie die gefundenen Ordner und klicken Sie auf **Markierte löschen**, um die ausgewählten Einträge zu entfernen.

## Voraussetzungen

- Windows 7 / 8 / 10 / 11 (nutzt die integrierte `mshta.exe`).
