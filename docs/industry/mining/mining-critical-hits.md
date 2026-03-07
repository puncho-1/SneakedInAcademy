# Mining Critical Hits

**Mining Critical Hits** sind eine zusätzliche Mining-Mechanik in **EVE Online**.

Wenn ein Mining-Zyklus kritisch erfolgreich ist, liefert er **mehr Ertrag als normal**.  
Ein Crit erhöht also deinen persönlichen Output, ohne einfach nur das Vorkommen schneller leer zu räumen.

Gerade weil Mining Crits oft mit Waste verwechselt werden, ist der wichtigste Grundsatz:

> Ein Crit erhöht deinen Ertrag.  
> Er ist **nicht** dasselbe wie Waste / Residue.

---

## Was ein Mining Crit bedeutet

Im normalen Fall liefert dein Mining-Modul genau den üblichen Ertrag pro Zyklus.

Bei einem **Crit** passiert zusätzlich:

- dein Zyklus läuft normal
- am Ende dieses Zyklus gibt es **zusätzlichen Bonus-Yield**
- dieser Bonus erhöht deinen persönlichen Output

Für eine einfache Erklärung kannst du dir merken:

> Ein Crit ist ein Bonus auf einen einzelnen Mining-Zyklus.

---

## Für welche Module Crits aktuell gelten

Mining Critical Hits gelten aktuell für:

- **Mining Lasers**
- **Strip Miners**
- **Ice Harvesters**

Das ist wichtig, weil Crits nicht einfach pauschal für jede Form des Resource Harvestings gleich beschrieben sind.

---

## Basiswerte von Mining Crits

Die offiziellen Startwerte sind:

- **1% Crit-Chance**
- **200% Bonus-Yield** bei einem Crit

Das bedeutet:

- ein normaler Zyklus kann mit einer kleinen Grundchance kritisch erfolgreich sein
- wenn das passiert, liefert dieser Zyklus zusätzlich **200% des normalen Zyklus-Yields** als Bonus

Anders formuliert:

- normaler Zyklus = `Y`
- Crit-Bonus = `2Y`
- Crit-Zyklus gesamt = `Y + 2Y = 3Y`

Ein Basis-Crit ergibt also insgesamt **300% des normalen Zyklus-Yields**.

---

## Skills für Mining Crits

Es gibt zwei wichtige Skills:

### Mining Precision

Dieser Skill erhöht die **Crit-Chance**.

Bonus:

- **+10% auf die Crit-Chance pro Level**

Bei einer Basis von 1% ergibt das:

- Level 1: `1.0% × 1.1 = 1.1%`
- Level 2: `1.0% × 1.2 = 1.2%`
- Level 3: `1.0% × 1.3 = 1.3%`
- Level 4: `1.0% × 1.4 = 1.4%`
- Level 5: `1.0% × 1.5 = 1.5%`

### Mining Exploitation

Dieser Skill erhöht den **Crit-Bonus-Yield**.

Bonus:

- **+5% auf den Crit-Bonus pro Level**

Bei einem Basis-Bonus von 200% ergibt das:

- Level 1: `200% × 1.05 = 210%`
- Level 2: `200% × 1.10 = 220%`
- Level 3: `200% × 1.15 = 230%`
- Level 4: `200% × 1.20 = 240%`
- Level 5: `200% × 1.25 = 250%`

Mit beiden Skills auf 5 ergibt sich also:

- **1,5% Crit-Chance**
- **250% Crit-Bonus**

Dann ist ein Crit-Zyklus insgesamt:

- `Y + 2.5Y = 3.5Y`

Also **350% des normalen Zyklus-Yields**.

---

## Warum Crits wichtig sind

Crits wirken auf den ersten Blick zufällig, sind aber über viele Zyklen hinweg ein **Durchschnittsbonus**.

Das bedeutet:

- einzelne Zyklen fallen besser aus als andere
- über längere Zeit gleicht sich das aus
- dein Durchschnittsertrag steigt

In der Praxis sind Crits also vor allem ein **langfristiger Yield-Bonus**.

---

## Einfaches Beispiel ohne Crit

Angenommen, dein Mining-Modul liefert:

- **1.000 m³ pro Zyklus**

Dann gilt:

- persönlicher Yield: **1.000 m³**
- Vorkommen verliert: **1.000 m³**

---

## Einfaches Beispiel mit Basis-Crit

Angenommen, derselbe Zyklus crittet mit dem Basis-Bonus von **200%**.

Dann gilt:

- normal: **1.000 m³**
- Crit-Bonus: **2.000 m³**
- gesamt: **3.000 m³**

Ergebnis:

- persönlicher Yield: **3.000 m³**
- das Vorkommen verliert weiterhin nur den normalen Abbauanteil, nicht zusätzlich wegen des Crits

Das ist der Kern der Mechanik:

> Der Crit erhöht deinen Output, ohne das Vorkommen durch den Crit selbst zusätzlich zu leeren.

---

## Beispiel mit maximalen Skill-Boni

Angenommen:

- normaler Yield: **1.000 m³**
- Crit-Bonus mit Skills: **250%**

Dann gilt:

- normal: **1.000 m³**
- Crit-Bonus: **2.500 m³**
- gesamt: **3.500 m³**

---

## Warum Boosts Crits wertvoller machen

**Porpoise** und **Orca** verbessern deinen normalen Yield über **Mining Foreman Bursts**.

Zusätzlich ist der **Mining Laser Efficiency Charge I** besonders relevant, weil er als Burst-Charge:

- **+50% mining critical success chance**
- **-15% mining residue chance**

als Basiswert gibt.

Das Entscheidende bleibt:

> Ein Crit wird auf deinem gebufften Grundyield berechnet.

Das heißt:

- höherer Grundyield = stärkerer Crit in absoluten Zahlen
- mehr Crit-Chance = Crits treten häufiger auf
- Boosts erhöhen also nicht nur deinen normalen Yield
- Boosts machen auch jeden einzelnen Crit wertvoller

---

## Einfaches Boost-Beispiel

### Ohne Boost

- normaler Yield: **1.000 m³**
- Basis-Crit-Bonus: **+200%**
- Crit-Zyklus: **3.000 m³**

### Mit Porpoise/Orca-Buff auf den Grundyield

Angenommen, dein Yield steigt auf:

- **1.200 m³**

Dann gilt mit Basis-Crit:

- normal: **1.200 m³**
- Crit-Bonus: **2.400 m³**
- Crit-Zyklus: **3.600 m³**

Das zeigt:

> Mehr Grundyield macht Crits absolut stärker.

---

# Für Nerds: Crits technisch

## Variablen

Wir definieren:

- `Y` = normaler Yield pro Zyklus
- `p` = Crit-Wahrscheinlichkeit pro Zyklus
- `b` = Crit-Bonus als Vielfaches des normalen Yields

Wichtig:

- Basis-Crit-Chance: `p = 0.01`
- Basis-Crit-Bonus: `b = 2.0`

---

## Erwartungswert pro Zyklus

Dann gilt als vereinfachtes Erwartungswert-Modell:

```text
E[Yield pro Zyklus] = Y × (1 + p × b)
```

### Erklärung

- ohne Crit bekommst du `Y`
- mit Wahrscheinlichkeit `p` bekommst du zusätzlich `Y × b`
- über viele Zyklen ergibt sich deshalb ein Erwartungswert von `Y × (1 + p × b)`

---

## Beispielrechnung mit Basiswerten

```text
p = 0.01
b = 2.0

E = Y × (1 + p × b)
E = Y × (1 + 0.01 × 2.0)
E = Y × 1.02
```

Das entspricht:

- **+2% durchschnittlicher Yield über Zeit**

---

## Beispielrechnung mit Skill-Maximum

Mit:

- `p = 0.015`
- `b = 2.5`

gilt:

```text
E = Y × (1 + p × b)
E = Y × (1 + 0.015 × 2.5)
E = Y × 1.0375
```

Das entspricht:

- **+3,75% durchschnittlicher Yield über Zeit**

Das erklärt auch, warum Crits sich kurzfristig oft kaum bemerkbar machen, über lange Sessions aber durchaus relevant werden.

---

## Maximalwerte mit Skills und Fleet-Boosts

Wenn man Mining Crits wirklich technisch betrachtet, sind drei Ebenen wichtig:

1. **Basiswert des Spiels**
2. **eigene Skills**
3. **Fleet-Boni durch Mining Foreman Bursts**

### Maximale Skillwerte

Mit den beiden Crit-Skills auf 5 ergibt sich:

#### Mining Precision V

```text
1.0% × 1.5 = 1.5%
```

#### Mining Exploitation V

```text
200% × 1.25 = 250%
```

Damit ist der reine Skill-Maximum-Crit:

```text
Y + 2.5Y = 3.5Y
```

also insgesamt **350% des normalen Zyklus-Yields**.

---

### Mining Laser Efficiency Charge I

Der **Mining Laser Efficiency Charge I** gibt als Basis:

- **+50% mining critical success chance**
- **-15% mining residue chance**

Diese Werte skalieren mit:

- Burst-Modul-Stärke
- Skills
- Ship-Boni
- Mindlink

---

### Maximal verifizierbare Burst-Skalierung

Für die folgenden Rechnungen wird die offiziell beschriebene Burst-Skalierung verwendet:

- **Tech 2 Command Burst Module**: `× 1.25`
- **Mining Director V**: `× 1.50`
- **Mindlink**: `× 1.25`
- **Porpoise V**: `× 1.10`
- **Orca V**: `× 1.15`

#### Porpoise V + T2 Burst + Mining Director V + Mindlink

```text
1.25 × 1.50 × 1.25 × 1.10 = 2.578125
```

Damit wird der Charge-Bonus:

```text
+50% × 2.578125 = +128.90625%
```

#### Orca V + T2 Burst + Mining Director V + Mindlink

```text
1.25 × 1.50 × 1.25 × 1.15 = 2.6953125
```

Damit wird der Charge-Bonus:

```text
+50% × 2.6953125 = +134.765625%
```

---

### Maximal verifizierbare Crit-Chance mit Burst

Jetzt kombinieren wir den Skill-Maximumwert von **1.5% Crit-Chance** mit dem Burst-Bonus.

#### Mit Porpoise-Maxburst

```text
1.5% × (1 + 1.2890625)
= 1.5% × 2.2890625
= 3.43359375%
```

#### Mit Orca-Maxburst

```text
1.5% × (1 + 1.34765625)
= 1.5% × 2.34765625
= 3.521484375%
```

### Ergebnis

Die **maximal sauber verifizierbare Crit-Chance** aus:

- Basismechanik
- Skills
- Mining Laser Efficiency Charge I
- Mining Director V
- Mindlink
- T2 Burst Module
- Porpoise/Orca Hull-Bonus

liegt also ungefähr bei:

- **3,43% mit Porpoise**
- **3,52% mit Orca**

---

## Wichtiger Hinweis zu echten Gesamt-Maxima

Zusätzlich gibt es laut offiziellen Texten auch **Mining Survey Chipsets**, die:

- Crit-Chance erhöhen
- Crit-Bonus-Yield erhöhen
- Residue-Chance senken

Da in den hier geprüften offiziellen Texten jedoch keine exakten Zahlenwerte für diese Modulvarianten genannt werden, ist das oben **nicht zwingend das absolute globale Maximum aller theoretischen Kombinationen**.

Es ist aber das **sauber verifizierbare Maximum** auf Basis der offiziell auffindbaren Skill-, Burst-, Mindlink- und Ship-Boni.

---

## Für Nerds: Erwartungswert mit max verifizierter Orca-Crit-Chance

Wenn wir die verifizierte Orca-Maxchance einsetzen:

- `p = 0.03521484375`
- `b = 2.5`

Dann:

```text
E[Yield pro Zyklus] = Y × (1 + p × b)
E = Y × (1 + 0.03521484375 × 2.5)
E = Y × 1.088037109375
```

Das entspricht ungefähr:

- **+8,80% durchschnittlicher Yield über Zeit**

Das ist ein nützlicher Näherungswert, wenn du einen stark gebufften Flotten-Miner bewerten willst.

---

## Yield pro Sekunde statt pro Zyklus

Mining vergleicht man oft besser nicht nur pro Zyklus, sondern pro Zeit.

Wir definieren:

- `Y_cycle` = Yield pro Zyklus
- `t_cycle` = Zyklusdauer in Sekunden

Dann gilt:

```text
Yield/s = Y_cycle / t_cycle
```

Mit Crit-Erwartungswert:

```text
E[Yield/s] = (Y_cycle × (1 + p × b)) / t_cycle
```

Diese Formel ist besonders nützlich, wenn du:

- verschiedene Fits vergleichen willst
- Boosts vergleichen willst
- Zykluszeit gegen Yield-Bonus abwägen willst

---

## Boosts als Multiplikatoren

Wenn Skills, Schiff, Module und Bursts deinen Yield verändern, kann man das als Multiplikatoren schreiben.

Wir definieren:

- `Y0` = Basis-Yield deines Moduls
- `m1, m2, m3 ...` = Yield-Multiplikatoren
- `t0` = Basis-Zykluszeit
- `c1, c2, c3 ...` = Zykluszeit-Multiplikatoren

Dann gilt:

```text
Y_cycle = Y0 × m1 × m2 × m3 × ...
t_cycle = t0 × c1 × c2 × c3 × ...
```

Und damit:

```text
E[Yield/s] = (Y0 × m1 × m2 × m3 × ... × (1 + p × b)) / (t0 × c1 × c2 × c3 × ...)
```

Das ist die saubere technische Gesamtsicht auf Yield inklusive Crits.

---

## Kurzfazit

**Mining Critical Hits** erhöhen deinen durchschnittlichen Ertrag über Zeit.

Sie gelten aktuell für **Mining Lasers, Strip Miners und Ice Harvesters**, starten bei **1% Crit-Chance** und **200% Bonus-Yield**, und werden durch Skills, Bursts und andere Boni verbessert.

Für Miner ist wichtig:

- Crits erhöhen deinen persönlichen Output
- Crits leeren das Vorkommen nicht zusätzlich durch den Crit selbst
- höherer Grundyield macht Crits absolut wertvoller