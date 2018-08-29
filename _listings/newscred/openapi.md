swagger: "2.0"
x-collection-name: NewsCred
x-complete: 1
info:
  title: News Cred
  description: returns-a-list-of-articles-according-to-the-specified-set-of-parameters-
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