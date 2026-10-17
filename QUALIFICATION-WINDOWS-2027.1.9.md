# StageFlow 2027.1.9 — Windows et macOS

## Français

Windows provient de `c855b1820281592c27feb19e4553a6c1fa6945ca`. Les quatre fichiers macOS déjà publiés restent strictement inchangés et proviennent de `bbd980c0c7f858ed53fb3c04bc3f378308cace50`. Le correctif de fermeture concerne Windows ; aucun nouveau paquet Mac n'a été reconstruit pour ce correctif.

### Windows

La fermeture finale est reportée après l'événement de fermeture WPF. Cela évite de devoir demander deux fois de quitter lorsque les opérations de nettoyage hors ligne se terminent immédiatement.

- Version installée : `2027.1.9+c855b1820281592c27feb19e4553a6c1fa6945ca`, fichiers Windows 2027.1.9.0, x64 autonome.
- Installeur `StageFlow-Setup.exe` : 63554632 octets, SHA-256 `9fb61cc666bbd7af9d6bda1ff6565e0292775d66c825261d015c66dce0b8a0b4`. Installeur non signé Authenticode.
- Recette officielle exécutée sur Windows ; guides approuvés vérifiés. L'extraction de cet installeur retrouve exactement les 631 fichiers applicatifs et les 5 fichiers du connecteur AutoCAD construits.
- 28 essais ciblés réussis chez le propriétaire des sources (3 WPF et 25 sauvegarde/workspace/arrêt/contrats) ; ils ne sont pas comptés comme de nouveaux essais rejoués par l'atelier.
- Dans la véritable application extraite de cet installeur : projet synthétique V1 de 42 paires et deux groupes copié explicitement vers V2, modification enregistrée puis retrouvée à la réouverture. Les 12 fichiers de départ sont intacts. Chaque instance quitte dès sa première demande normale de fermeture, sans arrêt forcé.
- Installation personnelle standard 2027.1.8 vers 2027.1.9 réussie, même identifiant et emplacement, après deux sauvegardes sur disques physiques distincts et répétition de restauration isolée : 709 fichiers / 232098739 octets dans chaque copie, droits, registre et 2220 dates contrôlés. Le connecteur déjà installé est mis à jour ; AutoCAD était fermé.
- Les 631 fichiers applicatifs et les 5 fichiers du connecteur installés sont conformes. Les 57 fichiers existants du profil, des sauvegardes Excel et du projet personnel sont identiques. Le démarrage ajoute seulement un journal de diagnostic. La véritable application installée démarre en français/thème sombre et quitte dès sa première demande, sans profil de test.
- Exactement un raccourci Bureau `StageFlow v2027`, vers le bon exécutable.

Limites : nettoyage immédiat hors ligne qualifié ; pas de nouvelle recette Excel actif, des dialogues Enregistrer/Annuler, de toute la matrice langues/thèmes/DPI ni du matériel réseau, MIDI, Stream Deck ou AutoCAD. Les notices sont les quatre PDF approuvés, vérifiés octet pour octet ; pas de nouvelle recette visuelle PDF. La restauration a été exercée dans un dossier isolé, pas en remplaçant ensuite le profil personnel par une ancienne version.

V1 reste le parcours par défaut. V2 nécessite une nouvelle copie locale explicite ; aucune migration automatique sur place. V2 réseau/LIVE/AutoCAD n'est pas pris en charge dans cette tranche. Gardez l'original V1 pour les applications anciennes. Les limites déjà publiées concernant les échecs en milieu de copie et les destinations injectées tardivement restent ouvertes.

### macOS — paquets existants conservés

macOS 14 minimum selon les paquets autonomes .NET/ASP.NET 10.0.13. Le producteur Mac rapporte 508 tests Mac réussis et un lancement ARM depuis DMG monté en lecture seule, sans recette visuelle ; Intel est compilé et inspecté, sans exécution native Intel. Signature ad hoc, sans Developer ID ni notarisation. Démontage propre du DMG non établi indépendamment. Ces résultats ne sont pas de nouveaux contrôles Windows. Les quatre fichiers Mac et leurs sommes restent inchangés.

## English

Windows is built from `c855b1820281592c27feb19e4553a6c1fa6945ca`. The existing four macOS assets remain byte-for-byte unchanged, built from `bbd980c0c7f858ed53fb3c04bc3f378308cace50`. This deferred-final-close fix is Windows-specific; no Mac package was rebuilt for it.

The actual Windows Setup was extracted and its 631 application files plus 5 AutoCAD connector files matched the build. A real native synthetic 42-pair/two-group V1 project was explicitly copied to V2, edited, saved and reopened with the edit preserved; all 12 original files remain unchanged. Both native instances exited after their first normal close request. The source owner's 28 targeted passing tests were not rerun or counted again here.

The standard personal upgrade from 2027.1.8 to 2027.1.9 completed successfully with the same application ID and path. Two backups on distinct physical disks and one isolated restore copy each verified 709 files / 232098739 bytes, including permissions, registry and 2220 timestamps. The installed application and existing optional AutoCAD connector matched the verified payload. All 57 existing profile, Excel-backup and personal-project files were preserved; starting the app only added a diagnostic log. The actual installed app started without test-profile overrides and exited on its first close request. One correctly targeted StageFlow v2027 desktop shortcut was verified. Setup is unsigned; its 63554632 bytes have SHA-256 `9fb61cc666bbd7af9d6bda1ff6565e0292775d66c825261d015c66dce0b8a0b4`.

Acceptance covers the immediate offline cleanup path and the observed French/dark interface. Active Excel cleanup, interactive Save/Cancel, the complete language/theme/DPI matrix and physical network/MIDI/Stream Deck/AutoCAD were not newly qualified. The four approved PDFs were checked byte-for-byte, with no new PDF visual review. Restore rehearsal was isolated; no personal downgrade was performed.

V1 remains the default. V2 requires an explicit new local copy, without automatic in-place migration; V2 LAN/LIVE/AutoCAD exchange is not supported in this tranche. Retain V1 originals for older apps. Previously stated mid-copy failure and late destination-injection limitations remain open.

Existing macOS packages declare macOS 14 minimum, self-contained .NET/ASP.NET 10.0.13. The Mac producer reported 508 passing Mac tests and an ARM launch from a read-only mounted DMG without visual acceptance. Intel was cross-built and inspected, not run on native Intel. Ad-hoc integrity signing only; no Developer ID or notarization. Clean DMG unmount was not independently established. These are separate producer results, not new Windows tests.
