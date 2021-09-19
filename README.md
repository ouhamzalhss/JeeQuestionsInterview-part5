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

- 7 .	Registration service (Eureka) : Est un microservice qui enregistre la localisation des micro-services créer par Netflix :
  *  Nom de micro-service
  *  Adresse IP
  *  Port

- 8 .	Configuration service : Est un microservice qui centralise la configuration de tous micro-services.

- 9 .	Proxy service : Dispatcher toutes les requêtes des clients vers les instances, donc il fait équilibrage de charge (load balancer)
  *  ZUUL : Model multi threads avec IO bloquantes
  *  Spring cloud Gateway : Model single threads avec IO Non bloquantes

- 10 .	Spring Cloud : Projet Spring pour créer des applications microservices, fournit registration, configuration et Proxy service.

- 11 . Circuit breakers: permet d'éviter une défaillance sur le système. créer un système tolérant aux pannes et qui peut survivre sans problème lorsque les autres services sont indisponibles ou ont une latence élevée. Par exemple, si le service de catalogue de produits n'est pas disponible, alors l'UI peut récupérer la liste de produits dans le cache.

- 12 . Hystrix: C'est une implementation de Circuit breaker fournit par Netflix. (spring-cloud-starter-hystrix)

- 13 . Spring Sleuth: est un outile qui va donner un ID unique à chaque requête à travers nos Microservices, de façon à pouvoir les suivre avec précision. (spring-cloud-starter-sleuth)

- 14 . Zipkin: Est une dépendence pour tracer et suivre des requêtes , C-à-d voir le chemin qu'une requête a parcouru afin de détecter où le problème s'est déclenché. (spring-cloud-sleuth-zipkin)

- 15 .	OpenFeign : Faire communiquer les micro-services distants en mode synchrone, et basé sur Ribbon pour faire l’équilibrage de charge.
       (spring-cloud-starter-openfeign)

- 16 . Pourquoi les conteneurs sont-ils utilisés dans les Microservices ? Parce que nous devons déployer beaucoup, et scaler notre microservice dans plusieurs machines.

- 17 . quelle est la signification de OAuth ?  un protocole d'autorisation permet à vos clients de créer un compte sur votre application web en se connectant sur un compte appartenant à une société vérifiée, comme Google, Facebook, Twitter, Okta ou GitHub...

- 18 .	Base de données NoSql : Quand la quantité de données est très importante, exemple MongoDb

- 19 .	Swagger : faire documenter les services web.

- 20 .	MapStruct : Pour faire le mapping objet / objet ( DTO)
