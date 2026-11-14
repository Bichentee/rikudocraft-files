# rikudocraft-files

Fichiers lus par le launcher RikudoCraft :

- `manifest.json` : la version du mod, de Minecraft et de NeoForge, l'adresse du serveur, les actualités, la liste
  EXACTE des mods (le launcher retire tout autre .jar du dossier mods) ;
- `mods/` : les fichiers hébergés ici (RikudoCraft) ; les autres mods sont lus sur le CDN officiel de Modrinth ;
- `launcher/` : le code du launcher le plus récent (mise à jour automatique des launchers installés).

Les launchers relisent le manifeste à chaque clic sur JOUER (et toutes les 5 minutes) : tout ce qui est poussé ici
arrive chez les joueurs au prochain lancement, sans rien réinstaller.

## Publier (depuis le dossier du launcher)

```
node tools/publish.js status                        # ce qui est publié
node tools/publish.js mod <rikudocraft-X.Y.Z.jar>   # nouvelle version du mod
node tools/publish.js add modrinth:<projet>         # ajouter / mettre à jour un mod Modrinth
node tools/publish.js remove <nom>                  # retirer un mod
node tools/publish.js server <hôte:port>            # adresse du serveur
node tools/publish.js launcher                      # nouveau code du launcher (après npm run dist)
```

Puis, ici : `git add -A`, `git commit`, `git push` — c'est le push qui publie.
