# API Choice

- Étudiant :Nana Aichatou
- API choisie :CountAPI
- URL base :https://api.countapi.xyz
- Documentation officielle / README :https://countapi.xyz/
- Auth : None / API Key / OAuth
- Endpoints testés :
  - GET https://api.countapi.xyz/hit/demo/key
  - GET https://api.countapi.xyz/get/demo/key
- Hypothèses de contrat (champs attendus, types, codes) :La réponse de l’API est au format JSON et contient généralement les champs suivants :

namespace : chaîne de caractères (string) qui représente l’espace de nom utilisé
key : chaîne de caractères (string) qui identifie le compteur
value : entier (integer) correspondant au nombre de fois que l’endpoint a été appelé (nombre de “hits”)

Exemple de réponse JSON :

{
"namespace": "demo",
"key": "key",
"value": 12
}
- Limites / rate limiting connu :API gratuite et publique
Pas de limite officiellement stricte documentée
Mais peut être instable si trop utilisée (service non garanti)
- Risques (instabilité, downtime, CORS, etc.) :Pas de garantie de disponibilité (service gratuit)
Possible downtime (API éducative / simple compteur public)
Données non sécurisées (tout le monde peut modifier les compteurs)
CORS généralement autorisé, mais dépend du navigateur / contexte
Pas adapté à un projet critique ou production
