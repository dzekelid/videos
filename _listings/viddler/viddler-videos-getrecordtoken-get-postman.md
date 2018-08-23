{
  "info": {
    "name": "Viddler  API Videos GetRecordToken",
    "_postman_id": "21ee4340-aeb1-4b52-a54a-f3d01d05e83e",
    "description": "Return a record token to use with Viddler&#8217;s Flash video recorder.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Viddler",
      "item": [
        {
          "id": "a75ac7c2-0111-4889-9c05-59c3a22eccac",
          "name": "videos-addclosedcaptioning",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.addClosedCaptioning?closed_captioning_url=%7B%7D&default=%7B%7D&language=%7B%7D&sessionid=%7B%7D&video_id=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Add new closed captioning file for a specific video. All uploaded closed captioning files are enabled by default. The first uploaded file is default for a video."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2712a1f3-1fda-4d8d-81e3-202d3fae10cc"
            }
          ]
        },
        {
          "id": "1a8f1828-d6e1-4e51-b1bc-1d9aab917593",
          "name": "videos-comments-get",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.comments.get?page=%7B%7D&parent_id=%7B%7D&per_page=%7B%7D&sessionid=%7B%7D&video_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get comments for a video. If logged in and querying comments for own video &#8211; all comments with any moderation status will be returned. If quering comments as logged out or for not owned video &#8211; only approved comments will be returned if the video itself is public."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f191ca4e-17d7-411f-9170-635c1d80af22"
            }
          ]
        },
        {
          "id": "c0ce7df6-a4b7-4e61-8292-c788c8013123",
          "name": "videos-delclosedcaptioning",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.delClosedCaptioning?closed_captioning_id=%7B%7D&sessionid=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Remove an existing closed captioning file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "77db77de-4f61-4ee4-aeaf-7f44b482a9b0"
            }
          ]
        },
        {
          "id": "5da55d49-6205-48b1-849a-0a955b58fc84",
          "name": "videos-delete",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.delete?sessionid=%7B%7D&video_id=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a video."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ddc6376-2649-4ff2-974d-1aa588b5fec6"
            }
          ]
        },
        {
          "id": "f7aed369-d9f3-4231-8396-a6096de98481",
          "name": "videos-enableads",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.enableAds?sessionid=%7B%7D&video_ids=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Turn ads off for specified videos."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a6cc19c9-05ec-48d1-a562-4e723b0434f0"
            }
          ]
        },
        {
          "id": "0e764ab6-905b-4f36-affb-9c67dee69419",
          "name": "videos-getadsstatus",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.getAdsStatus?sessionid=%7B%7D&video_id=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "viddler.videos.getAdsStatusnGET"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "892a58df-6094-4c71-9ffc-6cde493baccf"
            }
          ]
        },
        {
          "id": "d6bf8f9b-5089-42da-94f1-442cac8701c0",
          "name": "videos-getembedcodetypes",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.getEmbedCodeTypes?sessionid=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a list of the embed code types for your account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c769ffe3-d24f-4c61-8024-e9171a0f8583"
            }
          ]
        },
        {
          "id": "92c91645-b9da-4562-8c04-bf659b0d58d5",
          "name": "videos-getrecordtoken",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.getRecordToken?sessionid=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a record token to use with Viddler&#8217;s Flash video recorder."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "86e2b910-371b-4ebf-be6d-99ebe1473d0f"
            }
          ]
        }
      ]
    }
  ]
}