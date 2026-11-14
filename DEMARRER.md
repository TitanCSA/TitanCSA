# Choisir un projet TitanCSA

Des outils Windows pour automatiser un navigateur, travailler avec des entrées physiques, créer des périphériques virtuels et préparer des diagnostics.

**[Tous les projets par usage](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md)** · **[Paquets SDK et commandes d’installation](https://github.com/TitanCSA/sdk-packages)** · **[English](https://github.com/TitanCSA/TitanCSA)**

## Commencer sans installer de pilote d’entrée

| Votre besoin | Projet | Premier essai |
| --- | --- | --- |
| Automatiser un navigateur dédié depuis un script ou un client MCP | [Browser Control SDK](https://github.com/TitanCSA/Browser-Control-SDK) | Extraire le ZIP Windows x64, ouvrir `BrowserControl.exe`, puis suivre l’exemple de page locale du README. Le runtime WebView2 est nécessaire. |
| Préparer un rapport de support sur les périphériques et pilotes Windows | [Driver Readiness Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector) | Ouvrir l’application, sélectionner un périphérique et exporter un rapport HTML ou JSON local. Aucun pilote supplémentaire ni déverrouillage payant. |
| Converser avec un modèle de texte local dans une interface française | [Titan Local AI](https://github.com/titanfyre/Titan-Local-AI) | Ouvrir le ZIP de distribution et choisir un modèle GGUF acquis séparément, ou un fournisseur local compatible. Les confirmations des actions sont activées par défaut. |
| Vérifier une fixture HID JSON avant de l’utiliser dans un test | [Input CI Runner](https://github.com/titanfyre/Input-CI-Runner) | Lancer la validation hors ligne. L’envoi réel des rapports est un mode distinct, avec le pilote Vdevice correspondant. |

Les trois premières applications ont leur propre licence MIT ; les composants tiers et les modèles conservent leurs conditions. L’inférence locale ne signifie pas que les téléchargements initiaux ou les pages visitées fonctionnent sans réseau.

## Choisir une entrée physique ou un périphérique virtuel

| Ce que vous voulez faire | Point de départ |
| --- | --- |
| Lire ou transformer les entrées d’un clavier ou d’une souris physique | [Interceptor Keyboard & Mouse](https://github.com/TitanCSA/Interceptor-Keyboard-Mouse) |
| Travailler avec une manette physique compatible | [Interceptor Gamepad & Controller](https://github.com/TitanCSA/Interceptor-Gamepad-Controller) |
| Réunir clavier, souris et manettes avec l’API combinée | [Interceptor](https://github.com/TitanCSA/Interceptor) |
| Créer un périphérique USB/HID virtuel avec ses descripteurs et rapports | [Vdevice](https://github.com/TitanCSA/Vdevice) |
| Utiliser AutoHotkey avec des abonnements par périphérique | [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor), adapté d’AutoHotInterception d’evilC |
| Étudier un éditeur de courbes de joystick | [Curve Controller](https://github.com/TitanCSA/Curve-Controller) |

Ces projets utilisent des éditions précises de pilote et de SDK. Choisissez leurs exemples correspondants : les éditions ne deviennent pas interchangeables en changeant seulement un nom de paquet. Les pilotes d’évaluation d’entrée ont une limite d’une heure par démarrage du noyau Windows ; la licence de l’application ou du SDK ne supprime pas cette limite. Le README décrit l’installation, les périphériques qualifiés et les conditions de la version complète.

## Explorer les autres usages

- **[Applications d’entrée et tests de périphériques](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#input-applications-and-device-qa)** : remappage, scénarios de test, scanners et inspection de manettes.
- **[Périphériques virtuels et médias](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#virtual-devices-and-media)** : caméra, écran, audio et aperçus de transport série.
- **[Réseau et accès distant](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#networking-and-remote-workflows)** : captures, connexions, émulation et transport distant.
- **[Stockage et fichiers](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#storage-and-file-workflows)** : disque virtuel, erreurs contrôlées, suivi des blocs et fichiers à la demande.
- **[Diagnostics et règles ciblées](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#system-diagnostics-and-scoped-policies)** : processus, USB, registre et observations de latence.
- **[Autres éditions d’API](https://github.com/TitanCSA/TitanCSA/blob/main/PROJECTS.md#other-api-editions-and-sdk-source-packages)** : retrouver la documentation de votre édition et les sources SDK associées.

L’index indique aussi les aperçus techniques dont la qualification en fonctionnement réel reste incomplète. Pour un premier essai, ouvrez le README du projet choisi et sa Release produit ; le dépôt central des paquets sert aux SDK et à leur documentation.

## Poser une question utile

Pour un problème reproductible, utilisez le dépôt concerné et indiquez votre version Windows, le paquet et sa version, le type de périphérique ou de connexion, les étapes et le résultat attendu. Une observation de compteur ou d’intervalle logiciel ne remplace pas une mesure matérielle de bout en bout.

Pour une intégration OEM, du support ou les conditions d’un pilote complet, mon pseudo Discord est **titancsa**. Le support commercial est facultatif pour les utilitaires MIT qui ne nécessitent pas de pilote d’évaluation.

Présentation préparée avec assistance IA à partir de la documentation des projets. Les README individuels restent la référence pour les licences, les limites et les versions disponibles.
