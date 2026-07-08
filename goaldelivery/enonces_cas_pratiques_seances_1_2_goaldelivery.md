# Énoncés des cas pratiques — Séances 1 et 2

Module Protocole et Tests Utilisateurs — M1 UX/UI

---

## Projet de fond : GoalDelivery

**GoalDelivery** est une application mobile fictive de livraison de repas et boissons, conçue pour les groupes d'amis ou de famille qui se retrouvent pour regarder ensemble les matchs de la Coupe du Monde. L'application met en avant des formats "plateaux à partager", des offres "spécial avant-match", et affiche pour chaque commande une estimation du temps de livraison par rapport à l'heure du coup d'envoi du match sélectionné.

**Cible principale :** groupes d'amis ou familles, 20-45 ans, organisant des soirées de visionnage à domicile pendant la compétition.

**Fonctionnalités principales :**
- Recherche de restaurants et menus par match, horaire ou type de plat
- Fiche restaurant/menu (plats, formats "plateau à partager", délai de livraison estimé)
- Panier avec sélection des quantités
- Indicateur "temps restant avant le coup d'envoi" affiché pendant la commande
- Commande, paiement et suivi de livraison

Ce projet sert de support aux exercices des séances 1 et 2.

---

# SÉANCE 1 — Pourquoi tester ? Fondamentaux et types de tests

## Cas 1.1 : Autopsie de rapports de test
**Durée :** 30-40 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Groupes de 3

### Contexte
Trois extraits de rapports de test (anonymisés et simplifiés), réalisés sur GoalDelivery à différentes périodes, vous sont fournis ci-dessous.

### Documents fournis

**Rapport A**
> *Méthodologie : 5 participants ont été reçus individuellement dans nos bureaux pour des sessions de 45 minutes, organisées la semaine précédant le début de la Coupe du Monde. Chaque session a été menée par un animateur, qui a demandé aux participants de verbaliser leurs pensées pendant qu'ils naviguaient sur l'application ("pensez à voix haute"). Trois tâches ont été proposées : trouver un menu "plateau à partager", l'ajouter au panier, passer la commande. Les sessions ont été enregistrées avec l'accord des participants.*
>
> *Résultats : 4 participants sur 5 n'ont pas remarqué l'indicateur "temps restant avant le coup d'envoi" affiché dans le panier. Plusieurs participants ont exprimé de la confusion à voix haute ("je ne sais pas si je vais recevoir ça à temps pour le match").*

**Rapport B**
> *Méthodologie : Un lien vers un prototype interactif a été envoyé à 60 participants recrutés via un panel en ligne, pendant la phase de groupes de la compétition. Chaque participant a réalisé les tâches seul, depuis son domicile, en suivant des instructions écrites affichées à l'écran. L'outil a automatiquement enregistré le temps passé sur chaque écran et le taux de complétion de chaque tâche.*
>
> *Résultats : Taux de complétion de la tâche "passer commande avant le coup d'envoi" : 71%. Temps moyen sur l'écran panier : 110 secondes (contre 45 secondes attendus). 29% des participants ont abandonné avant la fin.*

**Rapport C**
> *Méthodologie : Un consultant UX a analysé l'application pendant 2 jours, écran par écran, en s'appuyant sur les 10 heuristiques de Nielsen (visibilité de l'état du système, correspondance avec le monde réel, contrôle utilisateur, etc.). Aucun utilisateur n'a été impliqué dans cette phase.*
>
> *Résultats : 12 problèmes d'ergonomie ont été identifiés et classés par sévérité. Exemple : "Le badge 'temps restant avant le coup d'envoi' ne se met pas à jour en temps réel pendant que l'utilisateur compose son panier, ce qui viole l'heuristique de visibilité de l'état du système."*

### Mission
1. Pour chaque rapport, identifiez la méthode utilisée selon les trois axes vus en cours (modéré/non-modéré, qualitatif/quantitatif, distance/présentiel)
2. Repérez dans le texte les indices qui vous ont permis de le déduire (citez les passages)
3. Pour chaque rapport, évaluez si la méthode choisie était adaptée à ce qui est observé dans les résultats
4. Identifiez une force et une limite de chaque rapport

### Livrables
- Tableau d'analyse (méthode identifiée + indices + force/limite) pour les 3 rapports
- Restitution orale de 3 minutes par groupe

---

## Cas 1.2 : Matrice de choix de méthode
**Durée :** 30 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Individuel

### Contexte
Quatre scénarios de projets liés à la Coupe du Monde vous sont présentés ci-dessous.

### Documents fournis

**Scénario A — La startup en idéation**
> Une équipe de 3 personnes a esquissé sur papier le concept d'une application de pronostics entre amis pour la Coupe du Monde. Rien n'est développé. L'équipe veut savoir si l'idée a du sens avant d'investir dans le développement.

**Scénario B — GoalDelivery en production**
> GoalDelivery, avec 10 000 utilisateurs actifs pendant la compétition, souhaite tester deux versions différentes de sa fiche menu pour voir laquelle génère le plus d'ajouts au panier avant un match.

**Scénario C — L'équipe sans budget**
> Une petite équipe doit livrer un retour sur l'utilisabilité de l'écran panier de GoalDelivery dans 3 jours, avant le prochain match à forte audience, sans budget pour recruter des participants externes ni pour un outil payant.

**Scénario D — Le déploiement international**
> GoalDelivery est lancée simultanément dans 5 pays hôtes ou intéressés par la compétition (France, Allemagne, Espagne, Maroc, Canada). L'équipe veut comprendre comment ces utilisateurs vivent le parcours de commande "avant-match".

### Mission
1. Pour chaque scénario, choisissez une combinaison de méthode sur les trois axes (modéré/non-modéré, qualitatif/quantitatif, distance/présentiel)
2. Justifiez chaque choix en une phrase
3. Identifiez le scénario le plus contraint méthodologiquement et expliquez pourquoi

### Livrables
- Grille de choix complétée (4 scénarios × 3 axes + justification)

---

## Cas 1.3 : Chasse au biais d'équipe
**Durée :** 25 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Binômes

### Contexte
Voici la description de l'écran "Panier" de GoalDelivery, accompagnée de commentaires de son équipe de conception recueillis lors d'une réunion interne.

### Documents fournis

**Description de l'écran "Panier"**
> L'écran affiche la liste des plats ajoutés, avec pour chacun : une photo, le nom, le prix, et un sélecteur de quantité (+ / -). En haut de l'écran, un badge affiche un ballon de football animé accompagné d'un compte à rebours (ex : "1h32 avant le coup d'envoi"). En bas de l'écran, un bouton "Commander" devient actif une fois qu'au moins un plat est dans le panier.

**Commentaires de l'équipe**
> *Designer : "Le badge avec le ballon qui clignote et le compte à rebours, c'est évident, tout le monde comprend que ça indique s'il reste assez de temps pour recevoir la commande avant le match."*
>
> *Chef de projet : "On n'a pas besoin de mettre un texte sous le bouton + / -, la fonction de réduction/augmentation de quantité est universelle, personne ne se trompe là-dessus."*
>
> *Développeur : "Le bouton 'Commander' ne s'active qu'avec un plat dans le panier, c'est logique, pas la peine d'expliquer pourquoi il est grisé sinon."*

### Mission
1. Identifiez, dans les 3 commentaires, l'affirmation qui relève potentiellement du biais d'équipe (curse of knowledge)
2. Pour chacune, formulez l'hypothèse de conception implicite qu'elle cache (sous la forme "Nous pensons que...")
3. Pour chaque hypothèse, proposez une question ou une tâche de test qui permettrait de la vérifier

### Livrables
- Tableau : commentaire de l'équipe → hypothèse implicite → question/tâche de test associée

---

## Cas 1.4 : Test utilisateur ou pas ?
**Durée :** 20 min | **Difficulté :** ⭐☐☐☐☐ | **Format :** Individuel

### Contexte
Voici 8 situations décrivant des démarches d'évaluation menées par différentes équipes autour de GoalDelivery et d'applications comparables.

### Documents fournis

1. Un expert UX évalue seul l'application GoalDelivery avec une grille de 10 critères ergonomiques, sans faire intervenir d'utilisateur.
2. Deux versions de l'écran panier sont envoyées chacune à 50% du trafic réel pendant une semaine de matchs, et les taux de commande sont comparés.
3. Cinq utilisateurs sont filmés en train de manipuler une maquette papier d'une nouvelle fonctionnalité "compte à rebours", en présence d'un animateur qui leur pose des questions.
4. Une agence envoie un questionnaire à 2000 personnes pour savoir si elles seraient intéressées par une application de livraison spécial Coupe du Monde dans leur ville.
5. Un animateur observe à distance, via partage d'écran, un utilisateur naviguant sur GoalDelivery un soir de match et lui pose des questions de relance en direct.
6. Un outil en ligne envoie automatiquement des tâches à 80 participants qui les réalisent seuls, sans aucune interaction avec l'équipe.
7. Un designer compare l'interface de GoalDelivery à celle de 3 applications de livraison concurrentes pour s'en inspirer, sans utilisateur ni grille de critères.
8. Dix participants testent en même temps, chacun sur sa propre tablette, deux versions différentes du bouton "Commander", et leurs clics sont enregistrés automatiquement.

### Mission
1. Pour chaque situation, classez-la dans une catégorie : test utilisateur / audit ergonomique expert / étude de marché / test A/B / aucune de ces catégories
2. Pour les situations classées "test utilisateur", précisez si elle est modérée ou non-modérée
3. Pour la situation 7, expliquez pourquoi elle ne correspond à aucune des catégories proposées

### Livrables
- Tableau de classification complété et justifié

---

## Cas 1.5 : La courbe de coût de l'erreur, version chiffrée
**Durée :** 25 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Groupes de 2-3

### Contexte
Un même problème d'ergonomie — le bouton "Commander" de GoalDelivery est peu visible car sa couleur se confond avec le fond de l'écran — est détecté à 4 moments différents du projet.

### Documents fournis

**Moment 1 — Sur un croquis papier**
> Le problème est repéré lors d'un atelier de co-conception, alors que l'écran n'existe que sous forme de croquis dessiné sur une feuille A4.

**Moment 2 — Sur un wireframe numérique**
> Le problème est repéré lors d'une revue de wireframes en basse fidélité (formes grises, sans couleurs définitives), avant le début du design visuel.

**Moment 3 — Sur un prototype interactif**
> Le problème est repéré lors d'un test utilisateur sur un prototype Figma cliquable, avec les couleurs et le design final déjà appliqués, juste avant le passage en développement.

**Moment 4 — 2 mois après la mise en production**
> Le problème est repéré grâce à des retours du support client, 2 mois après que l'application a été publiée sur les stores, en plein pic d'utilisation pendant la compétition.

### Mission
1. Pour chaque moment, estimez (ordre de grandeur : minutes / heures / jours / semaines) le temps nécessaire pour corriger le problème
2. Pour chaque moment, listez les personnes ou équipes qui seraient mobilisées par la correction (ex : designer seul, designer + développeur, designer + développeur + QA + déploiement, etc.)
3. Rédigez une conclusion de 3-4 lignes sur l'intérêt de tester tôt, en vous appuyant sur vos estimations. Le moment 4 a-t-il une particularité supplémentaire liée au contexte (pic d'utilisation pendant la compétition) ?

### Livrables
- Tableau comparatif des 4 moments (temps estimé, équipes mobilisées)
- Conclusion synthétique (3-4 lignes)

---

# SÉANCE 2 — Construire un protocole de test

## Cas 2.1 : Repérer les hypothèses cachées
**Durée :** 30 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Binômes

### Contexte
Voici un extrait du cahier des charges de GoalDelivery décrivant une nouvelle fonctionnalité.

### Documents fournis

> *"Sur l'écran panier, un badge affichera un compte à rebours dynamique indiquant le temps restant avant le coup d'envoi du match sélectionné par l'utilisateur. Si le délai de livraison estimé dépasse ce temps restant, le badge passera automatiquement au orange et affichera le message 'Risque de retard'. L'utilisateur pourra alors choisir de modifier son panier (en retirant des plats nécessitant plus de préparation) ou de confirmer sa commande malgré l'avertissement."*

### Mission
1. Repérez 4 hypothèses de conception implicites contenues dans cette description (ex : "les utilisateurs comprendront que le badge orange signale un risque de retard par rapport au match", "les utilisateurs sauront quels plats retirer pour réduire le délai"...)
2. Reformulez chacune sous la forme "Nous pensons que..."
3. Parmi vos 4 hypothèses, identifiez celle qui vous semble la plus risquée si elle s'avère fausse, et expliquez pourquoi en 2-3 phrases

### Livrables
- Liste des 4 hypothèses reformulées
- Hypothèse la plus risquée surlignée, avec justification

---

## Cas 2.2 : Bonnes et mauvaises tâches
**Durée :** 30 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Individuel

### Contexte
Voici 8 formulations de tâches destinées à un test sur GoalDelivery. Certaines sont correctement écrites, d'autres présentent des problèmes.

### Documents fournis

1. *"Essayez de trouver facilement un menu 'plateau à partager' pour 4 personnes."*
2. *"Ce soir, vous regardez le match à 21h avec des amis et vous voulez commander à manger. Que faites-vous ?"*
3. *"Cliquez sur l'icône en forme de ballon en haut de l'écran, puis vérifiez le compte à rebours."*
4. *"Imaginez que le match commence dans 1 heure. Composez un panier que vous pensez recevoir à temps."*
5. *"Vous trouvez que le badge de compte à rebours est plutôt clair, n'est-ce pas ? Passez votre commande."*
6. *"Modifiez la quantité d'un plat dans votre panier."*
7. *"Accédez au module de gestion des préférences alimentaires et activez le filtre 'végétarien'."*
8. *"Le badge est passé au orange : décidez de ce que vous faites avant de valider votre commande."*

### Mission
1. Pour chaque tâche, indiquez si elle est correctement formulée ou problématique
2. Pour les tâches problématiques, identifiez précisément le type de problème : suggestion du résultat attendu, révélation de la solution (procédure au lieu d'un but), vocabulaire technique non adapté à l'utilisateur, question orientée/jugement de valeur
3. Reformulez chaque tâche problématique de façon neutre et orientée but

### Livrables
- Tableau : tâche originale → statut (correcte/problématique) → type de problème (si applicable) → reformulation (si nécessaire)

---

## Cas 2.3 : Construire un script de test sur GoalDelivery
**Durée :** 45-60 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
Vous devez concevoir un script de test complet pour GoalDelivery, centré sur le parcours suivant : recherche d'un menu "plateau à partager" → ajout au panier → lecture du badge "compte à rebours" → validation de la commande.

### Document fourni — Brief de départ

> *Besoin business : GoalDelivery constate que de nombreux utilisateurs ajoutent des plats au panier à l'approche d'un match, mais abandonnent leur commande sans la valider, en particulier dans la dernière heure avant le coup d'envoi.*
>
> *Objectif de test : Comprendre à quel moment et pour quelle raison les utilisateurs hésitent ou rencontrent des difficultés entre l'ajout au panier et la validation de la commande, en particulier autour du badge "compte à rebours" et du risque de retard.*

### Mission
1. Rédigez une introduction de test (présentation du déroulé, consentement, mise à l'aise — 3 à 5 phrases)
2. Formulez 3 hypothèses testables liées à l'objectif de test fourni (en appliquant les critères vus en chapitre 1 : spécifique, observable, falsifiable)
3. Rédigez 3 scénarios de tâches dans un ordre logique, couvrant le parcours recherche → panier → lecture du badge → validation
4. Rédigez 2-3 questions post-test (ressenti général + 1 question ouverte de clôture)

### Livrables
- Script de test complet structuré : introduction → hypothèses/objectifs → 3 tâches → questions post-test

---

## Cas 2.4 : Choisir les bonnes questions post-test
**Durée :** 20 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Binômes

### Contexte
Voici une liste de 10 questions post-test envisagées pour clôturer un test sur GoalDelivery.

### Documents fournis

1. *"Sur une échelle de 1 à 5, à quel point avez-vous trouvé cette application facile à utiliser ?"*
2. *"Avez-vous apprécié les couleurs de l'application ?"*
3. *"Y a-t-il un moment, pendant ce test, où vous vous êtes senti perdu ou hésitant ? Si oui, lequel ?"*
4. *"Recommanderiez-vous cette application à un proche ? Pourquoi ?"*
5. *"Trouvez-vous que cette application est meilleure que [nom d'un concurrent] ?"*
6. *"Avez-vous des suggestions ou remarques que vous souhaiteriez ajouter ?"*
7. *"Combien de temps avez-vous mis pour valider votre commande ?"*
8. *"Le badge de compte à rebours vous a-t-il aidé à prendre une décision ? Si oui, comment ?"*
9. *"Sur une échelle de 1 à 5, à quel point étiez-vous confiant que votre commande arriverait avant le match ?"*
10. *"Avez-vous trouvé l'application intuitive, comme la plupart des gens ?"*

### Mission
1. Parmi ces 10 questions, sélectionnez les 4 plus pertinentes pour clôturer le test conçu dans le Cas 2.3
2. Pour chaque question sélectionnée, justifiez en une phrase ce qu'elle permet de recueillir
3. Identifiez 2 questions à exclure et expliquez le problème de chacune (question orientée, hors sujet, donnée déjà mesurée automatiquement, etc.)

### Livrables
- Sélection justifiée des 4 questions retenues
- Explication des 2 exclusions

---

## Cas 2.5 : Relecture croisée de scripts
**Durée :** 25-30 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Échange entre groupes

### Contexte
Chaque groupe échange le script de test produit au Cas 2.3 avec un autre groupe.

### Document fourni — Grille de relecture

| Critère | Vérifié ? | Commentaire |
|---|---|---|
| L'introduction met-elle le participant à l'aise sans révéler les hypothèses du test ? | | |
| Les hypothèses sont-elles spécifiques, observables et falsifiables (pas des hypothèses-solutions) ? | | |
| Les tâches sont-elles formulées comme des buts, sans révéler la procédure ni le vocabulaire interne ? | | |
| Les tâches sont-elles dans un ordre logique (progression, pas de dépendance bloquante) ? | | |
| Les questions post-test sont-elles neutres et non redondantes avec les données déjà collectées ? | | |

### Mission
1. Complétez la grille de relecture pour le script reçu
2. Identifiez 2 points forts du script reçu
3. Identifiez 2 points à améliorer, avec une proposition concrète de reformulation pour chacun
4. Restituez oralement vos retours au groupe concerné (5 minutes par échange)

### Livrables
- Grille de relecture complétée
- Script annoté avec les 2 points forts et les 2 points à améliorer (+ reformulations proposées)
