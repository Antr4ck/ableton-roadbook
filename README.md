# Ableton Roadbook

Roadbook interactif en français pour structurer un morceau : direction artistique, arrangement, checklist et notes. Base proposée : DnB atmosphérique en 4/4.

## Prérequis

- Un navigateur récent prenant en charge JavaScript et le stockage local.
- Aucun compte, serveur, gestionnaire de paquets ni plugin nécessaire pour la version autonome.
- Ableton Live n’est pas nécessaire pour ouvrir le roadbook : cette version est un compagnon de production, sans connexion au logiciel.

## Installation

### Méthode 1 — Télécharger le ZIP

1. Ouvrir https://github.com/Antr4ck/ableton-roadbook.
2. Cliquer sur **Code**, puis **Download ZIP**.
3. Extraire entièrement l’archive dans un dossier permanent.
4. Ouvrir le fichier `index.html` extrait dans un navigateur. Si nécessaire, utiliser **Ouvrir avec** et sélectionner le navigateur.
5. Conserver le dossier au même emplacement et utiliser le même navigateur pour retrouver plus facilement les données locales.

Ne pas ouvrir uniquement l’aperçu du code HTML sur GitHub : télécharger puis ouvrir le fichier local.

### Méthode 2 — Cloner avec Git

Si Git est installé :

```sh
git clone https://github.com/Antr4ck/ableton-roadbook.git
cd ableton-roadbook
```

Ouvrir ensuite `index.html` depuis l’explorateur de fichiers dans un navigateur. Aucune commande de compilation ou d’installation de dépendances n’est nécessaire.

## Première utilisation

1. Renseigner le nom du projet, le tempo et la tonalité.
2. Définir l’émotion, l’ambiance, l’élément signature et l’évolution souhaitée.
3. Ouvrir les sections de l’arrangement et ajuster leurs premières et dernières mesures.
4. Reporter manuellement les repères dans Ableton.
5. Ajouter les notes et cocher les tâches ainsi que les sections terminées.
6. Utiliser la zone d’écoute critique pour noter les problèmes par mesure.

Le calcul des minutages suppose une mesure en 4/4 et un tempo constant. Il n’inclut pas les queues de réverbération ou de delay. Les avertissements signalent les plages invalides, les trous et les chevauchements.

## Sauvegarder et restaurer

Les modifications sont enregistrées automatiquement dans le stockage local lorsque le navigateur l’autorise. Cette sauvegarde n’est ni synchronisée avec GitHub ni intégrée au Live Set. Le comportement du stockage des fichiers locaux peut varier selon le navigateur.

- **Exporter JSON** : conserver une copie des données dans un fichier, idéalement dans le dossier du projet musical.
- **Importer JSON** : sélectionner une sauvegarde exportée par cette version, puis confirmer le remplacement des données actuelles.
- **Imprimer / PDF** : ouvrir la boîte d’impression et sélectionner une destination PDF si disponible. Le PDF est un document de consultation, pas une sauvegarde réimportable.
- **Réinitialiser** : effacer les données locales après confirmation. Exporter avant de réinitialiser.

Exporter régulièrement, et toujours avant un changement de navigateur, un déplacement du fichier ou un nettoyage des données de navigation. Éviter le mode privé pour un usage durable.

### Plusieurs morceaux

La version actuelle ne fournit pas de bibliothèque de projets : changer le nom du morceau ne crée pas une sauvegarde distincte. Exporter un JSON par morceau, puis importer celui du morceau à reprendre.

## Mettre à jour

1. Exporter une sauvegarde JSON.
2. Télécharger la nouvelle version du ZIP et remplacer les fichiers de l’application, ou exécuter `git pull` depuis le dossier cloné si aucune modification locale ne bloque la mise à jour.
3. Rouvrir ou recharger `index.html`.
4. Si nécessaire, réimporter une sauvegarde compatible.

## Fonctionnalités

- Fiche projet et direction artistique.
- Dix sections ajustables avec minutage calculé.
- Checklist et progression.
- Notes par section et écoute critique.
- Sauvegarde locale, import/export JSON et impression via le navigateur.

## Max for Live — intégration non fournie

Ce dépôt ne contient actuellement ni device `.amxd`, ni patch Max prêt à charger, ni liaison à l’API Live. L’installation ci-dessus ne crée donc pas de périphérique dans Ableton.

L’interface HTML peut servir de base à un affichage dans un objet `jweb`, mais cette intégration reste à construire et à tester dans votre configuration. L’import/export, le stockage et l’impression dans cet environnement ne sont pas validés. Les notes ne sont pas enregistrées dans le Live Set, les pistes ne sont pas liées et les repères ne sont pas créés automatiquement.

## Dépannage

- **Du code s’affiche à la place de l’interface** : vérifier que le fichier extrait porte bien l’extension `.html` et l’ouvrir avec un navigateur plutôt qu’un éditeur de texte.
- **Les données ne reviennent pas** : vérifier le navigateur, le profil et l’emplacement utilisés ; importer le dernier JSON exporté.
- **Le stockage est indisponible** : utiliser l’export JSON avant de fermer la page et vérifier les restrictions du navigateur.
- **L’import échoue** : sélectionner un JSON exporté par cette version. Les sauvegardes de prototypes antérieurs peuvent avoir un format différent. La taille maximale acceptée est de 2 000 000 octets.
- **Le minutage semble incorrect** : vérifier le tempo, les plages de mesures et l’hypothèse de 4/4 à tempo constant.

## Statut

Version autonome compacte issue du roadbook conçu dans la conversation ; interface réorganisée, non identique octet pour octet au premier HTML. Pas de dépendances externes ni de requêtes réseau. Les tests dans les différents navigateurs et dans Max restent à effectuer.
