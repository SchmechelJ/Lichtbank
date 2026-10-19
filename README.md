# Lichtbank

Interaktive Simulation zur Beugung und Interferenz von Licht für den Physikunterricht der Sekundarstufe II.

**Direkt im Browser öffnen:** [https://SchmechelJ.github.io/lichtbank/](https://schmechelj.github.io/Lichtbank/)

Ein Lichtbündel trifft auf ein Objekt und erzeugt ein Bild auf einem Schirm. Die Simulation zeigt dazu drei Ansichten:

- den Aufbau als Draufsicht,
- das Schirmbild, wie man es sieht,
- die gemessene Intensität je Bin als Diagramm.

Zwischen dem **Modell Lichtstrahl** und dem **Modell Lichtwelle** lässt sich jederzeit umschalten.

## Funktionen

- **Objekte:** Einzelspalt, Doppelspalt, Gitter, Kante, Hindernis (z. B. ein Haar) oder kein Objekt
- **Lichtquellen:** ein Laser mit wählbarer Wellenlänge, zwei Laser gleichzeitig oder weißes Licht
- **Einstellbar:**
  - Spaltbreite und Spaltabstand bzw. Strichzahl des Gitters
  - Strahldurchmesser
  - Abstand zum Schirm
  - Bildausschnitt
  - Anzahl der Bins
  - Belichtung des Schirmbilds
- **Messen:** Mit Maus oder Finger zeigt eine Messlinie Position x, Winkel α und Intensität an.
- **Vergleich:** Lage der Maxima bzw. Minima markieren, die Vorhersage des Strahlenmodells einblenden.
- **Geräte:** Die Seite läuft auf PC, Tablet und Smartphone.

## Einsatz im Unterricht: Freischaltungen

Über den Knopf **Freischaltungen** legt die Lehrkraft fest, welche Funktionen die Schülerinnen und Schüler nutzen dürfen. Daraus entsteht ein Link mit QR-Code, der genau diese Fassung öffnet.

1. Die Simulation so einstellen, wie sie die Schülerinnen und Schüler vorfinden sollen. Diese Einstellung ist der Startzustand.
2. Unter **Freischaltungen** auswählen, was verändert werden darf: Modelle, Objekte, Lichtquellen, einzelne Regler und Anzeigen.
3. Optional einen Auftrag eingeben. Er erscheint oben über der Simulation.
4. Mit **Vorschau der Schüleransicht** prüfen.
5. **Link erzeugen** und den Link oder den QR-Code weitergeben.

Sechs Beispielstufen sind hinterlegt. Sie führen vom Strahlenmodell am Spalt über Doppelspalt, Gitter und den Einfluss der Wellenlänge bis zum weißen Licht. Alle Stufen lassen sich anpassen.

Die gesamte Konfiguration steckt im Link. Es wird nichts gespeichert. Die Freischaltungen sind eine didaktische Hilfe, keine Zugangssperre: Wer den Teil des Links nach dem `#` entfernt, erhält die vollständige Fassung.

## Rechenmodell

- **Beleuchtung:** paralleles Lichtbündel mit gaußförmigem Profil. Spalte, Kanten und Hindernisse sind senkrecht zur Zeichenebene unendlich lang.
- **Modell Lichtwelle:**
  - Kirchhoff-Beugungsintegral mit exakter Weglänge vom Objekt zu jedem Schirmpunkt, also ohne Kleinwinkelnäherung.
  - Beim Gitter wird jede Beugungsordnung als eigenes Bündel in Richtung sin α = k·λ/g gerechnet. Die Lage auf dem Schirm ist L·tan α.
- **Modell Lichtstrahl:** geradlinige Ausbreitung. Auf dem Schirm erscheint der Teil des Bündels, der durch die Öffnungen gelangt.
- **Mehrere Wellenlängen:** Die Intensitäten werden addiert. Weißes Licht besteht aus gleich starken Anteilen von 400 nm bis 700 nm.
- **Aufbau-Schema:** Die Wellendarstellung ist schematisch. Die Wellenlänge ist darin stark vergrößert.

## Entstehung

- **Erzeugung:** Der Code wurde im Oktober 2026 mit dem KI-Modell Claude Opus 5.5 (Anthropic) erzeugt.
- **Vorgaben:** Konzept, fachliche und didaktische Vorgaben sowie Abnahme stammen vom Inhaber dieses Repositorys.
- **Fachliche Prüfung:** Die Physik wurde numerisch gegen analytische Lösungen geprüft:
  - Einzelspalt gegen das sinc²-Fernfeld
  - Kante gegen die Fresnel-Lösung
  - Lage der Gittermaxima gegen L·tan α mit sin α = k·λ/g
- **Technischer Test:** Chromium auf Desktop sowie simulierte Tablet- und Smartphone-Ansichten; dazu Safari auf iOS.

## Datenschutz

- Die Seite ist eine einzelne HTML-Datei.
- Sie setzt keine Cookies, speichert nichts im Browser, lädt nichts von anderen Servern und überträgt keine Daten.
- Schriften und Programmbibliothek sind in die Datei eingebettet.
- Beim Abruf über GitHub Pages protokolliert GitHub als Anbieter die IP-Adressen der Besucher aus Sicherheitsgründen.

## Lizenz

Die Lichtbank steht unter der **GNU General Public License v3.0**, siehe [LICENSE](LICENSE).

In `index.html` sind folgende Bestandteile Dritter eingebettet. Sie stehen unter ihren eigenen Lizenzen:

| Bestandteil | Urheber | Lizenz |
|---|---|---|
| Schrift IBM Plex Sans | Copyright 2019 IBM Corp. | SIL Open Font License 1.1, siehe [OFL.txt](OFL.txt) |
| Schrift IBM Plex Mono | Copyright 2017 IBM Corp. | SIL Open Font License 1.1, siehe [OFL.txt](OFL.txt) |
| Schrift Source Serif 4 | Copyright 2014–2021 Adobe, Reserved Font Name „Source“ | SIL Open Font License 1.1, siehe [OFL.txt](OFL.txt) |
| QR-Code-Erzeugung [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) 1.4.4 | Copyright (c) 2009 Kazuhiko Arase | MIT-Lizenz; der Lizenzhinweis steht im Quelltext von `index.html` |

„QR Code“ ist eine eingetragene Marke der DENSO WAVE INCORPORATED.
