# StageFlow 2027.1.6

## Français

- Corrige la suspension de la liaison Excel après une modification du patch dans les projets comportant plusieurs groupes. La pagination recto verso concerne uniquement les fiches de groupes ; la feuille récapitulative Commun n'est plus soumise à ce contrôle.
- Une erreur pendant la reconstruction d'une vue Excel restaure son contenu précédent et rétablit sa protection. Une vue volontairement déverrouillée reste préservée et bloque la synchronisation avant l'écriture des tables.
- Les erreurs de synchronisation sont consignées dans le journal de diagnostic pour conserver la première cause.
- La liaison Excel de bureau reste propre à Windows. Sur macOS, cette version conserve les onglets Monitoring/Notes et les exports XLSX, sans annoncer de liaison Office native.

## English

- Fixes Excel synchronization stopping after patch edits in projects with several groups. Duplex pagination applies only to group print sheets; the Commun overview is excluded from this check.
- An interrupted worksheet refresh restores its previous content and protection. Deliberately unlocked print sheets are preserved and stop synchronization before editing the data tables.
- Synchronization errors are written to the diagnostic log so that the original cause remains available.
- Desktop Excel synchronization remains Windows-only. macOS retains Monitoring/Notes tabs and XLSX exports; no native Office link is claimed.


## Livraison / Delivery

Windows 2027.1.6 ; macOS remains 2027.1.5 in its existing release. Native Excel integration is Windows-only.

21 nouveaux contrôles Office sur DLL livrées /21 new real Office checks on delivered DLLs. Standard Setup unpacked byte-for-byte; installation/upgrade/shortcuts/rollback and native StageFlow UI/keyboard/DPI not exercised.

[Contrôles et limites / checks and limits](QUALIFICATION-WINDOWS-2027.1.6.md).
