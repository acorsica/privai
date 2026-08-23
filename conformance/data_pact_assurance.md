---
title: Assurance Data Pact — donnée, computing et autorité
author: Jean Hugues Noël Robert
date: '2026-08-23'
language: fr
document_role: source
document_kind: framework
visibility: public
lifecycle_state: working
update_policy: UP-DEFAULT-REVIEWED
review:
  status: unreviewed
  reviewed_by: []
---

# Assurance Data Pact — donnée, computing et autorité

## Statut

Cadre de recherche et de préfiguration. Il ne délivre pas encore de
certification institutionnelle et ne remplace ni le droit applicable, ni une
vérification humaine ou sectorielle lorsque celle-ci est requise.

## Objet

Un Data Pact associe à une donnée ou à un Data Pack des usages permis,
interdits et des preuves attendues. Son évaluation ne peut pas se réduire à
une seule question de confiance. Elle sépare trois assurances liées, mais non
interchangeables.

```text
assurance de la donnée
  + assurance du computing
  + assurance d’autorité
  = usage vérifiable, dans les limites déclarées
```

## Assurance de la donnée

Elle répond à la question : **que peut-on affirmer sur cette donnée ?**

Elle peut couvrir, selon le scénario :

- la provenance et l’émetteur de l’assertion ;
- l’intégrité du paquet ou des références ;
- les éléments de preuve et leur niveau de vérification ;
- la date de production, de contrôle et de fraîcheur ;
- le périmètre de l’assertion et les incertitudes connues.

Une assertion source, une donnée dérivée, une estimation et une donnée vérifiée
par un tiers ne doivent pas être présentées au même niveau.

## Assurance du computing

Elle répond à la question : **que peut-on affirmer sur le traitement qui a
produit ou utilisé cette donnée ?**

Une épreuve ou conformance COP peut attester, pour une version, un profil et
un scénario déterminés, que la capacité a notamment :

- reçu et évalué un mandat ou un Data Pact identifié ;
- appliqué les limites déclarées ;
- identifié ses entrées, sorties, handler et version pertinents ;
- produit un reçu d’acte et des preuves proportionnées ;
- permis la suspension, la reprise, l’audit ou la contestation prévus.

Cette assurance établit la qualité observable du processus. Elle ne transforme
pas automatiquement les données d’entrée en faits vrais, complets ou actuels,
et ne prouve pas l’absence absolue d’actes effectués hors du système observé.

## Assurance d’autorité

Elle répond à la question : **qui avait le droit de produire, d’attester, de
transmettre ou d’utiliser cette donnée pour cet acte ?**

Elle peut relever d’un consentement, d’un mandat, d’un contrat KYS, d’une
compétence institutionnelle, d’un rôle fiduciaire ou d’une règle de droit. Le
Data Pact doit identifier l’autorité invoquée, son périmètre, sa durée et les
conditions de révocation ou de contestation.

## Chaîne de preuves

```text
source ou émetteur
  -> assertion avec provenance et niveau de confiance
  -> Data Pack soumis à un Data Pact
  -> computing évalué selon un profil COP
  -> reçu d’acte proportionné
  -> sortie dérivée avec limites et références amont
```

Chaque maillon doit rester vérifiable séparément. Une conformance COP du
producteur renforce la confiance dans le processus de dérivation ; elle ne
remplace pas la preuve de la source ni l’autorité d’usage.

## Traçabilité proportionnée

La preuve requise doit être le strict minimum nécessaire à la vérification.
Selon le cas, un reçu, une attestation ciblée, une empreinte, un manifest ou
une preuve sélective doit suffire à la place d’un accès aux données brutes, à
l’historique complet ou au raisonnement intime.

## Déclarations de conformance envisagées

Les déclarations futures devront toujours être limitées par version, scénario,
date, dépendances et niveau d’évaluation. Elles pourraient distinguer :

| Déclaration | Ce qu’elle qualifie | Ce qu’elle ne démontre pas seule |
|---|---|---|
| KYS data assurance | périmètre, provenance, intégrité et incertitude d’un profil | la vérité absolue de toutes les assertions |
| COP Data-Pact conformance | comportement traçable d’une capacité vis-à-vis d’un pacte | la licéité générale ni l’absence absolue d’actes hors trace |
| authority assurance | mandat, consentement ou titre invoqué | la qualité technique du computing |

Les termes « certification » et « accréditation » restent réservés à une
gouvernance ultérieure incluant méthode publique, évaluateurs identifiés,
durée de validité, contestation et révocation.
