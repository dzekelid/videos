---
swagger: "2.0"
x-collection-name: NewsCred
x-complete: 0
info:
  title: News Cred Videos
  description: Returns videos matching the given query string
  version: v1
host: api.newscred.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  topic/{guid}/videos/:
    get:
      summary: Topic Videos
      description: Returns a list of videos related to the specified topic.
      operationId: getTopicGuVeos
      x-api-path-slug: topicguidvideos-get
      parameters:
      - in: query
        name: access_key
        description: Unique API access key
      - in: query
        name: categories
        description: Limit videos to the categories specified
      - in: path
        name: guid
        description: The guid for the topic
      - in: query
        name: offset
        description: Number of videos to skip before beginning the result set
      - in: query
        name: pagesize
        description: Number of videos to return
      responses:
        200:
          description: OK
      tags:
      - News
      - Topic
      - Videos
  videos/:
    get:
      summary: Videos
      description: Returns videos matching the given query string
      operationId: getVeos
      x-api-path-slug: videos-get
      parameters:
      - in: query
        name: from_date
        description: Beginning of date range for which items are searched
      - in: query
        name: licensed
        description: Return only licensed videos
      - in: query
        name: maxduration
        description: Maximum duration for searched videos (in milliseconds)
      - in: query
        name: minduration
        description: Minimum duration for searched videos (in milliseconds)
      - in: query
        name: offset
        description: Number of items to skip before beginning the result set
      - in: query
        name: pagesize
        description: Number of items to return
      - in: query
        name: query
        description: Query that you want to search on
      - in: query
        name: to_date
        description: End of date range for which items are searched
      responses:
        200:
          description: OK
      tags:
      - News
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