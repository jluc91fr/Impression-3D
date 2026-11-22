# Statuette JN — « Au bienheureux retraité : Vive le Hard Rock ! »

Fichiers STL binaires (unités = mm, prêts pour le tranchage) :

| Fichier | Contenu | Dimensions (mm) |
|---|---|---|
| `statuette_JN.stl` | Ensemble complet : socle + plaque inclinée gravée + buste | 110 × 116 × 116 |
| `socle_JN.stl` | Socle seul : cylindre Ø110 + plaque inclinée 28° avec texte gravé | 110 × 110 × 44 |
| `buste_JN.stl` | Buste seul (tête + cheveux bouclés + lunettes + nez + cou/col) | 68 × 81 × 102 |

Texte gravé (en creux, ~1,2 mm) sur la plaque inclinée :
- Au bienheureux retraité
- Jean-Noël :
- Vive le Hard Rock !
- 26 nov. 2026

## Réglages conseillés Geeetech A20M (255 × 255 × 250, PLA)

- Hauteur de couche : 0,2 mm (0,12 si on veut affiner le texte)
- Buse : 0,4 mm ; texte gravé lisible dès 0,4
- Remplissage : 10–15 %, parois : 3
- Supports : aucun nécessaire (plaque inclinée 28° autoportante)
- Adhérence : brim conseillée (socle Ø110)
- Temps estimé : ~6–8 h (statuette complète)
- Double extrusion (A20M) : possibilité de colorer le col/chemin en rouge en découpant le buste à z≈14–28 mm dans le slicer, en imprimant la partie basse sur la buse rouge.

## Buste seul pour remplacer la tête d'une figurine existante

Échelle à régler dans le slicer : le buste fait 102 mm de haut (cou compris).
Pour une figurine de hauteur H, mettre le buste à l'échelle ≈ H/7,5 et noyer le cou
dans le corps. Il est aussi livrable séparément (`buste_JN.stl`).

## Note sur la méthode

Les 4 photos fournies (petites, angles proches, fond texturé) ne permettent pas une
photogrammétrie fiable (COLMAP ne parvient pas à initialiser une paire correcte).
Le buste est donc une **stylisation paramétrique** reprenant les attributs visibles :
cheveux bouclés clairs, lunettes sombres, chemise rouge (col), nez marqué. Pour une
vraie ressemblance : 25–40 photos nettes en orbite complet autour de la tête
(avec le haut du crâne) puis Meshroom/Polycam ou un scan.
