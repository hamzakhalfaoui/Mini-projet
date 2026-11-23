# Application Web Conteneurisée (Mini-projet 1)

Application web Flask légère répondant en HTTP sur le port `5000` avec un message d'accueil configurable par variable d'environnement.

## Image Docker Hub
- **Dépôt** : `hamza25122005/webapp-tp`
- **Tags disponibles** : `1.0.0`, `1.0.1`, `1.0` (pointe vers `1.0.1`)

## Lancement rapide depuis Docker Hub
```bash
docker run -d \
  --name webapp \
  -p 5000:5000 \
  -e APP_MESSAGE="Bonjour depuis un autre binome" \
  --memory 256m \
  --cpus 0.5 \
  hamza25122005/webapp-tp:1.0.1
```

Accès à l'application :
- Navigateur : `http://localhost:5000`
- Ligne de commande : `curl http://localhost:5000`

## Variables d'environnement
| Variable | Description | Valeur par défaut |
| :--- | :--- | :--- |
| `APP_MESSAGE` | Message affiché sur la page d'accueil | `Bonjour depuis Docker ! (v1.0.1)` |

## Construction locale (optionnel)
```bash
git clone [https://github.com/hamzakhalfaoui/Mini-projet.git](https://github.com/hamzakhalfaoui/Mini-projet.git)
cd Mini-projet
docker build -t hamza25122005/webapp-tp:1.0.1 .
```
