{
  "info": {
    "name": "Getty Images",
    "_postman_id": "108d2cdd-2ee0-4e2d-9bec-56e6438ffc12",
    "description": "Build applications using the world's most powerful imagery",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "images",
      "item": [
        {
          "id": "b813247b-16db-45e2-9f1f-2ba6a9b405a5",
          "name": "Artists_GetVideosByArtist",
          "request": {
            "url": "http://api.gettyimages.com/v3/artists/videos?artist_name=%7B%7D&fields=%7B%7D&page=%7B%7D&page_size=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept-Language",
                "value": "{}",
                "description": "Provide a header to specify the language of result values",
                "disabled": false
              },
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Provide access token in the format of 'Bearer {token}'",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search for videos by a photographer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d79800e7-9d9f-4096-8dc4-732ca29c5850"
            }
          ]
        }
      ]
    }
  ]
}