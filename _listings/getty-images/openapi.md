swagger: "2.0"
x-collection-name: Getty Images
x-complete: 1
info:
  title: Getty Images
  description: build-applications-using-the-worlds-most-powerful-imagery
  version: 1.0.0
host: api.gettyimages.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/artists/videos:
    get:
      summary: Search Artist ImaVideosges
      description: Search for videos by a photographer
      operationId: Artists_GetVideosByArtist
      x-api-path-slug: v3artistsvideos-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: query
        name: artist_name
        description: Name of artist for desired images
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: fields
        description: Comma separated list of fields
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      responses:
        200:
          description: OK
      tags:
      - Images
      - Artists
      - Videos
  /v3/downloads/videos/{id}:
    post:
      summary: Download a video
      description: "Use this endpoint to generate download URLs and related data for
        videos you are authorized to download.\r\n\r\nMost product offerings have
        enforced periodic download limits such as monthly, weekly, and daily. When
        this operation executes, the count of allowed downloads is decremented by
        one for the product offering. Once the download limit is reached for a given
        product offering, no further downloads may be requested for that product offering
        until the next download period.\r\n\r\nThe download limit for a given download
        period is covered in your product agreement established with Getty Images.\r\n\r\nYou'll
        need an API key and a [Resource Owner Grant or Implicit Grant](http://developers.gettyimages.com/en/authorization-faq.html)
        access token to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)
        page for more information on how to sign up for an API key. \r\n\r\n## Auto
        Downloads\r\nThe `auto_download` request query parameter specifies whether
        to automatically download the video.\r\n\r\nIf the `auto_download` request
        query parameter is set to _true_, the API will return an HTTP status code
        303 *See Other*.???Your client code will need to process this response and
        redirect to the URI specified in the *Location* header to enable you to automatically
        download the file. The redirection workflow follows the [HTTP 1.1 protocol](https://tools.ietf.org/html/rfc7231#section-6.4.4).\r\n\r\nClient
        Request:\r\n\r\n```\r\nhttps://api.gettyimages.com/v3/downloads/videos/[asset_id]?auto_download=true\r\n```\r\n\r\nServer
        Response:\r\n\r\n```\r\nHTTP/1.1 303 See Other\r\nLocation: https://delivery.gettyimages.com/...\r\n```\r\n\r\nIf
        the `auto_download` request query parameter is set to false, the API will
        return a HTTP status code 200, along with the URI in the response body which
        can be used to download the video. \r\n\r\nClient Request:\r\n\r\n```\r\nhttps://api.gettyimages.com/v3/downloads/videos/[asset_id]?auto_download=false\r\n```\r\n\r\nServer
        Response:\r\n\r\n```\r\nHTTP/1.1 200 OK\r\n{\r\n\t\"uri\": \"https://delivery.gettyimages.com/...\"\r\n}\r\n```"
      operationId: Downloads_PostVideoDownloads
      x-api-path-slug: v3downloadsvideosid-post
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: auto_download
        description: Specifies whether to auto-download the video
      - in: body
        name: download_details
        description: Additional information required from specific customers when
          downloading
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Id of video to download
      - in: query
        name: product_id
        description: Identifier of the instance for the selected product offering
          type
      - in: query
        name: size
        description: Specifies the size to be downloaded
      responses:
        200:
          description: OK
      tags:
      - Images
      - Downloads
      - Videos
  /v3/search/videos:
    get:
      summary: Search Editorial Videos
      description: "Use this endpoint to search over a blend of our premium stock,
        contemporary 4K and HD footage, celebrities, news, newsmakers, entertainment,
        events and archival videos.\r\n\r\nYou'll need an API key and access token
        to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)
        page for more information on how to sign up for an API key.\r\n\r\n\r\nYou
        can show different information in the response by specifying values on the
        \"fields\" parameter (see details below).\r\nYou can search with only an API
        key, and that will give you search results that are equivalent to doing a
        search on the GettyImages.com site without being logged in (anonymous search).
        \ If you are a Getty Images API customer and would like to ensure that your
        API searches return only assets that you have a license to use, you need to
        also include an authorization token in the header of your request.  Please
        consult our [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html)
        for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md)
        for code examples of getting a token.\r\n\r\n## Working with Fields Sets\r\n\r\nFields
        sets are used in the **fields** request parameter to receive a suite of metadata
        fields. The following fields sets are available:\r\n\r\n#### Summary Fields
        Set\r\n\r\nThe **summary_set** query string parameter fields value represents
        a small batch of metadata fields that are often used to build search response
        results. The following fields are provided for every video in your result
        set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\":\r\n    [\r\n        \"asset_family\",\r\n        \"caption\",\r\n
        \       \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n
        \       [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields
        value represents a large batch of metadata fields that are often used to build
        a detailed view of videos. The following fields are provided for every video
        in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\":\r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n
        \       \"asset_family\",\r\n        \"caption\",\r\n        \"clip_length\",\r\n
        \       \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\",\r\n
        \       \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n
        \       \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ],\r\n        \"era\",\r\n        \"license_model\",\r\n
        \       \"mastered_to\",\r\n        \"originally_shot_on\",\r\n        \"product_types\",\r\n
        \       \"shot_speed\",\r\n        \"source\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Display Fields Set\r\n\r\nThe **display_set** query string parameter fields
        value represents the fields that provide you with URLs for the low resolution
        files that are most frequently used to build a UI displaying search results.
        The following fields are provided for every video in your result set when
        you include **display_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n
        \   [\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ]\r\n    ]\r\n}\r\n```\r\n\r\n## Request Usage Considerations\r\n\r\n-
        Specifying the \"entity_details\" response field can have significant performance
        implications. The field should be used only when necessary."
      operationId: Search_GetVideosByPhrase
      x-api-path-slug: v3searchvideos-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: query
        name: age_of_people
        description: Provides filtering according to the age of individuals in a video
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: collections_filter_type
        description: Provides searching based on specified collection(s)
      - in: query
        name: collection_codes
        description: Provides filtering by collection code
      - in: query
        name: editorial_video_types
        description: Allows filtering by types of video
      - in: query
        name: exclude_nudity
        description: Excludes images containing nudity
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: format_available
        description: Filters according to the digital video format available on a
          film asset
      - in: query
        name: frame_rates
        description: Provides filtering by video frame rate (frames/second)
      - in: query
        name: keyword_ids
        description: Return only images tagged with specific keyword(s)
      - in: query
        name: license_models
        description: Specifies the video licensing model(s)
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      - in: query
        name: phrase
        description: Free-text search query
      - in: query
        name: product_types
        description: Filter images to those from one of your product types
      - in: query
        name: sort_order
        description: Allows sorting of results
      - in: query
        name: specific_people
        description: Provides filtering by specific peoples names
      responses:
        200:
          description: OK
      tags:
      - Images
      - Search
      - Videos
  /v3/search/videos/creative:
    get:
      summary: Search for creative videos
      description: "Use this endpoint to search premium stock video, from archival
        film to contemporary 4K and HD footage.\r\n\r\nYou'll need an API key and
        access token to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)\r\npage
        for more information on how to sign up for an API key.\r\n\r\nYou can show
        different information in the response by specifying values on the \"fields\"
        parameter (see details below).\r\nYou can search with only an API key, and
        that will give you search results that are equivalent to doing a search on
        the GettyImages.com site without\r\nbeing logged in (anonymous search).  If
        you are a Getty Images API customer and would like to ensure that your API
        searches return only \r\nassets that you have a license to use, you need to
        also include an authorization token in the header of your request.\r\nPlease
        consult our [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html)
        for more information on authorization tokens.\r\n\r\n## Working with Fields
        Sets\r\n\r\nFields sets are used in the **fields** request parameter to receive
        a suite of metadata fields. The following fields sets are available:\r\n\r\n####
        Summary Fields Set\r\n\r\nThe **summary_set** query string parameter fields
        value represents a small batch of metadata fields that are often used to build
        search\r\nresponse results. The following fields are provided for every video
        in your result set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\": \r\n    [\r\n        \"asset_family\", \r\n        \"caption\",\r\n
        \       \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n
        \       [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields
        value represents a large batch of metadata fields that are often used to build
        a \r\ndetailed view of videos. The following fields are provided for every
        video in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\": \r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n
        \       \"asset_family\", \r\n        \"caption\", \r\n        \"clip_length\",\r\n
        \       \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\",
        \r\n        \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n
        \       \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ],\r\n        \"era\",\r\n        \"license_model\",\r\n
        \       \"mastered_to\",\r\n        \"originally_shot_on\",\r\n        \"product_types\",\r\n
        \       \"shot_speed\",\r\n        \"source\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Display Fields Set\r\n\r\nThe **display_set** query string parameter fields
        value represents the fields that provide you with URLs for the low resolution
        files \r\nthat are most frequently used to build a UI displaying search results.
        The following fields are provided for every video in your result \r\nset when
        you include **display_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n
        \   [\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ]\r\n    ]\r\n}\r\n```"
      operationId: Search_GetCreativeVideosByPhrase
      x-api-path-slug: v3searchvideoscreative-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: query
        name: age_of_people
        description: Provides filtering according to the age of individuals in a video
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: collections_filter_type
        description: Provides searching based on specified collection(s)
      - in: query
        name: collection_codes
        description: Provides filtering by collection code
      - in: query
        name: exclude_nudity
        description: Excludes images containing nudity
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: format_available
        description: Filters according to the digital video format available on a
          film asset
      - in: query
        name: frame_rates
        description: Provides filtering by video frame rate (frames/second)
      - in: query
        name: keyword_ids
        description: Return only images tagged with specific keyword(s)
      - in: query
        name: license_models
        description: Specifies the video licensing model(s)
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      - in: query
        name: phrase
        description: Free-text search query
      - in: query
        name: product_types
        description: Filter images to those from one of your product types
      - in: query
        name: sort_order
        description: Allows sorting of results
      responses:
        200:
          description: OK
      tags:
      - Images
      - Search
      - Videos
  /v3/search/videos/editorial:
    get:
      summary: Search for editorial videos
      description: "Use this endpoint to search current and archival video clips of
        celebrities, newsmakers, and events.\r\n\r\nYou'll need an API key and access
        token to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)
        page for more information on how to sign up for an API key.\r\n\r\nYou can
        show different information in the response by specifying values on the \"fields\"
        parameter (see details below).\r\nYou can search with only an API key, and
        that will give you search results that are equivalent to doing a search on
        the GettyImages.com site without being logged in (anonymous search).  If you
        are a Getty Images API customer and would like to ensure that your API searches
        return only assets that you have a license to use, you need to also include
        an authorization token in the header of your request.  Please consult our
        [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html)
        for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md)
        for code examples of getting a token.\r\n\r\n## Working with Fields Sets\r\n\r\nFields
        sets are used in the **fields** request parameter to receive a suite of metadata
        fields. The following fields sets are available:\r\n\r\n#### Summary Fields
        Set\r\n\r\nThe **summary_set** query string parameter fields value represents
        a small batch of metadata fields that are often used to build search response
        results. The following fields are provided for every video in your result
        set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\": \r\n    [\r\n        \"asset_family\", \r\n        \"caption\",\r\n
        \       \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n
        \       [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields
        value represents a large batch of metadata fields that are often used to build
        a detailed view of videos. The following fields are provided for every video
        in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\": \r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n
        \       \"asset_family\", \r\n        \"caption\", \r\n        \"clip_length\",\r\n
        \       \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\",
        \r\n        \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n
        \       \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ],\r\n        \"era\",\r\n        \"license_model\",\r\n
        \       \"mastered_to\",\r\n        \"originally_shot_on\",\r\n        \"product_types\",\r\n
        \       \"shot_speed\",\r\n        \"source\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Display Fields Set\r\n\r\nThe **display_set** query string parameter fields
        value represents the fields that provide you with URLs for the low resolution
        files that are most frequently used to build a UI displaying search results.
        The following fields are provided for every video in your result set when
        you include **display_set** in your request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n
        \   [\r\n        \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ]\r\n    ]\r\n}\r\n```\r\n\r\n## Request Usage Considerations\r\n\r\n-
        Specifying the \"entity_details\" response field can have significant performance
        implications. The field should be used only when necessary."
      operationId: Search_GetEditorialVideosByPhrase
      x-api-path-slug: v3searchvideoseditorial-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: query
        name: age_of_people
        description: Provides filtering according to the age of individuals in a video
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: collections_filter_type
        description: Provides searching based on specified collection(s)
      - in: query
        name: collection_codes
        description: Provides filtering by collection code
      - in: query
        name: editorial_video_types
        description: Allows filtering by types of video
      - in: query
        name: entity_uris
        description: specify link data entity uri
      - in: query
        name: exclude_nudity
        description: Excludes images containing nudity
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: format_available
        description: Filters according to the digital video format available on a
          film asset
      - in: query
        name: frame_rates
        description: Provides filtering by video frame rate (frames/second)
      - in: query
        name: keyword_ids
        description: Return only images tagged with specific keyword(s)
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      - in: query
        name: phrase
        description: Free-text search query
      - in: query
        name: product_types
        description: Filter images to those from one of your product types
      - in: query
        name: sort_order
        description: Allows sorting of results
      - in: query
        name: specific_people
        description: Allows filtering by specific peoples names
      responses:
        200:
          description: OK
      tags:
      - Images
      - Search
      - Videos
      - Editoria
  /v3/videos:
    get:
      summary: Get Videos Metadatata
      description: "Use this endpoint to return detailed video metadata for all the
        specified video ids.\r\n\r\nYou'll need an API key and access token to use
        this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)
        page for more information on how to sign up for an API key.\r\n\r\nYou can
        show different information in the response by specifying values on the \"fields\"
        parameter (see details below).\r\nYou can search with only an API key, and
        that will give you search results that are equivalent to doing a search on
        the GettyImages.com site without being logged in (anonymous search).  If you
        are a Getty Images API customer and would like to ensure that your API searches
        return only assets that you have a license to use, you need to also include
        an authorization token in the header of your request.  Please consult our
        [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html)
        for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md)
        for code examples of getting a token.\r\n\r\n## Working with Fields Sets\r\n\r\nFields
        sets are used in the **fields** request parameter to receive a suite of metadata
        fields. The following fields sets are available:\r\n\r\n#### Summary Fields
        Set\r\n\r\nThe **summary_set** query string parameter fields value represents
        a small batch of metadata fields that are often used to build search response
        results. The following fields are provided for every video in your result
        set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\": \r\n    [\r\n        \"asset_family\",\r\n        \"caption\",\r\n
        \       \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n
        \       [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields
        value represents a large batch of metadata fields that are often used to build
        a detailed view of videos. The following fields are provided for every video
        in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\": \r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n
        \       \"asset_family\",\r\n        \"caption\",\r\n        \"clip_length\",\r\n
        \       \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\",\r\n
        \       \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n
        \       \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ],\r\n        \"download_sizes\",\r\n        \"era\",\r\n
        \       \"license_model\",\r\n        \"mastered_to\",\r\n        \"originally_shot_on\",\r\n
        \       \"product_types\",\r\n        \"shot_speed\",\r\n        \"source\",\r\n
        \       \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n#### Display Fields Set\r\n\r\nThe
        **display_set** query string parameter fields value represents the fields
        that provide you with URLs for the low resolution files that are most frequently
        used to build a UI displaying search results. The following fields are provided
        for every video in your result set when you include **display_set** in your
        request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n    [\r\n        \"display_sizes\":
        \r\n        [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ]\r\n    ]\r\n}\r\n```\r\n\r\n## Request Usage Considerations\r\n\r\n-
        Specifying the \"entity_details\" response field can have significant performance
        implications. The field should be used only when necessary."
      operationId: Videos_GetBatch
      x-api-path-slug: v3videos-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: ids
        description: Specifies one or more video ids to return
      responses:
        200:
          description: OK
      tags:
      - Images
      - Videos
  /v3/videos/{id}:
    get:
      summary: Get Video Metadatata
      description: "Use this endpoint to return detailed video metadata for the specified
        video id.\r\n\r\nYou'll need an API key and access token to use this resource.
        Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html)
        page for more information on how to sign up for an API key.\r\n\r\nYou can
        show different information in the response by specifying values on the \"fields\"
        parameter (see details below).\r\nYou can search with only an API key, and
        that will give you search results that are equivalent to doing a search on
        the GettyImages.com site without being logged in (anonymous search).  If you
        are a Getty Images API customer and would like to ensure that your API searches
        return only assets that you have a license to use, you need to also include
        an authorization token in the header of your request.  Please consult our
        [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html)
        for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md)
        for code examples of getting a token.\r\n\r\n## Working with Fields Sets\r\n\r\nFields
        sets are used in the **fields** request parameter to receive a suite of metadata
        fields. The following fields sets are available:\r\n\r\n#### Summary Fields
        Set\r\n\r\nThe **summary_set** query string parameter fields value represents
        a small batch of metadata fields that are often used to build search response
        results. The following fields are provided for every video in your result
        set when you include **summary_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\":\r\n    [\r\n        \"asset_family\",\r\n        \"caption\",\r\n
        \       \"collection_code\",\r\n        \"collection_name\",\r\n        \"display_sizes\":\r\n
        \       [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ],\r\n        \"license_model\",\r\n        \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n####
        Detail Fields Set\r\n\r\nThe **detail_set** query string parameter fields
        value represents a large batch of metadata fields that are often used to build
        a detailed view of videos. The following fields are provided for every video
        in your result set when you include **detail_set** in your request.\r\n\r\n```\r\n{\r\n
        \   \"videos\":\r\n    [\r\n        \"allowed_use\",\r\n        \"artist\",\r\n
        \       \"asset_family\",\r\n        \"caption\",\r\n        \"clip_length\",\r\n
        \       \"collection_code\",\r\n        \"collection_id\",\r\n        \"collection_name\",\r\n
        \       \"color_type\",\r\n        \"copyright\",\r\n        \"date_created\",\r\n
        \       \"display_sizes\":\r\n        [\r\n            {\r\n                \"name\":
        \"comp\"\r\n            },\r\n            {\r\n                \"name\": \"preview\"\r\n
        \           },\r\n            {\r\n                \"name\": \"thumb\"\r\n
        \           }\r\n        ],\r\n        \"download_sizes\",\r\n        \"era\",\r\n
        \       \"license_model\",\r\n        \"mastered_to\",\r\n        \"originally_shot_on\",\r\n
        \       \"product_types\",\r\n        \"shot_speed\",\r\n        \"source\",\r\n
        \       \"title\"\r\n    ]\r\n}\r\n```\r\n\r\n#### Display Fields Set\r\n\r\nThe
        **display_set** query string parameter fields value represents the fields
        that provide you with URLs for the low resolution files that are most frequently
        used to build a UI displaying search results. The following fields are provided
        for every video in your result set when you include **display_set** in your
        request.\r\n\r\n```\r\n{\r\n    \"videos\":\r\n    [\r\n        \"display_sizes\":\r\n
        \       [\r\n            {\r\n                \"name\": \"comp\"\r\n            },\r\n
        \           {\r\n                \"name\": \"preview\"\r\n            },\r\n
        \           {\r\n                \"name\": \"thumb\"\r\n            }\r\n
        \       ]\r\n    ]\r\n}\r\n```\r\n\r\n## Request Usage Considerations\r\n\r\n-
        Specifying the \"entity_details\" response field can have significant performance
        implications. The field should be used only when necessary."
      operationId: Videos_Get
      x-api-path-slug: v3videosid-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: fields
        description: comma delimited list of fields to retrive for the video
      - in: path
        name: id
        description: A video id
      responses:
        200:
          description: OK
      tags:
      - Images
      - Videos
  /v3/videos/{id}/similar:
    get:
      summary: Get Similar Videos
      description: Get videos similar to a video by supplying one video id
      operationId: Videos_GetSimilarVideos
      x-api-path-slug: v3videosidsimilar-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: fields
        description: comma delimited list of fields to retrive for the videos
      - in: path
        name: id
        description: A video id
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      responses:
        200:
          description: OK
      tags:
      - Images
      - Videos
      - Similiar