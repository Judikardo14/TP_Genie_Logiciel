# Modélisation d’un système de sécurisation des motos par démarrage biométrique

Devoir de Génie Logiciel — ENSGMM, UNSTIM (Génie Mathématique et Modélisation, 2ᵉ année)
**Auteur :** DOBOEVI Judicaël Karol — **Superviseur :** Dr CAPO-CHICHI Gilbert

## Contexte

Quatre cas de vol de moto enregistrés à l'UNSTIM en janvier 2025. Un hackathon a été lancé pour sécuriser les motos par démarrage biométrique.


## Contenu

| Fichier | Description |
|---|---|
| `README.md` | Index du projet et des diagrammes |
| `TP_Génie_Logiciel.pdf` | Analyse complète du dispositif |

## Diagrammes (Lucidchart)

**Document 1 (3 pages) :** [LIEN_DOC_1](https://lucid.app/lucidchart/0af655b8-c348-4b3f-874d-a76998b335e3/edit?viewport_loc=-991%2C-530%2C3289%2C1611%2C0_0&invitationId=inv_bcba9167-6261-42f5-b5e7-ea00134283e7)

| Page | Diagramme | Lien |
|:---:|---|---|
| 1 | Cas d'utilisation | [Page 1](https://lucid.app/lucidchart/0af655b8-c348-4b3f-874d-a76998b335e3/edit?viewport_loc=-991%2C-530%2C3289%2C1611%2C0_0&invitationId=inv_bcba9167-6261-42f5-b5e7-ea00134283e7) |
| 2 | Classes | [Page 2](https://lucid.app/lucidchart/0af655b8-c348-4b3f-874d-a76998b335e3/edit?viewport_loc=-296%2C-210%2C3034%2C1486%2CXrZPax2~2SjV&invitationId=inv_bcba9167-6261-42f5-b5e7-ea00134283e7) |
| 3 | Séquence | [Page 3](https://lucid.app/lucidchart/0af655b8-c348-4b3f-874d-a76998b335e3/edit?viewport_loc=-3615%2C-1315%2C2876%2C1409%2CdOZPFMDdV0LL&invitationId=inv_bcba9167-6261-42f5-b5e7-ea00134283e7) |

**Document 2 (2 pages) :** [LIEN_DOC_2](LIEN_DOC_2)

| Page | Diagramme | Lien |
|:---:|---|---|
| 1 | Composants | [Page 1](https://lucid.app/lucidchart/2c0a0cd5-9da6-4334-b8c1-dd97b5d26ad2/edit?viewport_loc=-365%2C467%2C2325%2C1045%2CmP0Pl2Vp92LS&invitationId=inv_38bd36c2-53f7-4bd0-bde5-ad277056424d) |
| 2 | Activité | [Page 2](https://lucid.app/lucidchart/2c0a0cd5-9da6-4334-b8c1-dd97b5d26ad2/edit?viewport_loc=-876%2C-231%2C3648%2C1640%2CSh1PrpzhVMn_&invitationId=inv_38bd36c2-53f7-4bd0-bde5-ad277056424d) |

## Acteurs

- Propriétaire de moto
- Utilisateur autorisé (proche, ami)
- Mécanicien
- Agent de sécurité (vigile)

## Composants

- Capteur d'empreintes digitales
- Unité de traitement (microcontrôleur)
- Mémoire locale chiffrée
- Relais de coupure
- Module d'alimentation
- Indicateurs lumineux et sonores
- Boîtier étanche et scellé
- Moyen de secours (carte maître ou code)
- Câblage d'interface

## Fonctionnement

1. L'utilisateur pose son doigt sur le capteur.
2. L'unité de traitement compare l'empreinte à la mémoire chiffrée.
3. Empreinte reconnue : voyant vert, bip bref, le relais ferme le circuit d'allumage et de démarrage.
4. Empreinte refusée : voyant rouge, bip, tentative enregistrée, nouvel essai après 60 s.
5. Au 3ᵉ échec : alerte sonore, démarrage bloqué jusqu'à l'usage de la carte maître.
6. Capteur en panne : démarrage par la carte maître.
