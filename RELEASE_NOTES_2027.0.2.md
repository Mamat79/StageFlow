# StageFlow v2027.0.2 - Windows

StageFlow reste gratuit, facultatif et utilisable seul. Cette corrective Windows
améliore les longues sessions de télécommande et la lisibilité de la suite.

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
