# Vorgehen bei einer DMAV-Modelländerung

Bei einer neuen Modellversion des DMAV wird folgendes Vorgehen vorgeschlagen:

1. Für die **bisherige** Modellversion einen eigenen Branch abzweigen, damit der alte Stand dauerhaft verfügbar bleibt.
2. Den **main Branch** auf die neue Modellversion aktualisieren – main enthält immer die aktuellste Version.
3. Einen **Release** für den alten Stand / aktuellen STand auf dem jeweiligen Branch publizieren, damit fixe Versionen einfach auffindbar und herunterladbar sind.

---

## 1. Neuen Branch für die alte Modellversion erstellen

Bevor Änderungen für eine neue Version auf main eingespielt werden, wird der aktuelle Stand der alten Version als Branch gesichert.

1. Auf [github.com/geostandards-ch/DMAV-Validierungsmodell/branches](https://github.com/geostandards-ch/DMAV-Validierungsmodell/branches) auf **«New branch»** klicken.
2. Als Branch-Name den alten Versionsnamen verwenden, z. B. `DMAV_V1_0`.
3. Als Quelle **main** auswählen (oder den aktuellen Stand, bevor neue Commits eingespielt werden).
4. Branch erstellen.

Alternativ lokal via Git:

```bash
git checkout main
git pull
git checkout -b DMAV_V1_0
git push origin DMAV_V1_0
```

---

## 2. Main Branch auf neue Modellversion aktualisieren

Nach dem Abzweigen des alten Branches werden die neuen Modelle und Validierungsregeln auf main eingespielt (z. B. via Pull Request oder direkten Push).

Der main Branch enthält **immer die aktuellste Modellversion**.

---

## 3. Release für eine Modellversion erstellen

Fixe Versionsstände werden als GitHub Release publiziert, damit sie einfach auffindbar und herunterladbar sind.

1. Auf [github.com/geostandards-ch/DMAV-Validierungsmodell/releases/new](https://github.com/geostandards-ch/DMAV-Validierungsmodell/releases/new) gehen.
2. Unter **«Choose a tag»** einen neuen Tag mit der Versionsnummer erstellen, z. B. `v1.0` (Empfehlung: [Semantic Versioning](https://semver.org/)).
3. Unter **«Target»** den Branch der entsprechenden Version auswählen, z. B. `DMAV_V1_0`.
4. Als **Releasetitel** den Versionstag verwenden, z. B. `DMAV V1.0`.
5. **Release Notes** schreiben mit den wichtigsten Änderungen gegenüber der Vorgängerversion.
6. Auf **«Publish release»** klicken.

