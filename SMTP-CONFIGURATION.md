# Configuration SMTP

Les identifiants SMTP sont désormais fournis par l’environnement, au lieu d’être inscrits dans `backend/app/Config/Email.php`.

## Configuration locale

Ajouter les entrées du fichier `.env.example` à `backend/.env`. Si ce fichier contient déjà une configuration, conserver ses autres paramètres et ne remplacer que les entrées `email.*` concernées.

Renseigner le serveur, l’utilisateur et le mot de passe SMTP dans ce fichier local. Ne jamais les ajouter dans Git. Les valeurs fournies dans `.env.example` ne permettent pas d’envoyer de messages : elles doivent être adaptées à l’environnement.

CodeIgniter charge les propriétés `email.SMTPHost`, `email.SMTPUser` et `email.SMTPPass` via le mécanisme de `BaseConfig` inclus dans le dépôt. Dans un environnement qui utilise des variables système, les formes `email_SMTPHost`, `email_SMTPUser` et `email_SMTPPass` sont également prises en charge par cette version.

Le port, le protocole et le chiffrement restent configurables avec les entrées correspondantes de l’exemple. Aucun envoi de message n’a été effectué pour cette modification.

## Périmètre

Cette modification concerne la copie `malo-perso/so-permis`. Elle ne modifie pas le dépôt de groupe ni le service de messagerie.

Les anciennes valeurs ont été conservées hors du dépôt, dans une sauvegarde locale remise au propriétaire de cette copie. Aucun secret ni fichier de sauvegarde n’est fourni ici.

Le changement supprime les identifiants du fichier courant ; il ne les supprime pas des anciens commits. Le dépôt doit rester privé jusqu’à la vérification de l’historique et des autres données à publier. Un identifiant réel déjà utilisé doit être remplacé auprès du fournisseur avant toute ouverture de cet historique.
