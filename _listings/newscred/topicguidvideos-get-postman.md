{
  "info": {
    "name": "News Cred Topic Videos",
    "_postman_id": "dcbb2606-06e2-4c88-b7d3-fbcf7b938960",
    "description": "Returns a list of videos related to the specified topic.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "News",
      "item": [
        {
          "id": "94a69d59-be9b-4dbb-8103-e23baf2ef951",
          "name": "getTopicGu]Articles",
          "request": {
            "url": "http://api.newscred.com/topic/{guid]/articles/?access_key=%7B%7D&article_filter_mode=%7B%7D&article_filter_name=%7B%7D&categories=%7B%7D&from_date=%7B%7D&get_topics=%7B%7D&guid=%7B%7D&has_images=%7B%7D&languages=%7B%7D&licensed=%7B%7D&media_types=%7B%7D&offset=%7B%7D&pagesize=%7B%7D&sort=%7B%7D&sources=%7B%7D&source_countries=%7B%7D&source_filter_mode=%7B%7D&source_filter_name=%7B%7D&to_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of articles related to the specified topic."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2b76e5ca-1717-456a-ba05-37b081d92824"
            }
          ]
        },
        {
          "id": "8e42854d-4a30-43e5-a0f4-9a4b699471d8",
          "name": "getArticles",
          "request": {
            "url": "http://api.newscred.com/articles/?access_key=%7B%7D&article_filter_mode=%7B%7D&article_filter_name=%7B%7D&boolean_operator=%7B%7D&categories=%7B%7D&exact=%7B%7D&from_date=%7B%7D&get_topics=%7B%7D&has_images=%7B%7D&languages=%7B%7D&licensed=%7B%7D&links=%7B%7D&max_length=%7B%7D&media_types=%7B%7D&min_length=%7B%7D&mm=%7B%7D&modified_since=%7B%7D&offset=%7B%7D&query=%7B%7D&query_fields=%7B%7D&safe_search=%7B%7D&sort=%7B%7D&sources=%7B%7D&source_countries=%7B%7D&source_filter_mode=%7B%7D&source_filter_name=%7B%7D&topics=%7B%7D&topic_filter_mode=%7B%7D&topic_filter_name=%7B%7D&to_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of articles according to the specified set of parameters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6d06ff7e-23f0-481e-9dd4-2a6b64fa8562"
            }
          ]
        },
        {
          "id": "df34694f-9855-4654-9337-48bb0efb21cc",
          "name": "getAuthorGuArticles",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "author/:guid/articles/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "article_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "article_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "categories",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "get_topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "has_images",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "languages",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "licensed",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "media_types",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sources",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "source_countries",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "source_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "source_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to_date",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns articles written by the specified author and matching the given query string."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b06b4fdc-7277-4d1e-8472-9ce0fc355ac4"
            }
          ]
        },
        {
          "id": "024ddbb6-0bf0-4564-95b4-185860c98576",
          "name": "getAuthorGuTopics",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "author/:guid/topics/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_classifications",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_subclassifications",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to_date",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of topics related to an author."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f192487f-a3aa-4487-97d6-1a35c62e595b"
            }
          ]
        },
        {
          "id": "c796d988-90c1-48c6-8deb-9c5b67a3c6ba",
          "name": "getCategories",
          "request": {
            "url": "http://api.newscred.com/categories/?access_key=%7B%7D&autosuggest=%7B%7D&query=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search for categories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "858dc14d-bda1-42b4-8f80-8a573a21d503"
            }
          ]
        },
        {
          "id": "81a7b0d3-4c86-4c4d-8ccc-0cfa8b9f3b74",
          "name": "getCategoryDashedNameSources",
          "request": {
            "url": "http://api.newscred.com/category/dashed-name/sources/?access_key=%7B%7D&from_date=%7B%7D&media_types=%7B%7D&offset=%7B%7D&pagesize=%7B%7D&sources=%7B%7D&source_countries=%7B%7D&source_filter_mode=%7B%7D&source_filter_name=%7B%7D&to_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of sources that write most frequently about the category specified by the dashed name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1cbdf848-41e1-400e-879d-a8b20c38b33f"
            }
          ]
        },
        {
          "id": "559fabd2-1017-4299-83fc-a1d8803026d0",
          "name": "getCategoryDashedNameTopics",
          "request": {
            "url": "http://api.newscred.com/category/dashed-name/topics/?access_key=%7B%7D&from_date=%7B%7D&offset=%7B%7D&pagesize=%7B%7D&topic_classifications=%7B%7D&topic_filter_mode=%7B%7D&topic_filter_name=%7B%7D&topic_subclassifications=%7B%7D&to_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of topics within the category specified by the dashed name."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14e3fc35-391d-4458-ae5f-25f10506ee04"
            }
          ]
        },
        {
          "id": "992f8007-07cb-4f5d-b662-1468dfc9f4d5",
          "name": "getCategoryCategoryName]Stories",
          "request": {
            "url": "http://api.newscred.com/category/{category-name]/stories/?access_key=%7B%7D&article_filter_mode=%7B%7D&article_filter_name=%7B%7D&cluster_size=%7B%7D&from_date=%7B%7D&get_topics=%7B%7D&has_images=%7B%7D&languages=%7B%7D&licensed=%7B%7D&media_types=%7B%7D&offset=%7B%7D&pagesize=%7B%7D&sources=%7B%7D&source_countries=%7B%7D&source_filter_mode=%7B%7D&source_filter_name=%7B%7D&to_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Find the top news stories related to a given category. A story is a collection of similar articles."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6fd4271-523d-42e5-8f2c-e6550cd15f98"
            }
          ]
        },
        {
          "id": "bca81c4f-da66-46b3-a0b8-fff8e1269e92",
          "name": "getCategoryDashedNameImages",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "category/:dashed-name/images/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "safe_search",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "dashed-name",
                  "value": "dashed-name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets images related to the specified category."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e868f4f-b22f-48e1-873d-f1dc861e4c1a"
            }
          ]
        },
        {
          "id": "1c70917a-247d-4ddc-9d2d-6b8198fe4e4e",
          "name": "getSourceGuArticles",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "source/:GUID/articles/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "article_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "article_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "categories",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "get_topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "has_images",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "languages",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "licensed",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "media_types",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to_date",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "GUID",
                  "value": "GUID",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of articles provided by the specified source"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d51795b9-e9f0-482c-95c3-90a1d4f1eac0"
            }
          ]
        },
        {
          "id": "0561539a-1558-45ec-b835-1a77cb0338ea",
          "name": "getSourceGuTopics",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "source/:GUID/topics/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_classifications",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_subclassifications",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to_date",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "GUID",
                  "value": "GUID",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of topics related to the source specified by the given GUID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "452672ab-75e8-4646-a7d5-dbbabeca4738"
            }
          ]
        },
        {
          "id": "3c138376-4e87-4fee-a5d0-e7a089932fb0",
          "name": "getSources",
          "request": {
            "url": "http://api.newscred.com/sources/?access_key=%7B%7D&autosuggest=%7B%7D&licensed=%7B%7D&media_types=%7B%7D&query=%7B%7D&sources=%7B%7D&source_countries=%7B%7D&source_filter_mode=%7B%7D&source_filter_name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search sources by name. Returns a list of sources objects"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89c1cf0b-ea7a-4a9c-8c71-fa80c294f694"
            }
          ]
        },
        {
          "id": "5f685368-520d-4bff-b491-7e0a15caf356",
          "name": "getStories",
          "request": {
            "url": "http://api.newscred.com/stories/?access_key=%7B%7D&article_filter_mode=%7B%7D&article_filter_name=%7B%7D&boolean_operator=%7B%7D&categories=%7B%7D&cluster_size=%7B%7D&exact=%7B%7D&from_date=%7B%7D&get_topics=%7B%7D&has_images=%7B%7D&languages=%7B%7D&licensed=%7B%7D&links=%7B%7D&max_length=%7B%7D&media_types=%7B%7D&min_length=%7B%7D&mm=%7B%7D&modified_since=%7B%7D&offset=%7B%7D&query=%7B%7D&query_fields=%7B%7D&safe_search=%7B%7D&sort=%7B%7D&sources=%7B%7D&source_countries=%7B%7D&source_filter_mode=%7B%7D&source_filter_name=%7B%7D&topics=%7B%7D&topic_filter_mode=%7B%7D&topic_filter_name=%7B%7D&to_date=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the top stories related to the specified query. A story is a group of similar articles. By default, stories are sorted by a combination of recency and importance. If the from_date and/or to_date parameters are specified, stories are sorted by importance only."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5c98790-1dc3-4fe0-9e48-ded806d6519b"
            }
          ]
        },
        {
          "id": "1e717b95-de24-4873-a1f6-20d93491da03",
          "name": "getTopicGueImages",
          "request": {
            "url": "http://api.newscred.com/topic/{guide{/images/?access_key=%7B%7D&guid=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns images related to the specified topic."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "048edb3a-d07a-490c-8559-ed231b80bce3"
            }
          ]
        },
        {
          "id": "28b5342c-e9fa-4e06-9fe3-420aa62b2bbf",
          "name": "getTopicGu",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "topic/:guid/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "guid",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return the topic specified by the given GUID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "677b173e-62b6-448a-ab38-a3a0a523a0ad"
            }
          ]
        },
        {
          "id": "346aef90-017f-4778-9277-70d9066f75d0",
          "name": "getTopicGuSources",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "topic/:guid/sources/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sources",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "source_countries",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "source_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "source_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "Topic Sources",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to_date",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "guid",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The guid for the topic."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "61a1581d-4656-47e3-9de3-5fff6b3241a7"
            }
          ]
        },
        {
          "id": "766fd962-1750-4477-b198-6ac01a500310",
          "name": "getTopicGuTopics",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "topic/:guid/topics/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "from_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topics",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_classifications",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_mode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_filter_name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "topic_subclassifications",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to_date",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of topics related to the topic specified."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4befd1b4-fd8c-4c7b-bb4c-310e06a86322"
            }
          ]
        },
        {
          "id": "bc699aeb-d9e1-4f44-8cfc-f34d94b43060",
          "name": "getTopicGuTweets",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "topic/:guid/tweets/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of real-time tweets related to the specified topic."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b62c916-75d2-4e9b-9f06-63403ece15a3"
            }
          ]
        },
        {
          "id": "09b860ba-304b-40ea-af37-da277b76e6cf",
          "name": "getTopicGuVeos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.newscred.com",
              "path": [
                "topic/:guid/videos/"
              ],
              "query": [
                {
                  "key": "access_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "categories",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "guid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of videos related to the specified topic."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6cd11953-09d6-4457-ae6f-10510552b3a7"
            }
          ]
        }
      ]
    }
  ]
}