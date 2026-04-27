# API Choice

- Étudiant :Nana Aichatou
- API choisie :ipify
- URL base :https://api.ipify.org
- Documentation officielle / README :https://www.ipify.org/
- Auth : None / API Key / OAuth
- Endpoints testés :
  - GET https://api.ipify.org?format=json
  - GET https://api.ipify.org
- Hypothèses de contrat (champs attendus, types, codes) :Réponse JSON attendue :
ip : string (ex: "82.123.45.67")
Codes HTTP :
200 OK → succès
400 Bad Request → paramètres invalides (rare ici)
Format possible : json, text, jsonp selon paramètre format
- Limites / rate limiting connu :Pas de limite officielle stricte annoncée
Usage raisonnable recommandé (éviter les appels en boucle massive)
Peut être temporairement bloqué si abus (rate limiting implicite)
- Risques (instabilité, downtime, CORS, etc.) :Service dépendant d’un service externe (donc possible downtime)
Pas garanti à 100% pour production critique
CORS généralement OK pour usage navigateur
Risque faible mais existant de limitation si trafic abusif
Réponse très simple → peu de risques techniques côté parsing
