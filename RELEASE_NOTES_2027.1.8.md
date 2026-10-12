# StageFlow 2027.1.8 — Tableur et mise à jour volontaire

## Français

La liaison avec Excel de bureau Windows détecte les changements sans les transmettre à chaque saisie. Dans le panneau **Tableur**, l’état précise si Excel ou StageFlow attend une mise à jour. **Mettre à jour…** affiche un comparatif puis applique les changements ensemble après validation.

- Les modifications indépendantes sont réunies automatiquement. Chaque conflit permet de conserver séparément la valeur StageFlow ou Excel. Annuler garde les deux versions en attente.
- Les sources, micros et commentaires communs se modifient directement dans **Commun**, ainsi que les sources et micros de groupe dans leurs colonnes existantes. Sa présentation est conservée. Les différences entre Commun et Édition Patch peuvent aussi être choisies dans le comparatif.
- Une saisie ou un changement fait pendant la comparaison empêche l’application d’une décision devenue obsolète.
- Une copie du classeur précède chaque transfert. Un échec conserve la base précédente, indique la mise à jour non terminée et permet une nouvelle comparaison.
- **Tableur** rassemble le classeur lié, son affichage dans Excel, le classeur imprimable et le PDF. Les exports utilisent les données actuelles de StageFlow et signalent les modifications Excel détectées qui attendent leur import.

Le patch complet au recto et Monitoring/Notes au verso restent disponibles. L’actualisation des fiches peut prendre quelques secondes, mais elle est déclenchée à votre demande. Enregistrez le projet et le classeur selon votre utilisation habituelle ; la synchronisation ne remplace pas l’enregistrement. La connexion n’est jamais reprise automatiquement au démarrage.

La liaison nécessite Microsoft Excel de bureau sous Windows. Elle ne fournit pas de complément Office et ne relie pas Excel pour le web ou Excel pour Mac. Les fonctions existantes de projet, Monitoring, Notes, export XLSX et impression sur macOS sont conservées.

## English

The Windows desktop Excel link detects changes without sending data on every edit. The **Spreadsheet** panel identifies whether Excel or StageFlow needs updating. **Update…** opens a comparison and applies the changes together after confirmation.

- Independent edits merge automatically. Choose StageFlow or Excel separately for every conflict. Cancel keeps both versions pending.
- Edit sources, microphones and common comments directly on **Commun**, including group-specific source and microphone columns, with its existing appearance. The comparison also resolves different edits in Commun and Edition Patch.
- A change made during review prevents stale decisions from being applied.
- A complete workbook copy precedes each transfer. An error keeps the previous baseline, reports an unfinished update and allows a fresh comparison.
- **Spreadsheet** groups the linked workbook, Show Excel, printable workbook and PDF. Exports use current StageFlow data and warn about detected Excel edits awaiting import.

The complete patch on the front and Monitoring/Notes on the reverse remain available. Sheet refresh can take a few seconds and happens only when requested. Save the project and workbook as usual; synchronization does not replace saving. The link never reconnects automatically at startup.

Linking requires Windows desktop Microsoft Excel. This release does not install an Office add-in or link Excel for the web or Mac. Existing macOS project, Monitoring, Notes, XLSX export and printing features are preserved.


## Livraison / Delivery

Windows 2027.1.8 ; macOS reste/remains 2027.1.5. 41 nouveaux contrôles sur DLL livrées / 41 new checks on delivered DLLs. Actual Setup contents and four PDF pages verified.

[Contrôles et limites / checks and limits](QUALIFICATION-WINDOWS-2027.1.8.md).
