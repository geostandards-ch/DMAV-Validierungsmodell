# DMAV Validierungsmodell
Umsetzung der offiziellen Prüfregeln zum Datenmodell der Amtlichen Vermessung (DMAV) als Validierungsmodell.

## Verzeichnisstruktur
* `models`: Datenmodelle DMAV + Validierungsmodell (`DMAV_V1_0_Validierung`)
* `rules` : Prüfregeln

## Pendenzen
* alle CONSTRAINT ohne neue Funktionen sind erfasst.
* alle CONSTRAINT die modellübergreifend sind, sind markiert mit Bemerkung " !! Kategorie: modellübergreifend" 
* Funktionen die es neu braucht sind mit "DMAV_" gekennzeichnet

## Arbeitsmethodik
Dieses Validierungsmodell bildet die Prüfregeln des offiziellen CheckDMAV der swisstopo ab. Die CheckRules von CheckDMAV bilden die Prüfregeln in Excel ab. Bei neuen Constrainst (Prüfregeln) wird die neue Liste per Mail an die registrierten Benutzer von CheckDMAV versendet und in diesem Repository unter den [rules](https://github.com/geostandards-ch/DMAV-Validierungsmodell/tree/main/rules) abgelegt. Ablauf bei neuen Constraints:

### native INTERLIS-Constraints
1. Erfasstung Failcase auf [Testbed DMAV](https://github.com/geostandards-ch/DMAV-Testsuite), der Failcase wird von Spezialistinnen und Spezialisten der amtlichen Vermessung geprüft, ob der neue Constraint rihtig verstanden wurde und der Failcase den richtigen Fehler abbildet

### nicht-native INTERLIS-Constraints
1. Notation in [Validierungsmodell](https://github.com/geostandards-ch/DMAV-Validierungsmodell/blob/main/models/DMAV_V1_0_Validierung.ili) gemäss Funktionsaufruf im Excel der CheckRules.
2. Erfasstung Failcase auf [Testbed DMAV](https://github.com/geostandards-ch/DMAV-Testsuite), der Failcase wird von Spezialistinnen und Spezialisten der amtlichen Vermessung geprüft, ob der neue Constraint rihtig verstanden wurde und der Failcase den richtigen Fehler abbildet
3. Falls nötig, Anpassung Funktionssignatur. Wenn immer möglich soll mit nativem INTERLIS oder bestehenden Funktionsmodellen gearbeitet werden. Wenn neue Funktionen zu definieren sind, sollen diese in Absprache mit den INTERLIS-Hütern abgesprochen werden, im Optimalfall in bestehende Funktionsmodelle übernommen werden.
