# Dossier complet — Le Bon Coin (Korhogo)
### Tout ce qu'on a construit, à transmettre à Claude Design pour la conception du site web

---

## 1. Identité de l'entreprise

- **Nom** : Le Bon Coin
- **Activité** : petit point de vente de motos, avec **livraison à domicile**
- **Ville** : Korhogo, Côte d'Ivoire
- **Marque principale vendue** : Apsonic
- **Contact** : bangalytoure6780@gmail.com
- **Ton de marque** : chaleureux, rassurant, proche du client
- **Ce à quoi les clients sont attachés** : de bonnes motos, la garantie, la nouveauté
- **Arguments de vente répétés partout** : motos bien entretenues · garantie incluse · livraison à domicile · « rouler l'esprit tranquille, sans surprise »
- **Langue du site** : français

---

## 2. Ce qui existe déjà (à réutiliser ou à harmoniser)

### a) Page de destination "Amberlight" (HTML)
Page construite à partir d'une identité "Amberlight Candies" (confiserie, couleurs chaudes), puis détournée pour vendre des motos. L'univers "atelier / lumière du soir" a été gardé.

**Palette**
- Fond crème `#FBF2E3`
- Texte brun foncé (cocoa) `#3B2415`
- Accents : `--honey` (miel), `--ember` (braise), `--amber-deep` (ambre profond), `--peach`, `--line` (bordures fines)

**Typo** : Karla en corps de texte.

**Style** : cartes blanches très arrondies (rayon ~28px) sur fond crème, bordures fines, boutons `btn-primary` (plein) et `btn-ghost` (contour).

**Structure**
1. Nav : *Quiz parfum* · *Notre histoire* · *S'inscrire* + bouton CTA « Accès anticipé »
2. Hero : titre « Des bonbons qui gardent la lumière du soir. » + accroche + 2 boutons
3. Section vedette → quiz interactif
4. Section « Notre histoire » / atelier
5. Formulaire d'inscription
6. Pied de page

**Le quiz olfactif** (3 questions, 3 options chacune, chaque option pointe vers une moto ; score simple, puis carte résultat)
1. Quelle odeur vous attire au réveil ? — miel/pain grillé · café et fumée de bois · épices et cuir
2. Comment aimez-vous rouler ? — ville tranquille · longues routes · une moto qu'on ne voit pas ailleurs
3. Une texture qui vous plaît ? — croquante et légère · fondante et profonde · intense, presque piquante

Carte résultat : nom du modèle, description, garantie, prix, bouton « Réserver un essai » + lien « Refaire le quiz ».

**Les trois motos de la page (fictives)**

| Modèle | Positionnement | Garantie | Prix |
|---|---|---|---|
| Ambre 125 | petite cylindrée révisée, carrosserie miel, débuter en ville | 12 mois | 2 190 € |
| Braise 400 | routière, ronronnement grave, selle basse, longs trajets | 12 mois | 3 450 € |
| Caramel Custom | repeinte à la main, pièce unique de l'atelier | 12 mois | 4 890 € |

### b) Présentation commerciale PowerPoint
Fichier `apsonic_le_bon_coin.pptx`, thème **Golden Hour** : moutarde, terracotta, beige, brun foncé.
6 diapositives : titre · présentation du Bon Coin · pourquoi vendre de l'Apsonic · tableau de la gamme · garantie et service après-vente · contact.

### c) Email de bienvenue (Omnisend)
- **Objet** : « Bienvenue chez Le Bon Coin 🏍️ -10% pour votre première moto »
- **Aperçu** : « Découvrez notre Apsonic Autumn Cabin, bien entretenue et garantie »
- Moto mise en avant : **Apsonic Autumn Cabin**, notée **7/10** en état général
- Offre : **-10% sur la première commande, code BIENVENUE10**
- Bouton : « Je découvre mes motos »
- Palette : terracotta `#C1653D` et crème
- Lien provisoire utilisé : `lebon-coin-korhogo.com` → **à remplacer par le vrai site**

### d) Inventaire Excel
Fichier `inventaire_bon_coin_moto.xlsx`. Colonnes : nom de l'article · modèle · coût de fabrication · prix de vente · marge (formule automatique) · quantité en stock, avec ligne de totaux.
8 modèles d'exemple : Yamaha YBR 125, Honda CG 125, Bajaj Boxer 150, TVS King Deluxe, Suzuki GN 125, Haojue DK150, Sanya SY 125, Royal Enfield Classic 350.

### e) Site PHP / MariaDB (existant)
Petit site développé sous Termux / Acode / SPCK : `index.php`, `connexion.php`, `login.php`, `logout.php`, avec base de données MariaDB. Base d'un espace connexion / compte client si le nouveau site doit s'y raccorder.

---

## 3. Données marché (recherche Apsonic — Côte d'Ivoire)

**Distribution** : Sincerity Group (fabricant) → filiales nationales / représentants de premier rang → plus de 4 500 points de vente au détail. Group Ivoire Moto SARL identifié comme revendeur officiel autorisé (avril 2025). Autres enseignes citées : Ivoire Moto, Lafiara, Blou Group.

**Coûts** : AP125-30 Aloba à environ 700 USD FOB, soit un coût rendu estimé entre **540 000 et 630 000 FCFA**.

**Prix de l'occasion** : annonces Apsonic 125 à Abidjan entre **200 000 et 405 000 FCFA**. Pour Korhogo (marché moins tendu), fourchette de travail retenue : **250 000 à 350 000 FCFA**, avec un repère autour de **300 000 FCFA** pour une moto en bon état visuel, sous réserve que le moteur tourne bien et que les papiers soient en règle.

**Ce qui fait le prix d'une occasion, par ordre d'importance** : état moteur → papiers/carte grise → pneus, freins, chaîne → kilométrage → carrosserie.

**Canaux de vente pertinents** : WhatsApp Business, Facebook Marketplace, TikTok, CoinAfrique. Le **paiement échelonné** est un vrai levier de conversion (Molo Molo Pay en Côte d'Ivoire).

**Les trois erreurs les plus fréquentes des nouveaux vendeurs de motos** :
1. sous-estimer le fonds de roulement et le coût de portage du stock ;
2. négliger le service après-vente et la disponibilité des pièces détachées ;
3. faire crédit aux clients sans mécanisme de recouvrement.

---

## 4. Recommandations pour le site web

**Sections à prévoir**
- Accueil : accroche + les 3 promesses (entretien, garantie, livraison à domicile)
- Catalogue des motos : photo, modèle, état noté sur 10, garantie, prix en FCFA, bouton WhatsApp
- Quiz « Quelle moto vous correspond ? » (reprendre le mécanisme du quiz, mais sur des critères réels : usage, budget, cylindrée)
- Livraison à domicile : comment ça marche, zones couvertes
- Garantie et service après-vente : point fort à mettre en avant, vu que c'est l'erreur n°2 du secteur
- Paiement échelonné, si mis en place
- Notre histoire / le point de vente à Korhogo
- Inscription à la newsletter (relié à Omnisend) avec le code BIENVENUE10
- Contact : WhatsApp en priorité, plus l'email

**Contraintes techniques à signaler**
- Public majoritairement sur mobile et sur connexion limitée → site léger, images compressées, mobile-first
- Bouton WhatsApp flottant plus utile qu'un formulaire de contact classique
- Prix en **FCFA**, pas en euros

---

## 5. Trois points à trancher avant la conception

1. **Le nom du site.** « Amberlight » (marque à part, univers ambre/braise) ou « Le Bon Coin » (le nom réel de l'activité) ? Le hero actuel parle encore de bonbons — il faut réécrire le titre.
2. **Les modèles affichés.** Ambre 125 / Braise 400 / Caramel Custom sont fictifs. À remplacer par les vraies motos en stock (Apsonic Autumn Cabin, etc.) avec leurs vrais prix en FCFA.
3. **Le nom de domaine.** `lebon-coin-korhogo.com` a été utilisé comme lien provisoire dans l'email Omnisend — à confirmer ou à changer, puis à reporter partout.
