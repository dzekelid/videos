{
  "info": {
    "name": "Vzaar API Post Api Videos",
    "_postman_id": "cc071178-4b31-4bb2-882a-8c1b4d5a0f9f",
    "description": "nnThis API call tells the vzaar system to process a newly uploaded video. This will encode it if necessary and then provide a vzaar video idea back.nn",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Api",
      "item": [
        {
          "id": "a70232cb-2728-416b-a5b2-323f78507536",
          "name": "postApiVeos",
          "request": {
            "url": "http://vzaar.com/api/videos?description=%7B%7D&guid=%7B%7D&labels=%7B%7D&profile=%7B%7D&replace_id=%7B%7D&title=%7B%7D&transcoding=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "nnThis API call tells the vzaar system to process a newly uploaded video. This will encode it if necessary and then provide a vzaar video idea back.nn"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee1f8990-f191-4698-802c-c8e5eec9a098"
            }
          ]
        }
      ]
    }
  ]
}