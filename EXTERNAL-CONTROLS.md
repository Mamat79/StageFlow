# Contrôles externes — OSC, MIDI et Stream Deck

StageFlow utilise une seule liste de commandes pour OSC, MIDI, Stream Deck et le LIVE réseau. Une commande garde donc le même identifiant quel que soit le contrôleur.

## Mise en route

Dans StageFlow, ouvrez **Outils → OSC · MIDI · Stream Deck**.

- OSC écoute par défaut uniquement ce PC sur `127.0.0.1:18040`.
- Pour recevoir depuis le réseau local, choisissez l’adresse de la carte réseau ou `0.0.0.0`, puis autorisez StageFlow dans le pare-feu Windows si Windows le demande.
- Le retour OSC est facultatif. Son adresse, son port et les commandes renvoyées se choisissent dans le même écran.
- En MIDI, choisissez une entrée, cliquez sur **Apprendre le prochain message**, puis actionnez le bouton ou contrôle voulu.
- Pour Stream Deck, installez le paquet proposé dans StageFlow, ajoutez l’action **SiLeMIO Suite**, puis choisissez sa commande dans l’inspecteur de propriétés.

StageMark et StageMon restent autonomes. Leurs commandes ci-dessous passent par StageFlow seulement lorsqu’ils sont connectés au projet et à la session LIVE courants.

## Tableau des commandes

| Logiciel | Fonction | Identifiant stable | Adresse OSC | Valeur |
|---|---|---|---|---|
| StageFlow | Enregistrer le projet | `stageflow.project.save` | `/silemio/stageflow/project/save` | — |
| StageFlow | Recharger le projet | `stageflow.project.reload` | `/silemio/stageflow/project/reload` | — |
| StageFlow | Choisir un groupe | `stageflow.group.select` | `/silemio/stageflow/group/select` | nom, numéro ou UUID |
| StageFlow | Groupe suivant | `stageflow.group.next` | `/silemio/stageflow/group/next` | — |
| StageFlow | Groupe précédent | `stageflow.group.previous` | `/silemio/stageflow/group/previous` | — |
| StageFlow | Afficher tout le commun | `stageflow.common.show-all` | `/silemio/stageflow/common/show-all` | — |
| StageFlow | Masquer tout le commun | `stageflow.common.hide-all` | `/silemio/stageflow/common/hide-all` | — |
| StageFlow | Activer LIVE | `stageflow.live.enable` | `/silemio/stageflow/live/enable` | — |
| StageFlow | Arrêter LIVE | `stageflow.live.disable` | `/silemio/stageflow/live/disable` | — |
| StageFlow | Basculer LIVE | `stageflow.live.toggle` | `/silemio/stageflow/live/toggle` | — |
| StageFlow | Suspendre les alertes LIVE | `stageflow.alerts.pause` | `/silemio/stageflow/alerts/pause` | — |
| StageFlow | Réactiver les alertes LIVE | `stageflow.alerts.resume` | `/silemio/stageflow/alerts/resume` | — |
| StageFlow | Basculer les alertes LIVE | `stageflow.alerts.toggle` | `/silemio/stageflow/alerts/toggle` | — |
| StageFlow | Réactiver et envoyer les changements en pause | `stageflow.alerts.send-pending` | `/silemio/stageflow/alerts/send-pending` | — |
| StageFlow | Acquitter les alertes de ce poste | `stageflow.alerts.acknowledge` | `/silemio/stageflow/alerts/acknowledge` | — |
| StageMark | AFFICHER | `stagemark.output.show` | `/silemio/stagemark/output/show` | — |
| StageMark | BLACKOUT | `stagemark.output.blackout` | `/silemio/stagemark/output/blackout` | — |
| StageMark | Choisir une cue | `stagemark.cue.select` | `/silemio/stagemark/cue/select` | nom, numéro ou UUID |
| StageMark | Cue suivante | `stagemark.cue.next` | `/silemio/stagemark/cue/next` | — |
| StageMark | Cue précédente | `stagemark.cue.previous` | `/silemio/stagemark/cue/previous` | — |
| StageMon | Clear Cue A | `monitoring.cue.clear-a` | `/silemio/stagemon/cue/clear-a` | — |
| StageMon | Clear Cue B | `monitoring.cue.clear-b` | `/silemio/stagemon/cue/clear-b` | — |
| StageMon | Choisir un patch | `monitoring.patch.select` | `/silemio/stagemon/patch/select` | nom, numéro ou UUID |
| StageMon | Patch suivant | `monitoring.patch.next` | `/silemio/stagemon/patch/next` | — |
| StageMon | Patch précédent | `monitoring.patch.previous` | `/silemio/stagemon/patch/previous` | — |
| StageMon | Démarrer l’audio | `monitoring.audio.start` | `/silemio/stagemon/audio/start` | — |
| StageMon | Arrêter l’audio | `monitoring.audio.stop` | `/silemio/stagemon/audio/stop` | — |
| StageMon | Mute écoute A | `monitoring.monitor-a.mute-toggle` | `/silemio/stagemon/monitor-a/mute-toggle` | — |
| StageMon | Mute écoute B | `monitoring.monitor-b.mute-toggle` | `/silemio/stagemon/monitor-b/mute-toggle` | — |

Pour une commande sans valeur, les contrôleurs envoient généralement `1` à l’appui et ignorent le relâchement à `0`. Pour une sélection, transmettez une chaîne. Les adresses OSC peuvent être personnalisées dans StageFlow ; conservez alors la même adresse dans l’émetteur.

## Alertes et disposition conseillée

Le catalogue comporte 29 commandes : 15 StageFlow, 5 StageMark et 9 StageMon.
Sur un Stream Deck de 15 touches, on peut par exemple organiser :

| Rangée | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Patch | Groupe précédent | Groupe suivant | Choisir un groupe | Enregistrer | Acquitter ce poste |
| Alertes | Pause alertes | Reprendre alertes | Reprendre + envoyer | LIVE activer | LIVE arrêter |
| Sorties | BLACKOUT StageMark | AFFICHER StageMark | Patch StageMon précédent | Patch StageMon suivant | Clear Cue A |

**Pause alertes** suspend la diffusion centrale des notifications de la session LIVE.
Les données continuent de circuler. Elle concerne les changements de labels déjà
pris en charge par les alertes ; monitoring et notes restent sans alertes.
**Reprendre alertes** autorise les notifications futures, sans rappel automatique.
**Reprendre + envoyer** réactive la diffusion et envoie volontairement
les changements conservés pendant la dernière pause : premier ancien nom → dernier
nom. Un label revenu à sa valeur initiale ou déjà republié après la reprise est écarté.
Un second appui ne renvoie rien. Chaque nouvelle pause repart du présent.

Les coupures d'émission propres à une application et les coupures de réception
propres à un destinataire restent respectées. **Acquitter ce poste** n'acquitte
jamais les alertes des autres postes. Le tampon, limité aux 200 derniers champs
modifiés comme le fil d'alertes, est éphémère et s'efface en fin de session.
Un dépassement est comptabilisé et renvoie `sent-with-omissions` avec avertissement
sur la touche ; il ne faut alors pas interpréter cet envoi comme exhaustif.

**BLACKOUT / AFFICHER** commande la sortie de projection de StageMark connecté,
et les boutons StageMon commandent le poste sélectionné dans la console de la
session courante. Ce catalogue ne commande pas un éclairage DMX, StageDesk,
Dante Config Editor ou AutoCAD.

Installez le plugin fourni avec cette génération de StageFlow : son « OK »
attend maintenant l'acceptation par StageFlow. Un refus ou une absence de réponse
affiche un avertissement ; consulter le journal OSC pour la cause. Une absence
de confirmation ne prouve pas qu'une commande n'a pas été exécutée : vérifier
l'état avant de réappuyer. Il n'y a pas de répétition automatique ni de voyant
permanent indiquant l'état réel de la suite.

Le plugin ajoute à chaque message OSC `silemio.streamdeck.v1` et un UUID de requête.
StageFlow répond à l'adresse/port source sur `/silemio/ack` avec UUID, booléen
d'acceptation et statut. Ce retour ponctuel ne nécessite pas de configurer le
port de retour OSC général. Les messages OSC et les réglages MIDI existants
restent compatibles.

## English quick start

Open **Tools → OSC · MIDI · Stream Deck**. OSC listens locally on `127.0.0.1:18040` by default. Select a network interface or `0.0.0.0` only when another computer must send commands. Optional OSC feedback, MIDI learn and the installable Stream Deck action are configured in the same window. StageMark and StageMon commands require those applications to be connected to the current StageFlow LIVE session.

The 29-command catalogue adds master alert pause, resume, toggle, explicit send
of paused changes and host-local acknowledgement. Resume never replays history.
Send resumes alerts and sends each field's net change once, respecting
individual emission/reception mute. Reverted or subsequently published changes
are discarded. The session-only buffer keeps the latest 200 fields and reports
any overflow. BLACKOUT/SHOW targets the connected StageMark projection output.
The Stream Deck OK indicator confirms host acceptance; warnings mean refusal,
overflow or missing confirmation. No automatic retry and no permanent state LED.
