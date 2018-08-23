{
  "info": {
    "name": "Viddler  API Videos EnableAds",
    "_postman_id": "a043ae57-476b-4923-b802-624b52eb50a4",
    "description": "Turn ads off for specified videos.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Viddler",
      "item": [
        {
          "id": "48fd32de-e88a-47bc-8301-c4865c67f344",
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
              "id": "d70a322c-9521-44c1-b9ff-19d546018c33"
            }
          ]
        },
        {
          "id": "7f61d718-3c53-44c0-8c95-34fcaa7c085a",
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
              "id": "309dd789-5e79-45c7-bc73-eb892772c203"
            }
          ]
        },
        {
          "id": "f457d8f2-457d-4024-94f3-7ade6fbc2aea",
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
              "id": "dc262bf3-3e8c-42de-a4b6-33fa0d19f366"
            }
          ]
        },
        {
          "id": "17a71dc6-169d-4b09-beac-eb544ebd72c7",
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
              "id": "db44fd06-5617-4a49-ae49-75ea9eb9d332"
            }
          ]
        },
        {
          "id": "fafea57d-9ed6-457a-bf49-5fdb4a9b403f",
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
              "id": "6fd59112-2a80-4aae-8dc4-3fc3f6494671"
            }
          ]
        }
      ]
    }
  ]
}