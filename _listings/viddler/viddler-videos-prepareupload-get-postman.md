{
  "info": {
    "name": "Viddler  API Videos PrepareUpload",
    "_postman_id": "9e8215cd-e3b7-4edd-85af-71efa324fe2c",
    "description": "Returns the end-point and token for a new upload session.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Viddler",
      "item": [
        {
          "id": "7f524fa2-f130-4352-844f-cf9e6e6c4bd9",
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
              "id": "57f9ef89-ff36-46e4-83cb-c3b1771d726a"
            }
          ]
        },
        {
          "id": "e1dfeadc-1fa2-4ace-bc84-e23f046bfcce",
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
              "id": "7b10df2d-849c-4387-9598-7543391fa0ed"
            }
          ]
        },
        {
          "id": "153c5029-28ac-41a4-bc60-507aa95075fe",
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
              "id": "13bd0b18-32fa-4467-95ac-368b6cfbcef5"
            }
          ]
        },
        {
          "id": "d57362be-6bfa-40de-bab4-7bab3a12e2fb",
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
              "id": "8a538b1c-7999-4811-9bfb-95ae665a1bd0"
            }
          ]
        },
        {
          "id": "056a8095-9d4d-412d-abce-77847e81594e",
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
              "id": "22abca43-4a83-4cd0-8071-b46d5a8aaa30"
            }
          ]
        },
        {
          "id": "573b8ad4-9ab9-46b3-b2c6-74c8260b0841",
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
              "id": "95a91b17-757c-457e-957f-fe5ea0ee8ecf"
            }
          ]
        },
        {
          "id": "05ccc007-c1d1-44fd-b3c8-4c8f2eb2c5ca",
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
              "id": "557c80cc-9396-45a4-abf2-6941bff0b3a6"
            }
          ]
        },
        {
          "id": "a329f1ca-5174-4c69-ae6b-d326a6d2fc76",
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
              "id": "23d05b3b-6262-4f04-bd6e-f75fc500bf86"
            }
          ]
        },
        {
          "id": "94d0fe4d-511c-44a9-bcd3-caabfb2af61f",
          "name": "videos-prepareupload",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.prepareUpload?allow_replace=%7B%7D&sessionid=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the end-point and token for a new upload session."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "77d61d0a-80e4-4fd8-ad06-4e22f3d1d1ec"
            }
          ]
        }
      ]
    }
  ]
}