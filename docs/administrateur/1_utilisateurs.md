---
title: Groupes & utilisateurs
sidebar_label: Groupes & utilisateurs
sidebar_position: 1
description: Configurations des bibliothèques, groupes, profils et utilisateurs dans NumaHOP.
---

import Icon from '@site/src/components/Icon';

:::warning En cours de rédaction
:::

# <Icon icon={["fa", "building-columns"]} /> Gestion des bibliothèques


## Présentation

Dans l’onglet  <Icon icon={["fa", "user"]} /> **Utilisateurs**, l’un des sous-onglets permet de gérer informations suivantes des **établissements utilisateurs** : 

| **Libellé**                       | **Commentaire** | **Voir aussi** |
|-----------------------------------|-----------------|----------------|
| **_Fiche_**                       |                 |                |
| Nom                               | 🔴 Obligatoire                |                |
| Website                           | 🔵 Facultatif                 |                |
| Téléphone                         | 🔵 Facultatif                |                |
| Courriel                          | 🔵 Facultatif                |                |
| Préfixe                           | 🔵 Facultatif                  |                |
| Courriel                          | 🔵 Facultatif                  |                |
| Configuration FTP - Bibliothèque  | 🔵 Facultatif                  |                |
| Identifiant service versant Cines | 🔵 Facultatif                |                |
| Configuration contrôle            | 🔵 Facultatif                |                |
| Configuration langage OCR         | 🔵 Facultatif               |                |
| Configuration format images       | 🔵 Facultatif                |                |
| Actif                             | 🔵 Facultatif               |                |
| Profil par défaut                 | 🔵 Facultatif               |                |
| Institution                       | 🔵 Facultatif               |                |
| **_Adresse_**                     |                 |                |
| Appartement, escalier, étage      | 🔵 Facultatif                |                |
| Bâtiment                          | 🔵 Facultatif                |                |
| Numéro de la voie                 | 🔵 Facultatif                |                |
| Complément d'adresse              | 🔵 Facultatif                 |                |
| Code postal                       | 🔵 Facultatif                |                |
| Ville                             | 🔵 Facultatif                |                |
| Pays                              | 🔵 Facultatif                |                |
| **_Responsable bibliothèque_**    |                 |                |
| Nom                               | 🔵 Facultatif                |                |
| Tel                               | 🔵 Facultatif                |                |
| Email                             | 🔵 Facultatif                |                |


 Les bibliothèques sont un des éléments prioritaires à configurer pour mettre en place des projets de numérisation.


## Créer une bibliothèque

Renseigner les informations la fiche de bibliothèque divisées en plusieurs parties :
- La première contient des informations d’identification et de paramétrages techniques.
- Les trois suivantes portent sur des renseignements plus concrets : l’adresse, les coordonnées du responsable de la bibliothèque et le logo.


:::danger Pour les instances mutualisées de NumaHOP
La liste des bibliothèques se présente dans l’ordre alphabétique, elle peut être <Icon icon={["fa", "filter"]} />  filtrée par les initiales et en y intégrant ou cachant les bibliothèques inactives.

Les bibliothèques ont un espace disque associé : quand une nouvelle bibliothèque est ajoutée, il faut alors configurer le disque dans le fichier de configuration du démarrage qui n’est pas accessible directement dans NumaHOP. Afin d’effectuer cela, contacter votre prestataire de service ou, si NumaHOP est installée sur vos serveurs  votre administrateur système.
:::


# <Icon icon={["fa", "user-gear"]} /> Gestion des utilisateurs

Pour pouvoir créer des utilisateurs, il est nécessaire de disposer de
l’habilitation USER-HAB1 (Gestion des utilisateurs : création).

## Créer un utlisateur

Pour créer des utilisateurs dans NumaHOP, cliquer sur l'icône <Icon icon={["fa", "user"]} /> **Utilisateurs** dans le menu latéral de gauche, puis choisir **Utilisateurs** dans le sous-menu.

Cliquer ensuite sur le bouton <Icon icon={["fa", "square-plus"]} /> situé à droite de la fenêtre de recherche. Un
formulaire de création d’utilisateur s’affiche dans la partie droite de
l’écran.

Remplir le formulaire. Les champs obligatoires sont :

- Le login : l’identifiant qui permet à l’utilisateur de se connecter
- Le nom de l’utilisateur
- Le prénom de l’utilisateur
- Le mot de passe : il sert à la 1ère connexion et pourra ensuite être modifié par l’utilisateur
- Le courriel
- La bibliothèque : à partir de la liste des [bibliothèques créées dans Numahop](docs/administrateur/1_Groupes%20&%20utilisateurs/1-bibliotheques.md)
- Le profil : dans la liste [des profils créés dans Numahop](docs/administrateur/1_Groupes%20&%20utilisateurs/4-profils.md)

Pour le champ **Actif**, cocher le bouton **oui** pour permettre à
l’utilisateur créé de pouvoir agir dans Numahop.

Cliquer ensuite sur le bouton **Enregistrer**. Le nouvel utilisateur est
créé et reçoit un mail l’informant de la création de son compte et lui
indiquant ses identifiant et mot de passe de connexion à NumaHOP.

## Rattacher l'utilisateur à un groupe

Pour compléter la création de l’utilisateur,il est nécessaire de l'[ajouter à un/des groupe(s) de workflows](docs/administrateur/1_Groupes%20&%20utilisateurs/3-groupes.md).

La rubrique **Utilisateurs** donne aussi accès à la liste des
utilisateurs créés avec des possibilités de recherche et de filtrage (<Icon icon={["fa", "filter"]} />).

## Modifier ou supprimer un utilisateur

Pour pouvoir modifier ou supprimer des utilisateurs, il est nécessaire de disposer des habilitations USER-HAB2 (Gestion des
utilisateurs : modification) et USER HAB3 : (Gestion des utilisateurs :
suppression) :

Pour modifier un utilisateur, cliquer sur nom de l’utilisateur à
modifier puis cliquer sur l'icône <Icon icon={["fa", "pen-to-square"]} /> **Modifier** en haut à droite. Enregistrer les
modifications.

Le bouton <Icon icon={["fa", "bars"]} /> **Autres actions** permet de :
- Supprimer un utilisateur
- Dupliquer un utilisateur 
- Configurer un nouveau mot de passe 


# <Icon icon={["fa", "users-gear"]} /> Gestion des groupes

## Qu'est-ce qu'un groupe d'utilisateurs ?

Les groupes sont un moyen de rassembler plusieurs utilisateurs de
NumaHOP qui sont mobilisés sur les mêmes tâches.

Cette fonctionnalité est liée aux Workflows, puisque ces groupes sont
ensuite assignés sur les différentes étapes des projets de numérisation.

## Configuration des groupes

Pour configurer les groupes, se rendre dans le menu <Icon icon={["fa", "gear"]} /> Administration, puis
**Workflow** et ensuite **Gestion des groupes**.

L’interface se présente ainsi :

- À gauche se trouve la liste des groupes créés, rangés dans l’ordre
alphabétique. 
- Des filtres permettent de sélectionner l’initiale ou la
bibliothèque souhaitée. 
- À droite de la barre de recherche se trouve le
bouton pour créer un nouveau groupe.

Pour créer un groupe, remplir les champs de sa fiche :

- Nom
- Description
- Bibliothèque

Puis, choisir les utilisateurs en tapant les premières lettres du nom dans la barre de recherche.

Les groupes sont ensuite utilisés dans les modèles de
[**Workflow**](docs/administrateur/3_Configurations/1_workflows.md#la-cr%C3%A9ation-de-mod%C3%A8les-de-workflow
)

# <Icon icon={["fa", "users-rectangle"]} /> Gestion des profils:

:::warning Page en cours de rédaction
:::