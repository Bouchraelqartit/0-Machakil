# 0machakil Cahier des charges et organisation du projet

**Version 2.0 - 26 novembre 2026 - Livraison cible en deux semaines - Bouchra, Sarra et Khalid**

0machakil est une application web citoyenne de signalement et de suivi des problèmes de l'espace public. Les habitants décrivent un problème, choisissent sa catégorie, ajoutent une photo et sa localisation, puis suivent son traitement. Les gestionnaires orientent le dossier vers le service adapté, organisent les interventions et documentent la résolution.

L'objectif est de livrer un produit fonctionnel et présentable à une collectivité, avec une démonstration complète utilisant des données fictives. Aucun partenariat institutionnel n'est actuellement établi. L'utilisation par des services municipaux sera organisée avec la collectivité qui acceptera le pilote.

# 1 Objectifs du produit

Le signalement doit être simple sur téléphone. Le citoyen peut signaler un dysfonctionnement de l'espace public sans connaître à l'avance le service compétent et sans créer obligatoirement un compte.  

Les responsables doivent disposer d'un point central pour localiser les problèmes, distinguer les doublons, affecter les interventions et conserver l'historique. Les habitants doivent pouvoir consulter les informations validées et les résultats.

**Objectifs de recette proposés :**

- Permettre à au moins quatre personnes sur cinq, découvrant le produit, de terminer un signalement en moins de deux minutes hors temps de transfert de leur photo.

- Démontrer le parcours complet de réception, vérification, affectation, intervention et résolution.

- Garantir que chaque changement de statut conserve son auteur, sa date et son motif.

- Fournir une preuve de résolution adaptée au problème : photo pour une correction matérielle, ou compte rendu documenté lorsque la photo ne permet pas de prouver le résultat.

- Livrer une installation reproductible, un environnement de démonstration et un guide d'exploitation.

Ces objectifs sont des cibles à vérifier pendant la recette.

# 2 Périmètre de la première version

## Fonctionnalités incluses

La V1 couvre une zone pilote configurable, envisagée à Aïn Sebaâ. Elle comprend un catalogue de catégories, l'orientation vers un service référent, le formulaire citoyen, la carte publique, le suivi personnel, la gestion des doublons, le tableau de bord interne, les comptes et permissions, l'affectation aux agents, les preuves de résolution, les courriels et les statistiques essentielles.

L'interface citoyenne est disponible en français et en arabe, avec une présentation adaptée au sens de lecture. L'interface interne peut être livrée en français dans cette version.

## Catégories et orientation

| Catégorie initiale | Exemples de signalements |
| --- | --- |
| Voirie et trottoirs | Trou, chaussée dégradée, trottoir abîmé |
| Éclairage public | Lampadaire éteint ou endommagé |
| Propreté et déchets | Dépôt sauvage, poubelle débordante |
| Eau et assainissement | Fuite visible, regard ou évacuation obstruée |
| Mobilier et signalisation | Banc, panneau ou équipement collectif dégradé |
| Accessibilité | Rampe inutilisable ou passage public obstrué |
| Espaces verts | Dégradation ou obstacle dans un espace vert public |
| Autre problème de l'espace public | Cas décrit par le citoyen et qualifié par le gestionnaire |

Ces catégories sont un catalogue de départ modifiable. Leur service référent est une règle de configuration à valider avec le partenaire ; une catégorie ne prouve pas à elle seule la compétence d'une collectivité ou d'un opérateur. La V1 propose un service et laisse le gestionnaire confirmer l'orientation.

## Limites et évolutions

Le déploiement dans plusieurs collectivités, une application mobile native, WhatsApp, les SMS, la classification par intelligence artificielle et l'intégration aux systèmes des opérateurs sont des évolutions distinctes. Le fonctionnement multi-catégories et l'orientation par service appartiennent dès la V1 au même parcours de signalement.

Le périmètre couvre les problèmes observables de l'espace public et des équipements collectifs. La catégorie « Autre » permet de recevoir un cas non prévu et de le qualifier avant son orientation. La première version ne constitue pas un service d'urgence ni un dispositif de règlement des litiges privés.

# 3 Utilisateurs et permissions

Les rôles du produit sont distincts des trois personnes qui développent le projet. Une même personne peut cumuler des rôles dans la démonstration.

| Rôle | Actions principales | Restrictions |
| --- | --- | --- |
| Visiteur ou citoyen | Consulter la carte publique, créer un signalement, utiliser son lien personnel et apporter un complément | Aucun accès aux coordonnées des autres citoyens ni à la gestion interne |
| Gestionnaire | Vérifier, publier, rejeter, rattacher les doublons, définir une priorité, affecter et planifier les interventions, valider les résolutions | Ne gère pas les permissions des comptes |
| Agent de terrain | Consulter les interventions affectées, déclarer le début des travaux, ajouter une note et une preuve de résolution adaptée | Accès limité aux dossiers affectés ; aucune publication publique directe |
| Administrateur | Créer ou désactiver les comptes internes, attribuer les rôles et configurer les catégories, les services et la zone pilote | Les actions sensibles sont également journalisées |

Un agent propose la clôture après avoir ajouté la preuve de résolution. Le gestionnaire valide le passage à « Résolu » et la publication des informations correspondantes. Un administrateur qui traite aussi les dossiers reçoit également le rôle de gestionnaire.

# 4 Parcours principaux

## Signaler un problème

1. Le citoyen ouvre le site et choisit « Signaler un problème ».

2. Il choisit une catégorie, photographie le problème ou sélectionne une photo existante.

3. Il confirme la position sur la carte, obtenue par géolocalisation ou placée manuellement.

4. Le site présente les signalements publics actifs de même catégorie à proximité.

5. Le citoyen peut compléter un signalement existant ou déclarer un problème distinct.

6. Après validation, il reçoit une référence et un lien personnel de suivi. Une adresse de courriel reste facultative.

La confirmation indique clairement que le dossier est reçu par l'équipe qui exploite 0machakil. La mention d'une transmission à une collectivité n'apparaît qu'après une transmission effectivement réalisée.

## Orienter et résoudre

Le gestionnaire examine la catégorie, la photo et la localisation, vérifie les doublons et décide de la publication. Il confirme le service référent, fixe la priorité et affecte le dossier. L'agent déclare le début de l'intervention puis soumet une preuve adaptée à la nature du problème. Le gestionnaire vérifie cette preuve, clôture le dossier et rend visible le résultat.

## Gérer un problème déjà signalé

Un nouveau témoignage reste enregistré avec ses photos et sa date. Si le gestionnaire confirme qu'il concerne le même problème, il le rattache au signalement principal. Son lien personnel continue de fonctionner et affiche l'évolution du dossier principal, sans exposer les informations privées des autres témoins.

# 5 Exigences fonctionnelles

## F01 Déposer un signalement

**Obligatoire.** Le formulaire contient une catégorie active, une à trois photos, une position confirmée et une description facultative de 500 caractères maximum. Pour la catégorie « Autre », une description d'au moins 20 caractères est demandée. Le nom et le numéro de téléphone ne sont pas demandés en V1. Un courriel facultatif permet de recevoir les mises à jour.

**Acceptation :** un formulaire valide crée un dossier et sa référence. Une catégorie absente ou inactive, une photo absente ou une position manquante bloque l'envoi avec un message adapté. Le bouton désactivé pendant l'envoi et une clé d'idempotence évitent deux créations lors d'une répétition de la même requête. La confirmation n'apparaît qu'après l'enregistrement effectif.

## F02 Recevoir et traiter les photos

**Obligatoire.** Les formats acceptés sont JPEG, PNG et WebP, avec une limite initiale proposée de 8 Mo par fichier et trois fichiers par envoi. La sélection d'un fichier HEIC affiche une explication et une solution de remplacement ; sa conversion native n'est pas requise dans la V1.

**Acceptation :** le serveur contrôle le format réel, le poids et la possibilité de décoder l'image. Il retire les métadonnées EXIF des fichiers conservés, produit une version d'affichage et rend les images non validées accessibles uniquement aux personnes autorisées. Un fichier refusé ne crée pas un signalement incomplet.

## F03 Localiser et contrôler la zone

**Obligatoire.** La demande de géolocalisation est déclenchée par une action de l'utilisateur. Celui-ci peut déplacer le repère et utiliser la saisie manuelle si la permission est refusée ou si la position est imprécise.

**Acceptation :** un refus de permission permet toujours de terminer le parcours. Une position hors de la zone pilote est refusée avec une explication. La zone est une configuration modifiable ; son tracé de démonstration reste à valider avec un futur partenaire.

La géolocalisation web demande un contexte sécurisé et une permission du navigateur : le déploiement utilisera HTTPS. [Référence MDN](https://developer.mozilla.org/fr/docs/Web/API/Geolocation_API).

## F04 Consulter la carte publique

**Obligatoire.** La carte affiche les dossiers vérifiés et publiés, avec une alternative sous forme de liste. Le visiteur peut filtrer par catégorie, statut et quartier configuré.

**Acceptation :** les dossiers reçus mais non vérifiés, rejetés et rattachés comme doublons ne produisent pas de points publics distincts. Une fiche publique contient la position du problème, une description modérée, les photos approuvées et l'historique public. Elle ne contient aucune adresse de courriel, note interne ou identité d'agent.

## F05 Suivre son dossier sans compte

**Obligatoire.** Après l'envoi, un lien personnel permet de retrouver la réception, le statut, les éventuelles demandes de précision et les étapes publiques de traitement.

**Acceptation :** la référence visible seule ne donne aucun accès au suivi privé. Le lien utilise un secret aléatoire d'au moins 128 bits, stocké sous forme d'empreinte côté serveur. Un secret invalide ou révoqué ne révèle pas le dossier. Si le lien est perdu, une récupération est possible seulement via un courriel préalablement vérifié ; sans courriel, le site explique que le lien doit être conservé.

## F06 Proposer et gérer les doublons

**Obligatoire.** Le site propose les dossiers publics non résolus de même catégorie dans un rayon initial de 30 mètres, réglable après les essais terrain. Le citoyen peut préciser qu'il s'agit d'un problème distinct.

**Acceptation :** la proximité ne déclenche aucune fusion automatique. Une fuite d'eau et un trottoir dégradé au même endroit restent des dossiers distincts. Le gestionnaire peut rattacher deux dossiers portant sur le même problème et annuler ce rattachement avec un motif. Les photos, les dates et les liens de suivi sont conservés. Le rattachement à soi-même, les cycles et le rattachement à un dossier déjà classé comme doublon sont refusés.

Les apports anonymes sont présentés comme des témoignages, sans les compter comme des personnes distinctes vérifiées.

## F07 Vérifier et publier les signalements

**Obligatoire.** Le gestionnaire dispose d'une file « Reçus », d'un aperçu de la localisation et des photos, ainsi que d'actions de validation, demande de précision, rejet et rattachement.

**Acceptation :** un rejet exige un motif compréhensible. Une photo contenant des éléments personnels peut être masquée et remplacée par une version préparée pour publication. Chaque changement de contenu déjà publié demande une nouvelle validation. Les notes internes restent séparées des messages au citoyen.

## F08 Organiser les interventions

**Obligatoire.** Le gestionnaire confirme la catégorie et le service référent proposé par la configuration, puis attribue une priorité, un agent actif et, si nécessaire, une date prévisionnelle. Les niveaux proposés sont faible, normale et élevée. Si le service compétent n'est pas encore identifié, le dossier reste à qualifier ; aucune transmission effective n'est annoncée.

**Acceptation :** la priorité élevée nécessite un motif. Les catégories actives et leur service suggéré sont administrables ; désactiver une catégorie ne supprime pas les anciens dossiers. Une correction de catégorie ou de service est historisée et entraîne la revue de l'affectation. Le nombre de témoignages ne fixe jamais seul la priorité. Une date prévisionnelle reste une estimation. La désactivation d'un agent oblige à traiter ses affectations en cours.

## F09 Suivre les interventions et valider la résolution

**Obligatoire.** L'agent consulte ses dossiers sur téléphone, déclare le début de l'intervention et soumet une preuve avec une note. Une photo après intervention est requise pour une correction matérielle visible, par exemple un dépôt de déchets enlevé ou un équipement réparé. Lorsque le résultat n'est pas démontrable par une photo, un compte rendu justifiant la résolution est requis. Le gestionnaire accepte ou demande une correction.

**Acceptation :** un agent ne modifie pas un dossier non affecté. Un dossier reste « En cours » tant que la preuve n'a pas été validée. Le passage à « Résolu » est impossible sans preuve conforme au type de problème. Le compte rendu de remplacement contient au moins 40 caractères et son choix est justifié. Une réouverture demande un motif et conserve les dates de résolution précédentes.

## F10 Administrer les accès internes

**Obligatoire.** Les comptes internes sont créés sur invitation ou par l'administrateur. Les agents et les gestionnaires se connectent avant toute action interne.

**Acceptation :** les contrôles de permissions existent côté serveur. Un visiteur reçoit un refus d'accès aux fonctions internes ; un agent connecté reçoit un refus sur les dossiers non affectés. Un compte désactivé perd l'accès à ses sessions actives. Les comptes de démonstration sont séparés des comptes d'exploitation.

## F11 Notifier les changements

**Obligatoire.** Le suivi par lien reste disponible sans courriel. Les citoyens qui le souhaitent vérifient leur adresse avant de recevoir les changements de statut et les demandes de précision.

**Acceptation :** les courriels de suivi sont envoyés uniquement après vérification de l'adresse et accord de notification. Une panne de messagerie ne bloque pas le traitement du dossier. Les envois sont journalisés et réessayés avec une limite ; un même événement ne produit pas plusieurs messages identiques. La désinscription fonctionne sans création de compte.

## F12 Consulter les indicateurs et exporter

**Obligatoire.** Le tableau de bord indique les dossiers reçus, actifs, résolus, rejetés et doublons sur une période choisie, avec filtres par catégorie et service. Le gestionnaire peut exporter les données utiles au traitement en CSV.

**Acceptation :** les doublons sont comptés séparément des problèmes distincts. Les délais sont calculés à partir de définitions affichées : réception vers première vérification et réception vers dernière résolution, uniquement pour les dossiers concernés. Les dossiers rouverts restent identifiables. L'export exclut les liens secrets et les coordonnées des citoyens ; il neutralise les cellules interprétables comme des formules.

## F13 Utiliser le produit sur téléphone et en deux langues

**Obligatoire.** Les parcours citoyens sont disponibles en français et en arabe avec prise en charge du sens de lecture.

**Acceptation :** formulaire, suivi, filtres et messages d'erreur restent utilisables à 360 pixels de largeur sans débordement horizontal de la page. Les champs sont étiquetés, les actions accessibles au clavier et les statuts identifiables autrement que par leur couleur. La carte possède une alternative en liste.

## F14 Présenter un environnement de démonstration

**Obligatoire.** Un jeu de données fictives permet d'essayer tous les rôles et statuts, avec un bandeau « Démonstration ».

**Acceptation :** les données, comptes et fichiers de démonstration sont séparés de ceux d'exploitation. Les courriels sont capturés dans une boîte de test. Une remise à zéro reproduit le scénario sans affecter un autre environnement.

# 6 Règles métier et cycle de traitement

| Statut actuel | Transitions autorisées | Condition |
| --- | --- | --- |
| Reçu | Vérifié, Rejeté, Doublon | Décision d'un gestionnaire et motif conservé |
| Vérifié | Planifié, En cours, Rejeté, Doublon | Affectation requise pour commencer ; motif pour rejet ou rattachement |
| Planifié | En cours, Vérifié | Agent affecté pour commencer ; motif si la planification est annulée |
| En cours | Résolu, Planifié | Résolution validée par le gestionnaire avec preuve adaptée ; motif en cas de replanification |
| Résolu | Vérifié | Réouverture décidée par le gestionnaire et motivée |
| Rejeté | Reçu | Réexamen motivé |
| Doublon | Reçu | Annulation du rattachement par un gestionnaire |

**Règles transversales :**

- Un nouveau signalement commence au statut « Reçu ».

- La publication est une décision distincte du statut ; seules les données approuvées d'un dossier admissible deviennent publiques.

- Un dossier ne peut pas être déclaré « transmis à la collectivité » sans trace de la transmission. Cette information ne constitue pas une promesse d'intervention.

- Un dossier principal résolu ne reçoit pas automatiquement un nouveau témoignage comme doublon ; un problème réapparu au même endroit peut justifier un nouveau dossier.

- Un changement de statut et son entrée d'historique sont enregistrés ensemble.

- Deux modifications concurrentes ne s'écrasent pas silencieusement : la seconde demande une actualisation.

- Un rattachement conserve les données du doublon et affiche l'évolution publique du dossier principal dans son suivi.

- La réception d'une alerte ne vaut pas vérification terrain. Le produit ne garantit pas un délai de résolution fixé par ses développeurs.

# 7 Données et confidentialité

| Élément | Informations conservées | Visibilité |
| --- | --- | --- |
| Signalement | Référence, description, catégorie, service référent, position du problème, quartier, statut, priorité, dates, publication et lien éventuel vers le principal | Version modérée publique ; détails de traitement internes |
| Photo | Clé du fichier, nature avant ou après, date et validation de publication | Privée avant validation ; version approuvée publique |
| Suivi citoyen | Empreinte du secret, courriel facultatif, vérification et préférence de notification | Accès technique restreint ; aucune présence dans l'API publique |
| Compte interne | Nom professionnel, courriel, rôle, état du compte et mot de passe protégé | Administration ; informations nécessaires affichées dans l'espace interne |
| Intervention | Agent, service, planification, début, notes et preuve de résolution | Interne ; étapes utiles publiées après validation |
| Historique | Auteur, date, action, anciens et nouveaux états, motif | Historique complet interne ; projection publique filtrée |
| Notification | Événement, destinataire, résultat et tentatives | Gestion technique restreinte |
| Zone pilote | Nom, contour et quartiers configurés | Contour et libellés utiles publics |
| Catégorie et service | Code stable, libellés français et arabe, état actif et service suggéré | Catégories publiques ; configuration et gestion internes |

Le produit collecte la position du problème, sans suivre les déplacements du citoyen. Il retire les métadonnées des photos et sépare les coordonnées privées des données publiques. Les journaux ne doivent contenir ni secret de suivi ni mot de passe.

**Proposition de conservation à arbitrer avant exploitation :** suppression du courriel et invalidation du lien personnel douze mois après la dernière clôture ; historique opérationnel et statistiques conservés sous une forme permettant d'évaluer le service ; journaux de sécurité conservés trente jours. Toute réouverture remet à jour l'échéance du suivi.

Les durées définitives, le responsable de traitement, les modalités de demande de suppression et les conditions de transfert à un partenaire seront fixés avant l'ouverture à des signalements réels. La notice de confidentialité doit correspondre aux choix retenus.

# 8 Architecture technique proposée

Le socle proposé tient compte des compétences Java, Spring et React déjà mobilisées par l'équipe. Les versions exactes seront fixées au démarrage et inscrites dans le dépôt.

| Partie | Proposition | Rôle |
| --- | --- | --- |
| Interface | React avec TypeScript | Parcours citoyens et espace de gestion responsive |
| Serveur | Java et Spring Boot | API REST, validation, permissions et règles métier |
| Données | PostgreSQL ; extension géographique si nécessaire | Persistance et recherche de proximité |
| Fichiers | Stockage objet ou volume persistant protégé, derrière une abstraction | Photos et versions publiables |
| Sécurité | Spring Security et sessions sécurisées | Authentification interne et autorisations |
| Migrations | Flyway | Évolution reproductible du schéma |
| Carte | Leaflet et fournisseur de fonds de carte interchangeable | Affichage des positions |
| Notifications | Adaptateur de messagerie et file persistante d'envois | Envoi et reprise après échec |
| Livraison | Docker Compose et intégration continue | Installation, vérifications et déploiement |

L'application sera un monolithe organisé en modules fonctionnels : signalements, interventions, accès, notifications et reporting. Chaque module conserve une séparation entre API, services et persistance. Les microservices ne sont pas nécessaires au périmètre V1.

Une session interne utilise des cookies sécurisés et une protection CSRF. Les permissions sont vérifiées côté serveur ; elles ne reposent pas sur l'affichage des boutons.

Le choix de la version Spring et du JDK doit respecter leur matrice officielle de compatibilité. [Documentation Spring Boot](https://docs.spring.io/spring-boot/system-requirements.html).

Le fournisseur cartographique est un choix d'exploitation : les serveurs de tuiles publics OpenStreetMap ont une capacité limitée et ne fournissent pas de garantie de disponibilité. Le produit doit afficher l'attribution et permettre de changer de fournisseur par configuration. [Politique officielle des tuiles OpenStreetMap](https://operations.osmfoundation.org/policies/tiles/).

# 9 Qualité et exploitation

## Fiabilité et sécurité

Les validations du formulaire sont répétées côté serveur. Les fichiers sont conservés hors des emplacements exécutables. Les erreurs ne révèlent pas de détails techniques au citoyen.

Les soumissions et tentatives de connexion disposent de limitations configurables. Une protection contre les soumissions automatisées peut être déclenchée en cas d'abus. Les mécanismes doivent tenir compte des utilisateurs partageant une connexion ; un témoignage anonyme reste non vérifié.

Les secrets d'exploitation restent dans la configuration de l'environnement. Les environnements de démonstration et d'exploitation disposent de bases, de comptes et de stockages séparés.

## Performances proposées pour la recette

Sur un environnement de référence documenté, avec 5 000 dossiers et 20 utilisateurs simultanés, 95 % des lectures API ordinaires doivent répondre en moins d'une seconde, hors transfert de photos et services externes. Les listes sont paginées, la carte charge les dossiers de la zone visible et les photos utilisent des versions adaptées à l'écran.

Ces valeurs sont des objectifs à mesurer, pas des résultats déjà obtenus. Une panne du fond de carte laisse un message explicite et permet de consulter la liste des dossiers.

## Sauvegarde et maintenance

Une sauvegarde quotidienne de la base et des photos est prévue, avec une rétention initiale proposée de sept jours. Un exercice de restauration doit être réalisé avant la livraison. L'objectif proposé est de pouvoir revenir à la dernière sauvegarde quotidienne et rétablir le service en moins de quatre heures sur l'infrastructure retenue.

Le guide d'exploitation décrit les sauvegardes, la restauration, la création des comptes, les mises à jour et la consultation des erreurs. Les coûts de serveur, stockage, domaine, courriel et cartographie feront l'objet d'un budget une fois les fournisseurs choisis.

# 10 Écrans à réaliser

| Espace | Écrans |
| --- | --- |
| Public | Accueil, carte et liste, fiche publique, formulaire, confirmation, suivi personnel, aide et confidentialité |
| Gestionnaire | Connexion, tableau de bord, file de vérification, détail du dossier, gestion des doublons, planification, validation des résolutions, indicateurs et export |
| Agent | Mes interventions, détail du dossier affecté, début des travaux, dépôt de la preuve |
| Administration | Comptes, rôles, activation, catégories, services référents et zone pilote |

Les maquettes doivent couvrir les états vides, les erreurs de réseau, le refus de géolocalisation, l'envoi d'une photo et la confirmation d'une action sensible. Un citoyen doit pouvoir comprendre si son dossier est reçu, vérifié ou résolu sans connaître le fonctionnement interne.

# 11 Recette et définition du produit livrable

| Scénario | Résultat attendu |
| --- | --- |
| Créer un signalement valide sur téléphone | Une seule référence, photos persistées et lien de suivi utilisable |
| Refuser le GPS | La position manuelle permet de terminer |
| Envoyer une position hors zone ou un fichier invalide | Erreur claire et aucune création partielle visible |
| Répéter la même soumission après une interruption réseau | Le dossier initial est retrouvé sans doublon technique |
| Vérifier puis publier | Le point apparaît publiquement sans information privée |
| Rattacher puis détacher un doublon | Les preuves et les deux liens de suivi sont conservés |
| Tenter une action interne sans le bon rôle | Refus côté serveur sans modification des données |
| Résoudre un dossier affecté | Preuve déposée puis résolution après validation du gestionnaire |
| Déclarer une résolution sans preuve adaptée | Action refusée |
| Rouvrir un dossier résolu | Motif et résolutions précédentes conservés |
| Modifier simultanément le même dossier | Une modification périmée est signalée explicitement |
| Interrompre le service de messagerie | Traitement conservé et envoi réessayé sans message en double |
| Utiliser les parcours en français et en arabe | Formulaire et suivi fonctionnels, sens de lecture correct |
| Restaurer la sauvegarde | Dossiers et photos cohérents sur un environnement propre |
| Réinitialiser la démonstration | Seules les données de démonstration sont remplacées |
| Signaler une panne d'éclairage, un dépôt de déchets ou une fuite d'eau | Le même parcours fonctionne avec la bonne catégorie et le service suggéré |
| Chercher les doublons d'une autre catégorie au même endroit | Aucun rattachement automatique entre problèmes distincts |
| Désactiver une catégorie déjà utilisée | Les anciens dossiers et leur historique restent consultables |

**La V1 est livrable lorsque :**

- Les scénarios critiques de recette passent et aucun défaut bloquant n'est ouvert.

- Les contrôles de permissions, transitions, doublons et conservation des preuves ont des tests pertinents.

- L'installation depuis le dépôt fonctionne avec les instructions fournies.

- L'API, la configuration et les procédures d'exploitation sont documentées.

- Les guides citoyen et gestionnaire, le scénario de démonstration et les identifiants de test sont disponibles.

- Le parcours de démonstration couvre le processus complet avec une connexion réseau et un stockage réels de test.

- La présentation commerciale distingue les fonctionnalités disponibles et les conditions d'une adoption municipale.

# 12 Organisation de l'équipe de trois collaborateurs

L'équipe réunit **Bouchra, Sarra et Khalid**, tous trois développeurs full-stack. La répartition ci-dessous est proposée pour identifier un référent par domaine et organiser une relecture croisée. Les disponibilités restent à préciser avant les affectations dans Jira.

| Collaborateur | Référent principal | Contributions et relecture |
| --- | --- | --- |
| Bouchra | Parcours citoyen, catégories, photos et localisation | Interface et API de signalement ; relecture des parcours publics de Sarra |
| Sarra | Carte, suivi et notifications | Interface et API de consultation ; relecture des fonctions de gestion de Khalid |
| Khalid | Gestion, services référents, interventions et exploitation | Interface et API internes ; relecture des validations et accès de Bouchra |

Chacun contribue au frontend, au backend, aux tests et à la documentation de ses fonctionnalités. Les tâches de configuration, de sécurité et de livraison sont réparties au démarrage. Le rôle de référent donne un point de contact, sans réserver un module à une seule personne.

Chaque fonctionnalité passe par une branche courte, une pull request et la relecture d'un autre collaborateur. Une synchronisation courte permet de traiter les blocages ; une démonstration et une revue du périmètre ont lieu à chaque fin de sprint.

# 13 Planning cible sur deux semaines

**Objectif retenu : livrer la V1 en quatorze jours calendaires, organisés en deux sprints d'une semaine.** Les quatorze fonctionnalités F01 à F14 restent dans le périmètre. Le planning prévoit un travail en parallèle des trois collaborateurs et une intégration continue dès les premiers jours. La capacité quotidienne reste à préciser et les tickets doivent être estimés au démarrage ; la date de départ n'est pas encore fixée.

| Sprint | Objectif | Résultat démontrable |
| --- | --- | --- |
| Sprint 1, J1 à J7 | Installer le socle et intégrer le parcours citoyen multi-catégories, la carte, les accès internes et le traitement des interventions | Un signalement est créé, vérifié, affecté et suivi jusqu'à la résolution avec preuve adaptée |
| Sprint 2, J8 à J14 | Terminer les courriels, indicateurs, doublons, bilinguisme, recette et livraison | V1 complète déployée en démonstration avec guides, sauvegarde et restauration vérifiées |

## Jalons des quatorze jours

| Période | Travaux coordonnés | Validation attendue |
| --- | --- | --- |
| J1 | Maquettes essentielles, modèle de données, catégories et services, contrats API, découpage et estimation des tickets ; création du socle partagé | Les trois collaborateurs lancent le projet et connaissent les interfaces entre leurs modules |
| J2 à J4 | Bouchra développe le dépôt multi-catégories, les photos et la localisation ; Sarra la carte et le suivi ; Khalid les accès internes, la vérification et les affectations | Première intégration réelle du formulaire, de l'API et de l'espace de gestion |
| J5 à J7 | Parcours terrain, preuve de résolution, règles de statut et rattachement des doublons ; intégration quotidienne | Démonstration complète du cycle de traitement à la fin de J7 |
| J8 à J10 | Sarra finalise les courriels et le bilinguisme ; Khalid les indicateurs et l'export ; Bouchra renforce les validations et prépare le déploiement avec l'équipe | Toutes les fonctionnalités obligatoires sont implémentées et intégrées au plus tard à J10 |
| J11 à J12 | Recette commune sur téléphone, droits d'accès, fichiers, erreurs et concurrence ; déploiement, sauvegarde et essai de restauration | Aucun défaut bloquant ; environnement de démonstration exploitable |
| J13 à J14 | Marge pour corrections, guides, jeu de données et répétition de la présentation | Version de livraison identifiée, scénario de démonstration reproductible et documentation disponible |

Les traductions et les tests sont réalisés avec les fonctionnalités ; les journées de recette vérifient leur cohérence d'ensemble. Chaque collaborateur livre des modifications intégrables quotidiennement. À partir de J11, l'équipe se concentre sur la recette et les corrections. Un point quotidien et une revue de capacité dès J1 rendent visibles les blocages et les dépendances. Ce planning est serré : toute incompatibilité entre la charge estimée et les disponibilités doit être signalée immédiatement. Un report de fonctionnalité nécessite un arbitrage explicite de l'équipe ; il n'est pas supposé dans ce calendrier.

# 14 Préparation de l'organisation Jira

Le projet Jira existant est **0-Machakil**, clé **NK0**, dans l'espace edu-team-m91pe19p.atlassian.net. Son tableau porte l'identifiant 70. Le dépôt identifié est **Bouchraelqartit/0-Machakil**. Le découpage comprend six epics et vingt-quatre tickets pour les deux semaines.

| Epic proposé | Objectif | Exigences concernées |
| --- | --- | --- |
| E01 Socle et accès | Installer, sécuriser, gérer les rôles et préparer les environnements | F10 et exigences de qualité |
| E02 Signalement citoyen | Recevoir une catégorie, une photo, une position et un dossier valide | F01, F02, F03 |
| E03 Carte et suivi | Publier les dossiers, assurer le suivi et gérer les doublons | F04, F05, F06 |
| E04 Gestion des interventions | Qualifier, orienter, prioriser, affecter et valider les résolutions | F07, F08, F09 |
| E05 Notifications et reporting | Informer et mesurer le traitement | F11, F12 |
| E06 Expérience et livraison | Finaliser le bilinguisme, la démonstration, la recette et les guides | F13, F14 et recette globale |

La structure proposée est **Epic → Story ou Task → sous-tâches si nécessaire**. Une user story décrit un résultat utilisateur complet ; les sous-tâches éventuelles distinguent API, interface, intégration ou documentation lorsqu'elles ont des responsables différents.

Les colonnes proposées sont « À faire », « En cours », « En revue », « À tester » et « Terminé ». Un blocage est signalé sur le ticket avec son motif. Chaque collaborateur limite son travail principal en cours à une fonctionnalité.

Chaque ticket comportera un objectif, les exigences F associées, des critères d'acceptation testables, les dépendances, une estimation commune, un responsable unique et un lien vers la pull request. Les bugs seront reliés à la fonctionnalité concernée.

**Exemple de story :** « En tant que citoyen, je peux signaler un problème de l'espace public en choisissant une catégorie, une photo et une localisation pour permettre son orientation et sa vérification. » Ses critères couvrent plusieurs catégories, le refus du GPS, une photo invalide et une soumission répétée.

Un ticket est prêt à commencer lorsque son résultat, ses critères et ses dépendances sont compris. Il est terminé après intégration, relecture, vérification des critères et mise à jour de la documentation utile.

# 15 Livrables et décisions de lancement

## Livrables prévus

1. Cahier des charges et décisions de périmètre.

2. Maquettes des parcours et modèle de données.

3. Dépôt de code, historique des contributions et installation.

4. Application déployée en démonstration, avec données fictives.

5. Documentation de l'API et collection de requêtes.

6. Résultats de recette, tests et procédure de restauration.

7. Guides citoyen, gestionnaire et exploitation.

8. Support de présentation et scénario de démonstration à une collectivité.

## Décisions à prendre avant les premières affectations

| Décision | Proposition de départ |
| --- | --- |
| Équipe et disponibilité | Bouchra, Sarra et Khalid, tous full-stack ; disponibilités à préciser |
| Calendrier | Objectif de quatorze jours calendaires, en deux sprints d'une semaine ; date de départ à fixer |
| Socle technique | React, Spring Boot et PostgreSQL ; versions à arrêter |
| Zone pilote | Aïn Sebaâ envisagée ; contour de démonstration à préparer |
| Projet Jira | Projet 0-Machakil existant ; clé NK0 |
| Fournisseurs et budget | À choisir après estimation du trafic et du volume de photos |
| Dépôt GitHub | Bouchraelqartit/0-Machakil, identifié comme dépôt de départ |

## Conditions de passage à un pilote réel

Un pilote avec de vrais habitants nécessite un responsable d'exploitation identifié, une équipe chargée de vérifier et traiter les dossiers, des coordonnées de support, un budget et un accord clair sur les données et les responsabilités.

La démonstration peut être prête avant ce partenariat. L'adoption par une collectivité permettra ensuite de définir les circuits réels d'intervention, les zones couvertes et les engagements de service.
