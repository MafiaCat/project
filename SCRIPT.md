# 📡 TRANSMISSION - Script Narratif Complet

## 🎮 Informations Générales

**Titre:** Transmission
**Genre:** Récit narratif pur à choix multiples (SMS survival game)
**Personnage principal:** Sarah, 11 ans (fille)
**Joueur:** Le père de Sarah, bloqué à l'étranger
**Contexte:** "Le Grand Silence" - catastrophe mondiale coupant toutes communications
**Lien unique:** Téléphone satellite laissé à Sarah

---

## 📖 PHILOSOPHIE DE CONCEPTION

**L'ARBRE PUR** - Ce jeu ne contient AUCUNE STATISTIQUE CACHÉE.
L'histoire est un arbre narratif pur. La survie ou l'échec de Sarah est le résultat direct et logique de l'enchaînement de vos décisions.

---

## 🌳 STRUCTURE NARRATIVE

```
TRONC COMMUN (Jour 1)
├── CONTACT
├── SITUATION
├── ÉVÉNEMENT
├── LA DURE VÉRITÉ
└── POINT DE RUPTURE 1: LA STRATÉGIE
    │
    ├── BRANCHE I: LE SIÈGE (Rester dans la maison)
    │   ├── Rameau I.A: L'ISOLEMENT
    │   ├── Rameau I.B: LA COMMUNAUTÉ
    │   ├── Rameau I.C: L'ASSAUT
    │   └── Rameau I.D: L'INCENDIE
    │
    ├── BRANCHE II: LA VILLE (Chercher Tante Claire)
    │   ├── Rameau II.A: LE LOUP SOLITAIRE
    │   ├── Rameau II.B: L'ALLIÉ (Sarah et Chloé)
    │   └── Rameau II.C: LA CAPTURE
    │
    └── BRANCHE III: L'EXODE (Rejoindre la base)
        ├── Rameau III.A: L'AUTOROUTE
        ├── Rameau III.B: LA FORÊT
        ├── Rameau III.C: LE VILLAGE
        └── Rameau III.D: LA BASE
```

---

## 📝 TRONC COMMUN - "LE GRAND SILENCE" (Jour 1)

### 🔵 NŒUD: START - Le Premier Contact

**Messages de Sarah:**
1. "Papa ?"
2. "Papa... tu es là ?"
3. "C'est moi... Sarah."
4. "S'il te plaît réponds..."
5. "..."
6. "Le téléphone normal marche plus. Internet marche plus."
7. "Y'a plus rien qui marche."
8. "Les lumières se sont éteintes d'un coup. Tout est noir."
9. "Même les voitures dans la rue... elles marchent plus."
10. "..."
11. "Papa, j'ai peur."
12. "Tante Claire est partie chercher des choses il y a 2 heures..."
13. "Elle m'a dit qu'elle revenait vite."
14. "Mais elle est pas revenue."
15. "J'entends des sirènes partout dehors."
16. "Et des gens qui crient."

**Choix unique:**
- "Sarah, écoute-moi bien. Où es-tu exactement ?" → SITUATION

---

### 🔵 NŒUD: SITUATION - Évaluation de la sécurité

**Messages de Sarah:**
1. "Je... je suis chez Tante Claire. Dans sa maison."
2. "J'ai fermé toutes les portes comme tu m'as appris."
3. "Mais..."
4. "Y'a des bruits dehors."
5. "Des gens qui crient. Et... et des vitres qui cassent."

**Choix unique:**
- "Reste calme. Tu es en sécurité à l'intérieur ?" → SECURE_CHECK

---

### 🔵 NŒUD: SECURE_CHECK - Vérification sécurité

**Messages de Sarah:**
1. "Je crois oui..."
2. "J'ai mis le meuble devant la porte d'entrée."
3. "Papa... c'est quoi ce qui se passe ?"
4. "Pourquoi tout le monde devient méchant ?"

**Choix:**
- "Il y a eu une panne générale. Les gens ont peur." → EXPLAIN_1
- "Je ne sais pas encore. Mais je vais te protéger." → EXPLAIN_1

---

### 🔵 NŒUD: EXPLAIN_1 - Premier événement dangereux

**Messages de Sarah:**
1. "..."
2. "Attends !"
3. "Y'a quelqu'un chez les voisins. J'entends des choses qui cassent."
4. "Ils sont en train de... de voler des trucs je crois."
5. "Papa... j'ai peur."

**Choix unique:**
- "Cache-toi. Ne fais AUCUN bruit. Où peux-tu te cacher ?" → HIDE_NOW

---

### 🔵 NŒUD: HIDE_NOW - Danger immédiat

**Messages de Sarah:**
1. "Je... je vais dans le placard de la chambre."
2. "..."
3. "..."
4. "Ça va. Ils sont partis."
5. "Papa... quand est-ce que tu rentres ?"

**Choix unique:**
- "Je... on ne peut pas rentrer pour l'instant." → HARD_TRUTH

---

### 🔵 NŒUD: HARD_TRUTH - La dure vérité

**Messages de Sarah:**
1. "Comment ça ?"
2. "Mais... mais je suis toute seule !"
3. "Tu dois rentrer ! S'il te plaît !"

**Choix:**
- "Sarah, écoute-moi. Tous les avions sont bloqués. Je ne peux pas." → ACCEPTANCE
- "Je ferais TOUT pour être là. Mais c'est impossible maintenant." → ACCEPTANCE

---

### 🔵 NŒUD: ACCEPTANCE - Acceptation de la situation

**Messages de Sarah:**
1. "..."
2. "Mais... mais je fais quoi alors ?"
3. "Je peux pas rester toute seule ici..."

**Choix unique:**
- "Tu n'es pas seule. Je suis là, par téléphone. On va s'en sortir." → STRATEGY_CHOICE

---

### 🔴 POINT DE RUPTURE 1: STRATEGY_CHOICE - Choix de la stratégie principale

**Messages de Sarah:**
1. "D'accord..."
2. "Qu'est-ce que je dois faire ?"
3. "Dis-moi quoi faire et je le ferai."

**CHOIX MAJEUR (définit la branche principale):**

**A.** "🏠 Reste dans la maison. Barricade-toi et attends que ça se calme."
→ Déclenche **BRANCHE I: LE SIÈGE**
→ Flag: `branch = 'siege'`

**B.** "🔍 Va chercher Tante Claire. Elle a besoin de toi."
→ Déclenche **BRANCHE II: LA VILLE**
→ Flag: `branch = 'ville'`

**C.** "🏔️ Rejoins notre maison de campagne. Tu te souviens du chemin ?"
→ Déclenche **BRANCHE III: L'EXODE**
→ Flag: `branch = 'exode'`

---

# 🏠 BRANCHE I: LE SIÈGE

**Thème:** Claustrophobie, gestion des intrusions, psychologie de l'isolement

---

## 🔵 NŒUD: BRANCH_SIEGE - Début du siège

**Messages de Sarah:**
1. "Rester ici... d'accord."
2. "Je vais vérifier les fenêtres."
3. "Il reste des conserves dans le placard. Et de l'eau."
4. "Je vais tenir le plus longtemps possible."
5. "..."
6. "Papa ?"
7. "Quelqu'un frappe à la porte."

**Choix:**
- "Ne réponds pas. Reste silencieuse." → SIEGE_KNOCK_IGNORE
- "Demande qui c'est, mais n'ouvre PAS." → SIEGE_KNOCK_ASK

---

## Rameau I.A: L'ISOLEMENT

### 🔵 NŒUD: SIEGE_KNOCK_IGNORE - Ignorer les coups

**Messages de Sarah:**
1. "..."
2. "Il frappe encore."
3. "S'il vous plaît... c'est M. Bernard. Votre voisin."
4. "J'ai besoin d'aide..."
5. "Papa, c'est vraiment le voisin. Je reconnais sa voix."

**Choix:**
- "Ouvre-lui. Mais sois prudente." → SIEGE_BERNARD_OPEN (Flag: bernardInside = true)
- "Non. C'est trop dangereux. Ne bouge pas." → SIEGE_BERNARD_IGNORE

---

### 🔵 NŒUD: SIEGE_KNOCK_ASK - Demander qui c'est

**Messages de Sarah:**
1. "Qui... qui est là ?"
2. "C'est M. Bernard, ton voisin. S'il te plaît, ouvre..."
3. "Il a l'air vraiment mal en point."

**Choix:**
- "Ouvre-lui." → SIEGE_BERNARD_OPEN (Flag: bernardInside = true)
- "Dis-lui que tu ne peux pas. C'est trop risqué." → SIEGE_BERNARD_REFUSE

---

### 🔵 NŒUD: SIEGE_BERNARD_OPEN - Accueillir M. Bernard

**Messages de Sarah:**
1. "Je... j'ouvre."
2. "..."
3. "C'est bon, il est entré. Je referme."
4. "Il a l'air très faible. Il tremble."
5. "Merci mon petit... Merci..."
6. "Papa, il dit qu'il est diabétique."
7. "Son insuline est chez lui mais... il peut plus y retourner."
8. "Les pilleurs ont défoncé sa porte."

**Choix:**
- "Il va falloir aller chercher son insuline. C'est vital." → SIEGE_INSULIN_MISSION
- "Qu'il se repose. On verra demain si ça se calme." → SIEGE_INSULIN_WAIT
- "Installe-le confortablement. Rationne l'eau et la nourriture." → SIEGE_BERNARD_SETTLE

---

### 🔵 NŒUD: SIEGE_BERNARD_IGNORE - Ignorer M. Bernard

**Messages de Sarah:**
1. "D'accord... je bouge pas."
2. "..."
3. "Il arrête pas de frapper..."
4. "S'il vous plaît... j'ai besoin de mon insuline..."
5. "..."
6. "Il est parti."
7. "..."
8. "Papa... j'entends quelqu'un crier dehors."
9. "C'est... c'est la voix de M. Bernard."
10. "Et puis plus rien."

**Choix unique:**
- "Tu as fait ce qu'il fallait. Ta sécurité d'abord." → SIEGE_NIGHT_1
  (Flags: bernardDead = true, guilt = true)

---

### 🔵 NŒUD: SIEGE_BERNARD_REFUSE - Refuser poliment

**Messages de Sarah:**
1. "Monsieur Bernard... je peux pas ouvrir. Désolée."
2. "Je comprends, petite... Reste en sécurité."
3. "Il s'en va."
4. "..."
5. "J'espère qu'il va s'en sortir."

**Choix unique:**
- "Tu as fait le bon choix. Maintenant, prépare-toi pour la nuit." → SIEGE_NIGHT_1
  (Flag: bernardRefused = true)

---

### 🔵 NŒUD: SIEGE_NIGHT_1 - Première nuit

**Messages de Sarah:**
1. "La nuit tombe."
2. "J'ai éteint toutes les lumières."
3. "Y'a des feux dehors. Des voitures qui brûlent."
4. "Papa... j'arrive pas à dormir."

**Choix:**
- "Je reste en ligne avec toi. Tu n'es pas seule." → SIEGE_DAY_2
- "Économise la batterie. On se parle demain matin." → SIEGE_DAY_2 (Flag: batterySaved = true)

---

### 🔵 NŒUD: SIEGE_DAY_2 - Jour 2 - Problème de nourriture

**Messages de Sarah:**
1. "Papa ?"
2. "C'est le matin. Jour 2."
3. "Les conserves commencent à diminuer."
4. "Si ça dure longtemps... je vais devoir sortir chercher à manger."

**Choix:**
- "Rationne tout ce que tu as. 2 repas par jour maximum." → SIEGE_RATION
- "On va planifier une sortie. Repère les maisons les plus sûres." → SIEGE_RECON

---

## Rameau I.B: LA COMMUNAUTÉ

**[À DÉVELOPPER]**
- Une famille (mère + enfant) demande refuge
- Choix: Accepter / Refuser
- Si accepter: gestion des tensions, partage des ressources
- Arc "La Trahison Interne" si confiance mal placée

---

## Rameau I.C: L'ASSAUT

**[À DÉVELOPPER]**
- Milice "Les Gardiens" ou pilleurs organisés encerclent la maison
- Arc "La Négociation"
- Arc "La Défense"
- Jonctions possibles vers BRANCHE III (fuite)

---

## Rameau I.D: L'INCENDIE

**[À DÉVELOPPER]**
- Maison en feu (accident ou combat)
- Choix: Sauter par la fenêtre / Passer par le garage
- Jonctions forcées vers BRANCHE II ou III

---

# 🏙️ BRANCHE II: LA VILLE

**Thème:** Chaos urbain, danger constant, perte de l'innocence, rencontres

---

## 🔵 NŒUD: BRANCH_VILLE - Départ vers la ville

**Messages de Sarah:**
1. "Chercher Tante Claire... oui, tu as raison."
2. "Je peux pas la laisser toute seule dehors."
3. "Je prends mon sac à dos. Et le téléphone."
4. "Elle allait au supermarché normalement."
5. "C'est à 20 minutes à pied."
6. "J'y vais."

**Choix:**
- "Reste sur les petites rues. Évite les grandes avenues." → VILLE_SMALL_STREETS (Flag: routeChoice = 'safe')
- "Prends le chemin le plus rapide. Mais sois très prudente." → VILLE_MAIN_ROAD (Flag: routeChoice = 'fast')

---

## Rameau II.A: LE LOUP SOLITAIRE

### 🔵 NŒUD: VILLE_SMALL_STREETS - Petites rues

**Messages de Sarah:**
1. "Je passe par les petites rues."
2. "C'est calme ici... presque trop calme."
3. "Toutes les voitures sont abandonnées."
4. "Y'a des alarmes qui sonnent partout."
5. "Attends... je vois quelque chose."
6. "La voiture de Tante Claire ! Elle est garée devant la pharmacie !"

**Choix:**
- "Entre dans la pharmacie. Elle est peut-être là." → VILLE_PHARMACY_ENTER
- "Appelle-la d'abord. Ne prends pas de risques inutiles." → VILLE_PHARMACY_CALL

---

### 🔵 NŒUD: VILLE_MAIN_ROAD - Grande avenue (danger)

**Messages de Sarah:**
1. "Je prends la grande avenue."
2. "..."
3. "Oh non..."
4. "Papa, c'est... c'est le chaos total."
5. "Y'a des gens qui pillent les magasins."
6. "Des voitures en feu."
7. "Je vois des silhouettes qui courent."

**Choix:**
- "CACHE-TOI ! Maintenant !" → VILLE_HIDE_QUICK
- "Cours ! Retourne dans les petites rues !" → VILLE_RETREAT

---

## Rameau II.B: L'ALLIÉ (Sarah et Chloé)

**[À DÉVELOPPER]**
- Arc "La Pharmacie": Rencontre avec Chloé, 13 ans
- Arc "La Voiture": Chloé veut voler une voiture
- Arc "L'Hôpital": Retrouver Tante Claire blessée
- Point de Rupture: "LE DILEMME DE CLAIRE"

---

## Rameau II.C: LA CAPTURE

**[À DÉVELOPPER]**
- Arc "Le Camp du Stade": Sarah prisonnière de "Les Gardiens"
- Arc "L'Évasion": Tentative de fuite
- Arc "La Taupe": Garde qui veut déserter

---

# 🏔️ BRANCHE III: L'EXODE

**Thème:** Le voyage, la route, la nature, l'épuisement

---

## 🔵 NŒUD: BRANCH_EXODE - Départ vers la base

**Messages de Sarah:**
1. "La maison de campagne... oui ! Je me souviens !"
2. "On y allait tous les étés."
3. "C'est loin... mais y'a le bunker là-bas."
4. "Tu m'avais montré où était la clé."
5. "Je prends des affaires. Des vêtements, de la nourriture..."
6. "Le chemin fait... 50 kilomètres je crois ?"

**Choix:**
- "Prends l'autoroute. C'est le plus direct." → EXODE_HIGHWAY (Flag: exodeRoute = 'highway')
- "Coupe par la forêt. C'est plus long mais plus sûr." → EXODE_FOREST (Flag: exodeRoute = 'forest')

---

## Rameau III.A: L'AUTOROUTE

### 🔵 NŒUD: EXODE_HIGHWAY - L'autoroute abandonnée

**Messages de Sarah:**
1. "Je prends l'autoroute."
2. "Mon vélo est dans le garage."
3. "En pédalant fort, je peux faire 15-20 km par jour."
4. "J'arrive sur l'autoroute..."
5. "Papa, c'est incroyable."
6. "Y'a des MILLIERS de voitures abandonnées."
7. "C'est comme dans les films de zombies."

**Choix:**
- "Fouille quelques voitures. Tu trouveras peut-être des provisions." → EXODE_LOOT_CARS
- "N'y touche pas. Continue à avancer." → EXODE_KEEP_MOVING

---

## Rameau III.B: LA FORÊT

### 🔵 NŒUD: EXODE_FOREST - La traversée de la forêt

**Messages de Sarah:**
1. "Je vais passer par la forêt."
2. "Y'a un sentier que tu m'avais montré une fois."
3. "Ça sera plus long mais... moins de gens."
4. "Je rentre dans la forêt."
5. "C'est bizarre... c'est tellement silencieux ici."
6. "On dirait que le monde extérieur existe plus."

**Choix:**
- "C'est bien. Profite du calme et avance régulièrement." → EXODE_FOREST_WALK
- "Reste vigilante. La nature peut être dangereuse aussi." → EXODE_FOREST_CAREFUL

---

## Rameau III.C: LE VILLAGE

**[À DÉVELOPPER]**
- Point de Rupture: "L'ÉTAT DU VILLAGE"
  - Situation A: Village Fantôme
  - Situation B: Village Barricadé
- Arc "La Communauté Villageoise"
- Choix: Rester au village / Continuer

---

## Rameau III.D: LA BASE

**[À DÉVELOPPER]**
- Arc "Les Occupants": La maison est déjà occupée
  - Amis (famille Martin) → Fin "Le Sanctuaire"
  - Milice → Arc "Reprendre la Base"
- Arc "Le Bunker": Code à trouver
  - Code correct → Fin "Le Bunker"
  - Code incorrect → Alarme → Arc "La Défense du Bunker"

---

# 🎬 FINS POSSIBLES

## Branche I: LE SIÈGE

- **Fin 1.1 "Le Fort"** - Sarah tient le siège seule (très difficile)
- **Fin 1.2 "La Capture (Siège)"** - Sarah est capturée par les pilleurs
- **Fin 1.3 "L'Intrusion"** - Les pilleurs entrent, Sarah se fait repérer
- **Fin 1.4 "Dépouillé"** - Milice prend le téléphone satellite
- **Fin 1.5 "Exécuté"** - Combat perdu contre la milice
- **Fin 1.6 "La Trahison"** - Trahi par quelqu'un qu'on a aidé

## Branche II: LA VILLE

- **Fin 2.1 "Perdu en Ville"** - Sarah est tuée par des pilleurs
- **Fin 2.2 "Le Camp"** - Sarah reste prisonnière au stade
- **Fin 2.3 "Retrouvailles"** - Sarah et Tante Claire survivent ensemble
- **Fin 2.4 "La Rupture"** - Sarah abandonne Tante Claire et part avec Chloé
- **Fin 2.5 "Libre"** - Sarah s'évade du camp du stade

## Branche III: L'EXODE

- **Fin 3.1 "Le Bunker"** - Sarah atteint le bunker en sécurité
- **Fin 3.2 "Le Sanctuaire"** - Sarah rejoint les amis à la base
- **Fin 3.3 "Jamais Arrivé"** - Sarah se perd, connexion perdue
- **Fin 3.4 "Le Nouveau Foyer"** - Sarah reste au village
- **Fin 3.5 "L'Évacuation"** - Sarah est prise en charge par l'armée
- **Fin 3.6 "Le Chasseur"** - Fin ambiguë avec un chasseur rencontré

## Fins Universelles (toutes branches)

- **Fin X.1 "CONNEXION PERDUE"** - Le téléphone satellite est perdu/volé/cassé
- **Fin X.2 "BATTERIE MORTE"** - Le téléphone s'éteint définitivement
- **Fin X.3 "SIGNAL PERDU"** - Sarah entre dans une zone sans couverture satellite

---

# 🎯 FLAGS ET CONDITIONS

## Flags Principaux
- `branch` : 'siege' | 'ville' | 'exode'
- `day` : Numéro du jour (1, 2, 3...)

## Flags Branche Siège
- `bernardInside` : boolean - M. Bernard est dans la maison
- `bernardDead` : boolean - M. Bernard est mort dehors
- `bernardRefused` : boolean - A refusé d'ouvrir à M. Bernard
- `guilt` : boolean - Culpabilité (mort de Bernard)
- `batterySaved` : boolean - A économisé la batterie

## Flags Branche Ville
- `routeChoice` : 'safe' | 'fast'
- `hasChloé` : boolean - Voyage avec Chloé
- `claireFound` : boolean - A retrouvé Tante Claire
- `claireDead` : boolean - Tante Claire est morte
- `claireAbandoned` : boolean - A abandonné Tante Claire

## Flags Branche Exode
- `exodeRoute` : 'highway' | 'forest'
- `injured` : boolean - Sarah est blessée
- `hasVehicle` : boolean - A un véhicule
- `villageStay` : boolean - Reste au village

---

# 📊 STATISTIQUES DE DÉVELOPPEMENT

## Nœuds Implémentés
- ✅ Tronc commun complet (8 nœuds)
- ✅ Branche I - Début (7 nœuds)
- ✅ Branche II - Début (2 nœuds)
- ✅ Branche III - Début (2 nœuds)
- **Total actuel: 19 nœuds**

## Nœuds À Développer
- ⏳ Branche I - Rameaux B, C, D (~15 nœuds)
- ⏳ Branche II - Rameaux B, C complets (~20 nœuds)
- ⏳ Branche III - Rameaux C, D complets (~15 nœuds)
- ⏳ Toutes les fins (~25 nœuds de fin)
- **Estimation total: ~95+ nœuds narratifs**

## Progression
- Phase 1 (Tronc + Débuts branches): ✅ 100%
- Phase 2 (Développement branches): 🔄 20%
- Phase 3 (Fins et polish): ⏳ 0%

---

# 💡 NOTES DE CONCEPTION

## Principes Narratifs
1. Chaque choix doit avoir des conséquences claires
2. Pas de "bon" ou "mauvais" choix absolu
3. Les dilemmes moraux sont au cœur du jeu
4. La survie n'est pas garantie
5. Certaines fins sont volontairement ambiguës

## Timing des Messages
- Messages courts: 1-2 secondes de délai
- Messages importants: 2-3 secondes
- Révélations: 3-4 secondes
- Pauses dramatiques ("..."): 2-3 secondes

## Jonctions Entre Branches
Certains événements peuvent forcer un changement de branche:
- Siège → Ville: Fuite après incendie
- Siège → Exode: Fuite par la cave
- Ville → Exode: Échapper au chaos urbain

---

**Dernière mise à jour:** Jour 1 de développement
**Version du script:** 1.0
**Statut:** En développement actif
