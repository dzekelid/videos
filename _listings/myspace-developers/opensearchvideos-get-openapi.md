---
swagger: "2.0"
x-collection-name: MySpace Developers
x-complete: 0
info:
  title: My Space Get Opensearch Veos
  description: Returns search results for videos.
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