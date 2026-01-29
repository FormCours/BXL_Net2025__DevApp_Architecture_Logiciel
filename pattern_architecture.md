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

