Après vous être connecté, sélectionné "créer une nouvelle organisation" et donnons-lui le nom de "mohamadoutestterraform"."Créer un nouvel espace de travail" avec le type "Flux de travail de contrôle de version"Sélectionnez le fournisseur en tant que "GitHub" dans l'onglet "Se connecter au VCS". Assurons-nous que votre bloqueur de fenêtres contextuelles est activé afin de pouvoir accéder à notre compte github et fournir un accès à terraform.

![terra1](https://user-images.githubusercontent.com/93289664/218149247-d947a6a1-43e1-4052-b478-2a9950d10438.PNG)

Choisissons un git repository et enfin fournissons le nom de l'espace de travail et enregistrez la configuration
![terra4](https://user-images.githubusercontent.com/93289664/218153594-96d8a0ab-51ff-41bc-bc91-6d7a17fbfda3.PNG)
![terra5](https://user-images.githubusercontent.com/93289664/218154107-c48a7dde-352e-46be-ae70-2d57db18a55f.PNG)

Visiteos la page Google Cloud Platform (https://console.cloud.google.com/)
Accédons à "IAM & Admin > Comptes de service" dans le menu de navigation et cliquons sur le bouton "Créer un compte de service" dans la barre d'outils supérieure. Entrons le nom du compte de service : (par exemple, git-terraform-gcp). Ensuite, accordons l'accès au compte de service au projet (par exemple, Rôle - > Basique - > Propriétaire) et cliqueons sur "Terminé". Sélectionnons ensuite le compte de service nouvellement créé et accédons à "Gérer les clés". Créer Clé avec le type de clé JSON, la clé sera téléchargée dans notre navigateur lorsque nous cliquerons sur "CRÉER". À l'étape suivante, nous utiliserons cette clé json pour nous connecter à notre compte Terraform.
![terra7](https://user-images.githubusercontent.com/93289664/218159219-1145ec6e-b92c-45ca-8e0a-cb51e2753921.PNG)

![terra8](https://user-images.githubusercontent.com/93289664/218159424-8df1fb0e-f72f-4278-b7ca-17e319a96e90.PNG)
