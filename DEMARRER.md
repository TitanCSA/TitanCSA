# Choisir un projet TitanCSA

[Chercher un projet](https://titancsa.github.io/fr/) · [Essayer un outil sans ajouter de pilote](https://titancsa.github.io/fr/essayer-sans-pilote/) · [Comparer les pilotes d’entrée Windows](https://titancsa.github.io/fr/pilotes-entree-windows/)

Des outils Windows pour automatiser un navigateur, travailler avec des entrées physiques, créer des périphériques virtuels et préparer des diagnostics.

> [!IMPORTANT]
> **Version sans la limite d’une heure**
>
> Ajoute **`titancsa`** sur [Discord](https://discord.com/app) et envoie le nom du projet. Le lien d’achat est communiqué en privé.

## Choisir une démo signée

| Ce que tu veux faire | Guide de premier essai |
| --- | --- |
| Lire ou modifier les actions d’un clavier, d’une souris et d’une manette | [Interceptor](https://titancsa.github.io/fr/essayer-interceptor/) |
| Distinguer plusieurs claviers ou souris | [Interceptor Keyboard & Mouse](https://titancsa.github.io/fr/tester-deux-claviers-windows/) |
| Lire ou modifier les boutons et sticks d’une manette compatible | [Interceptor Gamepad & Controller](https://titancsa.github.io/fr/remapper-manette-windows/) |
| Créer une souris, un clavier ou une manette virtuelle | [Vdevice](https://titancsa.github.io/fr/souris-usb-virtuelle-vdevice/) |
| Continuer à utiliser une application basée sur l’ancien SDK Interception | [Interception V2](https://titancsa.github.io/fr/migrer-interception-v2/) |
| Envoyer le son d’une application vers le micro virtuel d’une autre | [Titan Audio Link](https://titancsa.github.io/fr/micro-virtuel-titan-audio-link/) |

**[Tous les projets par usage](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md)** · **[Paquets SDK et commandes d’installation](https://github.com/TitanCSA/sdk-packages)** · **[English](https://github.com/TitanCSA/TitanCSA)**

## Commencer sans installer de pilote d’entrée

| Votre besoin | Projet | Premier essai |
| --- | --- | --- |
| Automatiser un navigateur dédié depuis un script ou un client MCP | [Browser Control SDK](https://github.com/TitanCSA/Browser-Control-SDK) | Extraire le ZIP Windows x64, ouvrir `BrowserControl.exe`, puis suivre l’exemple de page locale du README. Le runtime WebView2 est nécessaire. |
| Préparer un rapport de support sur les périphériques et pilotes Windows | [Driver Readiness Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector) | Ouvrir l’application, sélectionner un périphérique et exporter un rapport HTML ou JSON local. Aucun pilote supplémentaire ni déverrouillage payant. |
| Converser avec un modèle de texte local dans une interface française | [Titan Local AI](https://github.com/titanfyre/Titan-Local-AI) | Ouvrir le ZIP de distribution et choisir un modèle GGUF acquis séparément, ou un fournisseur local compatible. Les confirmations des actions sont activées par défaut. |
| Vérifier une fixture HID JSON avant de l’utiliser dans un test | [Input CI Runner](https://github.com/titanfyre/Input-CI-Runner) | Lancer la validation hors ligne. L’envoi réel des rapports est un mode distinct, avec le pilote Vdevice correspondant. |

Les trois premières applications ont leur propre licence MIT ; les composants tiers et les modèles conservent leurs conditions. L’inférence locale ne signifie pas que les téléchargements initiaux ou les pages visitées fonctionnent sans réseau.

## Autres outils pour les entrées Windows

| Ce que vous voulez faire | Point de départ |
| --- | --- |
| Utiliser AutoHotkey avec des abonnements par périphérique | [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor), adapté d’AutoHotInterception d’evilC |
| Étudier un éditeur de courbes de joystick | [Curve Controller](https://github.com/TitanCSA/Curve-Controller) |

Pour chaque démo signée, choisis le pilote, le SDK et les exemples de la même édition. Les démos durent une heure par démarrage du noyau Windows. Le guide de premier essai indique ce qui déclenche le compteur.

## Explorer les autres usages

- **[Applications d’entrée et tests de périphériques](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#outils-entree)** : remappage, scénarios de test, scanners et inspection de manettes.
- **[Périphériques virtuels et médias](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#usb-serie)** : caméra, écran, audio et aperçus de transport série.
- **[Réseau et accès distant](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#reseau)** : captures, connexions, émulation et transport distant.
- **[Stockage et fichiers](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#stockage-fichiers)** : disque virtuel, erreurs contrôlées, suivi des blocs et fichiers à la demande.
- **[Diagnostics et règles ciblées](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#diagnostics-politiques)** : processus, USB, registre et observations de latence.
- **[Autres éditions d’API](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#integrations-sdk)** : retrouver la documentation de votre édition et les sources SDK associées.

L’index indique aussi les aperçus techniques dont la qualification en fonctionnement réel reste incomplète. Pour un premier essai, ouvrez le README du projet choisi et sa Release produit ; le dépôt central des paquets sert aux SDK et à leur documentation.

## Poser une question utile

Pour un problème reproductible, utilisez le dépôt concerné et indiquez votre version Windows, le paquet et sa version, le type de périphérique ou de connexion, les étapes et le résultat attendu. Une observation de compteur ou d’intervalle logiciel ne remplace pas une mesure matérielle de bout en bout.

Pour une intégration OEM, du support ou les conditions d’un pilote complet, mon pseudo Discord est **titancsa**. Le support commercial est facultatif pour les utilitaires MIT qui ne nécessitent pas de pilote d’évaluation.

Présentation préparée avec assistance IA à partir de la documentation des projets. Les README individuels restent la référence pour les licences, les limites et les versions disponibles.

## Vérifier les preuves avant de choisir

[Le laboratoire public](https://titancsa.github.io/TitanCSA-Benchmarks/) conserve les mesures et les essais non validés. Les résultats décrivent les périphériques, les versions et les configurations testés. Le correctif du problème WDF-001 est inclus dans la démo signée Vdevice **1.0.6.1** et la Release signée **1.0.4.1**. Les essais d’installation et de désinstallation ont réussi sous Windows 10 et 11. [Résultats par version](https://titancsa.github.io/assets/vdevice-signed-versions-2026-11-25.json) · [Ticket résolu](https://github.com/TitanCSA/Vdevice/issues/1)
