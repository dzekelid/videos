{
  "info": {
    "name": "Getty Images Search for editorial videos",
    "_postman_id": "090bdf3c-4dc1-479e-93d9-2e09d1fbe357",
    "description": "Use this endpoint to search current and archival video clips of celebrities, newsmakers, and events.\r\n\r\nYou'll need an API key and access token to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html) page for more information on how to sign up for an API key.\r\n\r\nYou can show different information in the response by specifying values on the \"fields\" parameter (see details below).\r\nYou can search with only an API key, and that will give you search results that are equivalent to doing a search on the GettyImages.com site without being logged in (anonymous search).  If you are a Getty Images API customer and would like to ensure that your API searches return only assets that you have a license to use, you need to also include an authorization token in the header of your request.  Please consult our [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html) for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md) for code examples of getting a token.\r\n\r\n## Working with Fields Sets\r\n\r\nFields sets are used in the **fields** request parameter to receive a suite of metadata fields. The following fields sets are available:\r\n\r\n#### Summary Fields Set\r\n\r\nThe **summary_set** query string parameter fields value represents a small batch of metadata fields that are often used to build search response results. The following fields are provided for every video in your result set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\": \r\n    [\r\n        \"asset_family\", \r\n        \"caption\",\r\n        \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n            },\r\n            {\r\n                \"name\": \"thumb\"\r\n            }\r\n        ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n#### Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields value represents a large batch of metadata fields that are often used to build a detailed view of videos. The following fields are provided for every video in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\": \r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n        \"asset_family\", \r\n        \"caption\", \r\n        \"clip_length\",\r\n        \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\", \r\n        \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n            },\r\n            {\r\n                \"name\": \"thumb\"\r\n            }\r\n        ],\r\n        \"era\",\r\n        \"license_model\",\r\n        \"mastered_to\",\r\n        \"originally_shot_on\",\r\n        \"product_types\",\r\n        \"shot_speed\",\r\n        \"source\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n#### Display Fields Set\r\n\r\nThe **display_set** query string parameter fields value represents the fields that provide you with URLs for the low resolution files that are most frequently used to build a UI displaying search results. The following fields are provided for every video in your result set when you include **display_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n    [\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n            },\r\n            {\r\n                \"name\": \"thumb\"\r\n            }\r\n        ]\r\n    ]\r\n}\r\n```\r\n\r\n## Request Usage Considerations\r\n\r\n- Specifying the \"entity_details\" response field can have significant performance implications. The field should be used only when necessary.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "images",
      "item": [
        {
          "id": "f339d092-f548-4ff2-bdbb-10a0d2c07b6a",
          "name": "Search_GetEditorialVideosByPhrase",
          "request": {
            "url": "http://api.gettyimages.com/v3/search/videos/editorial?age_of_people=%7B%7D&collections_filter_type=%7B%7D&collection_codes=%7B%7D&editorial_video_types=%7B%7D&entity_uris=%7B%7D&exclude_nudity=%7B%7D&fields=%7B%7D&format_available=%7B%7D&frame_rates=%7B%7D&keyword_ids=%7B%7D&page=%7B%7D&page_size=%7B%7D&phrase=%7B%7D&product_types=%7B%7D&sort_order=%7B%7D&specific_people=%7B%7D",
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
            "description": "Use this endpoint to search current and archival video clips of celebrities, newsmakers, and events"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b7eaf8c-ee29-464e-ab7f-b89a5b2fff1d"
            }
          ]
        }
      ]
    }
  ]
}