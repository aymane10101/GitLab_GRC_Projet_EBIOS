# Évaluation des risques cybersécurité et gouvernance de GitLab

## Vue d'ensemble

Projet personnel de **GRC / gestion des risques cybersécurité** consacré à une évaluation externe de GitLab fondée exclusivement sur des sources publiques.

La démarche suit la chaîne :

**EBIOS Risk Manager → PSSI → Analyse d'écarts → Traitement des risques → Feuille de route de sécurité**

L'objectif est d'identifier et de prioriser les principaux risques cybersécurité, de les traduire en exigences de sécurité, puis de proposer des actions de traitement hiérarchisées et planifiées.

> **Important :** il s'agit d'une étude externe sur sources publiques. Ce projet ne constitue ni un audit interne, ni un test d'intrusion, ni une évaluation exhaustive des vulnérabilités, ni une certification ISO 27001. L'absence de preuve publique ne signifie pas l'absence du contrôle.

**Date d'arrêt des preuves : 4 octobre 2026.**

## Résultats clés

- **13 risques** identifiés : 2 critiques, 4 élevés, 6 moyens et 1 faible.
- **Score de risque total modélisé : 168 → 106**, soit **-37 %** après la feuille de route de 24 mois.
- **32 exigences PSSI** réparties dans **11 domaines**.
- Analyse d'écarts : **6** exigences fortement démontrées, **14** partiellement démontrées, **10** non vérifiables publiquement et **2** avec signal public d'exposition.
- **26 actions** de sécurité planifiées sur **24 mois**.
- **36 sources publiques** documentées dans le registre de preuves.

## Livrables

| Dossier | Contenu |
|---|---|
| [`docs/`](docs/) | Rapport principal, PSSI et guide explicatif en PDF/DOCX |
| [`ebios/`](ebios/) | Dossier complet des 5 ateliers EBIOS RM et registre des risques |
| [`roadmap/`](roadmap/) | Feuille de route 24 mois et représentation visuelle |
| [`evidence/`](evidence/) | Registre des 36 sources et analyse des preuves |

### Documents principaux

- [Rapport principal — PDF](docs/01_Rapport_principal.pdf)
- [PSSI — PDF](docs/03_PSSI.pdf)
- [Dossier EBIOS RM — Excel](ebios/02_Dossier_EBIOS_RM.xlsx)
- [Feuille de route — Excel](roadmap/04_Feuille_de_route_securite.xlsx)
- [Feuille de route — visuel](roadmap/04_Feuille_de_route_securite_visuel.png)
- [Registre de preuves — Excel](evidence/05_Registre_de_preuves.xlsx)

## Méthodologie

### 1. EBIOS Risk Manager

Les cinq ateliers sont couverts :

1. Cadrage et socle de sécurité
2. Sources de risque
3. Scénarios stratégiques
4. Scénarios opérationnels
5. Traitement du risque

### 2. PSSI

Les résultats de l'analyse de risques sont traduits en **32 exigences de sécurité**, avec responsables proposés, fréquences de revue, indicateurs et correspondances avec **ISO 27002, NIST CSF et SOC 2**.

### 3. Analyse d'écarts

Les exigences sont comparées aux éléments publiquement vérifiables. La qualification distingue les preuves fortes, partielles, l'absence de vérifiabilité publique et les signaux publics d'exposition.

### 4. Traitement et feuille de route

Les risques retenus donnent lieu à des actions priorisées sur 24 mois, avec responsables proposés, dépendances, urgence, effort et indicateurs.

## Modèles de calcul

**Risque = Impact × Vraisemblance**, avec une échelle de 1 à 5 :

- Critique : ≥ 20
- Élevé : 15–19
- Moyen : 8–14
- Faible : ≤ 7

**Indice de priorité de la feuille de route :**

`2 × score du risque lié le plus élevé + 4 × urgence + 2 × (6 − effort)`

- P1 : ≥ 62
- P2 : 48–61
- P3 : < 48

Les classeurs contiennent les formules et les cellules de jugement nécessaires au recalcul.

## Limites

- Les scores sont des jugements d'analyste fondés sur des informations publiques et devraient être validés avec des données internes dans un contexte réel.
- Certains éléments de vulnérabilité peuvent provenir de sources secondaires et nécessitent une validation auprès des sources primaires.
- Les responsables indiqués sont des rôles proposés et ne constituent pas l'organigramme réel de GitLab.
- Les noms de produits, identifiants CVE et titres de sources sont conservés dans leur forme originale lorsque nécessaire.

## Auteur

Projet personnel de portfolio — **Cybersécurité / GRC / Gestion des risques / Gouvernance de sécurité**.
