# StageFlow 2027.1.10 — qualification Windows / Windows qualification

## Français

Cette livraison ajoute cinq commandes d'alertes LIVE aux contrôles externes et au plugin Stream Deck : pause, reprise, basculement, reprise avec envoi volontaire des changements en pause et acquittement local. Le catalogue compte 29 commandes ; le plugin fourni est en version 2026.3.1.0. Mettre à jour StageFlow et son plugin ensemble.

Windows a été construit localement depuis le commit privé `32c4890dc63e3ad47c4049cd6407282f7391588d`, branche `feature/streamdeck-alert-controls`, avec la recette `scripts/build-windows-installer.ps1`, .NET SDK 10.0.401 et Inno Setup 6.4.3. Aucun GitHub Actions Windows n'a été lancé pour cette construction. Le paquet est autonome Windows x64 et son installeur n'est pas signé.

Le véritable installeur a été extrait : 632 fichiers d'application et 5 fichiers du connecteur AutoCAD correspondent au résultat de construction. Les quatre PDF approuvés restent inchangés. Ils décrivent les 24 commandes antérieures ; [l'aide complémentaire](EXTERNAL-CONTROLS.md) explique les cinq ajouts. Aucun PDF n'a été régénéré.

Les preuves source réutilisées comprennent 296 tests .NET et 6 tests Node ; les contrôles ciblés supplémentaires du propriétaire du code sont consignés séparément. La recette Windows a exécuté les 6 tests du plugin, l'audit des dépendances de production et la validation officielle Elgato du paquet. Ces résultats ne constituent pas une nouvelle exécution complète de tous les tests .NET sur Windows.

Le programme contenu dans l'installeur a été exécuté avec un profil et un projet V1 d'essai isolés. Des commandes OSC avec confirmations corrélées ont vérifié les groupes suivant/précédent, le refus de pause sans LIVE, le refus de BLACKOUT sans StageMark connecté, puis la pause LIVE, une véritable modification de label, la reprise et l'envoi volontaire. Le journal global contient exactement le changement attendu, émis au premier envoi ; un second envoi n'ajoute aucun événement. LIVE local n'a pas activé la diffusion réseau. Plusieurs fermetures normales ont terminé avec le code 0.

L'installation standard sur un poste Windows existant a ensuite réussi sans redémarrage. Les 632 fichiers installés et les 5 fichiers du connecteur correspondent au paquet. La version installée est `2027.1.10+32c4890dc63e3ad47c4049cd6407282f7391588d`. Le raccourci unique `StageFlow v2027` cible le bon EXE. Après deux sauvegardes vérifiées sur des volumes distincts, les 40 fichiers du profil personnel et les 16 fichiers du projet récent, dont ses classeurs, sont restés identiques. Le programme réellement installé a démarré sur un profil isolé, produit un rendu interne correct et quitté normalement avec le code 0. Le projet personnel n'a pas été ouvert ni modifié pour cette recette ; la restauration des sauvegardes n'a pas été exercée.

**Limites :** l'outil de capture native a renvoyé une fenêtre blanche pour l'ancienne version 1.9 comme pour la 1.10, tandis que leurs rendus internes étaient corrects. Cela n'établit pas une nouvelle régression d'affichage en 1.10 ; l'acceptation visuelle humaine de l'écran physique n'est pas revendiquée. Aucun Stream Deck physique, périphérique MIDI, réseau LIVE entre postes, projecteur, sortie audio ou AutoCAD en fonctionnement n'a été validé par cette recette. Les preuves macOS sont distinctes. Les projets V1 restent le parcours par défaut ; cette mise à jour ne constitue pas une qualification du partage réseau/LIVE/AutoCAD des projets V2.

## English

This release adds five LIVE-alert controls to the 29-command external-control catalogue and Stream Deck plugin 2026.3.1.0: pause, resume, toggle, resume with explicit sending of paused changes, and local acknowledgement. Update StageFlow and its matching plugin together.

Windows was built locally from private source commit `32c4890dc63e3ad47c4049cd6407282f7391588d` using the supported PowerShell recipe, .NET SDK 10.0.401 and Inno Setup 6.4.3. No Windows GitHub Actions build was used. The self-contained Windows x64 installer is unsigned.

All 632 application files and 5 AutoCAD connector files extracted from the actual installer matched the build output. The four approved PDFs are unchanged and describe the previous 24 commands; the external-controls addendum documents the five additions. Existing source evidence includes 296 .NET and 6 Node tests, with additional targeted owner checks recorded separately. The Windows recipe ran the six plugin tests, production dependency audit and official Elgato package validation; this is not a fresh full .NET test run on Windows.

The packaged application was exercised with an isolated profile and a V1 test project. Correlated OSC acknowledgements and actual application state verified group navigation, rejection without LIVE or a connected StageMark instance, LIVE-alert pause, a real label edit, resume, and explicit sending. The global journal recorded exactly one expected delta at the first send; a second send added nothing. Local LIVE did not enable LAN broadcasting. Normal shutdowns returned code 0.

A standard upgrade on an existing Windows installation succeeded without restarting Windows. Installed application and connector files matched the package, version and desktop shortcut were verified, and the 40 existing personal-profile files and 16 recent-project files, including workbooks, remained byte-identical after two independently verified backups. The installed EXE then produced a correct internal render and exited normally using an isolated profile. The personal project was not opened; backup restoration was not exercised.

**Limits:** native capture returned white for both previous 1.9 and current 1.10, while both internal renders were correct. No new 1.10 display regression was established; physical-screen visual acceptance is not claimed. Physical Stream Deck/MIDI, cross-machine LIVE networking, projection, audio and a running AutoCAD instance were not tested. macOS evidence is separate. V1 remains the default project format; network/LIVE/AutoCAD acceptance of V2 projects is not included.

## SHA-256

```text
617b506b034b7a0b383d14b94f8a4661874d301c164d5c77b44254f13aa3f63c  StageFlow-Setup.exe
3e527a813002618d6cc9a1604fda96899948bf91da79c0bbb2ab4782506f0a54  SiLeMIO-StageFlow.streamDeckPlugin
```
