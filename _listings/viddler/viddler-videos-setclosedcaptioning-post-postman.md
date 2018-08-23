{
  "info": {
    "name": "Viddler  API Videos SetClosedCaptioning",
    "_postman_id": "3555c10a-86bf-4d9b-ab48-b42c7f26ad8d",
    "description": "Update closed captioning details on a previously uploaded file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Viddler",
      "item": [
        {
          "id": "744b9d42-09db-4f3c-807e-1357ba425681",
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
              "id": "cf1ead27-d7bd-4819-8916-39ef79b452c6"
            }
          ]
        },
        {
          "id": "7166ed3e-eb11-4836-a43d-38dd5ab6b988",
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
              "id": "a20313aa-ccf0-46cc-9020-0760a8261178"
            }
          ]
        },
        {
          "id": "eb2db672-c381-43bc-af78-4187cd1894b4",
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
              "id": "769fc908-cfd7-4114-8097-48ed035283f5"
            }
          ]
        },
        {
          "id": "54580316-cc39-4520-8e56-e3d1d30c3e97",
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
              "id": "df87dd5c-87c2-4a96-9f96-cea8710ba292"
            }
          ]
        },
        {
          "id": "6f6265a4-2738-4ca9-a64f-b00559c5268d",
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
              "id": "f3040a24-42e7-4173-8233-96e908558cac"
            }
          ]
        },
        {
          "id": "29574b13-225a-4ce7-8296-49551df90fba",
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
              "id": "731e4162-4df5-4971-ad93-9a1200f85073"
            }
          ]
        },
        {
          "id": "04164aed-7710-4772-9f1f-42223e875057",
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
              "id": "cbd656a1-19bc-4c65-9a4e-43b11506a688"
            }
          ]
        },
        {
          "id": "3e510073-f970-4d3d-85e8-3497c004be0d",
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
              "id": "7f7c8b0a-9cc4-4b34-9ed4-d7715209e30d"
            }
          ]
        },
        {
          "id": "85f1bf33-f380-439c-8c88-29ae47bfe608",
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
              "id": "75fd9aab-17d3-44a6-92be-3c8d7c9bdd10"
            }
          ]
        },
        {
          "id": "87003317-80b5-4aa3-8e0d-af764f552c1f",
          "name": "videos-setclosedcaptioning",
          "request": {
            "url": "http://api.viddler.com/api/v2/viddler.videos.setClosedCaptioning?closed_captioning_id=%7B%7D&default=%7B%7D&enabled=%7B%7D&language=%7B%7D&sessionid=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Update closed captioning details on a previously uploaded file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6cc3430e-9813-4428-bbd8-ee402b414fdc"
            }
          ]
        }
      ]
    }
  ]
}