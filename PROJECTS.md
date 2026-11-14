# Choisir un projet Windows TitanCSA

Un guide par besoin pour **58 projets accessibles publiquement**, vérifiés le 14 novembre 2026. Chaque projet a son usage, un point de départ et une limite à connaître. Les README liés restent la référence pour la version publiée, ses licences et ses prérequis.

[English version](PROJECTS.en.md) · [Premier essai en français](DEMARRER.md) · [Paquets et commandes exactes](https://github.com/TitanCSA/sdk-packages) · [Catalogue produit](https://licences.configcsa.com/portfolio/catalog)

## Choisir son parcours

| Besoin | Projets | Accès |
| --- | ---: | --- |
| Filtrer les entrées de périphériques physiques | 7 | [Ouvrir](#entree-physique) |
| Choisir une intégration SDK | 7 | [Ouvrir](#integrations-sdk) |
| Utiliser des applications de remappage et d’automatisation | 7 | [Ouvrir](#outils-entree) |
| Tester, diagnostiquer et adapter les entrées HID | 6 | [Ouvrir](#tests-hid) |
| Simuler ou transporter des périphériques USB et série | 5 | [Ouvrir](#usb-serie) |
| Intégrer audio, vidéo et poste distant | 4 | [Ouvrir](#audio-video-distance) |
| Observer, filtrer et perturber un réseau de test | 6 | [Ouvrir](#reseau) |
| Construire un banc de stockage ou une intégration fichiers | 7 | [Ouvrir](#stockage-fichiers) |
| Diagnostiquer Windows et attribuer des décisions locales | 6 | [Ouvrir](#diagnostics-politiques) |
| Automatiser un navigateur, une IA locale ou un flux de scans | 3 | [Ouvrir](#automatisation-locale) |

## Avant de commencer

- Pour une application, extrais la release complète puis suis son README. Un paquet SDK ne remplace pas l’application ou son pilote.
- Les previews explicitement signalées permettent d’étudier une interface ou des sources ; elles ne constituent pas une fonctionnalité live prête à déployer.
- Licences des applications/SDK, licences des pilotes et droits d’évaluation peuvent différer. Vérifie les conditions propres au produit ; les démos n’ont pas toutes le même mécanisme.
- Les familles physiques et virtuelles, comme les différentes éditions d’un pilote, ne sont pas interchangeables. Les compatibilités annoncées restent limitées aux configurations documentées.

<a id="entree-physique"></a>
## Filtrer les entrées de périphériques physiques

Choisis la famille de périphériques avant de choisir un pilote. Les éditions regroupées et spécialisées ont leur propre SDK et leur propre installation ; vérifie la correspondance dans le README. Les démos documentées utilisent des droits limités par démarrage du noyau.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Interception-V2](https://github.com/TitanCSA/Interception-V2#readme) | Conserver une intégration utilisant l’API C historique Interception. | Compatibilité héritée ; utiliser le pilote et les fichiers de cette édition. |
| [Interceptor](https://github.com/TitanCSA/Interceptor#readme) | Lire ou remapper clavier, souris et manette dans une même intégration. | Édition combinée ; profils et matériels compatibles explicités dans le dépôt. |
| [Interceptor-Keyboard-Mouse](https://github.com/TitanCSA/Interceptor-Keyboard-Mouse#readme) | Travailler sur un clavier ou une souris sélectionnés. | Filtrage d’entrées physiques ; accès au pilote et sélection explicite nécessaires. |
| [Interceptor-Gamepad-Controller](https://github.com/TitanCSA/Interceptor-Gamepad-Controller#readme) | Observer et transformer les rapports d’une manette compatible. | HID, XInput/XUSB et GIP selon le matériel et les profils documentés. |
| [Windows-Input-Filter](https://github.com/titanfyre/Windows-Input-Filter#readme) | Intégrer l’édition Windows regroupant les familles d’entrée. | Consulter les exemples de cette édition ; ne pas mélanger les paquets de pilotes. |
| [Windows-Gamepad-Filter](https://github.com/titanfyre/Windows-Gamepad-Filter#readme) | Construire une intégration spécialisée manettes. | Vérifier les protocoles et la compatibilité matérielle avant un essai réel. |
| [Windows-Keyboard-Mouse-Filter](https://github.com/titanfyre/Windows-Keyboard-Mouse-Filter#readme) | Développer un filtre dédié clavier et souris. | Utiliser les exemples et l’installation correspondants à cette édition. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="integrations-sdk"></a>
## Choisir une intégration SDK

Un paquet installe les sources ou composants de son SDK ; il ne prouve pas que le pilote est installé ni que toutes les fonctions existent dans tous les wrappers. Les tableaux de chaque README distinguent les commandes disponibles des publications encore prévues.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Interceptor-MultiLang](https://github.com/TitanCSA/Interceptor-MultiLang#readme) | Intégrer Interceptor depuis plusieurs écosystèmes. | Commencer par l’exemple du wrapper choisi ; vérifier ses opérations et prérequis natifs. |
| [node-interceptor](https://github.com/TitanCSA/node-interceptor#readme) | Faire une intégration clavier/souris dans Node.js ou TypeScript. | Adaptateur spécialisé ; pilote Interceptor Keyboard & Mouse requis pour le mode réel. |
| [FyraInput](https://github.com/TitanCSA/FyraInput-SDK#readme) | Trouver les sources et paquets user-mode de FyraInput. | Le dépôt de paquets ne contient ni pilote noyau ni installateur. |
| [FyraInput-Gamepad](https://github.com/TitanCSA/FyraInput-Gamepad-SDK#readme) | Trouver les paquets de l’intégration FyraInput spécialisée manettes. | Vérifier les API de ce SDK et installer séparément ses dépendances produit. |
| [FyraInput-Keyboard-Mouse](https://github.com/TitanCSA/FyraInput-Keyboard-Mouse-SDK#readme) | Trouver les paquets FyraInput dédiés clavier et souris. | Les commandes encore prévues sont identifiées dans le README. |
| [FyraDevice](https://github.com/TitanCSA/FyraDevice-SDK#readme) | Trouver les paquets user-mode de FyraDevice. | Pilotes, activation et installateurs ne sont pas inclus dans ce dépôt de paquets. |
| [Windows-Virtual-Devices](https://github.com/titanfyre/Windows-Virtual-Devices#readme) | Créer des périphériques USB virtuels avec un SDK à descriptions brutes. | Pilote et exemples propres à cette édition ; démo et limites UdeCx documentées. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="outils-entree"></a>
## Utiliser des applications de remappage et d’automatisation

Ces projets apportent des interfaces et exemples au-dessus des pilotes d’entrée. Choisis d’abord le type d’action et la famille de périphérique ; conserve un moyen de relâcher la capture pendant les essais.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [AutoHotInterceptor](https://github.com/TitanCSA/AutoHotInterceptor#readme) | Écrire des scripts AutoHotkey ciblant un clavier ou une souris. | Adaptation du travail evilC / AutoHotInterception ; consulter les notices et versions AHK. |
| [Cronus-Interceptor](https://github.com/TitanCSA/Cronus-Interceptor#readme) | Éditer et observer des scripts GPC pour manettes sur Windows. | Projet indépendant ; consulter les diagnostics de compatibilité, sans supposer une compatibilité universelle. |
| [Curve-Controller](https://github.com/TitanCSA/Curve-Controller#readme) | Ajuster et visualiser la courbe de réponse d’un joystick. | Application basée sur Interceptor Gamepad & Controller ; choisir un matériel compatible. |
| [GamePad-Remapper](https://github.com/TitanCSA/GamePad-Remapper#readme) | Configurer le remappage d’une manette, ses scripts et macros. | Application d’exemple complète ; surveiller les entrées/sorties pendant un essai explicite. |
| [Keyboard-Mouse-Remapper](https://github.com/TitanCSA/Keyboard-Mouse-Remapper#readme) | Éditer un remappage clavier/souris, des scripts et des macros. | Application native ; le pilote d’entrée correspondant est une dépendance distincte. |
| [MouseControl](https://github.com/TitanCSA/MouseControl#readme) | Déclencher des séquences de déplacement avec des combinaisons maintenues. | Exemple d’automatisation souris ; vérifier les conditions de déclenchement et d’arrêt. |
| [Titan-Input-Tools](https://github.com/titanfyre/Titan-Input-Tools#readme) | Explorer le point d’entrée regroupant les outils d’entrée Titan. | Suivre les liens vers les composants et leurs propres guides d’installation. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="tests-hid"></a>
## Tester, diagnostiquer et adapter les entrées HID

Sépare validation hors ligne, acquisition sur un périphérique physique et création d’un périphérique virtuel. Les mesures décrivent les rapports observés ; elles ne constituent pas une certification du matériel.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Assistive-Pointer](https://github.com/titanfyre/Assistive-Pointer#readme) | Ajuster le gain, les axes et les mouvements d’une souris choisie. | Réglages par périphérique ; pilote Interceptor Keyboard & Mouse pour le mode réel. |
| [Controller-Repair-Bench](https://github.com/titanfyre/Controller-Repair-Bench#readme) | Préparer un rapport de réparation ou de QA pour une manette. | Observer axes, dérive et cadence ; exports HTML/CSV, sans remapper les boutons. |
| [HID-Access-Control](https://github.com/titanfyre/HID-Access-Control#readme) | Tester quelles applications peuvent ouvrir un contrôleur sélectionné. | Règles sur les nouvelles ouvertures ; les handles déjà ouverts conservent leurs accès. |
| [HID-Fixture-Studio](https://github.com/titanfyre/HID-Fixture-Studio#readme) | Éditer un descripteur HID et valider une fixture. | Commencer par la validation hors ligne ; Vdevice est requis pour les essais réels. |
| [Input-CI-Runner](https://github.com/titanfyre/Input-CI-Runner#readme) | Exécuter des fixtures JSON de rapports HID dans une chaîne de test. | Validation hors ligne distincte du mode réel ; une mise en file n’atteste pas la consommation par une application. |
| [Input-Replay-Lab](https://github.com/titanfyre/Input-Replay-Lab#readme) | Enregistrer une séquence locale puis la rejouer pour une QA autorisée. | Un clavier ou une souris sélectionné ; démarrage et rejeu explicites, exports JSON/CSV. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="usb-serie"></a>
## Simuler ou transporter des périphériques USB et série

Définis le contrat du périphérique et le scénario d’essai avant de le connecter. Un changement de VID/PID ne reproduit pas un firmware complet ; les rapports et endpoints restent soumis aux limites de chaque implémentation.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Vdevice](https://github.com/TitanCSA/Vdevice#readme) | Créer et contrôler des périphériques USB virtuels avec des descripteurs et rapports. | Utiliser les exemples de la famille voulue ; pilote et démo distincts du SDK user-mode. |
| [Virtual-mouse-input](https://github.com/TitanCSA/Virtual-mouse-input#readme) | Explorer une intégration spécialisée d’entrée souris virtuelle. | Consulter le contrat des rapports et les dépendances de cette édition. |
| [Serial-Device-Simulator](https://github.com/titanfyre/Serial-Device-Simulator#readme) | Étudier les modèles de simulation Modbus RTU et SCPI. | Source preview : démarrage COM live non validé, blocage observé en VM ; binaires utilisables retenus, pas de déploiement en production. |
| [Virtual-COM-Workbench](https://github.com/titanfyre/Virtual-COM-Workbench#readme) | Étudier un backend CDC ACM et des scénarios de câble série virtuel. | Source preview : aucun transfert COM réel validé, blocage observé en VM ; binaires utilisables retenus, pas de déploiement en production. |
| [USB-over-IP-SDK](https://github.com/titanfyre/USB-over-IP-SDK#readme) | Transporter une interface WinUSB sélectionnée sur une connexion chiffrée authentifiée. | Pont WinUSB borné ; ne redirige pas arbitrairement tous les périphériques ou classes USB. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="audio-video-distance"></a>
## Intégrer audio, vidéo et poste distant

Les contrats de format, de transport et de compatibilité sont propres à chaque produit. Commence par le format explicitement documenté plutôt que de supposer un périphérique multimédia universel.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Titan-Audio-Link](https://github.com/titanfyre/Titan-Audio-Link#readme) | Relier une sortie audio virtuelle à une entrée microphone virtuelle. | Format natif PCM16 stéréo 48 kHz et API flottante ; WASAPI partagé, capture exclusive non prise en charge. |
| [Virtual-Camera-SDK](https://github.com/titanfyre/Virtual-Camera-SDK#readme) | Envoyer ses propres images à une caméra virtuelle AVStream. | Contrat documenté : BGR24, 640×480, 30 images/s ; droits d’évaluation du pilote séparés. |
| [Virtual-Display-Studio](https://github.com/titanfyre/Virtual-Display-Studio#readme) | Créer un écran virtuel pour une intégration ou un banc de QA. | Le scénario documenté porte sur un écran 1080p60 ; vérifier la qualification Windows. |
| [Remote-Workstation-SDK](https://github.com/titanfyre/Remote-Workstation-SDK#readme) | Intégrer un viewer de bureau distant explicitement appairé. | Application hôte/viewer et API native ; vérifier les modes de connexion et leurs limites. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="reseau"></a>
## Observer, filtrer et perturber un réseau de test

Les événements WFP, les trames NDIS et les statistiques d’une carte virtuelle ne mesurent pas la même frontière. Garde les informations de perte, de troncature et d’attribution des règles dans tes résultats.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Connection-Trace-Studio](https://github.com/titanfyre/Connection-Trace-Studio#readme) | Corréler processus, adresses et étapes de connexion WFP. | Métadonnées du cycle de vie ; le capteur ne lit pas le contenu des paquets. |
| [Network-Emulation-SDK](https://github.com/titanfyre/Network-Emulation-SDK#readme) | Tester une application face à des défauts UDP IPv4 contrôlés. | Cibler le trafic du laboratoire ; respecter les bornes et la portée documentées. |
| [Packet-Capture-SDK](https://github.com/titanfyre/Packet-Capture-SDK#readme) | Observer des trames Ethernet IN/OUT sur un adaptateur explicite. | Captures bornées et pertes possibles ; l’envoi L2 est une opération distincte. |
| [Titan-Network-Filter](https://github.com/titanfyre/Titan-Network-Filter#readme) | Attribuer les décisions de règles locales processus/ports/CIDR. | Une décision Continue laisse agir les autres filtres Windows ; vérifier les nouveaux flux. |
| [Virtual-Network-Adapter-SDK](https://github.com/titanfyre/Virtual-Network-Adapter-SDK#readme) | Intégrer une carte réseau virtuelle à une application. | Lire le contrat des paquets, le cycle de vie et les prérequis du pilote. |
| [Remote-Device-Control](https://github.com/TitanCSA/Remote-Device-Control#readme) | Contrôler un bureau Windows distant avec un viewer et un hôte dédiés. | Sunshine et moonlight-common-c pour le transport ; Vdevice pour clavier/souris virtuels côté hôte. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="stockage-fichiers"></a>
## Construire un banc de stockage ou une intégration fichiers

Plusieurs outils ciblent volontairement un disque synthétique de laboratoire. Distingue les octets vus à la frontière d’un filtre, les intervalles logiciels et les données réellement persistées. Les previews de minifiltres restent séparées des captures réelles.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Changed-Block-Tracking-SDK](https://github.com/titanfyre/Changed-Block-Tracking-SDK#readme) | Obtenir des cartes conservatrices de blocs modifiés et des checkpoints. | Évaluation sur disque synthétique explicite ; suivre le protocole des checkpoints. |
| [Cloud-Files-SDK](https://github.com/titanfyre/Cloud-Files-SDK#readme) | Hydrater des fichiers Windows à la demande depuis un backend. | Backend en lecture seule, runtime requis et démo limitée ; vérifier le périmètre CFAPI. |
| [File-Trace-Studio](https://github.com/titanfyre/File-Trace-Studio#readme) | Explorer des diagnostics de complétion d’I/O fichiers par processus. | Preview : altitude Microsoft, signature et qualification live encore en attente dans la documentation. |
| [Storage-IO-Flight-Recorder](https://github.com/titanfyre/Storage-IO-Flight-Recorder#readme) | Observer statuts et complétions sur le disque synthétique du laboratoire. | Sélection initiale d’un disque de labo non partitionné ; aucune mesure de latence physique garantie. |
| [Titan-File-Filter](https://github.com/titanfyre/Titan-File-Filter#readme) | Explorer des règles d’audit et d’accès limitées à des dossiers. | Engineering preview : altitude, signature et validation live en attente ; aucun pilote installable ni protection de production livrés. |
| [User-Backed-Virtual-Disk-SDK](https://github.com/titanfyre/User-Backed-Virtual-Disk-SDK#readme) | Fournir une implémentation user-mode à un disque virtuel. | Contrat et cycle de vie propres au pilote ; vérifier les bornes des requêtes. |
| [Virtual-Storage-Fault-Lab](https://github.com/titanfyre/Virtual-Storage-Fault-Lab#readme) | Tester la gestion d’erreurs sur un disque RAM jetable. | Banc synthétique ; distinguer injection acceptée, résultat d’I/O et état du système de fichiers. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="diagnostics-politiques"></a>
## Diagnostiquer Windows et attribuer des décisions locales

Commence en lecture seule ou en preview quand le projet le permet. Une signature Microsoft ne garantit ni compatibilité universelle ni exhaustivité d’une collecte ; les politiques locales ne remplacent pas l’ensemble des protections Windows.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Driver-Readiness-Inspector](https://github.com/titanfyre/Driver-Readiness-Inspector#readme) | Préparer un rapport de support sur les périphériques et services de pilotes. | Lecture seule, exports HTML/JSON ; aucun pilote additionnel nécessaire pour cet utilitaire. |
| [Latency-inspector](https://github.com/TitanCSA/Latency-Inspector#readme) | Explorer des observations de timing et de charge Windows. | Lire les définitions de mesure ; ne pas confondre timestamps logiciels et latence matérielle. |
| [Process-Trace-Studio](https://github.com/titanfyre/Process-Trace-Studio#readme) | Observer des événements de processus avec leur attribution. | Vérifier la portée des événements et les conditions de collecte live. |
| [ProcessGuard-SDK](https://github.com/titanfyre/ProcessGuard-SDK#readme) | Auditer ou refuser des lancements directs appartenant à une application. | Portée limitée au client propriétaire et à ses règles ; composant d’intégration, pas un antivirus complet. |
| [RegistryGuard](https://github.com/titanfyre/RegistryGuard#readme) | Explorer des règles d’écriture sur une branche applicative du registre. | Preview : allocation d’altitude, signature et qualification live en attente ; périmètre HKLM\SOFTWARE. |
| [USB-Trace-SDK](https://github.com/titanfyre/USB-Trace-SDK#readme) | Observer des métadonnées de requêtes USB et des échantillons de payload bornés. | Un périphérique USB explicitement sélectionné ; vérifier les transferts et les limites de capture. |

[Revenir aux parcours](#choisir-son-parcours)

<a id="automatisation-locale"></a>
## Automatiser un navigateur, une IA locale ou un flux de scans

Ces trois points d’entrée servent des workflows différents : actions web explicites, modèles de texte locaux et collecte de codes depuis un scanner. Commence par le guide du produit choisi et garde ses dépendances visibles.

| Projet et documentation | Pour quel besoin ? | Premier essai et limite à connaître |
| --- | --- | --- |
| [Browser-Control-SDK](https://github.com/TitanCSA/Browser-Control-SDK#readme) | Piloter un navigateur WebView2 local depuis son application ou des outils MCP. | Navigation, inspection, formulaires et captures ; Microsoft Edge WebView2 Runtime requis. |
| [Titan-Local-AI](https://github.com/titanfyre/Titan-Local-AI#readme) | Utiliser une interface française pour des modèles de texte locaux GGUF. | Modèles acquis séparément ; outils fichiers/navigateur selon le modèle et confirmations par défaut. |
| [Scanner-Route](https://github.com/titanfyre/Scanner-Route#readme) | Valider un préfixe et exporter des scans USB HID en CSV local. | Scanner clavier US ASCII + Entrée ; pilote Interceptor Keyboard & Mouse pour le mode réel. |

[Revenir aux parcours](#choisir-son-parcours)

## Périmètre et sources

Ce guide a été préparé avec une assistance IA à partir des README publics de chaque projet. Il ne revendique pas de nouveaux tests matériels. Les états preview, dépendances et restrictions sont présentés pour aider à choisir un premier essai réaliste.

L’inventaire local comporte 62 dossiers de projets. Quatre adresses supplémentaires n’ont pas pu être ouvertes lors de la vérification et ne sont pas présentées comme publiquement disponibles ici. Les dossiers d’opérations et d’artefacts ne sont pas comptés comme projets.

Pour signaler une erreur de documentation, ouvre une issue sur le projet concerné en indiquant la version et le passage à corriger.
