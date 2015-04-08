# Documentation des classes de l'application c# gsb3
--
## Visiteur.cs 

### id
    nombre généré qui est unique et propre à un visiteur
### nom 
    le nom  du visiteur
### prenom
    le prenom du visiteur
### login
    chaîne de caractères qui permet de se connecter à l'application, propre à un visiteur
### mdp
    chaîne de caractères qui permet de se connecter à l'application, propre à un visiteur
### adresse
    adresse du visiteur
### cp
    code postal du visiteur
### ville
    ville où habite le visiteur
### dateeEmbauche
    date où a été embauché le visiteur
### competences
    liste des compétences propre à un visiteur qui définit les produits qu'il peut représenter
### inscription
    liste des séminaires pour lesquels le visiteur est inscrit
--
## Seminaire.cs

### id
    nombre généré qui est unique et propre à un séminaire
### produit
    produit présenté au séminaire
### debut
    date à laquelle se déroule le séminaire
### departement
    département dans lequel se déroule le séminaire
### ville
    ville dans laquelle se déroule le séminaire
--
## Produit.cs

### id
    nombre généré qui est unique et propre à un produit
### nom
    nom du produit présenté
--
## Database.cs

### Visiteur
    chemin vers le fichier json qui est la table visiteur
### Produit
    chemin vers le fichier json qui est la table produit
### Seminaire
    chemin vers le fichier json qui est la table séminaire
--
## MainWindow.xalm.cs
    programme correspondant à la l'application lancée où la principale partie du code est écrite.
### v_serial, v_deserial, p_serial, p_deserial, s_serial, s_deserial
    variables de type string qui permettent de récupérer des données (serial) ou d'en enregistrer (deserial) avec v pour visiteur, p pour produit et s_ pour séminaire.
### ObservableCollection <Visiteur> visiteur
    collection de visiteur pour créer une liste de login non visible dans l'application
### ObservableCollection <Produit> produit
    collection de produit pour créer une liste de produit visible suivant la personne connectée dans l'application
### ObservableCollection <Seminaire> séminaire
    collection de séminaire pour généré une liste de séminaire disponible suivant le produit
### ObservableCollection <Seminaire> inscription
    collection de séminaire pour généré une liste de séminaire où l'utilisateur est inscrit et qui est consultable suivant la personne
### loginCmd_Click
    procédure qui permet de se vérifier si la connexion est bien faite
### login()
    procédure qui permet de se connecter en cliquant sur le bouton correspondant
### b_inscription_Click
    procédure qui permet de s'inscrire au séminaire sélectionné
### b_annulation_Click
    procédure qui permet de se désinscrire d'un séminaire sélectionné
### b_deco_Click
    proccédure qui permet de se déconnecter de l'application
### lv_seminaire_SelectionChanged
    procédure qui aide à l'annulation d'un séminaire
--
## UniqId
    sert à générer un Id unique lors de l'enregistrement de données.
