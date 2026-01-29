# Pattern d'architecture

## Monolithe
Application réaliser en unité indivisible (un package).  
Toutes les fonctionnalités sont dans un même process !

**Avantage** : 
- Structure simple
- Performence élévé (Pas de communication - Pas de dépendence)

**Inconvénient** : 
- Complexe à faire évolué
- Debug plus long

## Couches
Séparé les responsabilités en package indépendent.  
Quelques exemples :  
 → [3 tiers (APP, BLL, DAL)](./ressources/pattern_3tiers.png)  
 → [3 tiers + Domain](./ressources/pattern_3tiers+domain.png)  
 → [Clean Architecture](./ressources/pattern_clean_architecture_(Simple).png)

**Avantage** : 
- Maintenance et évolution plus simple
- Séparation des préocupations
- Réutilisation possible
- Possibilité des tester une couche individuellement

**Inconvénient** : 
- Plus complexe (Work flow)
- Performance potentiellement réduite

## Micro-Service
Décomposition de l'application en un ensemble de service indépendent et autonome.  
La communication entre les services peut être réaliser par : 
- Distributed event store and streaming : `Kafka`
- Message Broker : `RabbitMQ`, `ActiveMQ` 
- RestFull WebAPI **[Non recommandé !]**

**Avantage** : 
- Découplage des services
- Meilleur performance (Gestion de la charge des services indiduellement)
- Maintenance partiel possible (Couper un service, mais le reste tourne)

**Inconvénient** : 
- Mise en place beaucoup plus complexe (Chaque service → Un projet !) 
- Point de défaillance critique possible → Le systeme de communication