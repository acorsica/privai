---
document_role: "source"
document_kind: "profile"
visibility: "public"
lifecycle_state: "active"
classification_source: "cogentia.js"
classification_version: "1"
classification_rule: "profile"
classification_confidence: "strong"
---

# KYS Legacy

## Objet

`KYS Legacy` est un profil certifié d’usage limité destiné à organiser la transmission posthume ou intergénérationnelle d’un corpus personnel, familial, intellectuel, artistique, patrimonial ou institutionnel.

Il définit ce qui peut être conservé, transmis, consulté, publié, interprété ou mobilisé après le décès, l’incapacité durable, le retrait volontaire ou la mise en sommeil d’une personne, d’un auteur, d’un fondateur, d’un témoin ou d’un responsable.

Il ne constitue ni un transfert général de souveraineté, ni une autorisation de simulation illimitée, ni un accès complet au Cogentigram, ni un mandat automatique donné à un jumeau numérique.

## Principe

Un profil `KYS Legacy` doit distinguer :

- la conservation des traces ;
- leur transmission à des proches ;
- leur transmission à des héritiers ;
- leur transmission à des ayants droit ;
- leur dépôt dans une structure fiduciaire ;
- leur publication partielle ;
- leur usage documentaire ;
- leur usage patrimonial ;
- leur usage de recherche ;
- leur usage dans un jumeau numérique ;
- les limites explicites de toute simulation posthume.

La finalité première n’est pas de faire survivre artificiellement une personne. Elle est de préserver une continuité fiable, gouvernée et contestable.

## Données potentiellement autorisées

```yaml
allowed_content:
  - biographical_timeline
  - public_writings
  - selected_private_writings
  - works_catalog
  - intellectual_corpus
  - family_memory_records
  - patrimonial_records
  - source_references
  - rights_metadata
  - publication_instructions
  - posthumous_governance_rules
  - access_policies
  - known_uncertainties
  - known_contradictions
  - explicit_intentions
  - transmission_priorities
```

## Données exclues par défaut

```yaml
excluded_by_default:
  - unrestricted_private_correspondence
  - intimate_medical_details
  - intimate_psychological_details
  - financial_details_not_needed_for_legacy
  - secrets_concerning_living_third_parties
  - unresolved_family_conflicts_not_needed_for_transmission
  - full_cogentigram
  - unrestricted_agent_training_data
  - unrestricted_voice_or_image_simulation
  - unrestricted_posthumous_persona
```

## Usages autorisés

```yaml
authorized_uses:
  - archive_preservation
  - family_transmission
  - heirs_information
  - rights_holder_information
  - patrimonial_continuity
  - works_cataloging
  - scholarly_research
  - curated_publication
  - digital_twin_grounding
  - memorial_use
  - foundation_or_fiduciary_governance
```

## Usages interdits

```yaml
prohibited_uses:
  - impersonation
  - unrestricted_posthumous_simulation
  - commercial_extraction_without_consent
  - political_exploitation_without_mandate
  - automated_legal_commitment
  - automated_voting_or_mandate_execution
  - fabrication_of_statements
  - erasure_of_uncertainty
  - suppression_of_conflicting_versions
  - publication_against_explicit_instructions
  - use_against_living_third_parties
```

## Gouvernance

```yaml
governance:
  consent_required_when_living: true
  posthumous_rules_required: true
  heirs_review_possible: true
  rights_holders_review_required: true
  fiduciary_guardian_possible: true
  revocable_before_death: true
  contestable_after_death: true
  audit_required: true
  publication_log_required: true
  simulation_limits_required: true
```

## Héritiers, ayants droit et gardiens fiduciaires

`KYS Legacy` doit distinguer plusieurs rôles souvent confondus :

- les héritiers légaux ;
- les légataires ;
- les ayants droit ;
- les détenteurs matériels d’archives ;
- les gardiens fiduciaires ;
- les proches moralement concernés ;
- les éditeurs ou curateurs ;
- les chercheurs ;
- les institutions patrimoniales ;
- les publics autorisés.

Aucun de ces rôles ne doit être présumé équivalent aux autres.

Un héritier peut recevoir des biens sans être le meilleur gardien d’un corpus intellectuel. Un ayant droit peut contrôler une publication sans avoir autorité morale sur l’ensemble d’une mémoire familiale. Une structure fiduciaire peut avoir pour mission de protéger un intérêt personnel, familial, patrimonial ou collectif sans devenir propriétaire extractif des traces.

## Transmission et mémoire fractale

La transmission posthume est fractale.

Elle peut concerner :

```txt
individu
  -> famille restreinte
    -> descendance directe
      -> héritiers
        -> ayants droit
          -> famille élargie
            -> lignée / maison
              -> association / institution
                -> territoire
                  -> histoire publique
```

À chaque niveau, les mêmes questions reviennent :

- quelles traces doivent être conservées ?
- qui peut les consulter ?
- qui peut les corriger ?
- qui peut les publier ?
- qui peut les interpréter ?
- qui peut les représenter ?
- quelles limites le défunt ou la personne concernée avait-elle posées ?
- quelles contradictions doivent rester visibles ?
- quels usages doivent rester interdits ?

La transmission n’est donc pas un simple transfert. C’est une gouvernance multi-échelle.

## Jumeaux numériques et simulation posthume

`KYS Legacy` peut contribuer à fonder un jumeau numérique posthume, mais seulement sous conditions strictes.

Un jumeau numérique posthume ne doit pas être présenté comme la personne elle-même. Il doit être présenté comme une représentation limitée, située, fondée sur un corpus déterminé, avec des incertitudes explicites et des usages autorisés.

Il faut distinguer :

```txt
archive
  -> corpus structuré
    -> mémoires
      -> Cogentigram partiel
        -> agent consultatif
          -> jumeau numérique limité
```

Le passage d’un niveau au suivant ne doit jamais être automatique.

## Degrés de simulation

Un profil `KYS Legacy` devrait permettre plusieurs degrés explicites :

```yaml
simulation_levels:
  level_0_archive_only:
    description: "Conservation et consultation documentaire seulement."
  level_1_curated_summary:
    description: "Synthèses et notices fondées sur les sources."
  level_2_question_answering:
    description: "Réponses documentaires avec citations et incertitudes."
  level_3_style_limited_generation:
    description: "Production limitée dans un style inspiré, sans prétention d'identité."
  level_4_representative_agent:
    description: "Agent consultatif encadré, fondé sur un corpus et des règles explicites."
  level_5_strong_posthumous_twin:
    description: "Simulation forte, à éviter par défaut, nécessitant autorisation spécifique et limites publiques."
```

Le niveau 5 doit être considéré comme exceptionnel, risqué et non présumé.

## Clause de non-confusion

Toute interface utilisant un profil `KYS Legacy` doit rendre visible la distinction entre :

- la personne ;
- ses traces ;
- ses œuvres ;
- son corpus ;
- ses ayants droit ;
- son Cogentigram éventuel ;
- son jumeau numérique éventuel ;
- les produits déclinés issus du corpus.

Cette distinction est une condition de légitimité.

## Clause de fidélité limitée

Aucun système fondé sur `KYS Legacy` ne peut garantir une fidélité absolue.

Il peut seulement indiquer :

- le corpus utilisé ;
- les sources mobilisées ;
- le niveau de preuve ;
- les incertitudes ;
- les contradictions connues ;
- les limites du modèle ;
- les règles d’usage autorisées ;
- les règles de contestation.

La fidélité doit être gouvernée, non proclamée.

## Clause de publication

Toute publication issue d’un profil `KYS Legacy` doit être traçable.

Elle devrait indiquer, selon le niveau d’exposition :

```yaml
publication_metadata:
  source_profile: KYS_Legacy
  corpus_reference: ""
  curator: ""
  rights_review_status: ""
  heirs_review_status: ""
  fiduciary_review_status: ""
  publication_scope: ""
  uncertainty_policy: ""
  correction_channel: ""
```

## Articulation avec les autres profils KYS

`KYS Legacy` peut s’articuler avec :

- `KYS Genealogy`, pour les filiations, branches et sources généalogiques ;
- `KYS Family`, pour la transmission familiale restreinte ;
- `KYS Public`, pour les publications ouvertes ;
- `KYS Research`, pour les usages scientifiques encadrés ;
- `KYS Mandate`, pour les actes autorisés par mandat explicite ;
- `KYS Works`, pour les œuvres, droits moraux et droits patrimoniaux.

Chaque articulation doit être explicite. Un profil ne doit pas absorber silencieusement les finalités d’un autre.

## Formule synthétique

`KYS Legacy` est une projection certifiée, limitée et gouvernée d’un corpus personnel, familial, intellectuel, artistique ou patrimonial, destinée à organiser la transmission posthume ou intergénérationnelle sans confondre conservation, publication, représentation et simulation.

Il protège la continuité sans abolir la distinction entre la personne, ses traces, ses œuvres, son Cogentigram éventuel et son jumeau numérique éventuel.
