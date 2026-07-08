# Énoncés des cas pratiques — Séances 5 et 6

Module Protocole et Tests Utilisateurs — M1 UX/UI

Ces exercices poursuivent le fil rouge GoalDelivery : le script finalisé au Cas 3.2 et les sessions menées en séance 4 (Cas 4.2) servent de matière première directe aux cas ci-dessous.

---

# SÉANCE 5 — Tests à distance et outils (Maze/Lookback + GA4/Hotjar)

## Cas 5.1 : Paramétrer un test non-modéré sur GoalDelivery
**Durée :** 45-60 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
Le script finalisé au Cas 3.2 doit être transposé en version non-modérée sur un outil gratuit (Maze ou Lookback), afin de tester un plus grand nombre de participants avant le prochain match à forte audience.

### Mission
1. Reprenez le script finalisé du Cas 3.2 et identifiez les éléments qui nécessitent une reformulation pour l'autonomie totale du participant (notamment les "notes pour l'animateur" qui ne pourront plus être utilisées en relance live)
2. Paramétrez les 3 tâches du script dans l'outil choisi (Maze ou Lookback)
3. Définissez, pour chaque tâche, les métriques automatiquement collectées par l'outil (taux de complétion, temps sur tâche, taux de clic sur une zone précise)

### Livrables
- Test paramétré et fonctionnel sur l'outil choisi
- Note récapitulative des reformulations effectuées (script modéré → script non-modéré)

---

## Cas 5.2 : Rédiger des consignes 100% autonomes
**Durée :** 25 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Individuel

### Contexte
Voici une tâche du script GoalDelivery rédigée initialement pour un test modéré.

### Document fourni

> *"Le match commence dans 1h30. Trouvez un plateau à partager pour 4 personnes et ajoutez-le au panier, je vous guiderai si vous bloquez sur un élément."*

### Mission
1. Identifiez ce qui ne fonctionnerait pas en mode non-modéré dans cette consigne (référence à l'aide de l'animateur, ambiguïté sur le moment où la tâche est considérée comme terminée)
2. Réécrivez la consigne pour qu'elle soit totalement autosuffisante, sans référence à un animateur
3. Ajoutez une consigne de "sortie" si le participant ne trouve pas l'élément demandé (ex : "si vous ne trouvez pas de plateau pour 4 personnes après 2 minutes, passez à la tâche suivante")

### Livrables
- Consigne reformulée, autonome et complète, avec sa consigne de sortie

---

## Cas 5.3 : Lire un funnel GA4
**Durée :** 25-30 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Binômes

### Contexte
Sur le compte de démonstration GA4, un funnel de conversion adapté à GoalDelivery est mis à disposition : recherche d'un menu → fiche menu → ajout au panier → commande validée.

### Document fourni — Données du funnel (relevé simplifié, sur une semaine de matchs)

| Étape | Utilisateurs entrant dans l'étape | Taux de passage à l'étape suivante |
|---|---|---|
| Recherche d'un menu | 10 000 | 62% |
| Fiche menu consultée | 6 200 | 71% |
| Ajout au panier | 4 402 | 58% |
| Commande validée | 2 553 | — |

### Mission
1. Identifiez l'étape du funnel présentant le taux d'abandon le plus élevé (donc le taux de passage le plus faible vers l'étape suivante)
2. Formulez 2 hypothèses explicatives de cet abandon, en lien avec ce que vous savez déjà de GoalDelivery (badge "compte à rebours", risque de retard, format plateau à partager)
3. Proposez une question de test utilisateur qui permettrait de vérifier l'une de ces deux hypothèses

### Livrables
- Identification de l'étape critique avec le calcul justifiant ce choix
- 2 hypothèses explicatives + 1 question de test associée

---

## Cas 5.4 : Analyser une heatmap Hotjar
**Durée :** 25-30 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Binômes

### Contexte
Une heatmap de clics (essai gratuit Hotjar ou capture fournie) sur l'écran panier de GoalDelivery est mise à disposition.

### Document fourni — Description de la heatmap

> *La zone la plus cliquée de l'écran panier est le sélecteur de quantité (+ / -) des plats, avec une forte concentration de clics. La deuxième zone la plus cliquée, de façon inattendue, se situe directement sur le badge "compte à rebours" en haut de l'écran — alors que ce badge n'est pas un élément cliquable et ne déclenche aucune action. Le bouton "Commander", en bas de l'écran, présente une densité de clics relativement faible par rapport au nombre de sessions ayant atteint cet écran.*

### Mission
1. Identifiez la zone "chaude" la plus surprenante au regard de sa fonction réelle dans l'interface (clic fantôme)
2. Formulez un finding à partir de cette observation (constat factuel + hypothèse explicative)
3. Mettez en relation cette observation avec les données du funnel GA4 du Cas 5.3 : ce clic fantôme pourrait-il expliquer une partie du taux d'abandon observé à l'étape "ajout au panier" ?

### Livrables
- Description de la zone chaude analysée
- 1 finding rédigé (constat + hypothèse explicative)
- Paragraphe de mise en relation avec les données GA4 (3-4 lignes)

---

## Cas 5.5 : Croiser un insight quantitatif et un finding qualitatif
**Durée :** 30 min | **Difficulté :** ⭐⭐⭐⭐☐ | **Format :** Groupes de 3

### Contexte
Vous disposez de l'insight issu de GA4 ou Hotjar (Cas 5.3 ou 5.4) et des observations issues du test qualitatif mené en séance 4 (Cas 4.2, sur le même écran panier et le même badge "compte à rebours").

### Mission
1. Mettez en regard les deux types de données : convergent-elles, se contredisent-elles, se complètent-elles ?
2. Formulez une conclusion combinée : que pouvez-vous affirmer en combinant les deux sources, que vous ne pourriez pas affirmer avec une seule des deux ?
3. Identifiez la limite de chaque source de données prise isolément (ex : GA4/Hotjar ne disent pas *pourquoi* un clic a lieu ; le test qualitatif ne dit pas si l'observation se généralise à l'ensemble des utilisateurs)

### Livrables
- Fiche de synthèse croisée (quantitatif + qualitatif → conclusion combinée)
- Limite de chaque source identifiée (2-3 phrases chacune)

---

# SÉANCE 6 — Analyse des résultats et rapport de recommandations

## Cas 6.1 : Calculer le SUS à partir de réponses brutes
**Durée :** 25-30 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Individuel

### Contexte
Voici les réponses brutes de 5 participants au questionnaire SUS (10 questions, échelle de 1 à 5), recueillies après leur test sur GoalDelivery.

### Document fourni — Réponses brutes

| Question SUS | P1 | P2 | P3 | P4 | P5 |
|---|---|---|---|---|---|
| Q1 (formulation positive) | 4 | 3 | 5 | 2 | 4 |
| Q2 (formulation négative) | 2 | 3 | 1 | 4 | 2 |
| Q3 (formulation positive) | 4 | 4 | 5 | 2 | 3 |
| Q4 (formulation négative) | 2 | 2 | 1 | 4 | 3 |
| Q5 (formulation positive) | 4 | 3 | 5 | 3 | 4 |
| Q6 (formulation négative) | 2 | 3 | 1 | 4 | 2 |
| Q7 (formulation positive) | 5 | 4 | 5 | 2 | 4 |
| Q8 (formulation négative) | 1 | 2 | 1 | 4 | 2 |
| Q9 (formulation positive) | 4 | 4 | 5 | 3 | 4 |
| Q10 (formulation négative) | 2 | 3 | 1 | 4 | 3 |

### Mission
1. Appliquez la méthode de calcul du score SUS pour chaque participant (rappel : pour les questions à formulation positive, score = réponse − 1 ; pour les questions à formulation négative, score = 5 − réponse ; sommer les 10 scores puis multiplier par 2,5)
2. Calculez le score moyen de l'échantillon des 5 participants
3. Situez ce score sur la grille d'interprétation (excellent, bon, correct, médiocre) et rédigez une interprétation en 1 paragraphe, en identifiant si un participant se distingue nettement des autres

### Livrables
- Tableau de calcul des scores individuels et du score moyen
- Interprétation du résultat (1 paragraphe)

---

## Cas 6.2 : Identifier et formuler des findings
**Durée :** 30-40 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
Les notes d'observation collectées en séance 4 (Cas 4.2 et 4.4) et les données de séance 5 (Cas 5.3, 5.4, 5.5) servent de matière première.

### Mission
1. Extraire 6 à 8 findings à partir de l'ensemble des observations brutes et données collectées sur le parcours panier de GoalDelivery
2. Vérifiez que chaque finding est formulé de façon factuelle et actionnable (pas une simple description, pas une opinion) — réutilisez si besoin la distinction observation factuelle/interprétation vue au Cas 4.4
3. Regroupez les findings par thème si des redondances apparaissent (ex : tous les findings liés au badge "compte à rebours" ensemble)

### Livrables
- Liste de findings formulés et regroupés par thème

---

## Cas 6.3 : Matrice sévérité/fréquence
**Durée :** 25-30 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
La liste de findings produite en Cas 6.2 est reprise.

### Mission
1. Placez chaque finding dans une matrice sévérité (faible/moyenne/élevée) × fréquence (rare/occasionnel/systématique)
2. Sélectionnez les 5 findings prioritaires
3. Justifiez la priorisation pour les 2 findings les plus débattus du groupe (par exemple : le clic fantôme sur le badge du Cas 5.4 doit-il être classé sévérité élevée même s'il est rare, ou sévérité moyenne mais fréquent ?)

### Livrables
- Matrice complétée
- Top 5 des findings prioritaires, avec justification pour 2 d'entre eux

---

## Cas 6.4 : Rédiger une recommandation actionnable
**Durée :** 25 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Binômes

### Contexte
Un finding prioritaire (issu du Cas 6.3), par exemple lié à la confusion autour du badge "compte à rebours" ou au clic fantôme observé en Cas 5.4, est repris.

### Mission
1. Rédigez une recommandation directement liée à ce finding
2. Vérifiez qu'elle répond aux critères d'une recommandation actionnable (qui fait quoi, sur quel élément, avec quel résultat attendu)
3. Proposez un indicateur permettant de vérifier, après mise en œuvre, que la recommandation a eu l'effet attendu (vous pouvez vous appuyer sur les métriques GA4 du Cas 5.3 : taux de passage à l'étape suivante, ou taux de clic erroné mesuré par Hotjar)

### Livrables
- Recommandation rédigée + indicateur de suivi associé

---

## Cas 6.5 : Adapter le message selon l'audience
**Durée :** 30 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
Un même finding et sa recommandation (Cas 6.4) doivent être communiqués à deux audiences différentes chez GoalDelivery : l'équipe technique (développeurs) et la direction générale, qui doit valider un budget de correction avant le prochain pic de matchs.

### Mission
1. Rédigez une version du message destinée à l'équipe technique (niveau de détail, vocabulaire, référence précise à l'élément d'interface concerné)
2. Rédigez une version destinée à la direction (impact business : lien avec le taux d'abandon du funnel GA4, urgence liée au calendrier des matchs à venir, priorisation)
3. Identifiez les éléments qui changent entre les deux versions et ceux qui restent identiques (le finding et la recommandation de fond ne changent pas, seule leur présentation s'adapte)

### Livrables
- Deux versions du message (technique / direction)
- Note comparative (ce qui change, ce qui reste identique)
