# TIBOCHOC — Site vitrine

Site vitrine statique (HTML / CSS / JS, sans framework) pour TIBOCHOC, artisan chocolatier à Sapois (Jura).

## Structure du projet

```
/
├── index.html              → page principale (toutes les sections)
├── mentions-legales.html   → page des mentions légales
├── confidentialite.html    → page de politique de confidentialité
├── style.css               → toute la mise en forme et le responsive
├── script.js               → menu mobile, galerie/lightbox, animations légères
├── images/                 → dossier destiné aux vraies photos (voir plus bas)
└── README.md
```

Aucun framework n'a été utilisé. La seule ressource externe est **Google Fonts** (police "Fraunces" pour les titres, "Karla" pour le texte courant), chargée via une simple balise `<link>` — ce n'est pas une bibliothèque logicielle, seulement un fichier de police hébergé par Google, ce qui reste léger et n'ajoute aucune dépendance de code.

## ⚠️ À propos des photos — important

Conformément à votre demande, **aucune image générée par IA n'a été utilisée, et aucune photo trouvée sur Internet n'a été intégrée au site.**

Lors de mes recherches ("Tibochoc Sapois", "Tibochoc chocolatier", etc.), j'ai bien trouvé des photos publiées sur la page Facebook officielle de TIBOCHOC ainsi que sur des fiches d'annuaires (Jura Tourisme, Petit Futé, Mappy...). Cependant, je ne peux pas vérifier avec certitude que ces photos sont libres de droits pour un usage commercial sur un site vendu à un client — les droits d'auteur des photographies appartiennent en général à celui qui les a prises (le photographe, l'auteur du contenu de l'annuaire, etc.), pas automatiquement à TIBOCHOC lui-même. Les utiliser sans autorisation explicite exposerait le site à un risque de contrefaçon.

**Recommandation :** demandez directement à Thibaut (TIBOCHOC) de vous fournir ses propres photos en haute définition (boutique, atelier, produits), ou faites réaliser une séance photo dédiée. C'est la seule option totalement sûre juridiquement, et le résultat sera aussi bien plus fidèle à la véritable identité de la boutique.

En attendant, chaque emplacement photo du site est un bloc "placeholder" élégant (dégradé brun cacao avec une étiquette du type `PHOTO À REMPLACER — ...`) plutôt qu'une image cassée. Cela permet de présenter la maquette au client sans donner l'impression d'un site inachevé.

### Comment remplacer un placeholder par une vraie photo

Dans `index.html`, chaque emplacement photo est un `<div>` ou `<button>` avec la classe `ph-image`, précédé d'un commentaire HTML qui indique exactement quel `<img>` insérer à la place. Exemple :

```html
<!--
  PHOTO À REMPLACER — HERO
  Remplacer le bloc .hero-media ci-dessous par :
  <img src="images/hero-chocolat.jpg" alt="Chocolats artisanaux TIBOCHOC" class="hero-photo">
-->
<div class="hero-media ph-image" data-label="..."></div>
```

Il suffit de :
1. Déposer la photo dans le dossier `images/` (voir noms suggérés dans `images/README-images.txt`).
2. Remplacer le `<div class="ph-image" ...></div>` correspondant par la balise `<img>` indiquée en commentaire juste au-dessus.
3. Garder un texte `alt` descriptif (déjà rédigé dans les commentaires) pour le référencement et l'accessibilité.

## Avis clients

Une section "Avis clients" a été ajoutée (entre la galerie et les informations pratiques), reprenant 3 avis Google que vous m'avez transmis (Burlet Delphine, Patricia Bourge, Coco B.). Le premier avis était tronqué par l'interface Google (bouton "...Plus") : je l'ai indiqué clairement dans le texte plutôt que d'inventer la fin. Si vous avez le texte complet, il suffit de remplacer ce passage dans `index.html` (section `id="avis"`).

## Informations trouvées lors de mes recherches (à vérifier avant publication)

Pour préparer la carte "Nous trouver" et vous faire gagner du temps, j'ai recherché TIBOCHOC sur des sources publiques. Voici ce que j'ai trouvé — **rien n'a été intégré au site en dur sans être marqué comme "à vérifier"**, à l'exception de l'adresse (que vous aviez fournie) et de la carte Google Maps intégrée (qui est un simple plan interactif, pas une photo) :

- Gérant de la société : Thibaut/Thibault Faivre-Vuillin (registre du commerce, RCS Lons-le-Saunier, SARL, SIREN 902 622 968).
- Page Facebook officielle : "Tibochoc-Sapois" — indique un téléphone (06 47 00 24 66) et un e-mail (tibochoc@gmail.com).
- Les horaires trouvés varient selon les fiches et les dates de mise à jour (annuaires professionnels) ; je n'ai donc rien affiché en dur sur le site pour éviter d'indiquer une information erronée aux clients.
- Une seconde boutique semble exister à Champagnole (39300), en plus de l'atelier de Sapois — à confirmer si vous souhaitez la mentionner sur le site.

Merci de confirmer ou corriger ces éléments avant la mise en ligne définitive.

## SEO

- Balises `<title>` et `<meta name="description">` optimisées pour "chocolatier artisanal", "Sapois", "Jura".
- Structure de titres H1 (nom du site) → H2 (titres de section) → H3 (sous-éléments, produits, étapes).
- Données structurées locales (schema.org, type `Bakery`) dans `index.html`, à compléter avec une vraie photo une fois disponible.
- Attributs `alt` prêts à recevoir une description dès l'ajout des vraies photos.

## Déploiement

Le site est 100% statique : il peut être déployé tel quel sur n'importe quel hébergement (OVH, Netlify, Vercel, GitHub Pages...) en copiant simplement l'ensemble du dossier.
