# Projet de gouvernance cybersécurité GitLab - Guide explicatif

**De quoi s'agit-il ?** Une évaluation **externe, sur sources publiques**, du risque cyber et de la gouvernance de GitLab :
**EBIOS RM -> PSSI -> analyse d'écarts -> feuille de route** (Risque -> Exigence -> Action).
Preuves arrêtées au 4 octobre 2026. Ce n'est *ni* un audit interne, *ni* un test d'intrusion, *ni* une évaluation de vulnérabilités, *ni* un audit de certification ISO 27001, et cela n'affirme pas que GitLab est peu sûr.
**Règle d'or : « non vérifiable publiquement » ne veut pas dire « absent ».**

## Les 5 livrables

| N° | Fichier | Format | Contenu |
|----|---------|--------|---------|
| 1 | `01_Rapport_principal.docx` | Word | Synthèse de direction, méthodologie, aperçu de GitLab, les cinq ateliers EBIOS, registre des risques, résumé de la PSSI, analyse d'écarts, plan d'amélioration, feuille de route, annexes (~36 pages) |
| 2 | `02_Dossier_EBIOS_RM.xlsx` | Excel | Valeurs métier, biens supports, événements redoutés, sources de risque, écosystème, scénarios stratégiques et opérationnels, registre des risques, traitement. Scores en formules actives |
| 3 | `03_PSSI.docx` | Word | 32 exigences de sécurité en 11 domaines, chacune avec responsable, fréquence de revue, indicateurs et correspondance ISO 27002 / NIST CSF / SOC 2 ; exceptions, suivi, processus de revue (~20 pages) |
| 4 | `04_Feuille_de_route_securite.xlsx` (+ `.png`) | Excel / image | 26 actions sur 24 mois avec indice de priorité, responsables, dépendances, indicateurs et Gantt piloté par des formules |
| 5 | `05_Registre_de_preuves.xlsx` | Excel | 36 sources (URL, date, fiabilité A/B/C, assertion paraphrasée, risques/mesures soutenus) + analyse d'écarts |

Pourquoi Excel pour les n° 2, 4 et 5 : ce sont des tableaux de travail avec formules de calcul et filtres ; le récit se trouve dans les deux documents Word.

## Lecture rapide (10 minutes)
1. Section 1 du rapport (synthèse de direction).
2. Registre des risques (section 6 du rapport ou onglet `Registre_Risques`).
3. Analyse d'écarts (section 8) : ce qui est démontrable de l'extérieur.
4. Feuille de route (section 10 ou livrable 4).

## Résultats clés
- 13 risques : 2 Critiques (compromission d'identité privilégiée ; exploitation de vulnérabilités produit critiques), 4 Élevés, 6 Moyens, 1 Faible.
- Cible après la feuille de route de 24 mois : score de risque total 168 -> 106 (-37 %).
- Analyse d'écarts des 32 exigences : 6 fortement démontrées, 14 partiellement, 10 non vérifiables publiquement, 2 avec signal public d'exposition.
- Faits publics notables : départ du RSSI divulgué dans le 10-K FY2026 (26 févr. 2026, intérim en place) ; CVE-2026-85706 (CVSS 10, inscrite KEV, sept. 2026).

## Fonctionnement des scores
Risque = Impact (1-5) x Vraisemblance (1-5) : Critique >= 20, Élevé 15-19, Moyen 8-14, Faible <= 7.
Indice de priorité de la feuille de route = 2 x score du risque lié le plus élevé + 4 x urgence + 2 x (6 - effort) : P1 >= 62, P2 48-61, P3 < 48.
Les cellules en gras sur fond gris des classeurs sont des saisies de jugement : modifiez-les et tout se recalcule.

## Limites, en toute honnêteté
- Les scores sont des jugements d'analyste fondés sur des preuves publiques ; à valider avec les données internes de GitLab.
- Certains détails de vulnérabilités de sept. 2026 viennent de sources secondaires (notes B/C) : à vérifier dans les notes de version de GitLab.
- Certaines pages du handbook ou documents de conception peuvent retarder sur la réalité (p. ex. le plan directeur de reprise après sinistre ; la formulation de l'édition ISO 27001).
- Les responsables sont des rôles proposés, pas l'organigramme réel de GitLab.
- Les sources citées et leurs assertions sont en français (traduction) ; les noms de produits, identifiants CVE et titres de sources restent dans leur forme d'origine.
- Sommaire Word : ouvrir dans Word et choisir « Mettre à jour le champ ».
