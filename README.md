Du beschreibst das typische Problem mit zu großer Fläche bei Randbedingungen in FEFLOW:
🧠 Dein konkretes Problem:
Q schwankt ordentlich (17.000–43.000 m³/d) → ✅ gut
Aber durch Division durch A=470.000 m2A = 470.000\, \mathrm{m}^2A=470.000m2 wird:q=QA=0.036–0.091 m/dq = \frac{Q}{A} = 0.036 – 0.091\, \mathrm{m/d}q=AQ=0.036–0.091m/d
FEFLOW verteilt diesen winzigen spezifischen Fluss auf alle 470.000 m², und das:
führt zu sehr kleinen Flüssen an jedem Knoten
erschwert numerische Auswertung und Sichtbarkeit
kann sogar zu massiven Rundungsproblemen oder Glättung führen# Feflow_Flux_Issue
