# StageFlow Windows 2027.1.7 — contrôles et limites / checks and limits

## Français

Commun permet l'édition directe des sources, microphones et commentaires communs, ainsi que des sources et microphones des groupes. Les échanges vont dans les deux sens, les numéros et titres restent protégés, les formules personnelles sont préservées et les valeurs concurrentes différentes demandent une résolution.

Le patch de 42 paires tient au recto dans les deux exports représentatifs vérifiés, puis Monitoring et Notes commencent au verso. Les colonnes de tous les groupes sont conservées dans Commun. Les contrôles Office vérifient pagination paire, absence de débordement horizontal et suppression des en-têtes superposés. Les quatre pages PDF réellement exportées sont examinées visuellement. Les longues notes peuvent produire des pages supplémentaires ; la lisibilité et l'impression papier dépendent aussi du contenu et du papier.

Source privée main bd620a5be22de044cce3c4b6b9c4398d3f5fe13a, compilée à nouveau pour cette livraison. Les preuves du développeur sont distinctes : 159 métier, 25 WPF, 39 Avalonia Windows et 1 CoreMIDI ignoré, 31 Office ; recette de compatibilité ciblée Core .NET8 et .NET10, 125 tests par cible, contrat et clients inchangés. Une première sélection générique de runtime .NET8 avait échoué ; ses relances explicites sont conservées et réussies. Il ne s'agit pas d'une recette matérielle ou LAN réelle de tous les logiciels.

Les 31 nouveaux essais Office sur les DLL livrées ont réussi : 16 généraux, 5 régressions de synchronisation et 10 Commun/impression. Copies personnelles et reçus bruts restent privés. Un import IO manquant dans le lanceur QA isolé a été corrigé avant ces essais ; son journal de préparation est conservé. Les cycles peuvent prendre plusieurs secondes ou dizaines de secondes, sans promesse d'actualisation instantanée. La liaison native exige Windows avec Excel de bureau installé.

Le véritable Setup standard a été extrait ; tous les fichiers application et du connecteur AutoCAD correspondent au payload. Le connecteur reste facultatif, .NET8, sans DLL Autodesk redistribuée. Les quatre PDF et le manifeste des guides approuvés sont inchangés. Le plugin Stream Deck a passé la validation officielle et l'audit de ses dépendances dans la recette.

Au moment de la publication, le nouvel installeur n'a pas encore été exécuté : installation, mise à niveau, raccourcis et retour arrière restent non exercés dans ce reçu de publication. La mise à jour personnelle autorisée fera l'objet d'un reçu séparé, après sauvegardes. Interface native StageFlow, clavier, couverture DPI, audio physique, réseaux de spectacle et AutoCAD en fonctionnement ne sont pas qualifiés par ces essais Office/PDF. Le compte QA partagé reste hors périmètre.

macOS reste disponible en 2027.1.5 dans sa release existante, minimum macOS14. Aucun ancien DMG n'est renommé en 1.7. Le nouveau lot Mac est séparé et ne sera ajouté qu'après livraison réelle et qualification.

## English

Commun supports direct editing of common sources, microphones and comments, and each group's sources and microphones. Synchronization works both ways. Pair numbers and headings stay protected, personal formulas are preserved and conflicting new values require resolution.

The complete 42-pair patch fits the front in both verified representative exports; Monitoring and Notes start on the back. Commun keeps every group column. Office checks cover even duplex pagination, no horizontal spill and no duplicate printer headers. All four pages of the actual PDF exports were visually examined. Long notes may add pages; readability and physical printing also depend on content and paper.

Private main bd620a5be22de044cce3c4b6b9c4398d3f5fe13a was rebuilt for this delivery. Developer evidence is separate: 159 business checks, 25 WPF, 39 Windows Avalonia with 1 CoreMIDI skipped, and 31 Office. Targeted suite compatibility includes Core .NET8 and .NET10, 125 checks per target, with unchanged contracts and clients. The historical generic .NET8 runtime-selection failure and successful explicit reruns are retained. This is not hardware or live LAN acceptance of every product.

Thirty-one new real Office checks passed on delivered DLLs: 16 general checks, 5 synchronization regressions and 10 Commun/print checks. Personal fixtures and raw receipts are private. A missing IO import in the standalone QA launcher was fixed before testing; its preparation log is retained. Refresh may take seconds or tens of seconds, without an instant-update guarantee. Native integration requires Windows desktop Excel.

The actual standard installer was unpacked and all application/optional AutoCAD payload files matched. AutoCAD remains optional, .NET8, without redistributed Autodesk DLLs. The approved four PDF guides and manifest are unchanged. Stream Deck passed official validation and runtime dependency auditing in the recipe.

At publication time the new standard installer has not yet been executed: installation, upgrade, shortcuts and rollback are unexercised in this publication receipt. The authorized personal update requires backups and a separate receipt. Native StageFlow UI, keyboard, full DPI, physical audio, show networks and the actual AutoCAD host are not qualified by these Office/PDF checks. The shared QA account is outside this scope.

macOS remains 2027.1.5 in its existing release, requiring macOS14 or later. No old DMG is renamed 1.7. New Mac artifacts remain separate until actually delivered and qualified.
