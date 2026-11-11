# Stark bis zum Schluss: Bayer Leverkusen 2023/24

Analyse der 34 Bundesligaspiele der Leverkusener Meistersaison in 15-Minuten-Blöcken:
Wie verändern sich Tore, Chancenqualität und Pressingintensität im Spielverlauf, und welche Rolle spielen Einwechselspieler?

<img width="1389" height="802" alt="uebersicht_kennzahlen" src="https://github.com/user-attachments/assets/1a7fb4fa-8f2c-4b25-ab94-c373fafb9d8a" />


## Kernaussagen
- **Stärkste Phase am Ende:** 22 der 86 Tore fielen ab der 75. Minute (26 %), im letzten Block liegt die Tordifferenz bei +18.
- **Verdient, nicht Glück:** Die Chancenqualität (xG pro Spiel) steigt von 0,16 in den ersten 15 Minuten auf 0,56 ab der 75. Minute.
- **Intensität gehalten:** Leverkusen lässt über 90 Minuten konstant 3,1 bis 3,2 gegnerische Pässe pro Pressing zu. Bei den Gegnern steigt der Wert von 3,4 auf bis zu 4,0, sie pressen also zunehmend weniger.
- **Joker entscheiden:** 11 der 14 Tore von Einwechselspielern fielen ab der 75. Minute.
- **Ligavergleich:** Aufsteiger Heidenheim verbesserte sich in der 2. Halbzeit von einer Tordifferenz von −13 auf +8 und wurde Achter. Aufsteiger Darmstadt brach nach der Pause weiter ein (−25 auf −31) und stieg ab.

## Kennzahlen
- **Pressing:** Laut StatsBomb jede Situation, in der ein Spieler den ballführenden Gegner auf etwa fünf Meter unter Druck setzt.
- **Pressingintensität:** Gegnerische Pässe pro eigenem Pressing, angelehnt an PPDA. Ein niedriger Wert bedeutet intensiveres Pressing. Durch das Verhältnis wird der Ballbesitz herausgerechnet.
- **xG (Expected Goals):** Die Wahrscheinlichkeit, dass ein Schuss zum Tor führt, summiert pro Block.
- **Joker-Tore:** Tore von Spielern, die im selben Spiel eingewechselt wurden.

## Grenzen
- Event-Daten zeigen, was auf dem Platz passiert, aber nicht, wie viel die Spieler laufen. Ob Fitness die Ursache ist, ließe sich nur mit Laufdaten wie High-Speed-Running und Sprints belegen.
- Die Blöcke 30-45+ und 75-90+ enthalten die Nachspielzeit und sind daher länger. Tore und xG sind dort automatisch etwas höher. Die Pressingintensität ist davon nicht betroffen, weil sie ein Verhältnis ist.
- Spielstand und Taktik beeinflussen die Werte, zum Beispiel pressen Teams im Rückstand häufiger.
- Eigentore der Gegner sind in den Toren nicht enthalten (86 statt offiziell 89).

## Methode und Daten
Python (pandas, matplotlib) in Google Colab.

Daten: [StatsBomb Open Data](https://github.com/statsbomb/open-data), Halbzeitstände für den Ligavergleich: [openfootball](https://github.com/openfootball/football.json)
