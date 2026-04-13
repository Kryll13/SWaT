# Atelier 2 - Sources de Risque et Objectifs Visés
## Modèle alternatif - Cas SWaT

---

## 1/ LES OBJECTIFS DE L'ATELIER

Le but de l'atelier 2 est d'identifier les sources de risque (SR) et leurs objectifs visés (OV), en lien avec le contexte particulier de l'étude. L'atelier vise à répondre à la question suivante : **qui ou quoi pourrait porter atteinte aux missions et valeurs métier identifiées dans l'atelier 1, et dans quels buts ?**

Les sources de risque et les objectifs visés sont ensuite caractérisés et évalués en vue de retenir les plus pertinents. Ils seront utiles à la construction des scénarios des ateliers 3 et 4.

### Questions génératrices

| Question | Contexte SWaT |
|----------|-------------|
| Qui pourrait attaquer l'usine ? | Hackers, employés, ext, ext |
| Quelle motivation ? | Financière, revenge, idéologique |
| Quels objectifs ? | Interrompre, compromettre, voler |
| Par quels moyens ? | Cyber, physique, erreur |
| Quelles conséquences ? | Contamination, interruption, fuga |

---

## 2/ LES PARTICIPANTS À L'ATELIER

| Participant | Rôle | Disponibilité |
|------------|------|---------------|
| Direction | Approbateur | Fin d'atelier |
| Métier (Directeur usine) | Contributeur clé | Required |
| RSSI Voelia | Expert sécurité | Required |
| Analyste EBIOS | Animateur | Required |
| Spécialiste menace numérique | Consultant | Optionnel |

### Répartition suggérée

| Fonction | Nombre |
|----------|--------|
| Animateur | 1 |
| Analystes | 2-3 |
| Métier | 1-2 |
| RSSI | 1 |
| **Total** | **5-7** |

---

## 3/ LES DONNÉES DE SORTIE

À l'issue de l'atelier, vous devez avoir établi les éléments suivants :

### 3.1 Couples SR/OV prioritaires

| Couple | SR | OV | Priorité |
|--------|----|----|----------|
| SR1/OV1 | Hackeurs externes | Interrompre traitement | 1 |
| SR1/OV2 | Hackeurs externes | Voler données | 2 |
| SR3/OV1 | Employé mécontent | Contaminer l'eau | 3 |
| SR4/OV3 | Employé négligent | Erreur manipulation | 4 |

### 3.2 Couples SR/OV secondaires

| Couple | SR | OV | Surveillance |
|--------|----|----|-------------|
| SR5/OV4 | ITexpert | Erreur config | Alerte |
| SR6/OV3 | SPE | Contractuel | Monitoring |
| SR7/OV4 | Hacktivistes | Dénaturation | Veille |

### 3.3 Cartographie des sources de risque

```
                    +------------------+
                    |   PERIMÈTRE SWaT  |
                    |  BE1 - BE5       |
                    +--------+---------+
                             |
         +----------------+-----+-----+----------------+
         |                |                     |
    +----+----+    +----+----+          +----+----+
    |   IT    |    |  OT   |          | Physique|
    +----+----+    +----+----+          +----+----+
       ^             ^                    ^
    +--+--+      +--+--+               +--+--+
    |SR1 |      |SR3 |               |SR4 |
    |SR2 |      |SR4 |               |SR5 |
    |SR7 |      |   |               |   |
    +----+      +----+               +----+
```

---

## 4/ LES ÉTAPES DE L'ATELIER

Cet atelier, d'une durée variable, peut nécessiter 2 heures à une journée de travail en vue de :
- A - identifier les sources de risque et les objectifs visés ;
- B - évaluer la pertinence des couples SR/OV ;
- C - sélectionner les couples SR/OV jugés prioritaires pour poursuivre l'analyse.

---

## A - Identification des sources de risque et objectifs visés

### A.1 Liste des sources de risque

| ID | Source de risque | Catégorie | Type |
|----|-----------------|-----------|------|
| SR1 | Hackeurs externes | Intentionnelle | Externe |
| SR2 | Groupes hacktivistes | Intentionnelle | Externe |
| SR3 | Employé mécontent | Intentionnelle | Interne |
| SR4 | Employé négligent | Accidentelle | Interne |
| SR5 | ITexpert (prestataire) | Accidentelle | Externe |
| SR6 | SPE (fournisseur) | Accidentelle | Externe |
| SR7 | Hacktivistes | Intentionnelle | Externe |
| SR8 | Opportunistes | Accidentelle | Externe |
| SR9 | Catastrophe naturelle | Naturelle | - |
| SR10 | Panne équipements | Technique | - |

### A.2 Objectifs visés associés aux BE

| BE | Objectifs visés (OV) | Description |
|----|------------------|-------------|
| BE1 | OV1 | Interrompre/altérer traitement |
| BE1 | OV2 | Contaminer l'eau |
| BE2 | OV3 | Arrêter distribution |
| BE3 | OV4 | Voler/exfiltrer données |
| BE4 | OV5 | Atteindre réputation |
| BE5 | OV6 | Détériorer équipements |

### A.3 Matrice SR/OV

| SR | OV1 | OV2 | OV3 | OV4 | OV5 | OV6 |
|----|-----|-----|-----|-----|-----|-----|
| SR1 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| SR2 | - | - | - | ✓ | ✓ | - |
| SR3 | ✓ | ✓ | - | - | ✓ | ✓ |
| SR4 | - | ✓ | ✓ | - | - | - |
| SR5 | - | - | ✓ | ✓ | - | ✓ |
| SR6 | - | - | ✓ | - | - | - |
| SR7 | - | - | - | ✓ | ✓ | - |
| SR8 | - | - | - | - | - | ✓ |
| SR9 | ✓ | - | ✓ | - | - | ✓ |
| SR10| - | - | ✓ | - | - | ✓ |

### A.4 Détail des couples SR/OV

#### Couple SR1/OV1 - Hackeurs → Interruption traitement

```
Source: SR1 (Hackeurs externes)
 Objectif: OV1 (Interruption traitement)
   Vecteur: exploitation réseau via Livebox
   Cible: HMI, PLCs
 Impact: BE1 (Qualité eau), BE2 (Continuité)
```

#### Couple SR1/OV2 - Hackeurs → Contamination

```
Source: SR1 (Hackeurs externes)
 Objectif: OV2 (Contamination chimique)
   Vecteur: accès HMI sans auth
   Cible: dosages P2 (PLC2)
 Impact: BE1 (Qualité eau) - CRITIQUE
```

#### Couple SR3/OV1 - Employé mécontent → Interruption

```
Source: SR3 (Employé mécontent ou malveillant)
 Objectif: OV1 (Interruption traitement)
   Vecteur: accès interne, manipulation
   Cible: vanne, pompe
 Impact: BE1, BE2 - CRITIQUE
```

#### Couple SR4/OV2 - Employé négligent → Erreur

```
Source: SR4 (Employé négligent)
 Objectif: OV2 (Erreur manipulation)
   Vecteur: non-respect procédure
   Cible: dosages, paramètres
 Impact: BE1 - HAUTE
```

#### Couple SR5/OV3 - ITexpert → Erreur maintenance

```
Source: SR5 (ITexpert)
 Objectif: OV3 (Erreur configuration)
   Vecteur: intervention sur réseau
   Cible: NAS, postes
 Impact: BE2, BE3 - HAUTE
```

---

## B - Évaluation de la pertinence des couples SR/OV

### B.1 Critères d'évaluation

| Critère | Échelle | Description |
|--------|---------|-------------|
| **Capacité** | 1-4 | Potentiel technique de la SR |
| **Motivation** | 1-4 | Intensité de la motivation |
| **Potentiel** | 1-4 | Probabilité de réalisation |
| **Impact** | 1-4 | Gravité si succès |

### B.2 Grille d'évaluation

| Couple | Capacité | Motivation | Potentiel | Impact | Score |
|--------|----------|------------|------------|---------|-------|
| SR1/OV1 | 3 | 4 | 3 | 4 | 14 |
| SR1/OV2 | 3 | 4 | 3 | 4 | 14 |
| SR1/OV3 | 3 | 4 | 3 | 4 | 14 |
| SR1/OV4 | 3 | 4 | 4 | 3 | 14 |
| SR2/OV4 | 1 | 2 | 1 | 3 | 7 |
| SR3/OV1 | 2 | 2 | 2 | 4 | 10 |
| SR3/OV2 | 2 | 2 | 1 | 4 | 9 |
| SR4/OV2 | 1 | N/A | 3 | 3 | 7 |
| SR5/OV3 | 1 | N/A | 2 | 3 | 6 |
| SR6/OV3 | 2 | 1 | 1 | 3 | 7 |

### B.3 Justification des scores

| Couple | Justification |
|--------|--------------|
| SR1/* | Capacité haute (APT), motivation financière forte, rends ciblées OT |
| SR3/* | Accès interne, connaissance système, mais motivation variable |
| SR4/* | Erreur humaine probable mais impact limité |
| SR5/* | Capacité limitée (TPE), mais accès directo |
| SR6/* | Accès contractuel, mais contrôle existant |

### B.4 Matrice de qualification

```
               POTENTIEL
                 1    2    3    4
           +----+----+----+----+
         1 |    |    |    |    |
IMPACT  2  |    |SM6 |    |    |
         3  |    |    |SM4 |    |
         4  |    |    |SM3 |SR1 |
           +----+----+----+----+
                  ^
               Zone critique
```

---

## C - Sélection des couples SR/OV prioritaires

### C.1 Couples prioritaires (Score ≥ 10)

| Priorité | Couple | Score | Action |
|----------|--------|-------|--------|
| 1 | SR1/OV1 | 14 | Atelier 3-4 |
| 1 | SR1/OV2 | 14 | Atelier 3-4 |
| 1 | SR1/OV3 | 14 | Atelier 3-4 |
| 1 | SR1/OV4 | 14 | Atelier 3-4 |
| 2 | SR3/OV1 | 10 | Atelier 3-4 |
| 3 | SR3/OV2 | 9 | Atelier 3 |

### C.2 Couples secondaires (Score 6-9)

| Priorité | Couple | Score | Action |
|----------|--------|-------|--------|
| 4 | SR4/OV2 | 7 | Veille |
| 4 | SR2/OV4 | 7 | Veille |
| 4 | SR6/OV3 | 7 | Veille |
| 5 | SR5/OV3 | 6 | Veille |

### C.3 Sources de risque exclues

| SR | Motivation | Raison |
|----|-----------|-------|
| SR7 | Capacité trop faible, pas d'intérêt |
| SR8 | Pas de capacité technique |
| SR9 | Risque naturel majeur non évalué |
| SR10 | Détection maintenance suffice |

### C.4 Cartographie finale

```
                    +------------------------+
                    |   PERIMÈTRE SWaT       |
                    |  BE: 1,2,3,4,5         |
                    +---------+------------+
                              |
          +------------------+--+------------------+
          |                  |                     |
     +----+----+      +-----+-----+          +------+-----+
     |   IT   |      |   OT      |          | Physique  |
     +----+---+      +----+-----+          +-----+-----+
        ^                  ^                    ^
     +--+---+          +---+----+            +----+----+
     |SR1 |          | SR1   |            |SR3 |SR4 |
     +----+          | SR3   |            +----+----+
                    +------+                +-----+-----+
                    | SR4 |                | SR5     |
                    +-----+                +----------------+
```

---

## Synthèse - Atelier 2

### Couples SR/OV prioritaires

| # | Couple | Description | Score |
|---|--------|-------------|-------|
| 1 | SR1/OV1 | Hackeurs → Interruption | 14 |
| 2 | SR1/OV2 | Hackeurs → Contamination | 14 |
| 3 | SR1/OV3 | Hackeurs → Arrêt distribution | 14 |
| 4 | SR1/OV4 | Hackeurs → Exfiltration | 14 |
| 5 | SR3/OV1 | Employé mécontent → Interruption | 10 |
| 6 | SR3/OV2 | Employé mécontent → Contamination| 9 |

### Points clés

- **Source principale** : SR1 (Hackeurs externes) - score maximum sur tous les critères
- **Vulnérabilités clés** : HMI/Historian sans auth facilitent SR1
- **Menace interne** : SR3, SR4 à surveiller
- **Risque externe** : ITexpert (SR5) à contrôler

### Livrables

- [x] 10 sources de risque identifiées
- [x] 6 objectifs visés définis
- [x] Matrice SR/OV complète
- [x] 6 couples prioritaires retenus
- [x] Cartographie finale

### Passage aux ateliers 3-4

- Les couples SR1/* seront détaillés en scénarios de risque
- SR3, SR4 comme menace interne
- SR5: surveillance maintenir