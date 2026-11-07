# Assistant quotidien

Application web autonome, séparée des projets Atelier IA et PROJECT ATLAS. Elle regroupe les priorités du jour, le suivi de la rénovation, les routines ménagères et les rubriques de connexion Gmail/Agenda.

## Accès en ligne

L’application publiée est disponible à l’adresse : https://doudou2000-oss.github.io/assistant-quotidien/.

Elle peut être installée depuis le navigateur d’un téléphone et conserve les données hors ligne. Les listes et préférences restent dans le navigateur de chaque appareil. Utilise l’import/export JSON dans Rubriques pour transférer une sauvegarde. La synchronisation automatique entre appareils et la connexion Gmail/Google Agenda ne sont pas encore intégrées.

## Développement local

Double-clique sur `Lancer_assistant_quotidien.bat`. L’application s’ouvre sur http://127.0.0.1:8610. Garde la fenêtre de lancement ouverte pendant l’utilisation ; Ctrl+C l’arrête.

Le workflow GitHub Actions publie automatiquement le contenu de `app` sur GitHub Pages à chaque mise à jour de la branche `main`.
