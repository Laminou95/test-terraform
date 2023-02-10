Après vous être connecté, sélectionné "créer une nouvelle organisation" et donnons-lui le nom de "mohamadoutestterraform"."Créer un nouvel espace de travail" avec le type "Flux de travail de contrôle de version"Sélectionnez le fournisseur en tant que "GitHub" dans l'onglet "Se connecter au VCS". Assurons-nous que votre bloqueur de fenêtres contextuelles est activé afin de pouvoir accéder à notre compte github et fournir un accès à terraform.

![terra1](https://user-images.githubusercontent.com/93289664/218149247-d947a6a1-43e1-4052-b478-2a9950d10438.PNG)

Choisissons un git repository et enfin fournissons le nom de l'espace de travail et enregistrez la configuration
![terra4](https://user-images.githubusercontent.com/93289664/218153594-96d8a0ab-51ff-41bc-bc91-6d7a17fbfda3.PNG)
![terra5](https://user-images.githubusercontent.com/93289664/218154107-c48a7dde-352e-46be-ae70-2d57db18a55f.PNG)

Visiteos la page Google Cloud Platform (https://console.cloud.google.com/)
Accédons à "IAM & Admin > Comptes de service" dans le menu de navigation et cliquons sur le bouton "Créer un compte de service" dans la barre d'outils supérieure. Entrons le nom du compte de service : (par exemple, git-terraform-gcp). Ensuite, accordons l'accès au compte de service au projet (par exemple, Rôle - > Basique - > Propriétaire) et cliqueons sur "Terminé". Sélectionnons ensuite le compte de service nouvellement créé et accédons à "Gérer les clés". Créer Clé avec le type de clé JSON, la clé sera téléchargée dans notre navigateur lorsque nous cliquerons sur "CRÉER". À l'étape suivante, nous utiliserons cette clé json pour nous connecter à notre compte Terraform.
![terra7](https://user-images.githubusercontent.com/93289664/218159219-1145ec6e-b92c-45ca-8e0a-cb51e2753921.PNG)

![terra8](https://user-images.githubusercontent.com/93289664/218159424-8df1fb0e-f72f-4278-b7ca-17e319a96e90.PNG)

Copions l'ID du projet depuis notre console GCP (second-drake-376011) et remplaçons-le dans le fichier main.tf du github repository, puis configurons notre environnement de variable en faisant cette declaration: credentials= "${file("service_account.json")}" et après avoir renommer la clé sous format json par "service_account.json"
![Capture d’écran du 2023-02-10 18-49-26](https://user-images.githubusercontent.com/93289664/218162000-dc284db8-ab13-404f-8b69-f1395953895b.png)

Après avoir installer terraform CLI, nous mettons les fichiers "main.tf" et "service_account.json" dans le meme dossier que terraform. puis nous lançons la commande $terraform init
![Capture d’écran du 2023-02-10 05-08-35](https://user-images.githubusercontent.com/93289664/218164359-a63484d5-5f2b-4f23-af03-acafe9329986.png)

Ensuite nous tapons la commande "$terraform apply".Une erreur nous renseigne de suivre un lien pour activer le "compute engine API" l'API qui permet de créer et exécuter des machines virtuelles sur Google Cloud Platform. Malheureusement pour nous pour activer l'api il faut un compte payant que j'ai tenté des jours et des pour activer l'essai de 3 mois de GCP en mettant les bonnes coordonées de ma cate bancaire valide, le processus echoue à chaque fois au niveau de verification du compte bancaire, ceci en utilisant différentes cartes valides. En plus Google facture la verification du compte.

![Capture d’écran du 2023-02-10 05-23-40](https://user-images.githubusercontent.com/93289664/218167798-4ceb578a-029f-424a-8f74-a55cbf30cb8f.png)

![Capture d’écran du 2023-02-10 05-18-30](https://user-images.githubusercontent.com/93289664/218168151-f3615d40-7caa-43d5-9336-d6b57752c4c1.png)

Normalement après activation de l'API et réessayant la commande "$terraform apply" l'instance de notre machine virtuelle devrait être créée avec succès et pour verifier il suffit d'aller sur gcp et dans le menu "VM instances" et regarder les caracteristique de notre VM(myvm-dev pour notre cas)






désolé pour le retard causé par la periode de présentation des projets. je tiens vraiment à coeur ce stage et sur tout le thème du stage Monsieur.
ce test a été fait avec des resssources que j'ai à ma disposition.

