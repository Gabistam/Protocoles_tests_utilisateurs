# Énoncés des cas pratiques — Séances 3 et 4

Module Protocole et Tests Utilisateurs — M1 UX/UI

GoalDelivery (présenté en séances 1-2) devient le fil rouge unique du module à partir de la séance 3 : les exercices ci-dessous s'appuient directement sur les productions des séances précédentes (hypothèses du Cas 2.1, script du Cas 2.3, relecture du Cas 2.5).

---

# SÉANCE 3 — Recrutement, échantillonnage et cadrage du protocole CC1

## Cas 3.1 : Cadrage du protocole pour le cycle de test complet
**Durée :** 20-30 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Groupes de 3

### Contexte
Le script produit au Cas 2.3 (et amélioré via la relecture croisée du Cas 2.5) va maintenant être utilisé pour de vraies sessions de test avec des participants (séances 4 à 7). Avant de recruter, il faut préciser la cible exacte et finaliser le périmètre.

### Document fourni — Rappel du contexte GoalDelivery

> *Cible générale de GoalDelivery : groupes d'amis ou familles, 20-45 ans, organisant des soirées de visionnage à domicile pendant la compétition.*
>
> *Parcours testé (Cas 2.3) : recherche d'un menu "plateau à partager" → ajout au panier → lecture du badge "compte à rebours" → validation de la commande.*

### Mission
1. Relisez votre script du Cas 2.3. À partir de la cible générale de GoalDelivery, définissez une cible précise de participants à recruter : quel(s) profil(s), parmi la cible générale, est/sont le(s) plus pertinent(s) pour ce protocole précis (ex : personnes commandant régulièrement en groupe, personnes ayant déjà subi un retard de livraison...) ?
2. Confirmez ou ajustez le périmètre du test au regard des retours reçus lors de la relecture croisée (Cas 2.5)
3. Finalisez la liste des hypothèses à tester : sélectionnez ou reformulez 3 hypothèses prioritaires (parmi celles du Cas 2.1 et du Cas 2.3)

### Livrables
- Fiche de cadrage finale : cible précise de recrutement, périmètre confirmé, 3 hypothèses prioritaires — base du dossier CC1

---

## Cas 3.2 : Finaliser le script de test pour le protocole CC1
**Durée :** 45 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
À partir du script du Cas 2.3, des retours de relecture du Cas 2.5 et de la fiche de cadrage du Cas 3.1, vous devez produire la version finale du script qui sera utilisée pour les sessions de test en séance 4 et pour le test à distance en séance 5.

### Mission
1. Intégrez au script les corrections issues de la relecture croisée (Cas 2.5)
2. Vérifiez la cohérence entre les 3 hypothèses prioritaires finalisées (Cas 3.1) et les tâches du script : chaque hypothèse doit être couverte par au moins une tâche
3. Pour chaque tâche, ajoutez une section "notes pour l'animateur" (points d'attention à observer, relances possibles en cas de blocage) — cf. séance 2, sous-partie 2.6
4. Produisez la version finale du script, prête à l'emploi pour la séance 4

### Livrables
- Script de test finalisé (version CC1), avec notes pour l'animateur intégrées

---

## Cas 3.3 : Construire un screener
**Durée :** 30 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Binômes

### Contexte
Vous devez présélectionner des participants correspondant à la cible précise définie au Cas 3.1 (groupes d'amis/familles regardant des matchs ensemble et commandant à manger).

### Mission
1. Définissez 4-5 critères d'inclusion (ex : regarde régulièrement des matchs avec d'autres personnes, a déjà commandé de la nourriture livrée pendant un événement sportif, utilise une application de livraison au moins une fois par mois) et 2-3 critères d'exclusion (ex : travaille dans la livraison ou la restauration, a déjà testé GoalDelivery)
2. Rédigez un questionnaire de présélection (screener) de 6-8 questions permettant de vérifier ces critères
3. Intégrez une question "piège" permettant de détecter un participant qui répondrait au hasard ou tenterait de paraître plus "qualifié" qu'il ne l'est réellement

### Livrables
- Questionnaire de screener complet (6-8 questions + critères d'inclusion/exclusion associés), prêt à diffuser

---

## Cas 3.4 : Trier des profils candidats
**Durée :** 30-40 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3

### Contexte
Voici les réponses (résumées) de 12 candidats ayant rempli un screener pour GoalDelivery.

### Documents fournis

| # | Âge | Activité professionnelle | Ville | Regarde des matchs avec d'autres personnes | Commande à manger pendant des événements sportifs | Utilise des apps de livraison | Remarque |
|---|---|---|---|---|---|---|---|
| 1 | 28 | Chargé de communication | Lyon | Oui, systématiquement | Oui, souvent | Oui, régulièrement | — |
| 2 | 54 | Comptable | Lyon | Rarement, regarde seul | Non | Non | — |
| 3 | 32 | Livreur indépendant | Lyon | Oui, souvent | Oui, souvent | Oui, régulièrement | Travaille pour une plateforme de livraison concurrente |
| 4 | 25 | Étudiant en école de commerce | Villeurbanne | Oui, systématiquement | Oui, souvent | Oui, régulièrement | — |
| 5 | 37 | Professeur des écoles | Lyon | Oui, parfois | Oui, parfois | Non | — |
| 6 | 23 | Développeur web | Lyon | Oui, souvent | Oui, souvent | Oui, régulièrement | A déjà utilisé GoalDelivery |
| 7 | 40 | Responsable RH | Lyon | Oui, systématiquement | Oui, souvent | Oui, régulièrement | — |
| 8 | 45 | Architecte | Caluire-et-Cuire | Oui, parfois | Oui, parfois | Oui, occasionnellement | — |
| 9 | 29 | Designer freelance | Lyon | Oui, systématiquement | Oui, souvent | Oui, régulièrement | Répond "oui" à toutes les questions, y compris contradictoires |
| 10 | 34 | Infographiste | Lyon | Oui, souvent | Oui, souvent | Oui, régulièrement | — |
| 11 | 48 | Cadre commercial | Lyon | Rarement, regarde seul | Oui, parfois | Oui, occasionnellement | — |
| 12 | 31 | Chef de projet marketing | Lyon | Oui, systématiquement | Oui, souvent | Oui, régulièrement | — |

### Mission
1. Appliquez les critères définis au Cas 3.3 pour présélectionner 5 profils parmi ces 12 candidats
2. Pour chaque profil exclu, justifiez l'exclusion (critère d'exclusion non respecté, incohérence dans les réponses, profil hors cible...)
3. Discutez en groupe : entre deux profils également valides, faut-il privilégier la diversité des profils retenus ou leur ressemblance avec la cible "type" ? Justifiez votre position en 2-3 phrases

### Livrables
- Sélection justifiée de 5 profils
- Liste des 7 profils exclus avec justification
- Réponse à la question de discussion (2-3 phrases)

---

## Cas 3.5 : Repérer les biais de recrutement
**Durée :** 20 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Individuel

### Contexte
Voici trois méthodes de recrutement envisagées pour le test GoalDelivery.

### Documents fournis

**Méthode A**
> L'équipe projet recrute les 5 participants parmi ses collègues de bureau, car "ils regardent tous les matchs ensemble à la pause déjeuner et c'est simple à organiser".

**Méthode B**
> Un post est publié sur le compte Instagram de GoalDelivery, invitant les abonnés à participer à un test en échange d'un bon de réduction sur leur prochaine commande. Les 5 premières personnes qui répondent sont retenues.

**Méthode C**
> Un message est envoyé aux 200 utilisateurs ayant déjà téléchargé l'application GoalDelivery mais ne l'ayant jamais utilisée depuis plus de 3 mois, leur proposant de participer à un test sur la nouvelle version de l'écran panier.

### Mission
1. Pour chaque méthode, identifiez le ou les biais de recrutement introduits
2. Évaluez l'impact potentiel de chaque biais sur la fiabilité des résultats du test (impact faible / moyen / élevé), en justifiant
3. Pour les méthodes A et B, proposez une alternative de recrutement qui réduirait le biais identifié

### Livrables
- Tableau : méthode → biais identifié → impact (faible/moyen/élevé) + justification → alternative proposée (pour A et B)

---

# SÉANCE 4 — Conduite de session : posture et biais

## Cas 4.1 : Repérer les erreurs de modération
**Durée :** 25-30 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Binômes

### Contexte
Voici un extrait de transcript d'une session de test sur GoalDelivery. Le participant doit commander un "plateau à partager" pour un match qui commence dans 1h30.

### Document fourni — Extrait de transcript

> **Animateur :** Bonjour ! Aujourd'hui on va tester l'application GoalDelivery, qui est plutôt sympa, vous allez voir. Le match commence dans 1h30 et vous voulez commander un plateau à partager pour 4 personnes, comment faites-vous ?
>
> **Participant :** D'accord... je vais chercher "plateau" dans la barre de recherche, je pense.
>
> *(Le participant tape "plateau" et obtient plusieurs résultats.)*
>
> **Participant :** Il y en a plusieurs... je ne sais pas trop lequel correspond à 4 personnes.
>
> **Animateur :** Vous pouvez cliquer sur le premier, c'est celui qui est mis en avant normalement.
>
> *(Le participant clique et arrive sur la fiche du menu.)*
>
> **Participant :** Ok, je vois le prix et la description... je l'ajoute au panier ?
>
> **Animateur :** Oui exactement, c'est plutôt logique non ?
>
> *(Le participant ajoute le plat au panier et arrive sur l'écran panier, où le badge affiche "1h30 avant le coup d'envoi" en vert.)*
>
> **Participant :** Ah, il y a un badge avec un ballon et un temps... je ne sais pas trop ce que ça veut dire pour ma commande.
>
> **Animateur :** Pourquoi ça vous pose question ? Le badge est vert, ça veut dire que tout va bien normalement.

### Mission
1. Surlignez (ou citez) chaque intervention de l'animateur qui constitue une erreur de modération
2. Pour chaque intervention surlignée, nommez le type d'erreur ou de biais introduit (aide apportée trop tôt, jugement de valeur, question suggestive, remise en cause du ressenti du participant...)
3. Pour chaque intervention problématique, proposez une reformulation neutre ou une réaction alternative de l'animateur

### Livrables
- Transcript annoté (interventions surlignées + type d'erreur identifié)
- Tableau des reformulations proposées

---

## Cas 4.2 : Jeu de rôle modérateur / participant / observateur
**Durée :** 45-60 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Groupes de 3 (rotation)

### Contexte
Le script de test finalisé au Cas 3.2 sert de support à une session de test simulée.

### Mission
1. Constituez des groupes de 3 : un animateur, un participant, un observateur
2. L'animateur mène la session en suivant le script finalisé du Cas 3.2 (introduction, questions pré-test, tâches, questions post-test)
3. Le participant joue un rôle réaliste (vous pouvez piocher l'un des profils retenus au Cas 3.4 pour vous mettre dans la peau d'un participant cohérent)
4. L'observateur prend des notes sur deux aspects :
   - Les écarts entre le script prévu et le déroulé réel (questions improvisées, étapes sautées, reformulations)
   - Les moments où l'animateur s'écarte de la neutralité (sans forcément que ce soit un "drame" — l'objectif est d'observer, pas de sanctionner)
5. Effectuez une rotation : chacun passe par les 3 rôles (3 sessions courtes au total)
6. À la fin des 3 rotations, chaque participant identifie individuellement un moment où il a ressenti le biais de désirabilité sociale (l'envie de "bien faire" ou de donner une réponse qu'il pensait attendue)

### Livrables
- Notes d'observation pour chacune des 3 rotations
- Synthèse individuelle du moment de désirabilité sociale ressenti ou observé (3-4 lignes par personne)

---

## Cas 4.3 : Reformuler des questions biaisées
**Durée :** 20 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Individuel

### Contexte
Voici 6 questions de relance qu'un animateur pourrait être tenté de poser pendant un test sur GoalDelivery.

### Documents fournis

1. *"Vous trouvez ça simple de commander avant un match, non ?"*
2. *"Pourquoi vous n'avez pas vu le badge de compte à rebours, il est pourtant bien visible en haut de l'écran ?"*
3. *"Est-ce que ça vous semble plus rapide que sur d'autres applications de livraison que vous utilisez ?"*
4. *"Vous n'avez pas eu envie d'annuler en voyant que le badge passait au orange ?"*
5. *"Qu'est-ce qui s'est passé quand vous avez cliqué sur ce badge ?"*
6. *"Vous êtes d'accord que ce message d'avertissement est plus clair que l'ancien ?"*

### Mission
1. Pour chaque question, indiquez si elle est neutre ou biaisée
2. Pour les questions biaisées, identifiez le type de biais (question suggestive, jugement implicite, comparaison orientée, présupposition d'un ressenti négatif/positif)
3. Reformulez chaque question biaisée de façon neutre et ouverte

### Livrables
- Tableau : question originale → statut (neutre/biaisée) → type de biais (si applicable) → reformulation (si nécessaire)

---

## Cas 4.4 : Observation factuelle vs interprétation
**Durée :** 25 min | **Difficulté :** ⭐⭐☐☐☐ | **Format :** Binômes

### Contexte
Voici 8 notes prises par un observateur pendant une session de test sur GoalDelivery.

### Documents fournis

1. *"Le participant a cliqué 3 fois sur la photo du menu avant de trouver le bouton 'Ajouter au panier'."*
2. *"Le participant semble stressé par le temps restant avant le match."*
3. *"Le participant a passé 22 secondes sur le badge 'compte à rebours' sans interagir."*
4. *"Le participant ne fait pas confiance à l'estimation de livraison affichée."*
5. *"Le participant a dit à voix haute : 'Je ne sais pas si 1h30 c'est suffisant pour un plateau comme celui-là.'"*
6. *"Le participant est perdu sur cet écran."*
7. *"Le participant a fait défiler la fiche du menu vers le bas puis vers le haut avant de cliquer sur 'Ajouter au panier'."*
8. *"Le participant trouve l'application peu fiable pour les commandes urgentes."*

### Mission
1. Classez chaque note : observation factuelle (ce qui peut être vu/entendu objectivement) ou interprétation (un jugement ou une supposition sur l'état mental du participant)
2. Pour chaque interprétation, reformulez-la en observation factuelle équivalente (ce qui a été vu ou entendu, sans supposition)
3. Discussion : pourquoi est-il important de séparer les deux au moment de la prise de notes, plutôt qu'au moment de l'analyse ?

### Livrables
- Tableau de classification (note → factuelle/interprétation → reformulation si interprétation)
- Réponse à la question de discussion (3-4 lignes)

---

## Cas 4.5 : Gérer un participant bloqué
**Durée :** 20-25 min | **Difficulté :** ⭐⭐⭐☐☐ | **Format :** Binômes (jeu de rôle court)

### Contexte
Voici trois mini-scénarios de blocage pendant un test sur GoalDelivery.

### Documents fournis

**Scénario A — Le silence prolongé**
> Le participant doit retirer un plat de son panier après que le badge soit passé au orange ("Risque de retard"). Il regarde l'écran, hésite, et reste silencieux pendant plus de 30 secondes sans rien dire ni cliquer.

**Scénario B — La demande directe d'aide**
> Le participant, face au badge orange "Risque de retard", se tourne vers l'animateur et demande : *"Bon, concrètement, qu'est-ce que je suis censé faire maintenant ?"*

**Scénario C — L'abandon verbalisé**
> Le participant, après avoir cherché un filtre "végétarien" dans le menu pendant une minute, dit : *"Je n'y arrive pas, je pense qu'il n'y a pas cette option, on passe à autre chose ?"*

### Mission
1. En binôme, jouez chaque scénario (rotation des rôles animateur/participant)
2. Pour chaque scénario, identifiez la limite à ne pas franchir : à partir de quand l'animateur basculerait-il d'une posture neutre à une aide qui fausserait l'observation ?
3. Formulez, pour chacun des 3 scénarios, la phrase exacte que l'animateur pourrait utiliser pour relancer sans aider directement

### Livrables
- Les 3 phrases-types formulées
- Pour chacune, une justification courte expliquant en quoi elle reste neutre (1-2 phrases)
