{
  "info": {
    "name": "Vzaar API Get Api Videos Signature",
    "_postman_id": "4d6b8c6a-01f8-4cf9-adf5-1391a8eca369",
    "description": "nnThis API call allows a user to request a GUID and an AWS S3 signature. With these credentials the user will then be able upload a file into vzaar video storage area.nnThe response for this must be parsed and used in the Upload step. The upload will fail if any of these details are incorrect.nn",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Api",
      "item": [
        {
          "id": "d87dfafd-991a-4b70-80bd-670c0e51a9a5",
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
              "id": "7551a200-b628-4b30-b711-75acf13369b6"
            }
          ]
        },
        {
          "id": "b3a8ed78-852a-4f48-b277-5a61e45afacd",
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
              "id": "251d6b34-5f17-4c12-8806-9d43b129a755"
            }
          ]
        }
      ]
    }
  ]
}