# StageFlow 2027.1.10

## Français

Le pilotage Stream Deck dispose de 29 commandes pour StageFlow, StageMark et
StageMon. Cinq commandes ajoutent la pause des alertes LIVE, leur réactivation,
le basculement ON/OFF, la reprise avec envoi volontaire des changements en pause
et l'acquittement sur le poste StageFlow.

La pause suspend les notifications centrales ; les données LIVE continuent de
circuler. Reprendre seul ne rejoue rien. Reprendre + envoyer diffuse le premier
ancien nom → dernier nom par champ, une seule fois. Les retours à la valeur
initiale et les changements déjà republiés sont écartés. Les préférences locales
d'émission/réception restent respectées. Le tampon éphémère conserve les 200
derniers champs et signale un dépassement ; il s'efface avec la session.
Monitoring et notes restent sans alertes.

Le plugin Stream Deck 2026.3.1.0 corrige son accès au catalogue au démarrage et
attend l'acceptation de StageFlow avant d'afficher OK. Refus et absence de
confirmation affichent un avertissement, sans nouvelle tentative automatique.
Un ancien hôte doit être mis à jour avec le plugin correspondant.

Groupe suivant/précédent, sélection directe, BLACKOUT/AFFICHER de la projection
StageMark et commandes de patch/cues/audio StageMon sont conservés. StageMark
et StageMon doivent être connectés au projet LIVE courant. La configuration
se trouve dans **Outils → OSC · MIDI · Stream Deck**.

Affichage Mac : OpenGL avec repli logiciel lorsque l'accélération n'est pas
disponible. Le repli Metal utilisé auparavant a rencontré des erreurs de
compilation de shaders pendant la qualification sur Mac.

Les PDF approuvés du lot 2027.4 restent inchangés et décrivent les 24 commandes
antérieures. Les cinq nouvelles et une disposition de 15 touches sont expliquées
dans l'aide complémentaire des contrôles externes. Cette évolution ne vaut pas
validation d'un Stream Deck physique, de la projection ou de l'audio sur site.

## English

Stream Deck control provides 29 commands for StageFlow, StageMark and StageMon.
Five new commands pause/resume LIVE alerts, toggle them, resume and explicitly
send paused changes, and acknowledge alerts on the StageFlow host only.

Pausing notifications does not stop LIVE data. Resume alone never replays
history. Resume + send publishes each field's first old name → latest name
once, discarding reverted or subsequently published changes. Individual
emission/reception mute remains respected. The session-only buffer retains the
latest 200 fields, reports overflow and clears when the session ends.
Monitoring and notes still produce no label alerts.

Stream Deck plugin 2026.3.1.0 fixes catalogue loading at startup and waits for
StageFlow acceptance before showing OK. Refusals or missing confirmation show
a warning without automatic retries. Update StageFlow and its matching plugin
together. Next/previous group, direct selection, connected StageMark projection
BLACKOUT/SHOW and StageMon patch/cue/audio commands remain available under
**Tools → OSC · MIDI · Stream Deck**.

Mac rendering uses OpenGL with a software fallback when acceleration is
unavailable. The previous Metal fallback encountered shader compilation
errors during Mac qualification.

The approved 2027.4 PDFs remain unchanged and describe the previous 24 commands.
The supplementary external-controls help documents the five additions and a
15-key layout. This update does not certify physical Stream Deck hardware,
projection or onsite audio.
