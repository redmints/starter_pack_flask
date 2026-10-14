# NSIN-Engine

Plateforme web officielle des 24 heures du code 2026.

## Installation d'un environnement de développement

- [ ] Installer Docker et récupérer l'image nsin-sandbox
- [ ] Cloner le dépot puis rentrer dedans

```
python3 -m venv venv
source venv/bin/activate
export DATABASE_URL="postgresql://USER:PASSWORD@24hducode.fr/DB_NAME"
export API_KEY="CLE_D_API"
export SUBMISSION_DIRECTORY="WORKDIR/nsin-engine/submissions"
python3 -m pip install -r requirements.txt
flask --app app --debug run
```

## Pour faire les migrations en BDD

```
flask --app app db migrate -m "Message de description"
flask --app app db upgrade
```
