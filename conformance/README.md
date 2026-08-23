---
title: Conformance PrivAI
author: Jean Hugues Noël Robert
date: '2026-08-23'
document_role: source
document_kind: framework
visibility: public
lifecycle_state: working
update_policy: UP-DEFAULT-REVIEWED
---

# Conformance PrivAI

Ce répertoire réunit des profils de conformance et des épreuves publiques.
Ils ne constituent pas encore une certification institutionnelle.

L’ambition initiale est modeste et vérifiable : publier des assertions
précises, leurs preuves, leurs limites et leur date de validité. Un résultat
ne vaut que pour la version, le scénario et les dépendances indiqués.

Le premier profil est [Migration-Tested v0.1](migration_tested_v0.1.md).
Il s’articule avec [STAKE / GAGE](../assurance/stake_gage.md), qui fournit
l’échelle générale de preuve fondée sur l’épreuve.

Le cadre [Assurance Data Pact](data_pact_assurance.md) distingue la validité
ou la provenance des données, le comportement vérifiable du computing qui les
traite et l’autorité qui rend cet usage admissible. Il prépare des profils KYS
et COP complémentaires, sans les confondre avec une certification
institutionnelle déjà établie.
