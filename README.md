# grr-app

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
bin/console doctrine:schema:update --force
./bin/console grr:install-data
symfony server:start -d
```