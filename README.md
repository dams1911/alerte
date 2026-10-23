# Données Alerte Radar

`lidars.json` est lu par l'appli Alerte Radar. Il est mis à jour automatiquement deux fois par semaine par une tâche planifiée
qui repère les emplacements de lidars publiés (presse régionale, sites des zones de police, listes hebdomadaires bruxelloises).

- `items` : lidars annoncés, avec `from` / `until` (au-delà de `until`, l'appli ne les annonce plus) et `source`.
- `frequent` : endroits où un lidar a déjà été placé plusieurs fois (`seen` = mois où il a été signalé).
- `lat` / `lon` peuvent être vides : l'appli convertit alors `street` + `commune` (+ `near`) en position GPS.
