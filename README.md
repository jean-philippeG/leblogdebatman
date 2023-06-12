# Projet Le Blog de Batman

### Cloner le projet

```
git clone https://github.com/jean-philippeG/leblogdebatman.git
```

### Déplacer le terminal dans le dossier cloné
```
cd leblogdebatman
```

### Installer les vendors (pour recréer le dossier vendor)
```
composer install
```

### Création BDD
Configurer la connexion à la BDD dans le fichier .env (voir le cours), puis taper les commandes suivantes :
```
symfony console doctrine:database:create
symfony console doctrine:migrations:migrate
```

### Cration des fixtures (fichier AppFixtures.php)
```
symfony console doctrine:fixtures:load
```
Cette commande créera :
* un compte ADMIN (email: batman@batman.bt, password: 'Azert#123'')
* 10 comptes USER (email aléatoire, password: 'Azert#123'')
* 50 articles

### Installation fichiers front-end des bundles (CKEditor)
```
symfony console assets:install public
```

### Lancer le serveur
```
symfony serve
```