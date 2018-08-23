---
swagger: "2.0"
x-collection-name: api.video
x-complete: 0
info:
  title: API.Video Parameters Videos Thumbnail
  description: Parameters videos thumbnail.
  version: 1.0.0
host: ws.api.video
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /videos/{id}/thumbnail:
    parameters:
      summary: Parameters Videos Thumbnail
      description: Parameters videos thumbnail.
      operationId: parametersVeosThumbnail
      x-api-path-slug: videosidthumbnail-parameters
      responses:
        200:
          description: Successful response
      tags:
      - Parameters
      - Videos
      - Thumbnail
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