# grr-app

Installation
-------------------

```bash
git clone https://github.com/jfsenechal/grr-app.git lolo
cd lolo/
mkdir src/Grr
cd src/Grr/
git clone https://github.com/acmarche/grr-bundle.git GrrBundle
git clone https://github.com/acmarche/grr-core.git Core
```
Revenir racine dossier

```bash
composer up
vim .env.local
```

Ajouté la ligne pour la connection sql

```yaml
DATABASE_URL=mysql://user:mdp@127.0.0.1:3306/grr_esquare?serverVersion=5.7
```

```bash
bin/console doctrine:schema:update --force
./bin/console grr:install-data
symfony server:start -d
```