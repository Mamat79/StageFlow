# StageFlow 2027.1.10 — qualification macOS / macOS qualification

## Français

Les deux DMG autonomes macOS 14 ou ultérieur proviennent du produit Mac `d3bcbd3fe510626630301fa797ce519566e86fa9`, construit par la recette `1a5ca52f506ee47b0bc590f6dc25f444a06a6eb9`, job Codemagic `6ade31b36a35c6f3d9b01e71`. Le paquet Windows de cette livraison provient séparément de `32c4890dc63e3ad47c4049cd6407282f7391588d` ; il n'a pas été reconstruit pour le correctif Mac.

Le démarrage graphique Mac privilégie désormais OpenGL, avec un repli logiciel. Le précédent chemin Metal avait rencontré des erreurs de compilation de shaders pendant la qualification. Le nouveau vrai DMG Apple Silicon a été monté puis son application exécutée au démarrage et après ouverture d'un projet d'essai : fermeture normale avec code 0 en respectivement 130 ms et 68 ms, sans arrêt forcé. Aucune des erreurs de shaders précédemment observées n'a été retrouvée dans ces deux journaux. Les trois fichiers d'entrée et les profils protégés sont restés inchangés ; le profil récent utilisait uniquement le projet d'essai.

**517 tests .NET ont réussi sur le runner Apple Silicon** : 43 Mac, 218 Desktop Core, 161 Core et 95 Remote. Les quatre fichiers TRX concordent avec ces résultats. Les 6 tests du plugin embarqué ont également réussi. La recette a contrôlé sa provenance avant l'environnement, avant les DMG et en fin de construction. Les deux manifestes de paquets concordent avec l'empreinte des 120 fichiers sources retenus ; l'assemblage principal livré correspond à son manifeste.

Les architectures et composants Mach-O des deux éditions, le caractère autonome .NET 10, les dépendances MIDI, les quatre PDF approuvés du lot 2027.4, le manifeste des guides, le plugin Stream Deck embarqué et l'aide complémentaire des 29 commandes ont été contrôlés. Les PDF restent inchangés et décrivent les 24 commandes antérieures ; les cinq ajouts sont documentés dans `EXTERNAL-CONTROLS.md`. Les sommes SHA-256 des DMG et leurs fichiers de contrôle ont été vérifiés.

**Limites :** les exécutions Apple Silicon sont non visuelles ; elles ne prouvent pas une recette humaine des fenêtres, du clavier, de la souris ou du DPI. Intel a été construit sur Apple Silicon et inspecté, sans exécution sur un Mac Intel. Aucun Stream Deck/MIDI physique, audio, projection, téléphone, réseau LIVE entre postes, AutoCAD ou Excel connecté n'a été validé. Les paquets portent uniquement une signature d'intégrité ad-hoc, sans Apple Developer ID ni notarisation. macOS 14 est le minimum déclaré ; aucune matrice d'anciens systèmes n'a été exercée. Le nettoyage du runner prévoit des tentatives de démontage et un recours forcé ; l'absence finale de tout montage n'a pas été prouvée indépendamment. Les deux tentatives antérieures en échec restent des échecs distincts ; leurs DMG ne sont pas ceux de cette livraison.

## English

The self-contained macOS 14+ Apple Silicon and Intel DMGs were built from Mac product commit `d3bcbd3fe510626630301fa797ce519566e86fa9`, recipe commit `1a5ca52f506ee47b0bc590f6dc25f444a06a6eb9`, Codemagic job `6ade31b36a35c6f3d9b01e71`. Windows uses its separately qualified product commit `32c4890dc63e3ad47c4049cd6407282f7391588d` and was not rebuilt for this Mac fix.

Mac rendering now prefers OpenGL with software fallback. The previous Metal path encountered shader compilation errors during qualification. The actual Apple Silicon DMG was mounted and its app launched both initially and with a test project. Normal quit returned exit code 0 in 130 ms and 68 ms respectively, without forced termination. No previous Metal shader compilation errors were observed in these logs. The three input files and protected profiles remained unchanged.

**517 .NET tests passed on the Apple Silicon runner**: 43 Mac, 218 Desktop Core, 161 Core and 95 Remote, corroborated by four TRX files. Six embedded-plugin tests also passed. Three provenance guards, a fingerprint of 120 selected source files, both candidate manifests and the shipped main assembly were checked. Both CPU architectures, Mach-O components, self-contained .NET 10 and MIDI dependencies, the four unchanged approved PDFs, their guide manifest, embedded Stream Deck plugin and 29-command help were inspected. DMG hashes and portable checksum sidecars were verified.

**Limits:** Apple Silicon launch/project/quit checks were nonvisual. Intel was cross-built and structurally inspected only. Full mouse/keyboard/DPI acceptance, physical MIDI/Stream Deck, audio, projection, phone, cross-machine LIVE networking and connected AutoCAD/Excel were not performed. Packages have ad-hoc integrity signing only, without Developer ID or Apple notarization. macOS 14 is the declared minimum; older OS versions were not tested. Runner cleanup includes detach retries with a forced fallback; the final absence of all mounts was not independently proven. Earlier failed attempts remain separate failures and their DMGs are not distributed here.

## SHA-256

```text
ecd519d10b774f2f7c700bed7675a00bd21f22135dbcf68e3f1a49a4bd730f6c  StageFlow-2027.1.10-macos-arm64.dmg
876b6b04d479e90472169e5af37df37cbdd32186c951f40d2fc20062e399f281  StageFlow-2027.1.10-macos-x64.dmg
5ecefc13ab77f1e2f4f3bae54dd862e7c4515cbde1aab9aca27b5204662e4a79  SiLeMIO-StageFlow-Mac.streamDeckPlugin
```
