```
cd /c/Users/$USERPROFILE
WIN_HOME=$(cygpath -u "$USERPROFILE")
echo "export HOME=\"$WIN_HOME\"" >> ~/.bashrc
export HOME="$WIN_HOME"
mkdir .ssh
chmod 700 .ssh
ssh-keygen -f /c/Users/$USERPROFILE/.ssh/id_rsa
# Copier la clé publique sur le compte github
ssh -i /c/Users/$USERPROFILE/.ssh/id_rsa -o UserKnownHostsFile=/c/Users/$USERPROFILE/.ssh/known_hosts -T git@github.com

python3 -m venv venv
source venv/bin/activate
export DATABASE_URL="postgresql://USER:PASSWORD@24hducode.fr/DB_NAME"
python3 -m pip install -r requirements.txt
flask --app app --debug run
```

