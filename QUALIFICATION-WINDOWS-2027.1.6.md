# StageFlow Windows 2027.1.6 — contrôles et limites / checks and limits

## Français

Correction de la liaison Excel après édition du patch : Commun est exclue du contrôle de pagination recto verso, limité aux fiches de groupes. En cas d’erreur pendant le rafraîchissement d’une vue, son contenu précédent et sa protection sont rétablis. Une vue volontairement déverrouillée est préservée et arrête la synchronisation avant écriture.

Source privée main c183a274d67f8bf8f6ce0188cf858f77aaf2880b, compilée à nouveau pour cette livraison. Les résultats du développeur (155 métier, 25 WPF, 39 Avalonia sous Windows et 1 ignoré, 16+5 Office) restent distincts des nouveaux essais du paquet. L’ancien échec de préparation Avalonia 18 est conservé comme historique et remplacé par la relance isolée 39/1 ; il n’est pas présenté comme un nouveau résultat du paquet.

L’atelier a extrait le véritable Setup standard puis comparé 631 fichiers de l’application et 5 du connecteur AutoCAD, octet pour octet. Quatre PDF et le manifeste du lot de guides approuvé sont inchangés. Le connecteur AutoCAD reste .NET 8, facultatif et sans DLL Autodesk redistribuée. Le plugin Stream Deck a passé la validation officielle et l’audit de ses dépendances d’exécution dans la recette.

Les 21 nouveaux scénarios dans Microsoft Excel réel utilisent les DLL livrées : 16 généraux et 5 de régression sur une copie privée de projet. Les deux sens, les libellés001/=literal, les formules, les conflits, les colonnes personnelles, la protection et la reprise après interruption sont contrôlés. Ces copies et preuves personnelles ne sont pas publiques. Les cycles peuvent prendre plusieurs secondes ou dizaines de secondes ; aucune actualisation instantanée n’est promise. La liaison native Office est limitée à Windows avec Excel de bureau installé.

Le nouveau Setup n’a pas été exécuté : installation réelle, mise à niveau, raccourcis et retour arrière ne sont pas exercés pour 1.6. Le compte QA partagé n’a pas été modifié. La recette native de l’interface StageFlow, du clavier et de la matrice DPI 1.6 reste non effectuée ; les tests Office et d’intégrité ne la remplacent pas. Aucun remplacement de l’installation personnelle, aucune fermeture de classeur personnel. Le matériel audio, les réseaux de spectacle et AutoCAD en fonctionnement restent hors de ces contrôles.

macOS reste disponible en 2027.1.5 dans sa release existante, minimum macOS 14 ; ses limites propres restent valables. Aucun DMG 1.5 n’est renommé en 1.6. Le nouveau lot Mac doit être qualifié séparément avant addition.

## English

Fixes desktop Excel synchronization after patch edits. Duplex pagination applies only to group print sheets, excluding the Commun overview. Interrupted view refresh restores its previous content and protection. Deliberately unlocked views are preserved and stop synchronization before data-table writes.

This delivery rebuilds private main c183a274d67f8bf8f6ce0188cf858f77aaf2880b. Developer evidence (155 business tests, 25 WPF, 39 Windows Avalonia with 1 skipped, 16+5 Office checks) is distinct from new package checks. The historical 18 setup failures are retained and superseded by the isolated 39/1 run.

The actual standard installer was unpacked; all 631 application files and 5 AutoCAD connector files match the prepared payload byte for byte. The four approved PDF guides and their manifest are unchanged. AutoCAD stays on .NET 8, optional and without redistributed Autodesk DLLs. The Stream Deck package passed official validation and runtime dependency auditing in the recipe.

Twenty-one new real Excel scenarios load the delivered product DLLs: 16 general checks and 5 regression checks on a private project copy. Both directions,001/=literal labels, formulas, conflicts, personal columns, protection and interruption recovery are checked. Personal fixtures and raw receipts are private. Refresh may take seconds or tens of seconds; instant completion is not promised. Native desktop Office integration requires Windows with desktop Excel installed.

The new standard installer was not executed: installation, upgrade, shortcuts and rollback are unexercised for 1.6. The shared QA account was untouched. StageFlow native UI rendering, keyboard navigation and full DPI coverage were not exercised for 1.6; Office and integrity tests do not replace these checks. No personal installation replacement or workbook closure was performed. Physical audio, show networks and the actual AutoCAD host remain outside these checks.

macOS remains 2027.1.5 in its existing release, requiring macOS 14 or later, with its own qualification limits. No 1.5 DMG was renamed 1.6. New Mac artifacts require separate qualification before addition.
