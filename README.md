# Assistant quotidien

Prototype web autonome, séparé des projets Atelier IA et PROJECT ATLAS. Il comprend les rubriques à activer, des priorités du jour, le suivi des pièces en rénovation, une liste de tâches ménagères et l'import/export de sauvegardes. Il est préparé comme une PWA installable sur téléphone, avec une mise en cache pour l'usage hors ligne.

## Démarrer

Double-clique sur Lancer_assistant_quotidien.bat. L'application s'ouvre sur http://127.0.0.1:8610. Garde la fenêtre de lancement ouverte pendant l'utilisation ; Ctrl+C l'arrête.

L'application utilise seulement Python standard et enregistre ses préférences et listes dans le navigateur de cet appareil. Tu peux exporter une sauvegarde JSON et la réimporter depuis Rubriques. En local, elle peut être installée depuis le navigateur de l'ordinateur ; l'installation sur téléphone requiert une adresse HTTPS publique.

Gmail et Google Agenda ne sont pas connectés dans cette version ; les accès accordés à ChatGPT ne sont pas partagés automatiquement avec cette application.

Le workflow GitHub Actions du dossier `.github/workflows` publiera automatiquement le contenu de `app` sur GitHub Pages après l'envoi du projet sur la branche `main`. Le site sera servi en HTTPS et pourra être installé depuis le navigateur du téléphone.

Le code publié ne contient pas les informations de rénovation personnelles. Elles sont gardées dans `.private-backup.json`, ignoré par Git, pour pouvoir les importer ensuite dans l'app sur le téléphone. Les listes restent enregistrées dans le navigateur de chaque appareil : la synchronisation automatique entre appareils n'est pas encore développée.

Pour le publier, crée un dépôt GitHub vide nommé `assistant-quotidien`, envoie le contenu de ce dossier sur la branche `main`, puis active GitHub Pages avec la source `GitHub Actions` dans les réglages du dépôt. Google OAuth n'est pas encore intégré.
