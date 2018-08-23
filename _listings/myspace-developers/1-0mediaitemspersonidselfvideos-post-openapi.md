---
swagger: "2.0"
x-collection-name: MySpace Developers
x-complete: 0
info:
  title: My Space Post Mediaitems Personid Self Videos
  description: Adds videos from a specified album.
  version: 1.0.0
host: api.myspace.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /opensearch/videos:
    get:
      summary: Get Opensearch Veos
      description: Returns search results for videos.
      operationId: opensearch.videos.get
      x-api-path-slug: opensearchvideos-get
      parameters:
      - in: query
        name: count
        description: Number of items to return
      - in: query
        name: culture
        description: The culture context of the search
      - in: query
        name: format
        description: Determines the format of the response
      - in: query
        name: searchTerms
        description: Free form search terms or query words
      - in: query
        name: startPage
        description: Which page to start at for the results
      - in: query
        name: tag
        description: Determine if searching on tags, as opposed to contents
      - in: query
        name: videoMode
        description: Search for specific video types
      responses:
        200:
          description: OK
      tags:
      - Opensearch
      - Videos
  /1.0/mediaItems/{personId}/@videos/@supportedcategories/{categoryId}:
    get:
      summary: Get Mediaitems Personid Videos Supported Categories Categoryid
      description: Retrieves videos for Category.
      operationId: 1.0.mediaItems.personId._videos._supportedcategories.categoryId.get
      x-api-path-slug: 1-0mediaitemspersonidvideossupportedcategoriescategoryid-get
      parameters:
      - in: path
        name: categoryId
        description: Indicates the video category about which you want to retrieve
          data
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: format
        description: Determines the format of the response
      - in: query
        name: msPrivacyLevel
        description: MySpace specific field
      - in: path
        name: personId
        description: The persons identifier
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - MediaItems
      - People
      - '@videos'
      - Supported
      - categories
      - CategoryId
  /1.0/mediaItems/{personId}/@videos/@supportedcategories:
    get:
      summary: Get Mediaitems Personid Videos Supported Categories
      description: Retrieves supported categories.
      operationId: 1.0.mediaItems.personId._videos._supportedcategories.get
      x-api-path-slug: 1-0mediaitemspersonidvideossupportedcategories-get
      parameters:
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: format
        description: Determines the format of the response
      - in: query
        name: msPrivacyLevel
        description: MySpace specific field
      - in: path
        name: personId
        description: The persons identifier
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - MediaItems
      - People
      - '@videos'
      - Supported
      - categories
  /1.0/mediaItems/{personId}/@self/@videos/{mediaItemId}:
    put:
      summary: Put Mediaitems Personid Self Videos Mediaitemid
      description: Updates an video.
      operationId: 1.0.mediaItems.personId._self._videos.mediaItemId.put
      x-api-path-slug: 1-0mediaitemspersonidselfvideosmediaitemid-put
      parameters:
      - in: query
        name: Content-Type
        description: Specifies Content Type
      - in: header
        name: Content-Type
        description: Specifies Content Type
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: format
        description: Determines the format of the response
      - in: path
        name: mediaItemId
        description: Indicates which single media item should be returned
      - in: query
        name: msPrivacyLevel
        description: MySpace specific field
      - in: path
        name: personId
        description: The persons identifier
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - MediaItems
      - People
      - Self
      - '@videos'
      - MediaItemId
    get:
      summary: Get Mediaitems Personid Self Videos Mediaitemid
      description: Retrieves a video.
      operationId: 1.0.mediaItems.personId._self._videos.mediaItemId.get
      x-api-path-slug: 1-0mediaitemspersonidselfvideosmediaitemid-get
      parameters:
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: format
        description: Determines the format of the response
      - in: path
        name: mediaItemId
        description: Indicates which single media item should be returned
      - in: query
        name: msPrivacyLevel
        description: MySpace specific field
      - in: path
        name: personId
        description: The persons identifier
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - MediaItems
      - People
      - Self
      - '@videos'
      - MediaItemId
  /1.0/mediaItems/{personId}/@self/@videos:
    post:
      summary: Post Mediaitems Personid Self Videos
      description: Adds videos from a specified album.
      operationId: 1.0.mediaItems.personId._self._videos.post
      x-api-path-slug: 1-0mediaitemspersonidselfvideos-post
      parameters:
      - in: query
        name: Content-Type
        description: Specifies Content Type
      - in: header
        name: Content-Type
        description: Specifies Content Type
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: format
        description: Determines the format of the response
      - in: query
        name: msPrivacyLevel
        description: MySpace specific field
      - in: path
        name: personId
        description: The persons identifier
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - MediaItems
      - People
      - Self
      - '@videos'
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---