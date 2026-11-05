<div align="center">

<img src="bilder/banner.jpg" alt="AUN Server" width="100%">

**Ein USB-Stick, der jederzeit ein fertiges NAS installiert.**

Debian 13 · Docker · Samba · Cockpit · Ansible

[Zum Projekt](https://github.com/AUN-Homserver/homeserver) · [Download (Releases)](https://github.com/AUN-Homserver/homeserver/releases) · [Bedienung](https://github.com/AUN-Homserver/homeserver/blob/main/docs/BETRIEB.md)

</div>

---

Vom Stick booten, ein paar Fragen beantworten, fertig: Danach läuft ein Heimserver mit Dateifreigaben, Medien-Apps, Überwachung, Backup und Fernzugriff. Eingerichtet wird reproduzierbar per Ansible, das Setup lässt sich jederzeit erneut ausführen, Einstellungen lassen sich bequem im Browser ändern.

<!-- SCREENSHOTS -->

## Was drin ist

| | |
|---|---|
| 🖥️ **Verwaltung im Browser** | Cockpit mit eigener Seite **aunserver**: Erststart-Assistent, Einstellungen, Setup mit Live-Protokoll |
| 📁 **Freigaben** | Samba für Windows, Mac und Linux, auf Wunsch SMB1 für die PS2 (OPL) |
| 🎬 **Medien** | Emby und der Servarr-Stack (Prowlarr, Sonarr, Radarr, Lidarr, Bazarr, SABnzbd), abschaltbar |
| 🌐 **Netz** | Caddy mit eigenen Zertifikaten, AdGuard Home, Homepage als Startseite, Tailscale für unterwegs |
| 📊 **Überwachung** | Beszel, Scrutiny (Festplatten), Dozzle, Uptime Kuma, Meldungen per ntfy aufs Handy |
| 💾 **Backup** | Tägliches restic-Backup der Einstellungen, Wiederherstellung direkt bei der Neuinstallation |
| 🔄 **Updates** | Debian und Docker automatisch, neue App-Versionen per Meldung und einem Befehl |

## Projekte

| Repo | Beschreibung |
|---|---|
| [**homeserver**](https://github.com/AUN-Homserver/homeserver) | Installer, Ansible-Setup, App-Vorlagen und Cockpit-Seite |
| **Recommendarr** | Film- und Serienvorschläge aus der eigenen Watch-History (Kodi oder Jellyfin), Hinzufügen zu Radarr/Sonarr per Klick (Image: `ghcr.io/aun-homserver/recommendarr`) |
| **PS2GameManager** | Web-Verwaltung der PS2-/PS1-Spielebibliothek für OPL und POPStarter (Cover, Configs, Cheats) (Image: `ghcr.io/aun-homserver/ps2gamemanager`) |

## Schnellstart

1. ISO vom [neuesten Release](https://github.com/AUN-Homserver/homeserver/releases/latest) laden und auf einen USB-Stick schreiben (Rufus im DD-Modus oder `dd`)
2. Vom Stick booten und „aunserver installieren“ wählen
3. Im Browser `https://<IP>:9090` öffnen, links **aunserver** wählen und dem Assistenten folgen (oder per SSH `sudo /opt/aunserver/bin/aunserver-setup`)

Alles Weitere steht im [README des Projekts](https://github.com/AUN-Homserver/homeserver#readme).
