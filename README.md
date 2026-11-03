# Agent traversée Corse — été 2027

Site statique qui affiche la veille automatique des tarifs ferry **France continentale → Corse** :

- **Aller** : départ entre le **15 et le 30 juillet 2027** (Marseille, Toulon ou Nice → Ajaccio, Bastia, Calvi, L'Île-Rousse, Propriano, Porto-Vecchio).
- **Retour** : départ de Corse entre le **15 et le 30 août 2027**.
- **2 adultes** + **Citroën Jumper L2H2 (5,41 m de long, 2,52 m de haut) tractant une remorque avec bateau de 9 m**, soit **14,4 m au total**.
- Compagnies : Corsica Ferries, Corsica Linea, La Méridionale (+ comparateurs).

Fichiers :
- `index.html` : la page (aucune dépendance, lit les fichiers de `data/`).
- `data/latest.json` : résultat de la dernière veille (`allers`, `retours`, `alertes`, `notes`).
- `data/runs/AAAA-MM-JJ.json` + `data/runs/index.json` : archive des veilles.
- `data/historique.csv` : meilleur aller-retour par jour (graphique).
- `data/historique_detail.csv` : toutes les traversées relevées.

## Publication
Activer GitHub Pages : *Settings → Pages → Deploy from a branch → `main` / root*.
Le site sera visible sur https://thurtel360-bot.github.io/agent-traversee-corse/

## Mise à jour
Chaque jour vers 7 h (Paris), la tâche planifiée met à jour `data/`, puis pousse sur `main`.
