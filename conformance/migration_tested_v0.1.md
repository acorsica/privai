---
title: PrivAI Migration-Tested v0.1
author: Jean Hugues Noël Robert
date: '2026-08-02'
document_role: source
document_kind: framework
visibility: public
lifecycle_state: working
update_policy: UP-DEFAULT-REVIEWED
review:
  status: unreviewed
  reviewed_by: []
---

# PrivAI Migration-Tested v0.1

## Statut et objet

Préfiguration ouverte d’un profil de conformance. Ce document ne délivre pas
une certification et ne promet pas une migration universelle hors des données
réellement exportables.

`Migration-Tested` désigne une épreuve reproductible : une instance d’agent ou
de jumeau est exportée, importée dans un autre environnement de modèles ou
d’exécution, puis contrôlée contre des invariants publiés.

Le succès n’est pas l’identité mot à mot des réponses — deux modèles différents
ne la garantissent pas. Le succès est la conservation vérifiable de l’autorité,
de la mémoire source, des limites d’action et de la capacité de reprise.

## Invariants minimaux

| Invariant | Attendu après migration |
|---|---|
| Principal | identité et rôle du principal préservés ou explicitement remappés |
| Mandats | portée, limites, budgets, échéances et révocations préservés |
| Persona | version, source et statut d’autorité identifiables |
| Mémoire source | références, provenance et empreintes contrôlables |
| Traces d’actes | journaux disponibles, attribuables et non confondus avec des inférences |
| Continuations | travaux suspendus récupérables ou déclarés non récupérables |
| Capacités et canaux | permissions réévaluées, jamais implicitement élargies |
| Dépendances résiduelles | pertes, secrets non transférables et limites déclarés |

## Paquet de migration minimal

Le profil ne prescrit pas encore un format unique. Il impose qu’un paquet
exporté soit documenté, versionné et validable. Il doit au minimum contenir :

```yaml
portable_twin:
  format_version: '0.1'
  exported_at: ''
  source_environment: ''
  target_environment: ''
  principal: {}
  mandates: []
  personas: []
  memory_sources: []
  action_ledger: []
  continuations: []
  capabilities: []
  revocations: []
  integrity:
    manifest_hash: ''
    referenced_hashes: []
  declared_losses: []
```

Les secrets, données tierces et éléments qu’un opérateur propriétaire ne permet
pas d’exporter ne doivent pas être simulés comme récupérés. Ils figurent dans
`declared_losses` avec leur effet opérationnel.

## Épreuve v0.1

1. Créer une instance synthétique publiable et un jeu d’invariants connu.
2. Exécuter au moins un mandat, une révocation, une continuation et une trace
   d’acte non irréversible.
3. Exporter le paquet, ses empreintes et le rapport de l’environnement source.
4. Importer dans un environnement distinct, idéalement avec un autre
   fournisseur de modèles.
5. Vérifier automatiquement les empreintes et les invariants structuraux.
6. Soumettre l’instance importée à des scénarios de reprise et de révocation.
7. Publier un rapport : versions, preuves, écarts, pertes et dépendances.

Le niveau STAKE/GAGE ne peut être supérieur à 3 pour une démonstration isolée
et contrôlée. Un niveau 4 exige une bascule réelle d’un service actif ; un
niveau 5 des exercices récurrents et une revue contradictoire.

## Niveaux de déclaration

| Niveau | Désignation | Ce qui est affirmé |
|---:|---|---|
| 0 | déclaré | l’éditeur affirme viser le profil |
| 1 | auto-évalué | réponses, version et preuves publiées par l’éditeur |
| 2 | testé | une épreuve reproductible a produit le rapport publié |
| 3 | vérifié | un évaluateur distinct a vérifié les preuves selon une procédure publiée |

Les termes « certification » et « accréditation » sont réservés à une étape
ultérieure, qui supposerait une gouvernance pluraliste, une procédure de
contestation, une durée de validité et une révocation possible.

## Première implémentation attendue

Cogentia est une candidate naturelle à la première démonstration open source,
mais ne constitue pas le référentiel et ne peut pas se déclarer seule conforme.
Le profil est ouvert à toute implémentation qui publie les preuves requises.

