# Relève pour macOS

Relève vit dans la barre des menus et tient à jour toutes les apps de la collection (Pince, Jauge, Penombre, Filoir,
Glisse, Veillon, Lueur, Corolle, AutoFolderIcon…) : elle les trouve sur ce Mac, dit lesquelles sont en retard et les
met toutes à jour d'un coup — empreinte et signature contrôlées, l'ancienne version reste en place si quoi que ce soit
échoue. Elle montre aussi les apps pas encore installées. Aucun compte, aucune télémétrie.

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
