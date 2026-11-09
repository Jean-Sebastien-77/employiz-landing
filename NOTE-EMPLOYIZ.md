# EmployiZ · Note de création

Maquette : `employiz/index.html` (fichier unique, sans dépendance, captures produit dans `employiz/assets/`).

## 1. Concept : « Rendre visible l'invisible », le Z comme chemin de la donnée

Le Z n'est pas un ornement : c'est le trajet de la donnée. Barre du haut = la DSN brute, diagonale = la lecture par EmployiZ, barre du bas = des indicateurs lisibles. Ce trajet est mis en scène une seule fois, en grand, dans la section 02 : six blocs réels de la DSN (S21.G00.30 Individu, .40 Contrat, .51 Rémunération, .60 Arrêt de travail, .62 Fin du contrat, .70 Affiliation prévoyance) sont lus un par un pendant que le Z se trace et que les indicateurs correspondants s'allument.

## 2. Choix de design

- **Rythme sombre / clair** : hero, révélation, cabinets, sécurité et conversion en encre profonde ; piliers, produit, feuille de route, fonctionnement et FAQ sur papier clair. Le produit, lui, reste clair partout (comme l'application réelle), ce qui le fait ressortir sur les fonds sombres.
- **Couleurs** : encre `#070A1C` (dérivée du bleu nuit de lezebre.io), papier `#F5F4F0`, **citron fluo `#C6FF2E` réservé à la marque et aux actions** (Z, boutons, état actif). Cyan `#36BCD4` pour la donnée et rose `#FF0093` pour le seul Signal leZèbre : ce sont les deux couleurs de graphique de l'application actuelle, conservées pour la cohérence.
- **Typographie** : une grotesque contemporaine à graisse variable pour tout, titres très serrés ; une monospace uniquement pour ce qui relève du fichier (codes DSN, noms de fichiers, index).
- **Cockpit** : reconstruit en HTML (net à toutes les tailles, animable) à partir des modules réels de RH BI : barre latérale identique (Accueil, Effectifs, Masse salariale, Détail salariés, Absentéisme, Turnover, Égalité professionnelle, Santé & Sécurité, Couvertures, Évolutions, Alertes), sélecteur de société et de période, bouton « Charger ma DSN ». Données fictives mais cohérentes entre elles (47 salariés, 162 480 € de masse mensuelle donc 3 457 € de moyenne, 43 couverts en santé sur 47 donc 91,5 % sous le seuil de 95 %, etc.).
- **Preuve** : les vraies captures de lezebre.tech sont montrées en section 04 (« Le produit existe »).

## 3. Le Z

Glyphe dessiné (pas un caractère de police), identique partout, aussi lourd que le Z rose de leZèbre, en citron fluo. Quatre apparitions seulement : logotype (nav, application, pied de page), trajet animé de la section 02, Z géant de la conversion finale. Le point final citron du titre du hero fait écho sans ajouter de Z.

## 4. Apports UX et commerciaux

- Le produit est visible dès le premier écran, CTA « Demander une démo » dans la nav, le hero, la section cabinets et la conclusion.
- Onglets produit accessibles au clavier (flèches, Début, Fin), aucune lecture automatique.
- Scène 02 épinglée au scroll sur grand écran ; sur mobile ou petit écran, séquence jouée à l'entrée dans l'écran, sans blocage du défilement. Préférence « réduire les animations » respectée.
- Mobile : cockpit recomposé (pas réduit), onglets en pastilles défilantes, aucun débordement à 390 px.
- Formulaire court (4 champs), validation en ligne. **Il n'envoie rien** et le dit explicitement après validation.
- SEO : title et description du brief, un seul H1, H2 par section, JSON-LD SoftwareApplication sans note ni avis inventés.

## 5. À valider avant mise en production

1. **Nom EmployiZ** : antériorité INPI / EUIPO et noms de domaine (aucun domaine n'est cité dans la page).
2. **Vue consolidée cabinet (Master KPI)** : lezebre.tech la classe dans les « prochaines étapes ». La section 06 est donc étiquetée « Feuille de route » et « Aperçu conceptuel, non disponible à ce jour ». À retirer ou à basculer si la fonction sort.
3. **« 100 indicateurs »** : non repris, introuvable sur le site actuel. À confirmer avant de l'afficher.
4. **Exports, partage, automatisation des dépôts** : annoncés à la feuille de route par lezebre.tech, donc non présentés comme disponibles.
5. **Sécurité** : formulations reprises du site actuel (France, chiffrement, cloisonnement, accès tracés, RGPD, sous-traitant). La phrase « le cabinet ou l'entreprise reste maître de ses données » découle du statut de sous-traitant : à faire relire par le DPO.
6. **FAQ « paie externalisée »** : réponse prudente (dépôt des fichiers transmis par le prestataire). À confirmer.
7. **Indicateurs affichés en maquette** : âge moyen, part variable, ancienneté moyenne, temps partiel. Tous dérivables de la DSN, mais à vérifier qu'ils sont bien calculés par l'application.
8. **Captures** : celles du site actuel portent la marque RH BI / leZèbre Tech et sont en basse définition. Prévoir de nouvelles captures HD une fois l'interface habillée EmployiZ.
9. **Formulaire** : à brancher (CRM, email) ; mentions légales et politique de confidentialité à lier.
10. **Polices** : chargées depuis Google Fonts ; à auto-héberger en production.

## V2 (`index-v2.html`) : rapprochement avec leZèbre

- **Bleu nuit du groupe** à la place de l'encre : dégradé `#010727` → `#000F57` (les tons de lezebre.io) sur le hero, la scène DSN, la section cabinets et la sécurité ; halo violet `#6C5CE7` en horizon derrière le cockpit.
- **Dégradés leZèbre** : rouge → rose du logo (`#DE1D27` → `#FF0093`) sur la pastille « Appuyez-vous sur le Zèbre », les puces de la section éditeur et un filet en haut du pied de page ; conclusion en dégradé bleu nuit → violet nuit `#1A1040` (couleur du groupe), avec un halo rose.
- **« by leZèbre »** dans la navigation : petit logo leZèbre (avec son dégradé d'origine) et mot « leZèbre » avec le Z rose. Les deux Z se répondent : rose pour le groupe, citron pour le produit. Le logo revient dans le pied de page, à côté de « Groupe leZèbre ».
- **Nouvelle section 08 « L'éditeur »** avec le film de lezebre.io/experts-comptables (réencodé en 720p, 0,9 Mo, sans son). Lecture automatique seulement quand la section est à l'écran, bouton pause, rien ne démarre si l'utilisateur a demandé de réduire les animations. C'est la seule représentation du zèbre dans la page.
- Sécurité et démonstration renumérotées 09 et 10.
- À valider : droit d'utiliser ce film hors de lezebre.io ; formulation « leZèbre accompagne déjà les experts-comptables » (reprise du site du groupe).

### V2, ajustements

- Navigation : EmployiZ seul (le trio citron, rose, blanc en haut de page est retiré).
- « by leZèbre » en texte sobre : signature « EmployiZ by leZèbre » dans le pied de page, et surtitre « 08 by leZèbre » de la section éditeur.
- Dégradé vers le citron : un halo citron en fond vire au vert-de-gris sur le bleu nuit, il est donc abandonné. Le dégradé est porté par le Z géant de la conclusion (bleu nuit vers citron) et par le filet citron en haut du pied de page. Les fonds restent bleu nuit purs ; le halo violet du hero est supprimé.

## V3 (`index-v3.html`) : la forme leZèbre

Reprise de la grammaire de lezebre.io : un grand aplat en dégradé, un seul coin très arrondi, qui sort du bord de l'écran, et le sujet qui déborde dessus.
- Hero : aplat en dégradé citron (du citron pâle au citron vif), le cockpit pose dessus comme le zèbre sur l'aplat rose du groupe ; second aplat bleu nuit à droite, en contrepoint.
- Section 08 by leZèbre : aplat rose vers corail du groupe derrière la vidéo. Même forme, couleur de chaque marque : le lien entre les deux est visuel, sans le dire.

### V3, ajustements

- Section 03 : en-tête retiré (les trois verbes portent déjà les cartes), titre gardé pour les lecteurs d'écran uniquement.
- Cartes Visualisez, Comprenez, Conseillez empilées au défilement : chaque carte se cale en haut et la suivante glisse par-dessus, la précédente recule légèrement. Sur mobile, ou si une carte ne tient pas dans la hauteur de l'écran, elles restent en liste simple pour ne rien couper.
- Bloc « Le produit existe, voici ses écrans » supprimé ; les captures restent dans `assets/` mais ne sont plus affichées dans la V3.
- Numérotation des sections rendue continue (02 à 08).

### V3, travail de rythme

- Conservés intacts : hero, révélation DSN → Z, cartes empilées, fonctionnalités à onglets.
- Pour les cabinets : composition éditoriale, sans tableau de bord. Grand titre révélé mot à mot (« bulletins de paie » en retrait), texte et appel à démo collants à gauche, quatre bénéfices numérotés à droite avec filets qui se tracent.
- Supprimés : vision portefeuille (« Tous vos clients. Une seule vision. »), « Comment ça marche », toute mention de feuille de route (y compris dans by leZèbre).
- Infos pratiques déplacées dans la FAQ : dépôt des fichiers depuis l'application, nouvelle question « Combien de temps pour démarrer ? ».
- Sécurité condensée sur fond clair (titre, une phrase RGPD, cinq lignes), enchaînée avec la FAQ.
- Alternance des fonds : sombre, sombre, clair, clair, sombre, sombre, clair, clair, sombre. Raccord bleu nuit continu entre cabinets et by leZèbre.
- Navigation : « Comment ça marche » remplacé par « leZèbre » ; numérotation 02 à 07.
- Logo du tableau de bord : Z citron cerné d'encre.
