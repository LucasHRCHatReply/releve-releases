# Relève pour macOS

Relève vit dans la barre des menus et tient à jour toutes les apps de la collection (Pince, Jauge, Penombre, Filoir,
Glisse, Veillon, Lueur, Corolle, AutoFolderIcon…) : elle les trouve sur ce Mac, dit lesquelles sont en retard et les
met toutes à jour d'un coup. Une mise à jour n'est installée que si son empreinte est juste et si elle porte la
signature de l'éditeur ; si la nouvelle version ne démarre pas ou ne se vérifie pas, l'ancienne est remise toute seule.
Elle montre aussi les apps pas encore installées. Aucun compte, aucune télémétrie.

Ce dépôt ne contient que les versions à installer. Le code source n'est pas public.

## Ce qu'il faut

- un Mac à puce Apple (M1 ou plus récent) ;
- macOS 14 ou plus.

## Installer

Dans Terminal (Cmd + Espace, « Terminal »), une seule commande, qui installe aussi les mises à jour :

```
curl -fsSL https://raw.githubusercontent.com/LucasHRCHatReply/releve-releases/main/installer.sh | zsh
```

Le script télécharge la dernière version, vérifie l'empreinte SHA-256 du zip, l'identifiant de l'app et sa signature
(équipe Apple `JT9FY7PP7K`, `codesign --verify --deep --strict`), copie l'app dans ~/Applications, puis l'ouvre.

Autre voie : télécharger `Releve.dmg` dans les [Releases](../../releases/latest), l'ouvrir, glisser Relève sur
Applications. Le disque est signé, non notarisé : au premier lancement, clic droit sur l'app › Ouvrir.
