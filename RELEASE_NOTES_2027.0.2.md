# StageFlow v2027.0.2 - Windows

StageFlow reste gratuit, facultatif et utilisable seul. Cette corrective Windows
améliore les longues sessions de télécommande et la lisibilité de la suite.

## Centre de connexion et télécommandes

- **Connexion StageFlow** garde son nom dans le bandeau, avec l’état et les
  compteurs visibles séparément. Le centre propose **StageFlow LIVE** et
  **Télécommande StageFlow**, avec le QR directement dans la page.
- **Retour au projet** ferme le centre sans arrêter la session. Les commandes
  restent accessibles dans une petite fenêtre et dans les deux langues/thèmes.
- Sur téléphone ou tablette, une carte StageMark ou StageMon indisponible
  explique pourquoi et quoi vérifier. Lire cette explication ne demande aucun
  accès et n’active aucun service.
- L’ouverture du contrôleur conserve les droits de l’application choisie.
  Un changement de poste cible ou de session retire l’ancien contrôleur. Une
  perte de connexion à StageFlow le retire également et affiche la cause.
- La liaison utilise la télécommande native de StageMark ou StageMon : elle
  ne démarre ni l’audio ni la projection. Les accès autonomes restent possibles.
- Le guide commun français/anglais explique ces parcours et distingue les
  versions Windows actuelles des paquets Mac conservés.

Si vous aviez déjà installé 2027.0.2, téléchargez de nouveau l’installateur de
cette release et réinstallez-le après avoir enregistré et fermé StageFlow.
Le numéro étant identique, la mise à jour numérique ne propose pas forcément
cette nouvelle fabrication. Les fichiers SHA-256 permettent de l’identifier.

## Correctif de stabilité du 6 septembre 2026

Cette nouvelle fabrication conserve le numéro **2027.0.2**. Elle empêche une
fermeture de StageFlow lors de l’affichage ou de l’actualisation des participants
dans **Connexion StageFlow**, notamment quand StageMark puis StageMon rejoignent
la session. L’ancienne fenêtre LIVE réseau bénéficie de la même correction.

Le bouton d’ouverture s’appelle désormais **Ouvrir un projet StageFlow…**.
Les notions de projet local et de session LIVE restent distinctes dans le
contexte du projet et l’aide.

L’installateur demande d’enregistrer puis de fermer StageFlow avant de remplacer
les fichiers. Il ne ferme pas automatiquement une application ouverte.
Le format de projet, le réseau et les autorisations des télécommandes ne changent
pas. Les paquets macOS v2027.0.1 sont inchangés.

## Ce qui change

- La télécommande continue après 4 096 commandes, sans redémarrer StageFlow ni
  recréer le QR. Les anciennes requêtes ne sont jamais rejouées automatiquement.
- Le bandeau s’adapte à la largeur de la fenêtre. Il affiche l’état de connexion,
  les alertes, le thème courant Clair/Sombre, FR/EN, le Guide de la suite et
  l’Aide propre à StageFlow. Les commandes communes suivent les repères de la suite.
- Connexion StageFlow regroupe le nom complet du projet, le fonctionnement local,
  l’hôte, les postes connectés, leurs commandes annoncées et l’accès QR. Les
  détails techniques restent consultables sans encombrer le parcours principal.
- Les alertes distinguent l’émission de toute la session et l’acquittement local.
  Pendant une préparation en lot, la suspension reste visible, avec le nombre
  de modifications locales. La reprise est volontaire et ne rejoue pas la pause.
- Quand le LIVE est arrêté, en attente d’enregistrement ou interrompu, le centre
  l’indique aussi dans la zone des alertes. L’aide reprend le nom exact du bouton
  Connexion StageFlow.
- Le Guide commun FR/EN édition 2027.2 corrige les versions par plateforme,
  notamment Dante Config Editor Windows. Son tableau est une référence datée ;
  chaque release reste la source de la version la plus récente.

## Utilisation

Ouvrez le projet puis **Connexion StageFlow** pour choisir le partage réseau ou
la télécommande. Le projet local, le LIVE réseau et le QR sont des états distincts.
Activer les alertes ne démarre plus implicitement le LIVE : activez-le d’abord
volontairement. **Alertes** suspend l’émission ; **Reprendre l’émission** la remet
en route. **Tout acquitter sur ce poste** ne coupe pas les alertes futures et
n’affecte pas les autres destinataires.

Aucune connexion ni reprise d’alertes ne démarre l’audio ou ne lève un blackout.
Le format de projet, les autorisations, les révisions et les sécurités métier
restent inchangés. Une ancienne page mobile peut être rechargée pour obtenir
le client à jour, sans redémarrer le serveur.

## Plateformes et limites

Cette corrective est Windows uniquement. Les paquets macOS Intel et Apple
Silicon v2027.0.1 restent disponibles dans leur release d’origine, avec leur
vrai numéro. Les essais logiciels ne constituent pas une recette matérielle
sur téléphone, réseau de show, projecteur ou interface audio.

---

# StageFlow v2027.0.2 - Windows

StageFlow remains free, optional and fully standalone.

## Connection centre and remote controls

- **StageFlow connection** keeps its name in the header, with separate status
  and counts. The centre offers **StageFlow LIVE** and **StageFlow remote
  control**, including the QR directly on the page.
- **Back to project** closes the centre without stopping the session. Controls
  remain accessible in narrow windows, both languages and both themes.
- Unavailable StageMark and StageMon mobile cards explain the reason and the
  next useful action. Reading this explanation requests no access and starts
  no service.
- Opening a controller preserves the selected application's permissions.
  Changing the target workstation or session removes the previous controller.
  Losing the StageFlow connection also removes it and explains the situation.
- Handoff uses the real StageMark or StageMon remote. It starts neither audio
  nor projection; standalone remote access remains available.
- The shared French/English guide explains these workflows and distinguishes
  current Windows versions from retained Mac packages.

If you already installed 2027.0.2, download this release's installer again and
reinstall after saving your work and closing StageFlow. Because the version
number is unchanged, the numeric updater may not offer this new build. The
SHA-256 files identify it precisely.

## Stability fix — 6 September 2026

This new build keeps version **2027.0.2**. It prevents StageFlow from closing
while displaying or refreshing participants in **StageFlow connection**,
including when StageMark and then StageMon join the session. The legacy network
LIVE window receives the same fix.

The opening button is now labelled **Open a StageFlow project…**. Local projects
and LIVE sessions remain distinct in project context and Help.

The installer asks you to save your work and close StageFlow before replacing
files. It does not automatically close a running application. Project format,
networking and remote-control permissions are unchanged. Existing macOS
v2027.0.1 packages are unchanged.

## Other improvements in 2027.0.2

- Remote sessions continue beyond 4,096 commands without restarting the
  application or its QR gateway. Old requests are not automatically replayed.
- The responsive suite header provides connection state, alerts, the current
  Light/Dark theme, FR/EN, the shared Guide and StageFlow-specific Help.
- StageFlow connection separates the local project, network host and connected
  applications from mobile QR control, with advertised controls and expandable
  technical details.
- Session-wide alert emission is clearly separate from local acknowledgement.
  Paused emission remains visible, with a local change count. Resume is explicit
  and does not replay edits from the pause. Enable LIVE explicitly before alerts.
- The alert area also reports when LIVE is off, waiting for a saved project or
  interrupted. Help uses the exact StageFlow connection button name.
- Shared guides edition 2027.2 correct the dated per-platform release matrix,
  including Dante Config Editor for Windows.

Connection and alert resumption never start audio or lift blackout. Project
format, permissions, revisions and application safety controls are preserved.
Reload an old mobile page to obtain the updated client; no QR restart is needed.

This corrective is Windows-only. Existing macOS Intel and Apple Silicon
v2027.0.1 packages keep their original version and release. Software tests are
not physical phone, show-network, projector or audio-interface acceptance.
