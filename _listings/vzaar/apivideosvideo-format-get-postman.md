{
  "info": {
    "name": "Vzaar API Get Api Videos",
    "_postman_id": "0500a89d-ce11-4094-9f0b-807d14d41b84",
    "description": "nnvzaar uses the oEmbed open standard for allowing 3rd parties to integrated with the vzaar. You can use the vzaar video URL to easily obtain the appropriate embed code for that video. To find out more about oEmbed view the specification here: http://oembed.com/nn",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Api",
      "item": [
        {
          "id": "c6678a99-745e-42b2-9dda-b99cd4853ce4",
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
              "id": "c34d419a-2f9d-46c4-a80e-01b7f73f744e"
            }
          ]
        },
        {
          "id": "f80aa54e-bf90-4c13-a100-4be7c9aa4277",
          "name": "getApiVeosSignature",
          "request": {
            "url": "http://vzaar.com/api/videos/signature?flash_request=%7B%7D&max_file_size=%7B%7D&success_action_redirect=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "nnThis API call allows a user to request a GUID and an AWS S3 signature. With these credentials the user will then be able upload a file into vzaar video storage area.nnThe response for this must be parsed and used in the Upload step. The upload will fail if any of these details are incorrect.nn"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f659e46a-94e3-41f8-814f-7492045c75af"
            }
          ]
        },
        {
          "id": "f467db90-1026-4e66-89a3-3d2cda291a54",
          "name": "getApiVeosVeo.Format",
          "request": {
            "url": {
              "protocol": "http",
              "host": "vzaar.com",
              "path": [
                "api/videos/:video.json"
              ],
              "query": [
                {
                  "key": "borderless,",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "embed_only,",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "videos is the vzaar video number for that video.",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "video",
                  "value": "video",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "nnvzaar uses the oEmbed open standard for allowing 3rd parties to integrated with the vzaar. You can use the vzaar video URL to easily obtain the appropriate embed code for that video. To find out more about oEmbed view the specification here: http://oembed.com/nn"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3278f489-d258-4501-a048-638fc595867a"
            }
          ]
        }
      ]
    }
  ]
}