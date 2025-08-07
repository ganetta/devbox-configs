# BI-Client – Azure Dev Box Konfiguration

Dieses Verzeichnis enthält die Konfigurationsdateien für die Azure Dev Box eines BI-Projekts.

## Struktur

```
BI-Client/
├── imagedefinition.yaml         # Referenziert die DSC-Konfigurationen für die Dev Box
├── bi-config.yaml               # Projektspezifische DSC-Konfiguration (Tools, Software)
```

## Funktionsweise

- **imagedefinition.yaml**  
  Definiert das Dev Box Image und verweist auf die DSC-Konfigurationen:
  - `common-config.dsc.yaml`: Zentrale Basiskonfiguration (z.B. Dev Drive, Git, Grundeinstellungen)
  - `bi-config.yaml`: Projektspezifische Software und Tools für das BI-Projekt

- **bi-config.yaml**  
  Installiert alle für das BI-Projekt benötigten Tools (z.B. Chrome, VS Code, Python, Azure CLI, etc.).

## Nutzung

1. Passe die DSC-Konfigurationsdateien nach Bedarf an.
2. Stelle sicher, dass alle referenzierten Dateien im Repository und auf GitHub verfügbar sind.
3. Verwende die `imagedefinition.yaml` zur Bereitstellung deiner Azure Dev Box.

## Hinweise

- Die Installation von Git und grundlegenden Einstellungen erfolgt zentral in der `common-config.dsc.yaml`.
- Zusätzliche projektspezifische Software wird in der `bi-config.yaml` gepflegt.
- Die URLs in der `imagedefinition.yaml` zeigen auf die Raw-Dateien dieses Repositories.

---