---
title: KYS Contracts
author: unknown
date: '2026-06-11'
document_role: source
document_kind: documentation
visibility: public
lifecycle_state: working
update_policy: UP-DEFAULT-REVIEWED
provenance:
  origin_type: repository
  origin_repository: acorsica/privai
  origin_ref: '8814485'
  origin_date: '2026-06-11'
  derived_from: []
review:
  status: unreviewed
  reviewed_by: []
---

# KYS Contracts

## Objet

Les contrats KYS définissent les conditions concrètes d’usage d’un profil KYS.

Un profil KYS décrit une projection certifiée, limitée et finalisée d’un corpus. Un contrat KYS précise, pour un cas déterminé, qui peut utiliser cette projection, à quelle fin, avec quelles données, pendant combien de temps, sous quelles limites, avec quelles obligations de traçabilité, de révocation, de contestation et d’audit.

```txt
corpus source
  -> profil KYS
    -> contrat KYS
      -> accès autorisé
        -> usage tracé
          -> révocation / contestation / audit
```

## Principe

Un contrat KYS ne doit jamais être une autorisation générale.

Il doit toujours être :

- finalisé ;
- limité ;
- traçable ;
- révocable selon les conditions prévues ;
- contestable ;
- auditable ;
- explicite sur les usages interdits ;
- explicite sur les droits des personnes concernées ;
- explicite sur la durée ;
- explicite sur les règles posthumes éventuelles ;
- explicite sur les responsabilités des parties.

## Distinction entre profil et contrat

Un profil KYS répond à la question :

> Quelle projection du corpus peut exister pour telle finalité ?

Un contrat KYS répond à la question :

> Qui peut utiliser cette projection, dans quel contexte, pour quels actes, sous quelles conditions ?

Exemple :

```txt
KYS Genealogy
  -> profil général pour usage généalogique

Genealogy contract with researcher X
  -> contrat concret autorisant un usage limité par un chercheur identifié
```

## Structure minimale d’un contrat KYS

Un contrat KYS devrait contenir au minimum :

```yaml
contract:
  id: ""
  title: ""
  version: ""
  status: draft

parties:
  subject_person: ""
  grantor: ""
  grantee: ""
  fiduciary_guardian: ""
  rights_holders: []
  heirs: []
  witnesses: []

profile:
  type: ""
  version: ""
  source_corpus: ""
  scope: ""

purpose:
  authorized_purposes: []
  prohibited_purposes: []

access:
  allowed_content: []
  excluded_content: []
  access_level: ""
  access_method: ""
  storage_policy: ""
  retention_policy: ""

duration:
  start_date: ""
  end_date: ""
  renewal_policy: ""
  posthumous_policy: ""

governance:
  consent_required: true
  revocable: true
  contestable: true
  auditable: true
  publication_log_required: true
  fiduciary_review_required: false

outputs:
  allowed_outputs: []
  prohibited_outputs: []
  publication_policy: ""
  citation_policy: ""
  attribution_policy: ""
  correction_channel: ""

ai_use:
  model_training_allowed: false
  retrieval_allowed: false
  summarization_allowed: false
  generation_allowed: false
  simulation_allowed: false
  digital_twin_use_allowed: false

audit:
  logs_required: true
  log_retention: ""
  review_frequency: ""
  incident_reporting: ""

revocation:
  revocation_channel: ""
  revocation_effect: ""
  data_deletion_policy: ""
  derivative_outputs_policy: ""

signatures:
  grantor_signature: ""
  grantee_signature: ""
  fiduciary_signature: ""
  date: ""
```

## Parties possibles

Un contrat KYS peut impliquer plusieurs catégories d’acteurs :

- personne concernée ;
- auteur ;
- héritier ;
- légataire ;
- ayant droit ;
- mandataire ;
- chercheur ;
- curateur ;
- éditeur ;
- développeur ;
- structure fiduciaire ;
- association ;
- fondation ;
- institution patrimoniale ;
- dépositaire technique ;
- opérateur d’IA ;
- utilisateur final.

Aucun rôle ne doit être présumé équivalent à un autre.

## Finalités

La finalité est l’élément central du contrat.

Exemples de finalités autorisées :

```yaml
authorized_purposes:
  - genealogical_research
  - archive_preservation
  - family_transmission
  - works_cataloging
  - public_publication
  - scholarly_research
  - fiduciary_governance
  - digital_twin_grounding
  - mandate_execution
```

Exemples de finalités interdites :

```yaml
prohibited_purposes:
  - commercial_extraction_without_consent
  - political_targeting
  - insurance_scoring
  - employment_screening
  - unrestricted_model_training
  - impersonation
  - unauthorized_publication
  - unrestricted_simulation
```

## Accès

Le contrat doit préciser la granularité de l’accès :

```yaml
access_levels:
  metadata_only:
    description: "Métadonnées sans contenu principal."
  excerpts:
    description: "Extraits limités et contextualisés."
  curated_subset:
    description: "Sous-corpus préparé pour la finalité."
  full_profile:
    description: "Profil KYS complet, sans accès au corpus source complet."
  supervised_access:
    description: "Accès sous contrôle d’un gardien fiduciaire."
  sealed_access:
    description: "Accès différé ou conditionnel."
```

L’accès au corpus source complet doit rester exceptionnel.

## Usage de l’IA

Un contrat KYS doit distinguer les usages IA :

```yaml
ai_use_categories:
  retrieval:
    description: "Recherche et récupération de passages."
  summarization:
    description: "Synthèse limitée."
  classification:
    description: "Classement ou indexation."
  extraction:
    description: "Extraction de métadonnées."
  generation:
    description: "Production de texte ou média dérivé."
  simulation:
    description: "Représentation active d’une personne ou d’un style."
  training:
    description: "Entraînement ou ajustement d’un modèle."
```

Aucun de ces usages ne doit être présumé inclus dans un autre.

Une autorisation de consultation ne vaut pas autorisation d’entraînement. Une autorisation de résumé ne vaut pas autorisation de simulation. Une autorisation d’analyse stylistique ne vaut pas autorisation de production “dans le style de”.

## Sorties produites

Le contrat doit définir les sorties autorisées.

```yaml
allowed_outputs:
  - private_notes
  - family_tree_update
  - archive_index
  - catalog_entry
  - scholarly_summary
  - public_notice
  - curated_publication
  - exhibition_note
  - rights_report
  - digital_twin_context_block
```

Il doit aussi définir les sorties interdites.

```yaml
prohibited_outputs:
  - false_attribution
  - fabricated_statement
  - misleading_completion
  - unrestricted_publication
  - unlabelled_ai_generated_work
  - simulated_person_without_notice
  - derivative_product_without_source_reference
```

## Révocation

Un contrat KYS doit prévoir la révocation.

La révocation peut porter sur :

- l’accès futur ;
- la conservation locale ;
- les copies ;
- les sorties non publiées ;
- les publications futures ;
- l’usage dans un modèle ;
- l’usage dans un jumeau numérique ;
- les produits déclinés ;
- les droits de citation ;
- les accès des tiers.

Certaines sorties déjà publiées peuvent ne pas être matériellement supprimables. Le contrat doit le dire clairement et prévoir, au minimum, une politique de correction, de signalement ou de retrait raisonnable.

## Contestation

Un contrat KYS doit prévoir un canal de contestation.

La contestation peut concerner :

- une erreur factuelle ;
- une attribution ;
- une filiation ;
- une version ;
- une publication ;
- un usage non autorisé ;
- une sortie générée par IA ;
- une interprétation abusive ;
- une atteinte aux droits d’un tiers ;
- une atteinte à la mémoire d’une personne décédée.

## Audit

Tout usage significatif doit laisser une trace.

Le journal d’audit devrait indiquer :

```yaml
audit_log:
  timestamp: ""
  actor: ""
  profile_used: ""
  contract_id: ""
  corpus_reference: ""
  action: ""
  purpose: ""
  output_reference: ""
  review_status: ""
```

L’objectif n’est pas la surveillance généralisée, mais la responsabilité.

## Contrats posthumes

Un contrat KYS posthume doit être particulièrement strict.

Il doit préciser :

- qui est compétent pour autoriser ;
- qui peut contester ;
- qui détient les droits ;
- qui détient les archives ;
- quelle était la volonté connue de la personne ;
- quelles incertitudes subsistent ;
- quelles simulations sont interdites ;
- quelles publications sont autorisées ;
- quelle structure fiduciaire peut arbitrer.

## Contrats et produits déclinés

Un contrat KYS doit indiquer si les produits déclinés sont autorisés.

```yaml
derived_products_policy:
  allowed: false
  requires_source_reference: true
  requires_review: true
  requires_public_label: true
  requires_rights_review: true
  requires_fiduciary_review: false
```

Un produit décliné ne doit pas effacer la source.

## Contrats et jumeaux numériques

Un contrat KYS peut autoriser certains usages dans un jumeau numérique, mais ceux-ci doivent être explicitement qualifiés.

```yaml
digital_twin_policy:
  allowed: false
  allowed_levels:
    - archive_grounding
    - retrieval_context
    - limited_question_answering
    - representative_agent
  prohibited_levels:
    - unrestricted_simulation
    - impersonation
    - autonomous_legal_action
    - autonomous_political_action
```

Le jumeau numérique ne doit jamais se substituer à la personne sans mandat explicite.

## Formule synthétique

Un contrat KYS transforme un profil KYS en usage autorisé, limité, traçable, révocable, contestable et auditable.

Il protège simultanément :

- la personne ;
- les proches ;
- les héritiers ;
- les ayants droit ;
- les œuvres ;
- le corpus ;
- la structure fiduciaire ;
- les utilisateurs légitimes ;
- la possibilité de transmission ;
- la possibilité de correction ;
- la distinction entre trace, œuvre, personne, Cogentigram et jumeau numérique.
