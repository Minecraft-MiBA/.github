# MiBA

**NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.**

MiBA is a small, free, non-commercial hobby project: a 1v1 mini-game inspired by MOBA games, played in Minecraft: Java Edition. It is developed by one individual, [@Mathyuux](https://github.com/Mathyuux), for a small group of friends. It is under development and not publicly available yet.

**Contact:** [ma.chambrion@gmail.com](mailto:ma.chambrion@gmail.com)

## What it is made of

- **MiBA Launcher**: a Windows desktop launcher that signs the player in, installs the game and joins the MiBA server.
- **A Fabric mod** (client) and **server plugins** (Paper and Velocity) that implement the game.

The source code is private for now.

## How sign-in works

MiBA Launcher is a public OAuth client registered in Microsoft Entra (application name: *MiBA Launcher*, application ID `03c7fd0d-41de-4767-8955-0e1ac7015013`).

1. The player signs in with their Microsoft account in their **system browser** (OAuth 2.0 authorization code flow with PKCE, scope `XboxLive.signin`). The launcher never sees or stores a password.
2. The launcher exchanges the result for a Minecraft access token (Xbox Live, XSTS, then the Minecraft services).
3. It checks that the account **owns Minecraft: Java Edition** before enabling the *Play* button. In released builds, authentication and the ownership check cannot be skipped.
4. The only thing kept on the device is a Microsoft refresh token, **encrypted** with the Windows secure storage.

The launcher does not redistribute Minecraft: the game files are downloaded from Mojang's official servers. The mod is distributed on its own, never bundled with a modified copy of Minecraft. Access to the MiBA server is reserved for players with a genuine, paid copy of Minecraft: Java Edition.

## Privacy

The launcher collects no analytics or telemetry. It downloads game and update files from servers run by the project, which, like any web server, can see the IP address of each request. Like any Minecraft server, the MiBA game server receives the player's Minecraft username and UUID when they connect.

## Rules we follow

This project follows the [Minecraft EULA](https://aka.ms/MinecraftEULA) and the [Minecraft Usage Guidelines](https://aka.ms/mcusageguidelines). It has no monetization and sells nothing.

---

# MiBA (version française)

**PAS UN PRODUIT MINECRAFT OFFICIEL. NON APPROUVÉ OU ASSOCIÉ À MOJANG OU MICROSOFT.**

MiBA est un petit projet de loisir, gratuit et non commercial : un mini-jeu en 1 contre 1 inspiré des jeux de type MOBA, à jouer dans Minecraft : Java Edition. Il est développé par une seule personne, [@Mathyuux](https://github.com/Mathyuux), pour un petit groupe d'amis. Il est en cours de développement et n'est pas encore accessible au public.

**Contact :** [ma.chambrion@gmail.com](mailto:ma.chambrion@gmail.com)

## De quoi il se compose

- **MiBA Launcher** : un launcher de bureau pour Windows qui connecte le joueur, installe le jeu et rejoint le serveur MiBA.
- **Un mod Fabric** (client) et des **plugins serveur** (Paper et Velocity) qui implémentent le jeu.

Le code source est privé pour l'instant.

## Fonctionnement de la connexion

MiBA Launcher est un client OAuth public enregistré dans Microsoft Entra (application *MiBA Launcher*, identifiant d'application `03c7fd0d-41de-4767-8955-0e1ac7015013`).

1. Le joueur se connecte avec son compte Microsoft dans son **navigateur système** (flux OAuth 2.0 code d'autorisation avec PKCE, scope `XboxLive.signin`). Le launcher ne voit ni ne conserve jamais de mot de passe.
2. Le launcher échange le résultat contre un jeton d'accès Minecraft (Xbox Live, XSTS, puis services Minecraft).
3. Il vérifie que le compte **possède Minecraft : Java Edition** avant d'activer le bouton *Jouer*. Dans les versions distribuées, l'authentification et cette vérification ne peuvent pas être contournées.
4. Seul un jeton de rafraîchissement Microsoft est conservé sur l'appareil, **chiffré** avec le stockage sécurisé de Windows.

Le launcher ne redistribue pas Minecraft : les fichiers du jeu sont téléchargés depuis les serveurs officiels de Mojang. Le mod est distribué seul, jamais avec une version modifiée de Minecraft. L'accès au serveur MiBA est réservé aux joueurs qui possèdent une copie légitime et payante de Minecraft : Java Edition.

## Confidentialité

Le launcher ne collecte aucune statistique ni télémétrie. Il télécharge les fichiers du mod et les mises à jour depuis des serveurs gérés par le projet, qui, comme tout serveur web, voient l'adresse IP de chaque requête. Comme tout serveur Minecraft, le serveur de jeu MiBA reçoit le pseudo et l'UUID Minecraft du joueur lorsqu'il se connecte.

## Règles respectées

Ce projet respecte le [CLUF de Minecraft](https://aka.ms/MinecraftEULA) et les [conditions d'utilisation de Minecraft](https://aka.ms/mcusageguidelines). Il n'a aucune monétisation et ne vend rien.
