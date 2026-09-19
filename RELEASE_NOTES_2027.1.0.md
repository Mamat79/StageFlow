# StageFlow v2027.1.0 — Windows et macOS

StageFlow reste gratuit, facultatif et autonome. Cette version consolide le
travail LIVE sur plusieurs postes, corrige deux causes réelles de fermeture ou
de blocage sous Windows et livre le même numéro sur Windows et macOS.

## Ce qui change

- La sélection du groupe actif peut être partagée avec StageMark et StageMon
  dans une Session StageFlow LIVE authentifiée. Elle reste transitoire : elle
  ne modifie pas le projet et disparaît à la déconnexion.
- La fermeture Windows ne relance plus une seconde fermeture interdite pendant
  le nettoyage LIVE.
- Une lecture momentanément impossible de la présence des autres logiciels ne
  bloque plus l'interface et ne simule pas leur départ.
- Les erreurs inattendues peuvent être relues depuis **Aide > Ouvrir les
  diagnostics**. Les journaux sont locaux, limités en taille et expurgés des
  secrets de connexion.
- Le bandeau conserve les commandes Connexion, alertes, thème, langue, Guide et
  Aide alignées à droite.
- La fenêtre du nombre de paires reste lisible aux petites tailles et les
  résumés utilisent correctement le singulier et le pluriel.
- L'import et l'export Excel expliquent clairement la différence entre le
  classeur StageFlow réimportable et le classeur imprimable.
- Le plugin Stream Deck, les commandes OSC et MIDI, le connecteur AutoCAD
  Windows et les guides français/anglais restent inclus.

## Compatibilité et limites

Le format `.stageflow` reste inchangé et extensible. Chaque logiciel conserve
ses propres données et préserve les domaines qu'il ne possède pas. Rejoindre
une session LIVE ne lance jamais l'audio, la projection ou une action Dante.

Le paquet macOS est construit et testé nativement sur Apple Silicon par le
pipeline Codemagic ; le paquet Intel est cross-compilé et son architecture est
contrôlée, sans prétendre à un test natif sur un Mac Intel. Le connecteur
AutoCAD reste réservé à AutoCAD 2026 sous Windows. Aucun test de matériel MIDI,
Stream Deck, audio ou projection physique n'est revendiqué.

---

# StageFlow v2027.1.0 — Windows and macOS

StageFlow remains free, optional and standalone. This release strengthens
multi-workstation LIVE operation, fixes two observed Windows close/freeze
causes, and ships the same version number on Windows and macOS.

## Changes

- The selected group can be shared with StageMark and StageMon inside an
  authenticated StageFlow LIVE session. Selection is transient: it does not
  modify the project and disappears when disconnected.
- Windows shutdown no longer requests a forbidden second close while LIVE
  cleanup is already in progress.
- A transient failure while reading other applications' presence no longer
  blocks the interface or reports a false departure.
- Unexpected failures can be reviewed from **Help > Open diagnostics**. Logs
  stay local, are size-bounded, and redact connection secrets.
- Connection, alerts, theme, language, Guide and Help remain aligned at the
  right edge of the header.
- The pair-count dialog remains readable at small sizes and summaries use the
  correct singular or plural form.
- Excel import and export now distinguish the re-importable StageFlow workbook
  from the print-ready workbook more clearly.
- The Stream Deck plugin, OSC and MIDI commands, Windows AutoCAD connector,
  and French/English guides remain included.

## Compatibility and limits

The `.stageflow` format remains unchanged and extensible. Each application
keeps ownership of its own data and preserves domains it does not own. Joining
a LIVE session never starts audio, projection, or Dante operations.

The macOS package is built and tested natively on Apple Silicon by Codemagic;
the Intel package is cross-compiled and architecture-checked, without claiming
native Intel-Mac testing. The AutoCAD connector remains limited to AutoCAD 2026
on Windows. No physical MIDI, Stream Deck, audio, or projection hardware
acceptance is claimed.
