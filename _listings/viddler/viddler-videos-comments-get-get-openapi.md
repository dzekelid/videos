---
swagger: "2.0"
x-collection-name: Viddler
x-complete: 0
info:
  title: Viddler  API Videos Comments Get
  description: Get comments for a video. If logged in and querying comments for own
    video &#8211; all comments with any moderation status will be returned. If quering
    comments as logged out or for not owned video &#8211; only approved comments will
    be returned if the video itself is public.
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
  viddler.videos.comments.get:
    get:
      summary: Videos Comments Get
      description: Get comments for a video. If logged in and querying comments for
        own video &#8211; all comments with any moderation status will be returned.
        If quering comments as logged out or for not owned video &#8211; only approved
        comments will be returned if the video itself is public.
      operationId: videos-comments-get
      x-api-path-slug: viddler-videos-comments-get-get
      parameters:
      - in: query
        name: page
      - in: query
        name: parent_id
        description: comment parent ID if you want to get the responses to that particular
          comment
      - in: query
        name: per_page
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
      - Comments
      - Get
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