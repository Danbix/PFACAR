Application de location de voitures
Cette application de location de voitures permet de gérer les clients, les voitures, les contrats et les utilisateurs. Les fonctionnalités principales sont les suivantes:
*	Ajouter un client
*	Ajouter une voiture
*	Rechercher une voiture
*	Ajouter un contrat
*	Charger les contrats
*	Page d'authentification (login)
Les principales fonctions du code sont:
*	update_expired_contracts(): Met à jour les contrats expirés
*	change_background_image(self, image_path): Change l'image de fond de l'application
*	set_background_image(self, image_path): Définit l'image de fond de l'application
*	connect_db(self): Connecte l'application à la base de données
*	create_book_now_page(self): Crée la page "Réserver maintenant"
*	on_book_now_clicked(self): Gère le clic sur le bouton "Réserver maintenant"
*	create_login_page(self): Crée la page de connexion
*	create_account(self, username, password): Crée un compte utilisateur
*	show_create_account_form(self): Affiche le formulaire de création de compte
*	create_registration_form(self): Crée le formulaire d'inscription
*	login(self): Gère le processus de connexion
*	load_clients(self): Charge la liste des clients
*	add_client(self, nom, prenom, email, telephone): Ajoute un nouveau client
*	add_car(self, marque, modele, image_path, type_carburant, nombre_places, transmission, prix_par_jour): Ajoute une nouvelle voiture
*	get_client_details(self, client_id): Récupère les détails d'un client
*	get_car_details(self, voiture_id): Récupère les détails d'une voiture
*	generate_contract_pdf(self, client_id, voiture_id, start_date, end_date): Génère un contrat PDF
*	load_cars(self): Charge la liste des voitures
*	show_add_client_form(self): Affiche le formulaire d'ajout de client
*	choose_image(self): Permet de choisir une image pour la voiture
*	show_add_car_form(self): Affiche le formulaire d'ajout de voiture
*	create_add_contract_form(self): Crée le formulaire d'ajout de contrat
*	create_contracts_table(self): Crée la table des contrats
*	show_search_car_form(self): Affiche le formulaire de recherche de voiture
*	search_car(self, model, transmission, places, marque, type_carburant, price): Recherche une voiture
*	create_search_car_form(self): Crée le formulaire de recherche de voiture
*	show_add_contract_form(self): Affiche le formulaire d'ajout de contrat
*	load_contracts(self): Charge la liste des contrats
*	show_reserved_cars(self): Affiche les voitures réservées
*	show_available_cars(self): Affiche les voitures disponibles
*	display_cars_in_table(self, cars): Affiche les voitures dans un tableau
*	add_contract(self, client_id, voiture_id, start_date, end_date): Ajoute un contrat de location
Pour utiliser cette application, assurez-vous d'avoir installé les bibliothèques nécessaires et de disposer d'une base de données MySQL configurée avec les tables fournies dans le code.

Installation et configuration
Avant d'utiliser cette application, assurez-vous d'avoir installé les bibliothèques nécessaires et de disposer d'une base de données MySQL configurée avec les tables fournies dans le code. Pour ce faire, suivez les étapes ci-dessous:
1.	Installez les bibliothèques nécessaires en utilisant pip:
Copy code
pip install PyQt5 pip install mysql-connector-python 
2.	Configurez votre base de données MySQL en important les tables client, voiture et contract fournies dans le code. Vous pouvez le faire en utilisant un outil comme MySQL Workbench ou phpMyAdmin.
3.	Assurez-vous que les informations de connexion à la base de données sont correctes dans le code. Modifiez la méthode connect_db(self) si nécessaire, en spécifiant le bon nom d'utilisateur, mot de passe et nom de la base de données.
4.	Exécutez l'application en lançant le fichier principal test.py:
Copy code
python test.py 
Utilisation de l'application
Une fois l'application lancée, vous devrez vous connecter ou créer un compte utilisateur. Après vous être connecté, vous pourrez accéder aux différentes fonctionnalités de l'application, notamment ajouter des clients et des voitures, rechercher des voitures, créer des contrats et afficher la liste des contrats existants.
Voici quelques conseils pour utiliser les différentes fonctionnalités de l'application:
*	Pour ajouter un nouveau client, cliquez sur le bouton "Ajouter un client" et remplissez les informations requises.
*	Pour ajouter une nouvelle voiture, cliquez sur le bouton "Ajouter une voiture" et remplissez les informations requises, y compris une image de la voiture.
*	Pour rechercher une voiture, cliquez sur le bouton "Rechercher une voiture" et remplissez les critères de recherche.
*	Pour créer un contrat, cliquez sur le bouton "Ajouter un contrat" et remplissez les informations requises, notamment l'ID du client, l'ID de la voiture, la date de début et la date de fin de la location.
*	Pour afficher la liste des contrats existants, cliquez sur le bouton "Charger les contrats".
N'hésitez pas à explorer l'application et à utiliser les différentes fonctionnalités pour gérer vos clients, vos voitures et vos contrats de location.


Fonctionnalités avancées
L'application offre également des fonctionnalités avancées pour gérer votre parc de véhicules et les contrats associés. Voici quelques exemples de fonctionnalités supplémentaires que vous pourriez trouver utiles :
*	Mise à jour des contrats expirés : La fonction update_expired_contracts() vous permet de mettre à jour les contrats expirés en fonction de la date de fin du contrat. Ceci est utile pour garder une trace des contrats qui sont toujours en cours ou qui ont été complétés.
*	Personnalisation de l'image de fond : L'application vous permet de changer l'image de fond en utilisant les fonctions change_background_image(self, image_path) et set_background_image(self, image_path). Vous pouvez ainsi personnaliser l'apparence de l'application selon vos préférences.
*	Génération de contrats PDF : La fonction generate_contract_pdf() permet de créer un fichier PDF avec les détails du contrat de location, comme l'identifiant du client, l'identifiant de la voiture, les dates de début et de fin de la location, ainsi que d'autres informations pertinentes. Vous pouvez utiliser cette fonction pour envoyer une copie du contrat au client ou pour archiver les contrats pour référence ultérieure.
*	Affichage des voitures réservées et disponibles : L'application vous permet de filtrer les voitures selon leur statut de réservation. En cliquant sur les boutons "Afficher les voitures réservées" et "Afficher les voitures disponibles", vous pouvez afficher les voitures selon leur disponibilité.
*	Recherche de voitures : La fonction search_car() permet de rechercher des voitures en fonction de différents critères, tels que le modèle, la transmission, le nombre de places, la marque, le type de carburant et le prix. Cette fonction est particulièrement utile pour aider les clients à trouver la voiture qui correspond le mieux à leurs besoins.
En plus de ces fonctionnalités avancées, l'application offre un système d'authentification pour protéger l'accès à vos données. Les utilisateurs doivent se connecter avec leur nom d'utilisateur et leur mot de passe pour accéder aux fonctionnalités de l'application.
Contribuer et obtenir de l'aide
Si vous rencontrez des problèmes avec l'application ou si vous souhaitez contribuer au développement de nouvelles fonctionnalités, n'hésitez pas à ouvrir un problème ou une demande d'extraction sur GitHub. Nous apprécions les contributions de la communauté et sommes toujours à la recherche de nouvelles idées pour améliorer l'application.
En outre, si vous avez des questions ou des préoccupations concernant l'utilisation de l'application, vous pouvez consulter la documentation en ligne ou demander de l'aide sur le forum de la communauté. Nous nous efforçons de fournir un soutien rapide et complet à tous nos utilisateurs.

