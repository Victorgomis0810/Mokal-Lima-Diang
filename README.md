# Xam-Xam

C'est un site qui aide étape par étape, comment fonctionnent la connexion à un site, certaines attaques courantes, quelques algorithmes de machine learning et les protections qui vont avec.

## Un projet pour apprendre, rien d'autre

Ce projet est purement pédagogique. Tout ce que tu y vois est inventé : les adresses IP, les mots de passe, les jetons, les paquets. Il n'y a aucun outil d'attaque dedans, seulement des schémas animés et des explications. Il ne fait aucun appel réseau, ne se connecte à rien et ne collecte aucune donnée.

Si tu veux tester la sécurité d'un système, fais-le seulement sur le tien, ou avec l'accord écrit de son propriétaire.

## Pourquoi je l'ai fait

En préparant mon mémoire de fin d'études (meet_VF_AI, une application de gestion de réunions), j'ai passé beaucoup de temps à comprendre des notions comme Nginx, Redis, les jetons JWT ou les en-têtes de sécurité. Je me suis dit que ces choses se comprennent mieux avec une image et une comparaison de la vie de tous les jours qu'avec une définition. L'idée du site vient de Protocol Explorer, que j'avais trouvé très clair.

## Comment ça marche

Quatre onglets : Authentification (8 sujets), Attaques (8), Machine Learning (5) et Sécurisation (8). Dans chacun, tu choisis un sujet, puis tu cliques sur Lecture ou Avancer pour suivre le trajet des messages entre les composants. En bas, le tableau montre ce qui circule, et un clic sur une ligne détaille le paquet.

Le bouton « Mode enfant » donne des explications avec des comparaisons simples. « Mode technique » donne les termes exacts. Le bouton « Thème » change les couleurs.

## L'essayer chez soi

Il suffit d'ouvrir `index.html` dans un navigateur. Pas d'installation, pas de dépendance.

Pour le mettre en ligne, par exemple sur Vercel : mets `index.html` dans un dépôt GitHub, importe le dépôt sur vercel.com, laisse « Other » comme framework et ne mets pas de commande de build.

## Pour les curieux

Tout est dans un seul fichier. Les couleurs sont des variables CSS au début du fichier. Chaque sujet est un objet dans les tableaux `AUT`, `ATK`, `SEC` (ou `ML` pour le machine learning), donc en ajouter un revient à copier un objet existant et à changer les textes.

## Limites

Les scénarios sont simplifiés pour rester lisibles : la réalité est plus nuancée. Ça ne remplace ni un vrai cours de cybersécurité ni la documentation officielle des outils. Il me reste à ajouter trois sujets de machine learning (Transformer, Whisper, modèles de langage).

## Qui

Victor Dacotine Gomis, étudiant en informatique à l'UCAO (Dakar). Mon portfolio : https://victordgomis.duckdns.org
