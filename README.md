---
title: PrivAI
author: unknown
date: '2026-08-23'
document_role: source
document_kind: documentation
visibility: public
lifecycle_state: working
update_policy: UP-DEFAULT-REVIEWED
provenance:
  origin_type: repository
  origin_repository: acorsica/privai
  origin_ref: 54fd9c5
  origin_date: '2026-06-03'
  derived_from: []
review:
  status: unreviewed
  reviewed_by: []
---

# PrivAI

**PrivAI** est une initiative en développement au sein de l’**Institut Mariani**,
émanation recherche et développement de l’association **C.O.R.S.I.C.A.**

Elle préfigure les conditions d’une **agence numérique portable et imputable** :
une personne ou un collectif doit pouvoir conserver la maîtrise de ses traces,
de ses représentations, de ses mandats et des actes accomplis en son nom, y
compris lorsqu’il change de modèle, d’opérateur ou d’infrastructure.

> Les données ne suffisent pas : il faut aussi gouverner leur usage et les
> actes qu’elles rendent possibles.

## Le problème

Les interactions avec des agents, assistants et systèmes d’IA produisent des
traces qui peuvent devenir une matière première de jumeau numérique. Elles
révèlent parfois préférences, modes de raisonnement, seuils d’acceptabilité,
corrections, décisions et signatures structurelles.

La question n’est donc pas seulement « qui héberge ces données ? », mais :

> **Qui peut agir, au nom de qui, dans quelles limites, et avec quelles
> preuves ?**

Un changement de fournisseur ne devrait ni détruire la mémoire source, ni
effacer un mandat, ni rendre un historique d’actes illisible ou impossible à
reprendre.

## Ce que PrivAI préfigure

| Instrument | Question traitée | État |
|---|---|---|
| [Charte PrivAI](charte.md) | Quels principes protègent les traces et représentations personnelles ? | socle public |
| [Profils KYS](profiles/README.md) | Quelle projection d’un corpus peut être exposée, pour quelle finalité ? | modèles de profils |
| [Contrats KYS](contracts/README.md) | Qui peut utiliser cette projection, sous quelles conditions ? | modèle contractuel |
| [STAKE / GAGE](assurance/stake_gage.md) | Quelle autonomie de capacité a réellement été exercée ? | cadre de preuve |
| [Assurance Data Pact](conformance/data_pact_assurance.md) | Que peut-on vérifier sur une donnée, le computing qui la traite et l’autorité applicable ? | cadre de conformance ouvert |
| [Migration-Tested v0.1](conformance/migration_tested_v0.1.md) | Un agent peut-il migrer sans perdre ses invariants de gouvernance ? | préfiguration ouverte |

## Solid et PrivAI

Solid porte principalement sur la souveraineté des données : où elles résident
et qui y accède. PrivAI porte sur leur **usage**, sur la délégation de capacité
à agir et sur l’imputabilité des conséquences. Les deux approches sont
complémentaires ; PrivAI ne dépend d’aucun stockage ou protocole particulier.

## Relation avec Cogentia

PrivAI maintient le référentiel, les profils et les épreuves publiques.
**Cogentia** est appelée à en être une première implémentation open source de
référence ; elle ne constitue pas la norme et ne s’auto-certifie pas.

Le premier objectif de démonstration est un export puis import d’une instance
de Twin entre deux environnements de modèles, avec conservation vérifiable du
principal, des mandats, de la mémoire source, des traces et de la capacité de
reprise. Voir [Migration-Tested v0.1](conformance/migration_tested_v0.1.md).

## Soutenir une preuve, non une capture

Une offre de sponsoring est en préparation autour de ce premier test public.
Les soutiens peuvent financer une épreuve et des adaptateurs ouverts, mais ne
reçoivent ni exclusivité, ni propriété sur le noyau, ni droit de modifier les
conclusions. Voir le [cadre des partenariats fondateurs](sponsorship/README.md).

## Dépôts et cadres liés

- [Cogentia](https://github.com/JeanHuguesRobert/cogentia) : implémentation et
  expérimentations de jumeaux, continuations et actes tracés ;
- [Institut Mariani](https://github.com/acorsica/institut-mariani) : cadre
  institutionnel actuel de l’initiative.

## Séparation

PrivAI n’est pas un parti, une campagne, un outil électoral, une activité commerciale exploitée par C.O.R.S.I.C.A., ni un dispositif de capture de données.

Les liens de PrivAI avec d’autres dépôts du corpus sont documentaires, doctrinaux ou techniques.

Ils ne valent ni fusion institutionnelle, ni transfert de données, ni portage juridique, ni financement, ni endorsement politique.

## Langue de référence

Le français est la langue de référence de ce dépôt tant que PrivAI est développé dans le périmètre de C.O.R.S.I.C.A. et de l’Institut Mariani.

Des produits déclinés peuvent être traduits ou adaptés dans d’autres langues.
