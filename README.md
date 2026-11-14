# Assistant quotidien

Application web autonome, séparée des projets Atelier IA et PROJECT ATLAS. Elle regroupe les priorités du jour, le suivi de la rénovation, les routines ménagères et un bilan quotidien connecté à Gmail et Google Agenda en lecture seule.

## Accès en ligne

L’application publiée est disponible à l’adresse : https://doudou2000-oss.github.io/assistant-quotidien/.

Elle peut être installée depuis le navigateur d’un téléphone et conserve les données hors ligne. Les listes et préférences restent dans le navigateur de chaque appareil. Utilise l’import/export JSON dans Rubriques pour transférer une sauvegarde. La synchronisation automatique entre appareils n’est pas intégrée.

Dans Services, ajoute l’identifiant client OAuth d’une application Web créée dans Google Cloud, puis connecte ton compte. Les API Gmail et Google Calendar doivent être activées, l’origine JavaScript autorisée doit être `https://doudou2000-oss.github.io`, et ton compte doit être inscrit comme utilisateur test de l’écran de consentement pendant les essais. Les autorisations demandées sont `gmail.metadata` et `calendar.events.readonly` : l’app lit l’objet, l’expéditeur, la date et le statut lu/non lu des 20 messages Inbox les plus récents, ainsi que les événements de la date sélectionnée. Elle ne lit pas le corps ni les pièces jointes des messages et n’écrit rien dans Gmail ou Google Agenda. Le jeton d’accès reste en mémoire de la page; les lignes importées sont stockées localement dans ce navigateur.

Les autorisations Gmail sont restreintes par Google. Pour sortir du mode test et distribuer l’accès au-delà des testeurs, l’application OAuth peut devoir passer par la vérification de Google.

## Développement local

Double-clique sur `Lancer_assistant_quotidien.bat`. L’application s’ouvre sur http://127.0.0.1:8610. Garde la fenêtre de lancement ouverte pendant l’utilisation ; Ctrl+C l’arrête.

Le workflow GitHub Actions publie automatiquement le contenu de `app` sur GitHub Pages à chaque mise à jour de la branche `main`.
