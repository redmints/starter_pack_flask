```
python3 -m venv venv
source venv/bin/activate
export DATABASE_URL="postgresql://USER:PASSWORD@24hducode.fr/DB_NAME"
python3 -m pip install -r requirements.txt
flask --app app --debug run
```

