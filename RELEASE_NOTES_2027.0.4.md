# StageFlow v2027.0.4 - Windows

StageFlow reste gratuit, facultatif et pleinement autonome. Cette corrective
Windows consolide la présentation de la suite et les échanges avec AutoCAD.

## Ce qui change

- Le bandeau conserve l'identité StageFlow à gauche et aligne Connexion,
  alertes, thème, langue, Guide et Aide à droite, y compris quand la fenêtre
  change de largeur.
- Les dialogues et contrôles utilisent des couleurs et polices lisibles dans
  les thèmes Clair et Sombre.
- Les alertes de labels et les projets commencés dans StageDesk ou StageMon
  conservent leur état et les domaines propres à chaque logiciel.
- L'impression Excel propose les formats disponibles et une pagination adaptée
  aux patchs denses, tout en conservant les métadonnées visibles au réimport.
- Le connecteur AutoCAD protège désormais son remplacement lorsqu'AutoCAD est
  ouvert. Le flux LIVE transmet l'alerte, puis l'actualisation explicite charge
  le nouveau label sans placement automatique.
- Le plugin Stream Deck, les notices françaises et anglaises et le guide commun
  sont inclus dans l'installateur.

## Compatibilité et sécurité

Le format `.stageflow` reste évolutif : chaque logiciel écrit uniquement son
domaine et préserve les données qu'il ne possède pas. Une connexion LIVE ne
démarre jamais l'audio, la projection ou une action Dante. Le connecteur AutoCAD
reste facultatif et réservé à AutoCAD 2026 sous Windows.

Fermez StageFlow et AutoCAD après avoir enregistré avant de lancer
l'installation. Cette livraison ne modifie pas les paquets macOS 2027.0.3.

---

# StageFlow v2027.0.4 - Windows

StageFlow remains free, optional and fully standalone. This Windows corrective
consolidates the suite presentation and AutoCAD interoperability.

## Changes

- The header keeps the StageFlow identity on the left and aligns Connection,
  alerts, theme, language, Guide and Help on the right at supported widths.
- Dialogs and controls remain readable in Light and Dark themes.
- Label alerts and projects originating in StageDesk or StageMon preserve each
  application's state and owned domains.
- Excel printing supports available paper sizes and practical pagination for
  dense patches while retaining visible metadata on reimport.
- The AutoCAD connector now protects replacement while AutoCAD is running.
  LIVE sends the label alert, then explicit refresh loads the new label without
  placing anything automatically.
- The Stream Deck plugin, French and English manuals and shared suite guide are
  included with the installer.

## Compatibility and safety

The `.stageflow` format remains extensible: each application writes only its
owned domain and preserves unknown data. A LIVE connection never starts audio,
projection or a Dante action. The optional AutoCAD connector remains limited to
AutoCAD 2026 on Windows.

Save and close StageFlow and AutoCAD before running the installer. This release
does not modify the macOS 2027.0.3 packages.
