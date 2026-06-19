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

# KYS Works

## Objet

`KYS Works` est un profil certifié d’usage limité destiné à organiser la conservation, le catalogage, la publication, l’adaptation, la citation, l’exposition, la licence et la transmission d’œuvres liées à une personne, une famille, une institution, une fondation, une association ou un corpus.

Il concerne notamment :

- textes ;
- carnets ;
- lettres ;
- essais ;
- articles ;
- dépôts Git ;
- logiciels ;
- schémas ;
- images ;
- photographies ;
- peintures ;
- dessins ;
- vidéos ;
- enregistrements audio ;
- œuvres mixtes ;
- archives préparatoires ;
- produits déclinés ;
- œuvres posthumes ou inachevées.

Il ne constitue ni une autorisation générale d’exploitation, ni une cession de droits, ni une autorisation d’entraînement illimité, ni une permission de simulation stylistique sans limites explicites.

## Principe

Un profil `KYS Works` doit distinguer :

- conservation ;
- inventaire ;
- catalogage ;
- authentification ;
- attribution ;
- citation ;
- reproduction ;
- publication ;
- exposition ;
- adaptation ;
- traduction ;
- édition critique ;
- licence ;
- exploitation commerciale ;
- entraînement ou évaluation d’un modèle ;
- génération dans un style associé à l’auteur ;
- usage posthume ;
- usage fiduciaire.

La finalité première est de permettre la circulation contrôlée des œuvres sans dissoudre les droits, les intentions, les incertitudes, les contextes et la distinction entre source et produit décliné.

## Source et produits déclinés

`KYS Works` doit préserver la distinction entre :

```txt
corpus source
  -> œuvre identifiée
    -> version
      -> édition
        -> publication
          -> adaptation
            -> produit décliné
```

Une œuvre peut avoir plusieurs versions. Une publication peut ne reprendre qu’une version. Une adaptation peut être légitime sans être une source. Un produit décliné peut être utile sans être souverain.

Le corpus source doit rester la référence principale lorsque cela est possible.

## Données potentiellement autorisées

```yaml
allowed_content:
  - work_title
  - work_type
  - author
  - coauthors
  - creation_date
  - publication_date
  - version_history
  - source_location
  - repository_location
  - archive_reference
  - rights_metadata
  - license_metadata
  - attribution_rules
  - citation_rules
  - publication_status
  - adaptation_status
  - provenance_notes
  - authenticity_level
  - uncertainty_level
  - related_works
  - derived_products
  - curatorial_notes
```

## Données exclues par défaut

```yaml
excluded_by_default:
  - unrestricted_private_drafts
  - private_correspondence_not_needed_for_work_context
  - sensitive_third_party_information
  - financial_contracts_not_needed_for_rights_review
  - unpublished_intimate_material
  - full_cogentigram
  - unrestricted_training_data
  - unrestricted_style_simulation
  - unrestricted_voice_or_image_generation
  - publication_against_explicit_author_instruction
```

## Usages autorisés

```yaml
authorized_uses:
  - preservation
  - inventory
  - cataloging
  - attribution_review
  - authenticity_review
  - source_comparison
  - scholarly_citation
  - curated_publication
  - public_exhibition
  - family_transmission
  - rights_holder_review
  - fiduciary_governance
  - limited_adaptation
  - edition_preparation
  - derivative_product_tracking
```

## Usages interdits

```yaml
prohibited_uses:
  - plagiarism
  - false_attribution
  - unauthorized_publication
  - unauthorized_commercial_exploitation
  - unauthorized_model_training
  - unrestricted_style_imitation
  - fabrication_of_missing_works
  - erasure_of_versions
  - suppression_of_context
  - removal_of_attribution
  - publication_against_rights_holders
  - publication_against_explicit_instructions
  - misleading_posthumous_completion
```

## Gouvernance

```yaml
governance:
  author_consent_required_when_living: true
  rights_holder_review_required: true
  moral_rights_review_required: true
  patrimonial_rights_review_required: true
  provenance_review_required: true
  version_tracking_required: true
  publication_log_required: true
  adaptation_log_required: true
  training_use_requires_specific_clause: true
  posthumous_rules_required: true
  fiduciary_guardian_possible: true
  contestable: true
  auditable: true
```

## Droits moraux et droits patrimoniaux

`KYS Works` doit distinguer les droits moraux et les droits patrimoniaux.

Les droits patrimoniaux concernent notamment :

- reproduction ;
- représentation ;
- adaptation ;
- diffusion ;
- licence ;
- exploitation commerciale ;
- rémunération éventuelle ;
- transmission aux ayants droit.

Les droits moraux concernent notamment :

- attribution ;
- respect de l’œuvre ;
- divulgation ;
- retrait ou repentir selon les cadres juridiques applicables ;
- protection contre les altérations trompeuses ;
- protection contre les attributions abusives.

Un usage peut être techniquement possible et économiquement avantageux tout en restant illégitime s’il trahit l’œuvre, son auteur ou ses conditions de transmission.

## Œuvres, IA et entraînement

L’usage d’œuvres pour entraîner, ajuster, évaluer ou conditionner un modèle doit être traité comme une finalité spécifique.

Il ne doit pas être présumé inclus dans une autorisation de consultation, de conservation, de citation ou de publication.

```yaml
ai_training_policy:
  default: prohibited_without_specific_authorization
  requires:
    - purpose
    - model_type
    - dataset_scope
    - retention_policy
    - output_policy
    - attribution_policy
    - opt_out_or_revocation_policy
    - audit_log
```

## Simulation stylistique

La simulation stylistique doit être distinguée de l’étude d’une œuvre.

Étudier un style, décrire des motifs, comparer des versions ou produire une analyse critique n’autorise pas automatiquement à générer de nouvelles œuvres “dans le style de” l’auteur.

```yaml
style_simulation:
  default: prohibited_without_specific_authorization
  allowed_levels:
    level_0_analysis_only:
      description: "Analyse descriptive du style, sans génération."
    level_1_limited_exercises:
      description: "Exercices internes non publiés."
    level_2_marked_homage:
      description: "Production explicitement signalée comme hommage ou inspiration."
    level_3_authorized_derivative:
      description: "Produit décliné autorisé, avec mention de statut."
    level_4_posthumous_completion:
      description: "Complétion posthume exceptionnelle, hautement encadrée."
```

Le niveau 4 doit rester exceptionnel.

## Œuvres inachevées

Une œuvre inachevée ne doit pas être présentée comme une œuvre achevée par l’auteur.

Elle peut être :

- conservée ;
- inventoriée ;
- publiée comme fragment ;
- éditée de manière critique ;
- contextualisée ;
- rapprochée d’autres œuvres ;
- prolongée sous forme de produit décliné clairement identifié.

La complétion ne doit jamais effacer l’inachèvement.

## Produits déclinés

`KYS Works` doit permettre de suivre les produits déclinés sans les confondre avec la source.

```yaml
derived_product:
  source_work: ""
  source_version: ""
  derivative_type: ""
  curator: ""
  adapter: ""
  publication_scope: ""
  status:
    - draft
    - reviewed
    - authorized
    - published
  relation_to_source:
    - excerpt
    - summary
    - translation
    - adaptation
    - commentary
    - educational_version
    - public_post
    - exhibition_note
    - model_prompt
    - digital_twin_component
```

Un produit décliné doit indiquer sa relation à la source.

## Œuvres et jumeaux numériques

Un profil `KYS Works` peut alimenter un jumeau numérique, mais seulement comme couche documentée et limitée.

Il faut distinguer :

```txt
œuvres
  -> corpus d’œuvres
    -> style observable
      -> préférences éditoriales
        -> Cogentigram éventuel
          -> jumeau numérique limité
```

Les œuvres ne suffisent pas à elles seules à autoriser la simulation d’une personne. Elles peuvent éclairer un style, une pensée ou une trajectoire, mais elles ne remplacent ni le consentement, ni les droits, ni les limites de représentation.

## Clause de non-confusion

Toute interface utilisant `KYS Works` doit rendre visible la distinction entre :

- œuvre source ;
- version ;
- brouillon ;
- fragment ;
- édition ;
- adaptation ;
- produit décliné ;
- commentaire ;
- simulation ;
- complétion posthume ;
- sortie générée par IA.

Cette distinction est une condition de fidélité.

## Clause de provenance

Toute œuvre ou produit décliné doit pouvoir être relié à une provenance.

```yaml
provenance:
  source_location: ""
  repository: ""
  commit: ""
  archive_box: ""
  physical_owner: ""
  digital_owner: ""
  rights_holder: ""
  curator: ""
  verification_status: ""
  uncertainty_notes: ""
```

## Clause de publication

Toute publication issue d’un profil `KYS Works` devrait indiquer, selon le niveau d’exposition :

```yaml
publication_metadata:
  source_profile: KYS_Works
  work_reference: ""
  version_reference: ""
  corpus_reference: ""
  rights_review_status: ""
  moral_rights_review_status: ""
  patrimonial_rights_review_status: ""
  curator: ""
  publication_scope: ""
  license: ""
  attribution: ""
  correction_channel: ""
```

## Articulation avec les autres profils KYS

`KYS Works` peut s’articuler avec :

- `KYS Legacy`, pour la transmission posthume ;
- `KYS Genealogy`, lorsque les œuvres éclairent une branche, une maison ou une lignée ;
- `KYS Family`, pour les œuvres familiales ou privées ;
- `KYS Public`, pour les œuvres publiées ;
- `KYS Research`, pour les études scientifiques ou critiques ;
- `KYS Mandate`, lorsqu’un mandataire est autorisé à publier, exposer, licencier ou défendre une œuvre.

Chaque articulation doit être explicite.

## Formule synthétique

`KYS Works` est une projection certifiée, limitée et gouvernée d’un corpus d’œuvres. Il permet de conserver, cataloguer, publier, adapter ou transmettre des œuvres sans confondre source, version, publication, produit décliné, simulation stylistique et jumeau numérique.

Il protège la circulation des œuvres contre deux risques symétriques : l’enfermement stérile et la capture extractive.
