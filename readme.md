Ce readme est basé sur deux (2) fichier a savoir fichier index.html et style.css.

A. Explication du fichier HTML

   <!DOCTYPE html>
# Indique au navigateur que le document est en HTML.

   <html lang="fr">
# Le contenu de la page est en français.

<head>
    <meta charset="UTF-8">
# Définit l’encodage en UTF-8 (gère les caractères spéciaux comme é, è, à...).

    <meta name="viewport" content="width=device-width, initial-scale=1.0">
# Rend la page responsive (adaptée aux mobiles et tablettes).

    <title>Single Price Grid</title>
# Titre de la page (visible dans l’onglet du navigateur).

    <link rel="stylesheet" href="style.css">
# Lien vers la feuille de style CSS externe.


#Corps du document
   <body>
     <main class="card">
# Le contenu principal est contenu dans une balise <main> avec la classe card (carte centrale).

Section 1 : En-tête
<section class="card-hearder">
    <h2>Join our community</h2>
    <p class="p1">30-day, hassle-free money back guarantee</p>
    <p>Gain access to our full library...</p>
</section>
# Cette partie contient le titre principal et un texte d’accroche.
# class="p1" sert à appliquer un style particulier au premier paragraphe.

Section 2 : Contenu principal
<section class="main">
# Conteneur principal des deux blocs : plan tarifaire et avantages.

Sous-section : Plan tarifaire
<section class="card-plan">
    <div class="div1">
        <h3>Monthly Subscription</h3>
        <p class="price">$29<span> per month</span></p>
        <p>Full access for less than $1 a day</p>
        <button class="button">Sign Up</button>
    </div>
</section>

# Contient le prix, la description, et un bouton d’inscription.
.price : met en avant le tarif.
<span> : texte secondaire (“per month”).
.button : bouton stylisé via CSS. #

Sous-section : Pourquoi nous choisir
<section class="card-whyus">
    <div class="div2">
        <h3>Why Us</h3>
        <ul>
            <li>Tutorials by industry experts</li>
            <li>Peer & expert code reviews</li>
            ...
        </ul>
    </div>
</section>
# Liste des avantages sous forme de puces (<ul> et <li>).

B. Explication du fichier CSS

Réinitialisation des marges
* {
    margin: 0;
    padding: 0;
}
# Supprime les marges et les espacements par défaut du navigateur.

Corps de la page
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: aliceblue;
    font-family: Arial, sans-serif;
}
# Centre la carte au milieu de l’écran (verticalement et horizontalement).
# Définit une hauteur de 100% de la fenêtre (100vh) et un fond bleu clair.

Carte principale
.card {
    border-radius: 10px;
    overflow: hidden;
    width: 620px;
}
# Crée une carte avec des bords arrondis.

En-tête
.card-hearder {
    background-color: white;
    padding: 40px;
}
.card-hearder h2 {
    margin-bottom: 15px;
}
.p1 {
    color: hsl(71, 73%, 54%);
    margin-bottom: 10px;
}
# Fond blanc pour la section supérieure, texte espacé et coloré pour l’accroche.

Section du plan tarifaire
.card-plan {
    background-color: #1eb8a8;
}
.div1 {
    display: flex;
    flex-direction: column;
    padding: 30px;
}
.price {
    font-size: 2rem;
    font-weight: bold;
}
.button {
    background-color: #c4f13b;
    border-radius: 10px;
    font-weight: bold;
}
# Couleur turquoise pour le plan, bouton vert vif et mise en page verticale.

Section “Why Us”
.card-whyus {
    background-color: #43d6c7;
}
.div2 {
    padding: 20px;
}
ul {
    list-style: none;
    line-height: 25px;
}
# Liste sans puces, bien espacée, sur fond bleu clair.

Responsive design
@media (max-width: 768px) {
  .main {
    flex-direction: column;
  }
}
# Quand la largeur de l’écran est inférieure à 768px (mobile/tablette),
les deux blocs s’empilent verticalement.