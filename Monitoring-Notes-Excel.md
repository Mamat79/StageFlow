# StageFlow — Monitoring, Notes et Excel

## Utiliser les onglets

Sélectionnez un groupe : son patch reste le premier onglet. Cochez **Monitoring** ou **Notes** pour afficher les onglets supplémentaires de ce groupe. Décochez-les pour les masquer ; leur contenu reste enregistré.

Dans Monitoring, ajoutez un wedge ou un circuit IEM. Chaque circuit possède un numéro, un nom, un destinataire, un modèle, une quantité et des notes multilignes. Le numéro doit être unique pour un même type dans ce groupe. La quantité indique le nombre d’enceintes ou de systèmes de ce circuit. Le résumé distingue le nombre de circuits wedges, le nombre d’enceintes et le nombre de circuits IEM.

Notes contient un texte libre propre au groupe. Les circuits et les notes suivent les enregistrements et le fonctionnement LIVE habituel du projet. Leur modification ne produit pas d’alerte de label. Une modification des sources du patch continue de produire les alertes prévues par la session.

## Exporter et imprimer

Dans l’export Excel, choisissez si vous souhaitez inclure Monitoring et Notes. Les informations apparaissent sous chaque patch dans la feuille d’ensemble et après le patch dans chaque fiche de groupe. La visibilité de l’onglet dans StageFlow ne supprime pas ses données et ne remplace pas le choix d’export.

Avec **une page de patch par groupe**, le patch complet est ajusté au recto et Monitoring et Notes commencent à la page suivante. Vérifiez la lisibilité dans l’aperçu et choisissez un papier plus grand si nécessaire. Avec plusieurs pages de patch, le patch peut continuer avant les informations supplémentaires. L’option recto verso réserve un nombre pair de pages à chaque groupe : le groupe suivant commence sur un recto. Les textes longs continuent sur des pages supplémentaires, puis une page de fin complète la fiche si nécessaire. Le bandeau de la fiche donne le nom du groupe ; le nom et le numéro de page figurent en pied de page, sans second titre au-dessus du bandeau.

Dans Excel, sélectionnez les feuilles de groupes à imprimer puis consultez **Fichier → Imprimer**. Activez le recto verso dans les réglages de votre imprimante ; l’option de StageFlow organise les pages du document. Les feuilles Commun et les feuilles techniques ne font pas partie de l’export PDF de fiches.

Sous Windows, le bouton PDF utilise Microsoft Excel de bureau installé. Sur macOS, exportez le XLSX et utilisez les fonctions d’impression ou de PDF de votre tableur. Le rendu PDF automatique par Office est disponible sous Windows.

## Relier volontairement Excel et StageFlow sous Windows

**Tableur** réunit la liaison Excel et les exports dans deux sections : **Classeur lié à Excel** et **Impression et partage**. **Connecter Excel** crée un nouveau classeur lié et l’ouvre dans une instance dédiée de Microsoft Excel de bureau. **Ouvrir un classeur lié** reprend un fichier existant fermé dans Excel. **Afficher Excel** rend visible l’instance liée. Un export XLSX imprimable reste autonome.

La connexion détecte les changements environ toutes les deux secondes sans les appliquer, écrire de cellules ou reconstruire les fiches. Vous pouvez saisir dans chaque application à votre rythme. L’indicateur précise **Excel à mettre à jour**, **StageFlow à mettre à jour** et le nombre de conflits. Cliquez sur **Mettre à jour…** pour comparer les changements puis les appliquer en un seul lot. La mise à jour est toujours volontaire, y compris à la reconnexion.

Dans le classeur connecté, vous pouvez saisir directement les **sources**, **micros** et **commentaires communs** dans **Commun**, ainsi que les **sources et micros propres à chaque groupe**, dans les colonnes déjà présentes. La présentation reste la même. Effacer une valeur propre à un groupe efface cette valeur locale, sans effacer la source commune. Les numéros de paires et les en-têtes restent protégés. Les fiches individuelles de groupes restent des vues imprimables protégées.

Le classeur conserve aussi les trois feuilles d’édition :

| Feuille | Données à modifier |
| --- | --- |
| Edition Patch | Source, Microphone, Notes, IncludeCommon par paire et par groupe |
| Edition Monitoring | Kind, Number, Name, Recipient, Model, Quantity, Notes par circuit |
| Edition Notes | Group, MonitoringVisible, NotesVisible, Notes par groupe |

Les colonnes techniques `_Id` et `_GroupId` sont masquées. Elles relient les lignes au projet même après un tri. Conservez ces colonnes et les noms des tableaux et colonnes. Les en-têtes techniques restent stables quelle que soit la langue d’affichage des fiches.

Pour ajouter un circuit, ajoutez une ligne dans le tableau Monitoring, laissez les identifiants vides et renseignez **Group** avec le nom unique du groupe, **Kind** avec `Wedge` ou `IEM`, **Number** avec un entier positif et **Quantity** avec un entier positif. StageFlow attribue l’identité. En copiant un circuit, copiez seulement les données visibles afin de ne pas dupliquer son identité.

Supprimer une ligne de Monitoring supprime ce circuit. Supprimer une ligne de Patch efface les données de la paire ; la paire conserve son numéro et une ligne vide est rétablie. Créez et supprimez les groupes ou changez le nombre de paires dans StageFlow. Après un changement de structure qui suspend la liaison, déconnectez puis reconnectez Excel en choisissant de créer un nouveau classeur. Les indicateurs utilisent `True` et `False`. Les champs sont validés avant leur application au projet ; un numéro dupliqué, une quantité invalide ou une identité endommagée suspend la liaison avec un message.

Les fiches imprimables sont actualisées lors de la mise à jour volontaire. Les exports utilisent les données actuelles de StageFlow ; un avertissement signale les changements Excel détectés et encore non importés. Dans Commun, seules les cellules du patch décrites ci-dessus sont modifiables ; Monitoring et Notes se modifient dans leurs feuilles d’édition. Les cellules et colonnes personnelles ajoutées dans les feuilles d’édition sont conservées. Une formule dont la valeur est compatible est conservée ; StageFlow suspend une écriture qui remplacerait une formule ou supprimerait des données personnelles ajoutées à une ligne. Une erreur de formule suspend la lecture. Si Commun et Edition Patch contiennent deux nouvelles valeurs différentes pour un même champ, le comparatif vous permet d’abord de choisir chaque valeur du classeur. Ces valeurs sont ensuite comparées à StageFlow, sans écriture intermédiaire. Déverrouiller volontairement une fiche suspend toujours son actualisation pour préserver votre travail.

La liaison conserve la feuille, la cellule sélectionnée et la position de défilement lors des actualisations. Les contrôles en lecture sont planifiés environ toutes les deux secondes. Le transfert et la régénération des fiches, déclenchés uniquement par votre validation, peuvent prendre plusieurs secondes selon le contenu et Office. Ce travail s’exécute sur un fil dédié et StageFlow reste utilisable. Pendant la phase d’écriture et de mise à jour des vues, la saisie dans cette instance Excel est temporairement suspendue ; la barre d’état Excel indique l’actualisation puis reprend son état précédent. Pendant une saisie bloquant Excel, la liaison attend puis reprend automatiquement. Si vous activez un autre classeur dans cette instance dédiée, elle attend que le classeur connecté soit de nouveau actif.

## Conflits, sauvegarde et déconnexion

Des changements indépendants sont réunis automatiquement dans le comparatif. Deux nouvelles valeurs identiques ne sont pas un conflit. Si un même champ contient des valeurs différentes, **Comparer et résoudre…** présente le groupe, la paire ou le circuit, l’ancienne valeur commune et les valeurs des deux applications. Choisissez **StageFlow** ou **Excel** séparément pour chaque conflit : aucun côté n’est choisi par défaut. **Annuler** conserve les deux versions en attente et n’applique rien. Une modification faite pendant la comparaison oblige à relire les valeurs avant tout transfert.

Avant d’écrire, StageFlow valide les données sur une copie du projet et conserve une copie du classeur dans `%LOCALAPPDATA%\StageFlow\ExcelBackups`. Un échec est indiqué comme une mise à jour non terminée, avec le chemin de cette copie ; il ne marque pas les applications comme synchronisées. Relancez le comparatif pour réessayer. Les données invalides, formules personnelles et changements de structure ne sont jamais écrasés silencieusement.

Enregistrez le projet selon votre utilisation habituelle de StageFlow et enregistrez le fichier dans Excel. La synchronisation en mémoire ne remplace pas la sauvegarde du fichier Excel. **Déconnecter Excel** arrête la liaison et laisse le classeur ouvert avec votre travail. Reconnecter reprend ce même classeur tant que StageFlow le conserve. Après une fermeture, **Ouvrir un classeur lié** ouvre volontairement un fichier connecté fermé dans Excel. Son état de synchronisation enregistré permet de détecter les changements faits séparément ; aucune donnée n’est appliquée avant **Mettre à jour…** et votre validation.

La liaison utilise Excel de bureau Windows et nécessite qu’il soit installé. Elle ne relie pas Excel pour le web, un autre tableur ou Excel pour Mac. Les onglets, leur persistance et l’export XLSX sont disponibles dans StageFlow sur Windows et macOS. La connexion Excel ne se réactive pas automatiquement au lancement.

---

## English

Each group opens on its Patch tab. Enable **Monitoring** and **Notes** to show optional tabs; hiding them preserves the data. Monitoring stores wedge and IEM circuits with stable identities, a number, name, recipient, model, quantity and multiline notes. Numbers are unique within a group and circuit type. Group notes are free text. Monitoring and notes use the existing project save and LIVE workflow without label alerts; patch source edits retain the session’s alerts.

Excel export can include monitoring and notes below each overview patch and after the patch in group sheets. With one patch page per group, the complete patch fits on the front and supplements start on the next page. Check readability and choose larger paper if needed. Multiple-page patch mode allows the patch to continue before the supplements. Duplex layout gives each group an even number of pages so the following group starts on a front side. Long notes continue on additional pages. The coloured title identifies the group, with its name and page number in the footer and no duplicate printer header. Enable duplex printing in your printer settings and select the group sheets. Windows PDF export uses installed Microsoft Excel; on macOS export XLSX and print or create a PDF in your spreadsheet application.

**Spreadsheet** groups **Linked Excel workbook** and **Print and share**. **Connect Excel** voluntarily creates and opens a linked workbook in a dedicated Windows desktop Excel instance. **Open a linked workbook** resumes an existing file closed in Excel. **Show Excel** makes that instance visible. An exported printable XLSX remains independent.

Read-only checks approximately every two seconds detect pending changes without applying values, writing cells or rebuilding sheets. The status identifies which application needs updating and counts conflicts. **Update…** compares the changes and applies them together only after your confirmation. Reconnecting never applies data automatically.

Edit sources, microphones and common comments directly on **Commun**, including group-specific sources and microphones in their existing columns. Its appearance stays unchanged. Clearing a group value clears its local override without changing the common source. Pair numbers and headings stay protected; individual group sheets remain protected print views. **Edition Patch**, **Edition Monitoring** and **Edition Notes** remain available. Monitoring and group notes are edited in their editing tables. Keep the table and column names and hidden `_Id` / `_GroupId` identity columns. Sorting does not change identities. Technical headers remain stable in both interface languages. Printable sheets refresh on explicit update. Exports use current StageFlow data and warn about detected Excel edits still awaiting import. Additional user cells and columns on editing sheets are preserved. If Commun and Edition Patch contain different new values for one field, first choose each workbook value in the comparison. The chosen values are then compared with StageFlow without an intermediate write. Deliberately unlocking a print view still suspends its refresh to preserve your work.

To add a circuit, insert a Monitoring table row with blank IDs, a unique **Group** name, **Kind** `Wedge` or `IEM`, and positive integer **Number** and **Quantity** values. Copy visible fields only when duplicating a circuit. Deleting a Monitoring row removes the circuit. Deleting a Patch row clears that pair and restores its blank row without renumbering it. Change group and pair structure in StageFlow. Flags accept `True` / `False`.

Independent edits are merged automatically in the comparison. Identical new values do not conflict. **Compare and resolve…** shows the group, pair or circuit, the last shared value and both current values. Choose StageFlow or Excel separately for each conflict; neither side is selected by default. Cancel keeps both versions pending. If data changes during review, the update is rejected and requires a fresh comparison. Before a write, a complete Excel copy is kept in `%LOCALAPPDATA%\StageFlow\ExcelBackups`. A failed update retains the previous baseline and reports an unfinished update with the backup path; compare again to retry. Invalid data or a formula error pauses synchronization before application. Compatible formulas are preserved; writes that would replace formulas or discard additional user row data are refused. Read-only checks are scheduled approximately every two seconds. Transfer and print-view regeneration can take several seconds and happen only after explicit confirmation. Office work uses a dedicated thread and StageFlow remains responsive. Input in the dedicated Excel instance is temporarily suspended during writes and managed-view updates, with an Excel status message. Excel editing otherwise temporarily suspends synchronization and it resumes automatically. Refreshes preserve the active sheet, selected cell and scroll position.

Save your StageFlow project as usual and save the workbook in Excel. In-memory synchronization does not save the Excel file automatically. Disconnecting leaves the workbook open. Reconnecting can resume the retained instance; **Open a linked workbook** voluntarily opens a connected file closed in Excel and compares against its saved baseline without applying changes until you confirm Update. The link does not reconnect automatically at startup.

Native Office linking is available with installed Windows desktop Excel. Excel for the web, other spreadsheet applications and Excel for Mac are not linked. StageFlow for macOS supports the optional tabs, persistence and XLSX export.
