---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Get Video
  version: 1.0.0
  description: Gets one video format by ID.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /userprofiles/{profileId}/videoFormats:
    get:
      summary: Get Video Formats
      description: Lists available video formats.
      operationId: dfareporting.videoFormats.list
      x-api-path-slug: userprofilesprofileidvideoformats-get
      parameters:
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Video
  /userprofiles/{profileId}/videoFormats/{id}:
    get:
      summary: Get Video
      description: Gets one video format by ID.
      operationId: dfareporting.videoFormats.get
      x-api-path-slug: userprofilesprofileidvideoformatsid-get
      parameters:
      - in: path
        name: id
        description: Video format ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Video
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