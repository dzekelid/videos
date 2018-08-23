{
  "info": {
    "name": "Getty Images Search for creative videos",
    "_postman_id": "be876ac7-7a92-4849-83e7-18d855d9c356",
    "description": "Use this endpoint to search premium stock video, from archival film to contemporary 4K and HD footage.\r\n\r\nYou'll need an API key and access token to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)\r\npage for more information on how to sign up for an API key.\r\n\r\nYou can show different information in the response by specifying values on the \"fields\" parameter (see details below).\r\nYou can search with only an API key, and that will give you search results that are equivalent to doing a search on the GettyImages.com site without\r\nbeing logged in (anonymous search).  If you are a Getty Images API customer and would like to ensure that your API searches return only \r\nassets that you have a license to use, you need to also include an authorization token in the header of your request.\r\nPlease consult our [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html) for more information on authorization tokens.\r\n\r\n## Working with Fields Sets\r\n\r\nFields sets are used in the **fields** request parameter to receive a suite of metadata fields. The following fields sets are available:\r\n\r\n#### Summary Fields Set\r\n\r\nThe **summary_set** query string parameter fields value represents a small batch of metadata fields that are often used to build search\r\nresponse results. The following fields are provided for every video in your result set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\": \r\n    [\r\n        \"asset_family\", \r\n        \"caption\",\r\n        \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n            },\r\n            {\r\n                \"name\": \"thumb\"\r\n            }\r\n        ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n#### Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields value represents a large batch of metadata fields that are often used to build a \r\ndetailed view of videos. The following fields are provided for every video in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\": \r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n        \"asset_family\", \r\n        \"caption\", \r\n        \"clip_length\",\r\n        \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\", \r\n        \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n            },\r\n            {\r\n                \"name\": \"thumb\"\r\n            }\r\n        ],\r\n        \"era\",\r\n        \"license_model\",\r\n        \"mastered_to\",\r\n        \"originally_shot_on\",\r\n        \"product_types\",\r\n        \"shot_speed\",\r\n        \"source\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n#### Display Fields Set\r\n\r\nThe **display_set** query string parameter fields value represents the fields that provide you with URLs for the low resolution files \r\nthat are most frequently used to build a UI displaying search results. The following fields are provided for every video in your result \r\nset when you include **display_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n    [\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n            },\r\n            {\r\n                \"name\": \"thumb\"\r\n            }\r\n        ]\r\n    ]\r\n}\r\n```",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "images",
      "item": [
        {
          "id": "609188ac-9317-4742-bf7e-1f38334df127",
          "name": "Search_GetCreativeVideosByPhrase",
          "request": {
            "url": "http://api.gettyimages.com/v3/search/videos/creative?age_of_people=%7B%7D&collections_filter_type=%7B%7D&collection_codes=%7B%7D&exclude_nudity=%7B%7D&fields=%7B%7D&format_available=%7B%7D&frame_rates=%7B%7D&keyword_ids=%7B%7D&license_models=%7B%7D&page=%7B%7D&page_size=%7B%7D&phrase=%7B%7D&product_types=%7B%7D&sort_order=%7B%7D",
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
            "description": "Use this endpoint to search premium stock video, from archival film to contemporary 4K and HD footage"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5d642abd-462b-4ee1-be4a-42329f8308cd"
            }
          ]
        }
      ]
    }
  ]
}