# StageFlow 2027.1.5 — Windows

## Français

- Onglets Monitoring et Notes facultatifs par groupe, masquables sans effacer les données.
- Circuits wedges et IEM : identités stables, numéro, nom, destinataire, modèle, quantité et notes multilignes. Totaux des circuits et wedges.
- Les informations de monitoring et notes sont conservées dans le projet et partagées par son fonctionnement LIVE, sans alerte de label. Le vrai patch conserve ses alertes.
- Export Excel avec choix monitoring/notes, informations sous chaque patch et fiches de groupes avec verso et pages supplémentaires lisibles. Export PDF Windows par Microsoft Excel installé.
- Liaison bidirectionnelle volontaire avec Excel de bureau Windows : tableaux d'édition identifiés, vues imprimables actualisées, conflits à résoudre explicitement et conservation des formules utilisateur. Excel reste requis et le classeur doit être ouvert pour la liaison.
- La liaison native Office est propre à Windows ; sur macOS, les onglets, la persistance et les exports XLSX sont disponibles. Aucune liaison Office Mac n'est annoncée.
- Aucun changement des autres logiciels de la suite, des guides approuvés ou de la cible .NET 8 du connecteur AutoCAD.

Le paquet Windows est construit et vérifié ; l’installeur standard et le remplacement de 2027.1.3 ont été contrôlés. Les tests métier, Excel 365 et PDF passent. La capture native de la fenêtre et le clavier restent non qualifiés ; les captures blanches/noires ne permettent pas d’en établir la cause. Le connecteur est vérifié par ses fichiers, sans recette réelle dans AutoCAD. Voir QUALIFICATION-WINDOWS-2027.1.5.md. Les paquets Mac 2027.1.5 ne sont pas inclus dans ce lot Windows ; leurs fonctions restent soumises à leur publication et qualification séparées.

## English

- Optional Monitoring and Notes tabs for each group; hiding a tab preserves its data.
- Wedge and IEM circuits: stable identities, number, name, recipient, model, quantity and multiline notes, with circuit and wedge totals.
- Monitoring and notes are saved in the project and shared through its existing LIVE workflow without label alerts. Actual patch edits retain their alerts.
- Excel export can include monitoring and notes below patches, with group sheets, reverse sides and readable overflow pages. Windows PDF export uses installed Microsoft Excel.
- Voluntary two-way link with Windows desktop Excel: identified editing tables, refreshed print views, explicit conflict resolution and preserved user formulas. Excel is required and the linked workbook must be open.
- Native Office linking is Windows only; macOS supports the tabs, persistence and XLSX exports. No Office Mac link is claimed.
- No changes to other suite products, approved guides or the AutoCAD connector's .NET 8 target.

The Windows package, standard installer and upgrade from 2027.1.3 were verified. Business, Microsoft 365 and PDF checks passed. Native window capture and keyboard behavior remain unqualified; white/black captures do not establish a cause. AutoCAD package files were verified without testing inside AutoCAD. See QUALIFICATION-WINDOWS-2027.1.5.md. macOS 2027.1.5 packages are not included in this Windows delivery and remain subject to separate release and qualification.
