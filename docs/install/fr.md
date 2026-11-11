# Installer VidoZavr 1.2.71

**[Русский](ru.md) | [English (US)](en.md) | [Français](fr.md) | [Deutsch](de.md) | [العربية](ar.md)**

Toutes les fonctions sont gratuites : vidéos YouTube, Shorts, chaînes, playlists,
directs, recadrage et gestion des téléchargements. Le traitement s'effectue sur votre PC.
Il faut **Windows 11 x64, Chrome 127+ et une connexion Internet pour la première
installation**. Python, Rust et Node.js ne sont pas nécessaires.
Le composant Windows relie Chrome aux outils locaux par Native Messaging :
**l'extension seule ne suffit pas**.

L'interface de l'extension est disponible en **Русский, English (US), Français, Deutsch
et العربية**. Le programme d'installation Windows reste en russe ; ses libellés sont
traduits ci-dessous.

La version 1.2.71 propose un éditeur commun aux vidéos et aux Shorts, avec brouillons enregistrés et jusqu’à huit masques minutés. L’effacement utilise l’interpolation locale de FFmpeg sur des rectangles fixes et sans rotation en SDR 8 bits. Un fond complexe peut laisser des traces. Un test de proxy réussi confirme la connexion. YouTube peut encore refuser les métadonnées avec `bot_check`. Choisissez le mode direct manuellement si nécessaire.

## Installation recommandée : neuf étapes

1. **Téléchargez [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr.exe).**
   Le ZIP de l'extension n'est pas nécessaire en plus. Utilisez la version officielle
   et comparez son [SHA-256](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/SHA256SUMS.txt).
2. **Lancez l'EXE et installez les composants Windows.** Le programme est en russe :
   **Далее = Suivant**, **Готово = Terminer**. Attendez le message **Компоненты Windows
   установлены** (« Composants Windows installés »). Les outils manquants aux versions
   fixées sont téléchargés et vérifiés ; les fichiers déjà installés et conformes
   sont réutilisés. Setup n'ouvre pas Chrome et ne vérifie pas la connexion au navigateur.
3. **Lisez la dernière page avant de la fermer.** Le champ de chemin indique le dossier
   permanent de l'extension. **Папка расширения = Dossier de l'extension** ouvre ce
   dossier ; **Инструкция = Instructions** ouvre le guide installé. Conservez le chemin
   exact pour l'étape 7.
4. **Ouvrez `chrome://extensions`** dans le profil Chrome utilisé pour YouTube.
   Saisissez cette adresse dans la barre d'adresse : c'est une page interne, pas un site web.
5. **Activez Mode développeur**, en haut à droite.
6. **Cliquez sur Charger l'extension non empaquetée.** Le sélecteur de dossiers Windows s'ouvre.
7. **Sélectionnez exactement le dossier installé `extension` de l'étape 3.**
   Accédez à ce dossier ou collez le chemin exact fourni par Setup dans le champ de
   dossier (**Папка** sous Windows en russe), puis confirmez la sélection (**Выбор папки**).
   Le fichier `manifest.json` doit se trouver directement dans ce dossier.
   Sélectionnez le dossier, pas le fichier, Téléchargements, le dossier parent de
   l'installation ou un ZIP.
8. **Vérifiez qu'une seule carte V1D0Z@VR 🦖 est activée**, en version **1.2.71**.
   En mode développeur, son ID est `bkihgeeibbodemeibfdcglojjkiepnlf`.
9. **Ouvrez le menu Extensions de Chrome, représenté par une pièce de puzzle → V1D0Z@VR.**
   Vérifiez **Téléchargeur connecté** (en russe : **Загрузчик подключён**).
   Vous pouvez épingler l'icône. La présence d'une carte ne prouve pas à elle seule
   la connexion au composant Native.

Dossier par défaut :

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

**Une installation personnalisée peut utiliser un autre chemin. Le chemin complet
affiché par Setup fait foi.** Conservez ce dossier permanent et laissez le mode
développeur activé. Si Setup est déjà fermé, retrouvez les instructions dans le menu
Démarrer ; utilisez le dossier choisi lors de l'installation, puis son sous-dossier
`extension`.

### Repérer les commandes

La capture est en **anglais** : **1 Developer mode = Mode développeur** ;
**2 Load unpacked = Charger l'extension non empaquetée**. Il s'agit d'un véritable
Chromium 149 isolé, sans fenêtre visible ; la zone inutilisée est exclue de la capture.

![Commandes anglaises numérotées 1 et 2](images/chrome-controls-en.png)

La véritable carte de l'extension montre son nom, sa version, son ID et son
interrupteur activé.

![Carte VidoZavr dans Chromium en anglais](images/extension-card-en.png)

<details>
<summary>Exemple de connexion confirmée - interface russe</summary>

**1** désigne « Загрузчик подключён », c'est-à-dire « Téléchargeur connecté ».
Cette image existante montre une véritable réponse Native dans un environnement
isolé, pas un nouveau test d'installation manuelle.

![Connexion Native vérifiée dans le menu réel](images/connected.png)

</details>

Ces images proviennent de profils jetables de **Chromium 149 sans fenêtre visible**,
pas de Chrome 156 ou d'une installation neuve de Windows. La carte sert d'illustration ;
la [vue complète d'origine](images/chrome-extensions.png) reste disponible.
Aucune capture française, page de fin de Setup ou fenêtre de sélection de dossier n'a été simulée.

## Autres options d'installation

- **ZIP autonome - [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Extension.zip)**
  Téléchargez uniquement cette archive, vérifiez son SHA-256 et extrayez tous les
  fichiers dans un dossier permanent. Lancez le fichier **Установить компоненты.exe**
  (installer les composants Windows) avec votre compte Windows habituel.
  Il installe le Native Host et les outils manquants vérifiés. Suivez ensuite les
  étapes 4 à 9 avec le dossier `extension` de l'archive, qui contient `manifest.json`.
  `Check.cmd` dans le dossier des composants vérifie les fichiers et l'enregistrement.
- **Beta/Experimental - [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Experimental.exe) :**
  tente une connexion automatique à Chrome avec la même installation Windows.
  Le mode développeur, le choix du profil ou des décisions sur les autorisations
  peuvent être nécessaires ; d'autres extensions peuvent interrompre la procédure.
  Le succès et un fonctionnement entièrement sans intervention ne sont pas garantis.
  La vérification sur une installation neuve de Windows reste incomplète.
  Consultez les [limites](EXPERIMENTAL.md).

## Sécurité et outils téléchargés

Les EXE **ne portent pas de signature Windows Authenticode**. SmartScreen peut signaler
un éditeur inconnu. Vérifiez la source officielle et l'empreinte ; en cas de doute,
annulez. Ne désactivez jamais les protections pour forcer l'installation.
Vérification facultative : `Get-FileHash .\VidoZavr.exe -Algorithm SHA256`.

Setup et l'installateur de composants du ZIP obtiennent directement auprès des fournisseurs désignés yt-dlp **2026.10.21**,
Deno **2.9.8** et FFmpeg/FFprobe **9.0.2**, dans la distribution Windows de Gyan Doshi.
Il vérifie la taille et le SHA-256. Ces EXE tiers ne sont pas inclus dans nos fichiers
à télécharger. La première installation ne peut pas se faire entièrement hors ligne.
[Composants, sources, licences et empreintes exactes](COMPONENTS.md).
**La signature Ed25519 des mises à jour de l'application est distincte de la signature
Windows de l'installateur.**

## Mettre à jour et désinstaller

**EXE standard et Experimental.** Les mises à jour signées maintiennent leur
propre dossier et attendent la fin des tâches protégées. Relancez le Setup
correspondant pour réparer. Si Chrome affiche une ancienne version, rechargez
la carte existante dans `chrome://extensions`, puis les onglets YouTube.

**Installation ZIP.** Vérifiez et extrayez séparément le nouveau ZIP officiel.
Après la fin des tâches protégées, exécutez son `Установить компоненты.exe`.
Remplacez le dossier `extension` complet au même emplacement, puis rechargez
la carte et les onglets. Les deux parties du ZIP se mettent à jour manuellement.
Pour réparer, relancez l'installateur des composants. En cas de conflit, utilisez
la procédure de l'installation existante.

Retirez les composants Windows dans **Paramètres Windows → Applications → V1D0Z@VR**.
Les médias, `native\data`, `.updates` et le dossier d'extension extrait sont conservés.
Retirez la carte Chrome manuellement si besoin. Cela peut effacer ses préférences.

## Dépannage

| Problème | Action prise en charge |
|---|---|
| Manifeste absent ou impossible à charger | Relancez Charger l'extension non empaquetée et sélectionnez exactement `extension` contenant `manifest.json`. Téléchargements, le dossier parent et le ZIP ne conviennent pas. |
| La carte existe, mais le téléchargeur est déconnecté | Vérifiez que le composant Windows est installé pour **le même utilisateur Windows**, dans le bon profil Chrome et avec le bon dossier. `Check.cmd` dans le dossier d'installation vérifie les fichiers et l'enregistrement ; le menu vérifie la connexion réelle. Relancez l'installateur correspondant à votre méthode. |
| Mode développeur désactivé | Activez-le dans le profil voulu, laissez-le actif et vérifiez que la carte existante est activée. |
| Mauvais profil ou copies en double | Identifiez le profil d'installation et le dossier permanent voulu. N'ajoutez pas une copie pour réparer la connexion ; retirer une carte peut supprimer ses préférences. |
| Mise à jour terminée, ancienne version dans Chrome | Après la fin des tâches protégées, rechargez la **carte existante** et les onglets YouTube. Ne supprimez pas les données en pause. |
| Réseau, routage VPN ou échec de téléchargement/empreinte | Vérifiez la connexion du téléchargeur, pas seulement celle de Chrome. Le routage sélectif du VPN peut leur donner des chemins différents. Réessayez la source officielle ; ne remplacez pas les fournisseurs ou les empreintes et ne désactivez pas les protections. |
| Avertissement SmartScreen | L'installateur n'est pas signé. Vérifiez sa source et son empreinte ; annulez en cas de doute. |
| Experimental bloqué par une autre extension | N'acceptez pas aveuglément des demandes sans rapport et ne désactivez pas d'autres extensions. Fermez normalement votre Setup et utilisez l'installation manuelle recommandée. |

[Autorisations et confidentialité](../../README.md#windows-warnings-permissions-and-privacy) |
[Options et langues](README.md)
