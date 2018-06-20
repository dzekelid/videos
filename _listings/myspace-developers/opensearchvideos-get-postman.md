{
  "info": {
    "name": "My Space Get Opensearch Veos",
    "_postman_id": "b234e566-587f-4f84-9922-719297fbb1b9",
    "description": "Returns search results for videos.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Opensearch",
      "item": [
        {
          "id": "0adc63bb-960f-4da9-834d-11091fb0a640",
          "name": "opensearch.videos.get",
          "request": {
            "url": "http://api.myspace.com/opensearch/videos?count=%7B%7D&culture=%7B%7D&format=%7B%7D&searchTerms=%7B%7D&startPage=%7B%7D&tag=%7B%7D&videoMode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns search results for videos."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b65f8e14-21db-48da-ad57-a3e1414345a2"
            }
          ]
        }
      ]
    }
  ]
}