# Statuette JN — « Au bienheureux retraité : Vive le Hard Rock ! »

Fichiers STL binaires (unités = mm, prêts pour le tranchage) :

| Fichier | Contenu | Dimensions (mm) |
|---|---|---|
| `statuette_JN.stl` | Ensemble complet : socle + plaque inclinée gravée + buste | 110 × 116 × 116 |
| `socle_JN.stl` | Socle seul : cylindre Ø110 + plaque inclinée 28° avec texte gravé | 110 × 110 × 44 |
| `buste_JN.stl` | Buste seul (tête + cheveux bouclés + lunettes + nez + cou/col) | 68 × 81 × 102 |
| `figurine_JeanNoel_socle_plaque.stl` | Figurine en pied : guitariste entier (tête intégrée) sur socle + plaque gravée | 170 × 126 × 210 |

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

## Figurine en pied — intégration de la tête (vérifiée)

`figurine_JeanNoel_socle_plaque.stl` : corps entier en pose de guitariste, tête sculptée
(cheveux bouclés, lunettes, nez) raccordée au cou, le tout sur le socle à plaque gravée.
Contrôles passés sur le maillage final :

- maillage unique et étanche (383 548 triangles), orientation cohérente ;
- aucune arête non-manifold, aucune face dégénérée ni doublon ;
- la jonction tête/cou est continue sur les sections z ≈ 160→183 mm, sans point
de pincement ni paroi trop fine ;
- la tête porte les attributs du buste : cheveux bouclés, lunettes, nez marqué
(voir les aperçus `rnd_tete_face.png`, `rnd_tete_profil.png`, et
`rnd_figurine_face.png` / `rnd_figurine_iso.png` pour l'ensemble).

Impression de cette figurine (Geeetech A20M) :

- hauteur 210 mm (≤ 250 mm) et empreinte 170 × 126 mm : tient sur le plateau 255 × 255 ;
- supports recommandés sous les bras et la guitare (porte-à-faux), le socle restant autoportant ;
- la tête et la plaque sont les zones de détail : 0,12–0,2 mm de couche conseillé ;
- volume du maillage ≈ 560 cm³ : session d'impression longue, prévoir une nuit.

## Note sur la méthode

Les 4 photos fournies (petites, angles proches, fond texturé) ne permettent pas une
photogrammétrie fiable (COLMAP ne parvient pas à initialiser une paire correcte).
Le buste est donc une **stylisation paramétrique** reprenant les attributs visibles :
cheveux bouclés clairs, lunettes sombres, chemise rouge (col), nez marqué. Pour une
vraie ressemblance : 25–40 photos nettes en orbite complet autour de la tête
(avec le haut du crâne) puis Meshroom/Polycam ou un scan.
