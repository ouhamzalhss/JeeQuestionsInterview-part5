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
  *  Facile à appliquer agilité et TDD

- 6 .	Désavantages d’une application basée sur micro-services
  *  la communication entre les méthodes est plus lente, 
  *  plus difficiles à déboguer, et doivent être sécurisés.
  *  il y aura un effort supplémentaire pour les opérations, le déploiement, scaling, configuration, monitoring et les tests car chaque service est séparé.

- 7 . Les cas d'utilsation de l'architecture microservices: 
  *  Application très large.
  *  Besion de scaler l'application.
  *  Des grandes équipes.

- 8 .	Eureka Server ou service registry : Est un microservice technique qui enregistre la localisation des micro-services créer par Netflix :
  *  Nom de micro-service
  *  Adresse IP
  *  Port
  
  Pour l'implementer:
  *  ajouter la dépendance (spring-cloud-starter-netflix-eureka-server)
  *  ajouter cette annotation dans la classe main. @EnableEurekaServer	// Enable eureka server

- 9 .	Configuration service : Est un microservice qui centralise la configuration de tous les micro-services.

- 10 .	Proxy service : Dispatcher toutes les requêtes des clients vers les instances, donc il fait équilibrage de charge (load balancer)
  *  ZUUL : Est un proxy qui utilise un model multi threads avec IO bloquantes, Il agit comme un client eureka @EnableEurekaClient 		
et @EnableZuulProxy		pour activer ZUUL. (spring-cloud-starter-netflix-zuul)
  *  Spring cloud Gateway : Est un proxy qui utilise un Model single threads avec IO Non bloquantes

- 11 .	Spring Cloud : Projet Spring pour créer des applications microservices, fournit registration, configuration et Proxy service.

- 12 . Circuit breakers: permet d'éviter une défaillance sur le système. créer un système tolérant aux pannes et qui peut survivre sans problème lorsque les autres services sont indisponibles ou ont une latence élevée. Par exemple, si le service de catalogue de produits n'est pas disponible, alors l'UI peut récupérer la liste de produits dans le cache.

- 13 . Hystrix: C'est une implementation de Circuit breaker fournit par Netflix, qui donne un contrôle sur la latence et l'échec entre les services distribués. (spring-cloud-starter-hystrix)

- 14 . Spring Sleuth: est un outile qui va donner un ID unique à chaque requête à travers nos Microservices, de façon à pouvoir les suivre avec précision. (spring-cloud-starter-sleuth)

- 15 . Zipkin: Est une dépendence pour tracer et suivre des requêtes , C-à-d voir le chemin qu'une requête a parcouru afin de détecter où le problème s'est déclenché. (spring-cloud-sleuth-zipkin)

- 16 .	OpenFeign : Faire communiquer les micro-services distants en mode synchrone, et basé sur Ribbon pour faire l’équilibrage de charge.
       (spring-cloud-starter-openfeign)

- 17 . Pourquoi les conteneurs sont-ils utilisés dans les Microservices ? Parce que nous devons déployer beaucoup, et scaler notre microservice dans plusieurs machines.

- 18 . quelle est la signification de OAuth ?  un protocole d'autorisation permet à vos clients de créer un compte sur votre application web en se connectant sur un compte appartenant à une société vérifiée, comme Google, Facebook, Twitter, Okta ou GitHub...

- 20 .	Swagger : un projet open source qui offre des outils permettant de générer la documentation pour les API Web. Il offre également une interface permettant d’explorer et tester les différentes méthodes offertes par ces services.

- 21 .	MapStruct : Pour faire le mapping objet / objet ( DTO)

- 19 .	Base de données NoSql : Quand la quantité de données est très importante, exemple MongoDb
