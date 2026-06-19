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

# KYS Genealogy

## Objet

`KYS Genealogy` est un profil certifié d’usage limité destiné à la recherche généalogique, à la correction de filiations, à la reconnexion de branches familiales, à l’identification d’archives et à la transmission patrimoniale.

Il constitue une projection partielle d’un corpus personnel, familial ou patrimonial. Il ne constitue ni un accès général à la personne, ni un Cogentigram complet, ni un jumeau numérique, ni une autorisation de simulation.

## Principe

Un profil `KYS Genealogy` doit exposer seulement ce qui est nécessaire à une finalité généalogique explicite : noms, dates, lieux, relations familiales, sources, degrés d’incertitude, branches, alliances, conflits de version strictement pertinents et règles d’accès.

Il doit exclure par défaut les éléments intimes, médicaux, psychologiques, financiers, politiques ou relationnels qui ne sont pas nécessaires à la finalité généalogique.

## Données potentiellement autorisées

```yaml
allowed_content:
  - names
  - dates_of_birth
  - dates_of_death
  - places
  - family_relations
  - branches
  - alliances
  - public_archival_sources
  - family_archival_references
  - uncertainty_levels
  - conflicting_versions
  - source_quality
  - publication_status
```

## Données exclues par défaut

```yaml
excluded_by_default:
  - intimate_psychological_profile
  - private_correspondence_content
  - medical_details
  - financial_details
  - political_preferences_of_living_persons
  - sensitive_family_conflicts
  - full_cogentigram
  - unrestricted_digital_twin_access
  - simulation_of_deceased_person_without_specific_authorization
```

## Usages autorisés

```yaml
authorized_uses:
  - genealogical_research
  - family_tree_correction
  - archival_identification
  - patrimonial_transmission
  - family_branch_reconnection
  - source_quality_review
  - conflicting_version_documentation
```

## Usages interdits

```yaml
prohibited_uses:
  - commercial_extraction_without_consent
  - psychometric_inference
  - political_targeting
  - insurance_scoring
  - employment_screening
  - automated_identity_claims
  - impersonation
  - unrestricted_publication
  - unrestricted_digital_twin_training
```

## Gouvernance

```yaml
governance:
  consent_required: true
  revocable: true
  contestable: true
  audit_required: true
  posthumous_rules_required: true
  fiduciary_guardian_possible: true
```

## Généalogie et mémoire fractale

La généalogie n’est pas seulement une liste de filiations. Elle constitue une couche particulière de la mémoire fractale : individu, famille restreinte, descendance directe, héritiers, ayants droit, famille élargie, lignée, maison, territoire.

À chaque niveau, les mêmes questions reviennent sous une forme différente : quelles traces existent, qui peut parler, qui peut corriger, qui peut hériter, qui peut publier, quelles versions sont contradictoires, quelles branches ont été perdues puis retrouvées.

`KYS Genealogy` doit donc rester strictement finalisé : il aide à établir ou corriger des liens, non à ouvrir l’ensemble du corpus personnel ou familial.

## Généalogie et jumeaux numériques

Un profil `KYS Genealogy` peut alimenter un jumeau numérique familial, patrimonial ou territorial, mais seulement par des données limitées et qualifiées.

Il ne doit pas autoriser la simulation générale d’une personne vivante ou décédée. Il ne doit pas permettre de faire dire à une personne ce qu’elle n’a pas dit, ni d’inférer des positions intimes à partir de simples liens généalogiques.

## Formule synthétique

`KYS Genealogy` est une projection certifiée, limitée et révocable d’un corpus personnel ou familial, autorisant un usage généalogique sans ouvrir l’accès au Cogentigram complet ni au jumeau numérique. Il permet de relier des personnes, branches, lieux, dates et sources, tout en protégeant les dimensions intimes, cognitives, sensibles ou non pertinentes.
