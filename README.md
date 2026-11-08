# LoxBerry-Plugin: Hue-Lox-Sync

Bidirektionale Synchronisation zwischen **Philips Hue** und **Loxone** als Plugin für **LoxBerry 4**.

Hue-Lampen (oder ganze Hue-Räume/Zonen) werden in einer Weboberfläche mit vorhandenen
Loxone-Lichtbausteinen verbunden (ColorPickerV2, Dimmer, Schalter unter einer Lichtsteuerung).
Änderungen in Loxone schalten Hue, Änderungen in der Hue-App erscheinen wieder in Loxone – ohne UDP,
virtuelle Eingänge oder neue Loxone-Objekte.

- Loxone-Zugang aus den Miniserver-Einstellungen des LoxBerry (eigene Zugangsdaten optional)
- Alarm-Mails über den Mailserver des LoxBerry (eigener SMTP-Server optional)
- Oberfläche in der LoxBerry-Plugin-Seite, geschützt durch die LoxBerry-Anmeldung
- Eigener systemd-Dienst mit Watchdog, Eintrag im LoxBerry-Healthcheck

## Voraussetzungen

- LoxBerry 4.0 oder neuer (Debian 12 oder 13)
- Internetzugang während der Installation (Node.js kommt als Debian-Paket `nodejs`)
- Philips Hue Bridge (API v2) und ein im LoxBerry eingetragener Loxone Miniserver

## Installation

1. Neueste ZIP unter [Releases](../../releases/latest) herunterladen.
2. LoxBerry → *System → Plugin-Verwaltung* → ZIP hochladen (oder „Plugin per URL installieren“ mit
   dem Link der ZIP) → SecurePIN eingeben.
3. LoxBerry → *Plugins → Hue-Lox-Sync* → Reiter *Oberfläche*: Hue Bridge koppeln, Zuordnungen anlegen.

## Updates

Neue Versionen meldet der LoxBerry selbst (über `release.cfg` in diesem Repository). Ob er nur
benachrichtigt oder Updates automatisch installiert, stellst du in der Plugin-Verwaltung ein.
Konfiguration und gelernte Stimmungen bleiben bei Updates erhalten.

## Wichtig

Pro Miniserver und Hue Bridge darf nur **eine** Hue-Lox-Sync-Instanz synchronisieren.

## Hinweise

Dieses Repository enthält nur die Plugin-Pakete; entwickelt wird in einem privaten Repository. Die
Plugin-ZIP enthält den vollständigen Quellcode (JavaScript). Lizenz: MIT (siehe `LICENSE`).
