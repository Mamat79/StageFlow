# StageFlow 2027.1.11 — macOS

## Français

Produit `b7be8d363aa24dd32751675efdebd6ee8277b748`, recette `8e821aed1b82bbc8ce10468f48a37b562468fc87` (verrou de source uniquement). Codemagic Apple Silicon a construit les DMG arm64 et x64 autonomes .NET10, macOS14 minimum. Les518 tests .NET ont réussi :44 Mac,218 DesktopCore,161 Core,95 Remote ; le cas CoreMIDI est cette fois exécuté sur Mac. Les6 tests du plugin Stream Deck réellement embarqué ont réussi : version2026.3.1.0,29 commandes. Les quatre PDF approuvés et les identités Mach-O ont été vérifiés.

Le véritable DMG Apple Silicon a été monté en lecture seule ; son application a été lancée sans et avec un projet d'essai puis fermée normalement, code0, sans arrêt forcé. Aucun diagnostic de compilation Metal observé ; OpenGL et repli logiciel sont conservés. Les entrées et profils réels protégés sont inchangés ; seules les écritures du profil d'essai et du runtime étaient permises. Cette recette CI est non visuelle : aucune capture d'écran native ni recette humaine de souris/clavier n'est revendiquée. Les rendus source sans écran restent une preuve séparée.

Le DMG Intel est cross-compilé et inspecté sur Apple Silicon, sans exécution native Intel. Signature d'intégrité ad-hoc, sans Developer ID ni notarisation Apple. Matériel MIDI/Stream Deck, audio, projection et réseau physique non validés. Liaison COM Excel et connecteur AutoCAD restent propres à Windows. V1 demeure le parcours par défaut ; les échanges réseau/LIVE/AutoCAD de V2 ne sont pas qualifiés.

## English

Product `b7be8d363aa24dd32751675efdebd6ee8277b748`, recipe `8e821aed1b82bbc8ce10468f48a37b562468fc87` (source-pin change only). Codemagic Apple Silicon built self-contained .NET10 arm64/x64 DMGs for macOS14+. All518 .NET tests passed:44 Mac,218 DesktopCore,161 Core and95 Remote, including CoreMIDI on Mac. Six tests exercised the actual embedded Stream Deck package2026.3.1.0 with29 commands. Approved PDFs and Mach-O identities were verified.

The actual ARM DMG was mounted read-only and its application started without/with a fixture project, then quit normally with exit0 and no forced termination. No Metal shader compilation error was observed; OpenGL/software fallback is retained. Inputs and protected real profiles remained unchanged; only fixture-profile/runtime scratch writes were permitted. This CI acceptance is nonvisual and does not certify native screenshot or human mouse/keyboard behavior. Source headless renders remain separate evidence.

Intel was cross-built and inspected on Apple Silicon, not executed on native Intel hardware. Ad-hoc integrity signing, no Developer ID or Apple notarization. No physical MIDI/Stream Deck, audio, projection or network acceptance. Excel COM linking and the AutoCAD connector remain Windows-only. V1 is the default; V2 network/LIVE/AutoCAD exchanges are unqualified.
