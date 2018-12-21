# Cours FULL STACK - Blog Front End VueJS
## Contexte
Dans le cadre d'un projet Full Stack, il fallait réaliser un blog en VueJS, dans un premier temps le Front et par la suite le Back.  Les participants à ce projet sont : Loublier Paul et Verlaine Juliette
## Specs
### Organisation des données
La base de données comprend 3 tables :

 - User
 - Comments
 - Articles

Un utilisateur peut créer un ou plusieurs articles.
Un utilisateur peut commenter un ou plusieurs articles.
Un commentaire appartient à un utilisateur et à un article.
Un article appartient à un utilisateur et peut être commenté à plusieurs reprises.

Des utilisateurs non authentifiés peuvent être amené à commenté avec un login unique : Visiteur.

Modèle JSON :

    {
       '_comment' : "User"
      'id_user': Number,
      'name': String,
      'firstName': String,
      'addres': String,
      'login': String,
      'password': String,
      'picture': String
    }

    {

       '_comment' : "Comment"
      'id_comment' : Number,
      'id_author' : Number,
      'name_author' : String,
      'contains' : String,
      'picture_author' : String,
     'dateComment' : Date,
      'id_article' : Number

    }

    {
       '_comment' : "Article"
      'id_article': Number,
      'title' : String,
      'category' : String,
      'contains' : String,
      'picture' : String,
      'author' : String,
      'author_id' : Number,
     'datePost': Date,
      'numberView' : Number

    }


### Features
L'API n'était pas développée à ce jour, les données sont décrites dans un fichier js et chargées directement sur le Front.
L'utilisateur peut accéder au blog et commenter sans être connecté. Dans ce cas, le nom de l'utilisateur sera par défaut visiteur. L'utilisateur peut sinon s'authentifier s'il est en enregistré ou dans le cas contraire, s'enregistrer et poster des commentaires de façon nominative.
L'utilisateur peut rechercher dans les articles selon son titre, sa catégorie ou bien l'auteur. La page des articles n'en affichent que 5 par page. La barre de navigation permet de lister la totalité des articles ou bien de récupérer l'un des 5 derniers récemment postés.

L'utilisateur ne peut pas encore à ce jour :

 - Editer son profil
 - Editer ses articles
 - Créer un nouvel article

### Développement
Le Front est développé en VueJS.

## Pour la suite
Le Back reste à développer ainsi que l'API pour gérer les données.
