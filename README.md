# ・Devoir BTS SIO — SISR 2ᵉ année.

**Sujet :** Travaux à partir des documents CEJMA (DCP — Identité numérique — Preuve électronique — Sécurité équipements — Obligations légales)  

J’ai traité tous les exercices demandés dans les 6 documents fournis. Les corrections et compléments juridiques ont été ajoutés pour renforcer la qualité du rendu (références RGPD, CNIL, Code pénal).


**・Documents fournis :**

* `Cours1-CEJMA-DCP.pdf`. 
* `Cours2-CEJMA-DCP.pdf`. 
* `Cours3-CEJMA-IdentitéNumérique.pdf`. 
* `Cours4-CEJMA-PreuveElectronique.pdf`. 
* `Cours5-CEJMA-SécuriserlesEquipements.pdf`. 
* `Cours6-CEJMA-ObligationsLegalesFaillesSecurite.pdf`. 

---

# ・Table des matières (Cliquez pour être redirigé.)

1. [Cours 1-Données à caractère personnel (DCP)](#cours-1)  
2. [Cours 2-Charte de confidentialité & base légale (CentreCall)](#cours-2)  
3. [Cours 3-Identité numérique (MQBanque)](#cours-3)  
4. [Cours 4-Preuve électronique et courriel frauduleux (MQBanque)](#cours-4)  
5. [Cours 5-Sécuriser les équipements — Audit MSAP (Marut)](#cours-5)  
6. [Cours 6-Habilitations, failles et segmentation SI (MSAP)](#cours-6)  
7. [Annexes utiles : modèles, matrices et schémas textuels](#annexes)  
8. [Références web citées (législation / autorités)](#references)

---

<a id="cours-1"></a>
# 1) Cours 1 — Données à caractère personnel (DCP)

*(Source : Cours1-CEJMA-DCP.pdf).* 

## Q1 — Données recueillies lors d’une étude de marché : identification et justification

**Données identifiées :**

* Identifiants directs : **nom, prénom, adresse postale, téléphone, courriel**.
* **Enregistrements audio** (conversation téléphonique) — voix.
* Données socio-démographiques et opinions : âge, profession, revenus déclarés, réponses d’enquête, préférences.

**Justification synthétique :**
Toute information permettant d’identifier une personne, directement ou indirectement, est une donnée à caractère personnel (principe du RGPD : finalité, minimisation, etc.). L’enregistrement vocal est considéré comme DCP car il peut permettre l’identification (par voix ou par contexte). 

---

## Q2 — Analyse de conformité de la situation décrite (accord oral + précision de la finalité)

**Constat :** l’enregistrement est effectué **après accord oral** et la finalité est précisée par l'opérateur. 

**Éléments de conformité / non-conformité (synthèse)**

* **Base légale (Art. 6 RGPD)** : le traitement doit reposer sur une base légale (consentement, exécution du contrat, intérêt légitime...). L’accord oral peut constituer un consentement **si** prouvé et éclairé. ([RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng))
* **Principe de transparence (Art. 5 et information)** : la personne doit être informée de façon complète (responsable, finalités, durée, droits, contact DPO). Le fait de préciser seulement la finalité est insuffisant selon la CNIL. ([RGPD (texte indexé)](https://gdpr-info.eu/))
* **Sécurité (Art. 32 RGPD)** : stockage chiffré, contrôle d’accès et journalisation nécessaires. ([RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng))
* **Notification en cas de fuite (Art. 33 RGPD)** : si les enregistrements exposent des données et constituent une violation à risque, notification CNIL en 72 h. ([RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng))

**Conclusion et actions immédiates recommandées**

1. Insérer au début de chaque appel la phrase de consentement prononcée (horodatée) et la conserver comme preuve.  
2. Fournir une information complète (responsable, motifs, durée, droits). Voir recommandations CNIL pour l’enregistrement des appels. ([CNIL — Écoute et enregistrement des appels](https://www.cnil.fr/fr/lecoute-et-lenregistrement-des-appels-sur-le-lieu-de-travail))  
3. Définir et documenter des durées de conservation (ex. qualité : ≤ 6 mois ; preuve contractuelle : durée justifiée). ([Article explicatif / Axialys](https://blog.axialys.com/enregistrement-des-appels-rgpd-bonnes-pratiques-2024/))  
4. Mettre en place chiffrement et contrôle d’accès, et journaliser les accès aux enregistrements. 

---

<a id="cours-2"></a>
# 2) Cours 2 — Charte de confidentialité (CentreCall)

*(Source : Cours2-CEJMA-DCP.pdf).* 

## Q1 — Vérification de conformité : checklist clé

La charte doit impérativement contenir / préciser :

* Responsable du traitement et coordonnées DPO ;
* Finalités claires et limitées ;
* Base légale (Art. 6 RGPD) pour chaque finalité ; ([RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng))
* Destinataires / sous-traitants ; transferts hors UE et garanties ;
* Durées de conservation explicites ;
* Modalités d’exercice des droits (accès, rectification, suppression, opposition, portabilité) ;
* Mesures de sécurité (chiffrement, accès restreint) ;
* Procédure de notification en cas de violation (Art. 33 RGPD). ([CNIL — notifier une violation](https://www.cnil.fr/fr/services-en-ligne/notifier-une-violation-de-donnees-personnelles))

**Évaluation** : absence d’un seul élément essentiel (base légale, durée, droits) = non-conformité partielle ; corriger dans la charte et dans le registre des traitements.

---

## Q2 — Base légale de la conservation (tableau + justification)

| Catégorie de données          | Finalité                            | Base légale                                                            | Justification                                                                                                                                                           |
| ----------------------------- | ----------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Coordonnées (nom, tel, email) | Gestion relation client             | **Exécution du contrat** (si client) ou **Consentement** (prospection) | Exécution du contrat justifie le traitement pour la relation commerciale ; prospection = consentement. ([RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng))                                                      |
| Enregistrements d’appels      | Contrôle qualité, formation, preuve | **Consentement** ou **Intérêt légitime** (évaluation cas par cas)      | L’intérêt légitime peut être invoqué pour la qualité sous condition de bilan d’intérêt ; le consentement est souvent la solution la plus sûre. ([Axialys](https://blog.axialys.com/enregistrement-des-appels-rgpd-bonnes-pratiques-2024/)) |
| Données d’étude (opinions)    | Étude de marché                     | **Consentement**                                                       | Opinions et profils pour étude → consentement spécifique, libre et documenté.                                                                                           |
| Données bancaires/fiscales    | Facturation, obligations légales    | **Exécution du contrat** / **Obligation légale**                       | Obligations comptables/fiscales justifient conservation selon durée légale.                                                                                             |

**Action requise** : inscrire chaque catégorie et sa base légale dans le registre des traitements et dans la charte.

---

<a id="cours-3"></a>
# 3) Cours 3 — Identité numérique (MQBanque)

*(Source : Cours3-CEJMA-IdentitéNumérique.pdf).* 

## Q1 — Éléments repérables sur un site défiguré (impact sur identité numérique)

* Logo, charte graphique ; mentions légales (SIRET, contacts) ; certificats SSL ; espace client (formulaires) ; liens vers réseaux sociaux ; documents téléchargeables. Ces éléments constituent l’identité numérique et, s’ils sont altérés, provoquent perte de confiance. 

## Q2 — Risques économiques & juridiques (synthèse)

**Économiques :** perte de clients, coûts de remédiation, fraude financière, atteinte à l’e-réputation.  
**Juridiques :** obligation de notification CNIL si DCP exposées (Art. 33 RGPD), responsabilité civile pour préjudices subis, risques contractuels et pénaux selon la gravité. ([RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng))

**Mesures d’urgence recommandées :**

1. Mettre site en maintenance et préserver preuves (logs, captures).  
2. Lancer forensic, corriger vulnérabilités, renouveler accès et certificats SSL.  
3. Évaluer obligation de notification CNIL et plan communication clients. ([CNIL — Violations de données : règles à suivre](https://www.cnil.fr/fr/violations-de-donnees-personnelles-les-regles-suivre))

---

<a id="cours-4"></a>
# 4) Cours 4 — Preuve électronique, courriel frauduleux et sanctions

*(Source : Cours4-CEJMA-PreuveElectronique.pdf).* 

## Q1 — Signes permettant de détecter un courriel frauduleux

* Expéditeur usurpé / typosquatting ; SPF/DKIM/DMARC échoués ; liens vers domaines suspects ; pièces jointes exécutables ; langage pressant/urgence ; absence de personnalisation ; incohérences d’IP. (Procédure : vérifier en-têtes, valider signature électronique, contacter via canal officiel.) 

## Q2 — Délits et peines encourues (synthèse juridique française)

**Usurpation d’identité** : Article **226-4-1** du Code pénal — réprime l’usurpation d’identité ou l’usage de données d’identification pour troubler la tranquillité ou porter atteinte à l’honneur (peine : 1 an d’emprisonnement et 15 000 € d’amende pour l’infraction prévue par l’article). ([Légifrance — Art. 226-4-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000042193593))  

**Accès frauduleux à un système** : Article **323-1** du Code pénal — accès frauduleux à un système automatisé d’information (peines encadrées, amende et peine d’emprisonnement possibles). ([Légifrance — Art. 323-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000047052655))  

**Escroquerie** : Article **313-1** du Code pénal — tromperie visant à obtenir un bien ou service ; peines variables selon le préjudice. ([Légifrance — Art. 313-1](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006418192))

> **Remarque** : la qualification précise dépendra des éléments (intention, préjudice, moyens). Pour un rendu scolaire, citer ces articles montre la connaissance du cadre pénal.

## Q3 — Démonstration que la solution proposée (Document 3) respecte la législation probatoire

**Exigences probatoires pour contrats électroniques** :

* **Authenticité / identification** : signature électronique qualifiée ou dispositif d’identification fiable. (eIDAS : la signature qualifiée a l’équivalence d’une signature manuscrite). ([eIDAS — texte officiel](https://eur-lex.europa.eu/eli/reg/2014/910/oj/eng))  
* **Intégrité** : empreinte (hash) et signature garantissant que le document n’a pas été modifié.  
* **Horodatage** : preuve temporelle (horodatage tiers) pour situer la signature.  
* **Conservation** : journalisation et stockage sécurisé (chiffrement, accès restreint).

**Conclusion** : si la solution Document 3 inclut signature qualifiée + horodatage + journal d’événements et conservation sécurisée, elle répond aux exigences d’authenticité, intégrité et non-répudiation prévues par eIDAS et le droit probatoire.

## Q4 — Avantages pour clients et e-réputation

**Clients** : sécurité juridique, traçabilité, accessibilité et rapidité.  
**MQBanque** : rétablissement de confiance, preuve de conformité, diminution du risque contentieux et meilleure e-réputation. 

---

<a id="cours-5"></a>
# 5) Cours 5 — Sécuriser les équipements — Audit MSAP (Marut)

*(Source : Cours5-CEJMA-SécuriserlesEquipements.pdf).* 

## Q1 — Situations à risque observées et remédiations proposées

**Risques majeurs repérés :**

* Postes non verrouillés ; mots de passe faibles ; périphériques USB inconnus ; Wi-Fi non isolé ; applications non autorisées ; absence de patching ; sauvegardes insuffisantes ; comptes admin trop répandus.

**Remédiations prioritaires :**

* Verrouillage automatique (GPO), MFA, gestionnaire de mots de passe, whitelist d’applications, contrôle/permissivité USB (scan et chiffrement), patch management centralisé, sauvegardes chiffrées et tests réguliers. 

## Q2 — Bonnes pratiques (texte prêt à insérer dans la charte)

(Version prête à coller — voir section Annexes pour texte complet et modèles rédigés.)

## Q3 — Limiter les risques liés à la messagerie

**Techniques** : SPF / DKIM / DMARC, filtrage anti-phishing, scan antivirus, blocage d’exécutables, chiffrement des courriels sensibles (S/MIME ou PGP), MFA.  
**Organisation** : procédure d’appel de vérification en cas de demande financière, classification des informations, signalement systématique via l’équipe sécurité. 

## Q4 — Points clés pour la rubrique « bonnes pratiques »

1. Identification et authentification.  
2. Verrouillage automatique.  
3. Politique mots de passe.  
4. Usage périphériques amovibles.  
5. Installations logicielles contrôlées.  
6. Règles messagerie & phishing.  
7. Usage Internet professionnel.  
8. Sauvegardes et restauration.  
9. Signalement d’incident.  
10. Formation obligatoire.

*(Voir Annexes — “Rubrique : Bonnes pratiques”)*

---

<a id="cours-6"></a>
# 6) Cours 6 — Obligations légales, failles de sécurité, habilitations et segmentation (MSAP)

*(Source : Cours6-CEJMA-ObligationsLegalesFaillesSecurite.pdf).* 

## Q1 — Configurations risquées (identification)

* Comptes locaux admin utilisés pour tâches quotidiennes ; ports RDP exposés ; services/applicatifs non patchés ; partages réseau non sécurisés ; absence de chiffrement de stockage.

**Mesures immédiates :** principe du moindre privilège, usage de comptes à privilèges via bastion/PAM, désactivation services inutiles, patch management.

## Q2 — Bonnes pratiques gestion des habilitations (synthèse)

* Principe du **Least Privilege** ; séparation des rôles ; gestion de comptes à privilèges (PAM) ; provisioning/deprovisioning automatisé connecté à RH ; revues périodiques d’habilitations ; journalisation et MFA pour accès sensibles. 

## Q3 — Autre problème lié aux privilèges excessifs

* **Mouvement latéral et escalade** : compte privilégié compromis → accès large au SI → exfiltration, chiffrement (ransomware), sabotage.

## Q4 — Note synthétique (solutions pour le responsable)

**Priorités :** annuaire central (AD/LDAP), IAM, MFA, bastion + PAM, segmentation réseau, chiffrement, SIEM/EDR, procédure d’incident documentée.

## Q5 — Préconisations de segmentation SI (schéma textuel)

**Zones proposées :**

* **DMZ** : site web, reverse proxy, VPN d’accès externe.  
* **Zone Bureautique** : postes utilisateur, internet ; accès restreint aux serveurs applicatifs.  
* **Zone Applicative** : serveurs métiers, API ; accès contrôlé via ACL.  
* **Zone Base de données** : stockage sensible, pas d’accès direct depuis internet.  
* **Zone Administrative** : RH, paie (isolation renforcée).  
* **Zone Sauvegarde** : accès via canaux sécurisés, stockage chiffré.  
* **Zone IoT / Impression** : VLAN séparé, accès limité.

**Règle de contrôle** : whitelist des flux, inspection inter-zones (IDS/IPS), authentification forte pour flux critiques. 

---

<a id="annexes"></a>
# Annexes utiles : modèles, matrices et schémas textuels

## A — Phrase de consentement (modèle probatoire — à prononcer et horodater)

> « Bonjour, je vous appelle de la part de [Nom du centre]. Cette conversation peut être enregistrée pour les besoins de [finalité : ex. contrôle qualité / formation / preuve contractuelle]. Acceptez-vous que j’enregistre cet appel ? »  
> **Procédure** : faire prononcer la phrase et la conserver dans l’enregistrement (horodatage automatique). Voir recommandations CNIL. ([CNIL — Écoute et enregistrement](https://www.cnil.fr/fr/lecoute-et-lenregistrement-des-appels-sur-le-lieu-de-travail))

## B — Log modèle (format à conserver pour preuve)

```

{
"call_id": "UUID-xxxx",
"datetime_start": "YYYY-MM-DDThh:mm:ssZ",
"operator_id": "OP123",
"caller_number": "+33xxxxxxxxx",
"consent_phrase": "Bonjour... Acceptez-vous que j'enregistre cet appel ?",
"consent_given": true,
"recording_file": "calls/UUID-xxxx.wav",
"recording_hash": "sha256:abcdef...",
"retention_policy": "quality:180d; proof:5y",
"access_log": [
{"user":"admin1","datetime":"...","action":"download"},
{"user":"auditor2","datetime":"...","action":"listen"}
]
}

```

> **But** : conserver horodatage, empreinte (hash) du fichier, preuve du consentement et journal des accès pour assurer force probante.

## C — Rubrique complète « Bonnes pratiques »

### ・Sécurité et authentification
- Utiliser un mot de passe fort, unique et confidentiel (≥12 caractères avec majuscules, minuscules, chiffres et symboles)
- Ne jamais partager ses identifiants ni enregistrer ses mots de passe dans le navigateur
- Activer la double authentification (MFA) sur les services compatibles
- Verrouiller sa session dès qu’on quitte son poste, même brièvement

### ・Hygiène numérique et matériel
- Ne pas brancher de périphériques USB inconnus ou personnels sans autorisation
- Ne pas installer de logiciels non validés par l’administrateur
- Effectuer les mises à jour système et antivirus dès qu’elles sont proposées
- Sauvegarder les données importantes sur des emplacements sécurisés et autorisés

### ・Messagerie et navigation Internet
- Être vigilant face aux courriels suspects (expéditeur inconnu, fautes, urgence inhabituelle)
- Ne jamais cliquer sur des liens douteux ni ouvrir des pièces jointes non sollicitées
- Vérifier l’adresse de l’expéditeur avant de répondre ou transférer un message
- Utiliser la messagerie professionnelle uniquement à des fins professionnelles

### ・Sensibilisation et comportement responsable
- Signaler immédiatement tout incident ou comportement suspect à l’équipe technique
- Participer aux formations de sensibilisation à la cybersécurité
- Respecter les droits d’auteur, la confidentialité et la législation sur les données personnelles
- Adopter un comportement numérique responsable et respectueux


## D — Matrice IAM synthétique (exemple)

| Rôle                      |             Accès minimum (exemples) |      MFA requis     | Revue périodique |
| ------------------------- | -----------------------------------: | :-----------------: | :--------------: |
| Agent télécentre          | Poste utilisateur, CRM customer-view |         Oui         |   Trimestrielle  |
| Superviseur               |  CRM full, stats, remontée incidents |         Oui         |   Trimestrielle  |
| Administrateur applicatif |             Serveur app, déploiement |    Oui + Bastion    |     Mensuelle    |
| Administrateur infra      |                    AD, PAM, pare-feu | Oui + Bastion + PAM |     Mensuelle    |

## E — Schéma textuel de segmentation (ASCII)

```

[Internet] --> [Reverse Proxy / WAF - DMZ] --> [Zone Applicative] --> [Zone BDD]
|
--> [Zone Bureautique]
--> [Zone Administrative (RH)]
--> [Zone Sauvegarde (isolée, chiffrée)]
--> [Zone IoT (VLAN isolé)]

```

---

<a id="references"></a>
# ・Références web citées (principales)

## ・Textes européens / RGPD / eIDAS
* [Règlement (UE) 2016/679 — RGPD (texte officiel, EUR-Lex)](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)  
* [RGPD — PDF officiel (CELEX)](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX%3A32016R0679)  
* [Version lisible / indexée du RGPD — gdpr-info.eu](https://gdpr-info.eu/)  
* [Règlement (UE) n°910/2014 — eIDAS (EUR-Lex)](https://eur-lex.europa.eu/eli/reg/2014/910/oj/eng)

## ・CNIL — enregistrements, notification, guides pratiques
* [CNIL — L’écoute et l’enregistrement des appels sur le lieu de travail](https://www.cnil.fr/fr/lecoute-et-lenregistrement-des-appels-sur-le-lieu-de-travail)  
* [CNIL — L’enregistrement des conversations téléphoniques afin d’établir la preuve de la formation d’un contrat](https://www.cnil.fr/fr/lenregistrement-des-conversations-telephoniques-afin-detablir-la-preuve-de-la-formation-dun-contrat)  
* [CNIL — Notifier une violation de données personnelles (téléservice)](https://www.cnil.fr/fr/services-en-ligne/notifier-une-violation-de-donnees-personnelles)  
* [CNIL — Violations de données personnelles : les règles à suivre](https://www.cnil.fr/fr/violations-de-donnees-personnelles-les-regles-suivre)  
* [CNIL — Q&A : Enregistrement ou écoute des conversations téléphoniques — faut-il informer ?](https://cnil.fr/fr/cnil-direct/question/enregistrement-ou-ecoute-des-conversations-telephoniques-faut-il-informer-ses)  
* [CNIL — Guide / fiche PDF ns57 (écoute et enregistrement)](https://cnil.fr/sites/cnil/files/atoms/files/ns57.pdf)

## ・Code pénal (France) — articles cités
* [Article 226-4-1 — Usurpation d’identité (Légifrance)](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000042193593)  
* [Article 323-1 — Accès frauduleux à un système (Légifrance)](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000047052655)  
* [Article 313-1 — Escroquerie (Légifrance)](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000006418192)

## ・ANSSI / Cyber.gouv — guides sécurité
* [ANSSI — Administration sécurisée des SI (guide PDF)](https://cyber.gouv.fr/sites/default/files/2018/04/anssi-guide-admin_securisee_si_v3-0.pdf)  
* [ANSSI — Référentiel PAMS (PDF)](https://cyber.gouv.fr/sites/default/files/2022-10/ANSSI_PAMS_referentiel_v1.1_vFR.pdf)  
* [ANSSI — Recommandations pour la protection des systèmes essentiels (PDF)](https://cyber.gouv.fr/sites/default/files/2020/12/guide_protection_des_systemes_essentiels.pdf)

## ・Autres ressources utiles
* [Axialys — Enregistrement des appels & bonnes pratiques (article)](https://blog.axialys.com/enregistrement-des-appels-rgpd-bonnes-pratiques-2024/)  
* [GDPR.info (indexation pratique du texte RGPD)](https://gdpr-info.eu/)  
* [CNIL — tag “Téléphonie” (regroupe articles CNIL)](https://www.cnil.fr/fr/tag/telephonie)  
* [Cybermalveillance.gouv.fr — Fiche réflexe : piratage d'un système informatique professionnel](https://www.cybermalveillance.gouv.fr/tous-nos-contenus/fiches-reflexes/piratage-systeme-informatique-pro)  
* [DocuSign — valeur légale & eIDAS (page explicative)](https://www.docusign.fr/produits/signature-electronique/valeur-legale)

---
