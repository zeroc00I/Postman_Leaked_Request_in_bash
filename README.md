# Postman Leaked Requests and secrets (Bash version)

1. Busca por IDs de solicitação com a palavra-chave fornecida:

curl -X POST -H "Content-Type: application/json" -d '{"service": "search", "method": "POST", "path": "/search-all", "body": {"queryIndices": ["runtime.request"], "queryText": "keyword_here", "size": 100, "from": 0, "requestOrigin": "srp", "mergeEntities": "true", "nonNestedRequests": "true"}}' https://www.postman.com/_api/ws/proxy

2. Recupera informações de solicitação com base nos IDs encontrados:

curl -X GET https://www.postman.com/_api/request/10017341-25fb3a00-e70c-4210-b56e-c0d31125d676
