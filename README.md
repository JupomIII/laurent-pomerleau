# Portfolio de Laurent Pomerleau — kayak de vitesse et basketball

Site vitrine statique (HTML, CSS et JavaScript), sans étape de compilation. Les textes et images se modifient directement dans les fichiers ci-dessous.

## Aperçu local

Ouvre `index.html` dans un navigateur. Pour tester aussi le PDF et les images avec un serveur local :

```bash
python -m http.server 4173
```

Puis visite <http://localhost:4173>.

## Où faire les changements ?

| Je veux…                                            | Fichier ou dossier  |
| --------------------------------------------------- | ------------------- |
| Modifier les textes et les sections                 | `index.html`        |
| Modifier couleurs, polices, espacements et mobile   | `style.css`         |
| Modifier le menu mobile ou le formulaire e-mail     | `script.js`         |
| Ajouter les photos                                  | `assets/photos/`    |
| Ajouter ou remplacer un logo de sponsor             | `assets/sponsors/`  |
| Mettre à jour les résultats sportifs | Section **Mes réalisations** dans `index.html` |

## Emplacements photo

Les photos ont été retirées du site. Chaque emplacement est un bloc `<div class="ph">` (ou `class="ph ph-dark"` sur fond sombre) qui affiche « photo à venir ». Pour mettre une image, dépose-la dans `assets/photos/` puis remplace le bloc par une balise `<img>` :

```html
<figure class="profile-photo">
  <img src="assets/photos/portrait.jpg" alt="Laurent Pomerleau sur le quai" loading="lazy" />
</figure>
```

Il y a six emplacements de galerie (section **En images**), un portrait dans **Mon profil**, un bandeau dans le hero et une photo verticale dans **Mes réalisations**. Garde le conteneur (`<figure>` ou `.hero-image`) : le style d’origine est déjà prévu pour une image qui remplit son cadre.

## Personnaliser le portfolio

1. Dans `index.html`, remplace les textes de présentation et les informations à personnaliser.
2. Dans la section **Mes réalisations**, ajoute ou modifie les saisons (`div class="season"`) et les blocs (`div class="season-block"`) : une année, puis une rubrique par discipline.
3. Dans la section **Partenaires**, remplace les emplacements « votre logo ici » par une carte. Dépose d’abord le logo dans `assets/sponsors/`, puis copie le bloc d’un partenaire :

   ```html
   <figure class="sponsor">
     <div class="sponsor-logo">
       <img
         src="assets/sponsors/nom-du-sponsor.png"
         alt="Nom du sponsor"
         loading="lazy"
       />
     </div>
     <figcaption>
       Nom du sponsor
       <small>depuis 2024</small>
     </figcaption>
   </figure>
   ```

   Le texte de la `figcaption` s’affiche sous le logo : le nom, puis une précision en petites capitales. Pour un logo clair ou blanc, ajoute la classe `sponsor-dark` à la `figure` pour obtenir un fond bleu encre :

   ```html
   <figure class="sponsor sponsor-dark">
   ```

   Les logos sont mieux rendus avec un fond transparent.

4. L’adresse de contact est `laurentpomerleau12@gmail.com` et le téléphone `873-878-3023` : ils figurent dans la section **Contact**, dans le pied de page (`index.html`) et dans `script.js` pour le formulaire. Modifie les trois endroits s’ils changent.

Les chemins des ressources sont relatifs à la racine du projet. Garde cette organisation et ces chemins quand tu déplaceras ou ajouteras des fichiers.
