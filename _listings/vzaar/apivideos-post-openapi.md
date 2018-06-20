---
swagger: "2.0"
x-collection-name: Vzaar
x-complete: 0
info:
  title: Vzaar API Post Api Videos
  description: nnThis API call tells the vzaar system to process a newly uploaded
    video. This will encode it if necessary and then provide a vzaar video idea back.nn
  termsOfService: http://vzaar.com/policies
  version: v1
host: vzaar.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/videos:
    post:
      summary: Post Api Videos
      description: nnThis API call tells the vzaar system to process a newly uploaded
        video. This will encode it if necessary and then provide a vzaar video idea
        back.nn
      operationId: postApiVeos
      x-api-path-slug: apivideos-post
      parameters:
      - in: query
        name: description
        description: Specifies the description for the video
      - in: query
        name: guid
        description: Specifies the guid to operate on
      - in: query
        name: labels
        description: Comma separated list of labels to be assigned to the video
      - in: query
        name: profile
        description: Specifies the size for the video to be encoded in
      - in: query
        name: replace_id
        description: Specifies the video ID of an existing video that you wish to
          replace with the new video
      - in: query
        name: title
        description: Specifies the title for the video
      - in: query
        name: transcoding
        description: True forces vzaar to transcode the video, false makes vzaar use
          the original source file (available only for mp4 and flv files)
      responses:
        200:
          description: OK
      tags:
      - Api
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