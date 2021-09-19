## <samp>Les Questions pour un entretien profile JAVA/JEE!</samp>

#### Partie 6: Micro-services

- 1 .	Deux architectures :
  *  Architecture basé sur une application monolithique 
  *  Architecture basé sur les micro-services.

- 2 .	Application monolithique : est une application qui est développée en un seul bloc ( jar, war )  avec une seule technologie. et déployée d’une manière unitaire dans un serveur d’application.

- 3 .	Problèmes d’une application monolithique : 
  *  Centralise tous les besoins fonctionnels
  *  Est réalisée dans une seule technologie. 
  *  Chaque modification nécessite la redéployèrent de toute application.
  *  Livraison en bloc, client attend beaucoup de temps pour commencer à voir les premières versions.

- 4 .	Les micro-services sont une approche d’architecture et de développement d’une application composée de petits services. L’idée étant de découper un grand problème en petites unités implémentée sous forme de micro-services.

- 5 .	Avantages d’une application basée sur micro-services
  *  Performances
  *  Redéploiement à chaud
  *  Technologies différents
  *  Equipes indépendantes
  * 	Facile à appliquer agilité et TDD

- 6 . Les cas d'utilsation de l'architecture microservices: 
  *  Application très large.
  *  Besion de scaler l'application.
  *  Des grandes équipes.

- 7 .	Registration service : enregistrer la localisation des micro-services :
  *  Nom de micro-service
  *  Adresse IP
  *  Port

- 8 .	Configuration service : centraliser la configuration de tous micro-services.

- 9 .	Proxy service : Dispatcher toutes les requêtes des clients vers les instances, donc il fait équilibrage de charge (load balancer)
  *  ZUUL : Model multi threads avec IO bloquantes
  *  Spring cloud Gateway : Model single threads avec IO Non bloquantes

- 10 .	Spring Cloud : Projet Spring pour créer des applications microservices, fournit registration, configuration et Proxy service.

- 11 . Circuit breakers:

- 11 . hestrix:

- 12 . Zipkin: 

- 12 .	OpenFeign : Faire communiquer les micro-services distants en mode synchrone, et basé sur Ribbon pour faire l’équilibrage de charge.

- 13 . Pourquoi les conteneurs sont-ils utilisés dans les Microservices ? Parce que nous devons déployer beaucoup, et scaler notre microservice dans plusieurs machines.

- 14 . quelle est la signification de OAuth ?  un protocole d'autorisation permet à vos clients de créer un compte sur votre application web en se connectant sur un compte appartenant à une société vérifiée, comme Google, Facebook, Twitter, Okta ou GitHub...

- 13 .	Base de données NoSql : Quand la quantité de données est très importante, exemple MongoDb

- 14 .	Swagger : faire documenter les services web.

- 15 .	MapStruct : Pour faire le mapping objet / objet ( DTO)
