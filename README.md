# rikudocraft-files

Fichiers lus par le launcher RikudoCraft :

- `manifest.json` : la version du mod, de Minecraft et de NeoForge, l'adresse du serveur, les actualités ;
- `mods/` : les fichiers du mod que le launcher télécharge (vérifiés par SHA-1).

Publier une version : `node tools/make-manifest.js --github-raw Bichentee/rikudocraft-files <mod.jar> --server <hôte:port>`
(dans le dépôt du launcher), copier `dist-manifest/raw/*` ici, puis commit et push.
