---
swagger: "2.0"
x-collection-name: Viddler
x-complete: 0
info:
  title: Viddler  API Videos AddClosedCaptioning
  description: Add new closed captioning file for a specific video. All uploaded closed
    captioning files are enabled by default. The first uploaded file is default for
    a video.
  termsOfService: http://www.viddler.com/terms-of-use/
  version: v2
host: api.viddler.com
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  viddler.videos.addClosedCaptioning:
    post:
      summary: Videos AddClosedCaptioning
      description: Add new closed captioning file for a specific video. All uploaded
        closed captioning files are enabled by default. The first uploaded file is
        default for a video.
      operationId: videos-addclosedcaptioning
      x-api-path-slug: viddler-videos-addclosedcaptioning-post
      parameters:
      - in: query
        name: closed_captioning_url
      - in: query
        name: default
      - in: query
        name: language
        description: 'The language of the file (Max Characters: 50)'
      - in: query
        name: sessionid
      - in: query
        name: video_id
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - AddClosedCaptioning
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