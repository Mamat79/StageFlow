# StageFlow Windows 2027.1.8 — contrôles et limites / checks and limits

## Français

Le panneau Tableur détecte les changements sans écrire ni régénérer les fiches à chaque saisie. Le transfert est volontaire : « Mettre à jour… », comparatif, choix séparé de chaque conflit, puis confirmation. Annuler conserve les versions en attente. Commun et Édition Patch peuvent être comparés ; les décisions périmées sont rejetées. Une copie du classeur précède le transfert. Un échec laisse la mise à jour non terminée et permet une nouvelle comparaison. La synchronisation ne remplace pas l'enregistrement ; aucune reconnexion automatique au démarrage.

Source finale privée main c94b10d5c48531353566e9b59ea00d110321f799. Les contrôles du développeur qualifient le parent fonctionnel ccdebffbf250bde61bbd42dda155a381786e1f69 : 478 logiciels réussis et un CoreMIDI ignoré (164 métier, 25 WPF, 125 Core net8, 125 Core net10, 39 Avalonia sur Windows), plus 41 Office/WPF. La source finale ajoute seulement deux numéros de version dans le Info.plist Mac ; l'équivalence des autres fichiers est vérifiée. Aucun nouveau passage de ces 478 contrôles sur la source finale n'est prétendu.

Le paquet Windows est compilé à nouveau depuis la source finale. 41 nouveaux contrôles Excel/WPF sur ses DLL exactes ont réussi : 10 panneau Tableur manuel, 16 généraux, 5 régressions, 10 Commun/impression. Ils contrôlent la détection sans mutation, la saisie Commun en attente, l'annulation, les échanges volontaires bidirectionnels, les choix différents par champ, le rejet d'une revue périmée, la copie avant transfert et la reprise après échec. Les choix sont injectés par un mécanisme QA dans le véritable chemin de commande WPF ; cela ne vaut pas recette humaine exhaustive des clics, clavier ou DPI.

Deux PDF représentatifs, quatre pages, ont été exportés par Excel et examinés visuellement : 42 paires et quatre groupes, patch complet au recto, Monitoring/Notes au verso, sans chevauchement observé. Notes longues et papier peuvent modifier la pagination et la lisibilité. Impression physique non exercée.

L'EXE réellement empaqueté a aussi démarré et chargé une copie privée complète de projet, rendu sa fenêtre puis quitté normalement avec code0. Le panneau Tableur, le comparatif WPF et ce rendu ont été examinés. Ce contrôle ciblé porte sur un seul viewport, avec zones de défilement ; il ne remplace pas une recette humaine complète clavier/DPI.

Le véritable Setup final a été extrait : 631 fichiers application et 5 connecteur conformes. Quatre guides approuvés et leur manifeste restent inchangés ; AutoCAD facultatif reste net8 sans DLL Autodesk redistribuée ; validation officielle Stream Deck et audit de dépendances dans la recette. L'intégration Excel exige Windows avec Excel de bureau ; aucun complément Office n'est installé, pas de liaison native Excel web/Mac. Les travaux Office prennent des secondes ou dizaines de secondes au clic, sans promesse d'instantanéité.

Au moment de la publication, le nouveau Setup n'est pas encore exécuté : installation, upgrade et raccourcis personnels sont qualifiés ensuite dans un reçu séparé avec sauvegardes. Retour arrière, couverture exhaustive de l'interface/clavier/DPI, matériel audio, réseaux de spectacle et AutoCAD en fonctionnement non exercés. Compte QA partagé hors périmètre. Projets personnels et preuves brutes non publiés. macOS réel 2027.1.5 reste disponible, minimum macOS14, sans renommage ; un nouveau lot Mac1.8 est séparé jusqu'à ses fichiers réellement qualifiés.

## English

The Spreadsheet panel detects pending changes without writing or regenerating sheets on every edit. Transfer requires Update…, review, separate choices for each conflict and confirmation. Cancel retains pending versions. Commun and Edition Patch can be compared, stale decisions are rejected, and a workbook copy precedes transfer. A failure reports an unfinished update and permits a fresh review. Synchronization does not replace saving and never reconnects automatically at startup.

Final private main c94b10d5c48531353566e9b59ea00d110321f799. Developer checks qualify functional parent ccdebffbf250bde61bbd42dda155a381786e1f69: 478 passed and one CoreMIDI skipped (164 business, 25 WPF, 125 Core net8, 125 Core net10, 39 Windows Avalonia), plus 41 Office/WPF checks. Only two Mac Info.plist version strings changed afterward; all remaining files are equivalent. No rerun of those 478 checks on the final source is claimed.

Windows was rebuilt from the exact final source. 41 new real Excel/WPF checks passed on delivered DLLs: 10 manual Spreadsheet checks, 16 general checks, 5 regressions and 10 Commun/print checks. They cover detection without mutation, pending Commun edits, cancellation, explicit two-way transfer, independent per-field choices, stale review rejection, real pre-transfer copies and recovery after failure. Decisions are injected through a QA hook in the actual WPF command path; this is not exhaustive human mouse/keyboard/DPI acceptance.

Two representative PDFs, four pages, were exported by Excel and visually checked: complete 42-pair patch with four groups on the front, Monitoring/Notes on the back, no observed overlap. Long notes and paper may affect pagination and readability. No physical printing test.

The actual packaged EXE also started, loaded a complete private project copy, rendered its window and exited normally with code0. The Spreadsheet panel, WPF review dialog and App render were examined. This single-viewport targeted check, with scrolling regions, is not full human keyboard/DPI acceptance.

The actual final standard Setup was unpacked; all 631 application and 5 optional connector files match. Four approved guide PDFs and their manifest are unchanged. AutoCAD remains optional net8 without redistributed Autodesk DLLs. Stream Deck passed official validation and dependency auditing. Native Excel linking requires Windows desktop Excel, without an Office add-in or web/Mac Excel link. Work may take seconds or tens of seconds after the click, without an instant-transfer guarantee.

At publication time Setup execution, personal upgrade and shortcuts are unexercised and have a later separate receipt with backups. Rollback, full native UI/keyboard/DPI, physical audio, show networks and running AutoCAD remain unexercised. The shared QA account is outside this scope. Private projects and raw receipts are not published. Existing macOS 2027.1.5 remains available for macOS14 or later without renamed files; genuine Mac1.8 artifacts require their separate qualification.
