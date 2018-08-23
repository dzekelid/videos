{
  "info": {
    "name": "Viddler  API Videos GetAdsStatus",
    "_postman_id": "061fb765-cab4-48bb-a886-910eb8d1749e",
    "description": "viddler.videos.getAdsStatusnGET",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Viddler",
      "item": [
        {
          "id": "e9687757-6856-4940-9310-c1bd8d74941c",
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
              "id": "e1400827-d67c-426c-8c57-acb572fc5cc3"
            }
          ]
        },
        {
          "id": "7dd5be65-364a-4364-9610-f07e3c6f1d48",
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
              "id": "007cac36-8c83-48b2-a208-274abd814011"
            }
          ]
        },
        {
          "id": "e6ac0c8d-fcb6-4c50-a76c-8709cf1a996a",
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
              "id": "319391ac-289b-4efa-a141-6d67f6e8c6aa"
            }
          ]
        },
        {
          "id": "75351361-2f35-40ef-bbb5-ea41024dab66",
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
              "id": "d223ab67-e818-41bc-915c-6f84235ad38e"
            }
          ]
        },
        {
          "id": "ffccc1c9-1d1b-42f2-9754-68b38804458b",
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
              "id": "72309a9f-7c5e-4926-8699-e66465d3d4e7"
            }
          ]
        },
        {
          "id": "7a57f967-751d-4cd5-a0af-22b0d43e3c47",
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
              "id": "cc3b243a-1a80-42dc-953e-281188f91aca"
            }
          ]
        }
      ]
    }
  ]
}