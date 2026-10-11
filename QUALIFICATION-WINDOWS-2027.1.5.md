# StageFlow 2027.1.5 — Windows checks and limits / Contrôles et limites

## Français

Source privée exacte : `96b1f8e2eaa8b5876d25218410ca84769ee14491`. Windows x64, autonome avec runtime fourni. Installeur standard non signé ; EXE `2027.1.5+96b1f8e2eaa8b5876d25218410ca84769ee14491`.

595 tests .NET et 41 tests JavaScript réussis. 16 scénarios Microsoft Excel 365 de bureau ont utilisé les DLL du produit livré : liaison dans les deux sens, tris, modifications concurrentes, conflits explicites, conservation des formules, sauvegarde/reconnexion et export PDF. La réactivité du dispatcher et la pagination avec notes longues ont été contrôlées.

L'installeur standard a été exécuté dans un compte de recette, puis pour remplacer la 2027.1.3 sur le poste Windows : 631 fichiers exacts, réglages personnels conservés, raccourcis et registre vérifiés. Le programme réellement installé a ouvert une démonstration isolée, produit un rendu interne lisible et quitté normalement.

**Limite connue de qualification** : la capture native de la fenêtre Windows et la navigation au clavier ne sont pas validées. Les essais de capture donnent du blanc/noir ; la cause n'est pas établie et ce constat ne prouve ni un affichage correct ni un défaut du produit. Les rendus internes ne remplacent pas une observation native. La matrice DPI 125/150/200 % n'a pas été qualifiée.

Le connecteur AutoCAD .NET 8 est inclus comme option et met à jour un connecteur déjà présent ; ses cinq fichiers sont vérifiés. L'exécution réelle dans AutoCAD, le matériel audio/MIDI/Stream Deck et le retour arrière n'ont pas été testés pour ce lot. Aucun paiement ou mécanisme d'activation n'est ajouté : StageFlow et son connecteur restent gratuits.

La liaison Office est propre à Excel de bureau Windows ; aucune liaison native Excel Mac n'est annoncée. Les téléchargements Mac doivent conserver leur numéro exact distinct de la version Windows jusqu'à publication de paquets qualifiés.

## English

Exact private source commit: `96b1f8e2eaa8b5876d25218410ca84769ee14491`. Self-contained Windows x64. Unsigned standard installer; executable product version `2027.1.5+96b1f8e2eaa8b5876d25218410ca84769ee14491`.

595 .NET tests and 41 JavaScript tests passed. 16 desktop Microsoft Excel 365 scenarios used the shipped product DLLs: two-way synchronization, sorting, concurrent edits, explicit conflicts, preserved formulas, saving/reconnection and PDF export. Dispatcher responsiveness and long-note pagination were checked.

The standard installer was run in a QA account and for an upgrade from 2027.1.3: 631 matching files, preserved personal settings, verified shortcuts and registry. The actually installed executable opened an isolated demonstration, produced a readable internal render and exited normally.

**Known qualification limit:** native Windows window capture and keyboard navigation are not validated. Capture attempts produce white/black images; their cause is not established. This proves neither correct display nor a product defect. Internal renders do not replace native observation. DPI 125/150/200% qualification remains incomplete.

The optional .NET 8 AutoCAD connector updates an existing connector; its five packaged files were verified. Actual use inside AutoCAD, audio/MIDI/Stream Deck hardware and rollback were not exercised for this delivery. StageFlow and its connector remain free, without activation.

Native Office linking requires Windows desktop Excel. No native Excel Mac link is claimed. macOS downloads retain their own exact version until corresponding qualified packages are published.
