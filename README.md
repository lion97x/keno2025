# Readme

Fichier d'analyse du keno avec les calculs par unité

# Ajout par Garlan Ngoune Nguetsa
# Corrigé par Christophe PRUD'HOMME
- Modification du 22/05/2025 (V1.4.1):

Le code ne se base plus sur les fichiers officiels du keno tant que ces champs sont présents :
"date", "heure" et "bouleN" (N de 1 à 20)

- Modification du 27/05/2025 (V2.0.0):

Le programme peut maintenant reboucler sur lui-même et filtre les échantillons en fonction de la période souhaitée par l'utilisateur

-  Modification du 03/06/2025 (V2.1.0):

J'ai reglé le problème sur le fait que le programme ne marchait plus après la nouvelle version. (j'avoue j'aurais du faire des tests avant)
Le programme reboucle normalement mais on ne peut pas modifier la période voulue pour l'instant

- Modification du 04/06/2025 (V2.1.1):

Le programme reprend son fonctionnement normal et n'est plus en debug continue

- Modification du 04/06/2025 (V2.1.2):

Le programme peut maintenant recommencer en prenant en compte de nouvelles dates

- Modification du 04/06/2025 (V2.1.3):

Petit changement d'esthétique

# Fonctionnement principal

Mon code est compatible inter-OS

/!\ :
    - Le programme ne fonctionne qu'en ligne de commandes pour l'instant

Voici comment l'utiliser en lignes de commandes :

.\AIProject.exe chemin_du_dossier_du/des_fichiers date_limite_basse/date_unique date_limite_haute

Légendes :

- .\AIProject.exe : Chemin de l'application

- chemin_du_dossier_du/des_fichiers : L'application cherche récursivement tous les fichiers csv qu'elle rencontre sans discrimination

- date_limite_basse/date_unique : La date limite que vous voulez observer (facultatif)

- date_limite_haute : La date limite que vous voulez observer (facultatif)

Les paramètres de date peuvent être construits de 2 manières différentes :

- date absolue : "JJ/MM/AAAA" (Le programme traitera toutes les dates de façon européenne)
- date relative : 'N' suivi d'un suffixe

Le programme prend aussi en compte l'inversion de dates entre la date max et la date min

Les suffixes en question sont : 

- t/T : Pour dire que le nombre voulu est le nombre de tirages
- j/J : Pour dire que le nombre voulu est le nombre de jours
- m/M : Pour dire que le nombre voulu est le nombre de mois
- a/A : Pour dire que le nombre voulu est le nombre d'années

Exemple :

.\AIProject.exe dossier 2025/04/01 05/03/2024 (Le programme traitera tous les tirages compris entre le 5 mars 2024 et le 1 avril 2025)

.\AIProject.exe dossier 45t (Le programme traitera les 45 tirages les plus récents)

.\AIProject.exe dossier 2025/04/01 8t (Le programme traitera les 8 tirages après le 1 avril 2025)

.\AIProject.exe dossier 2a 6m (Le programme traitera les tirages sur 6 mois d'il y a 2 ans)
