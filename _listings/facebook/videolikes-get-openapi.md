---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Get Veo Likes
  description: Users who like this video.
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{page}/videos:
    get:
      summary: Get Page Veos
      description: The videos contained on this page
      operationId: getPageVeos
      x-api-path-slug: pagevideos-get
      parameters:
      - in: path
        name: page
        description: Represents the ID of the page object
      responses:
        200:
          description: OK
      tags:
      - Page
      - Videos
    post:
      summary: Post Page Veos
      description: Publishes a video to the page
      operationId: postPageVeos
      x-api-path-slug: pagevideos-post
      parameters:
      - in: query
        name: description
        description: Video description
      - in: path
        name: page
        description: Represents the ID of the page object
      - in: query
        name: title
        description: Video title
      responses:
        200:
          description: OK
      tags:
      - Page
      - Videos
  /{user}/videos:
    get:
      summary: Get User Veos
      description: The videos this user has been tagged in
      operationId: getUserVeos
      x-api-path-slug: uservideos-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Videos
    post:
      summary: Post User Veos
      description: Publishes a video on behalf of the user
      operationId: postUserVeos
      x-api-path-slug: uservideos-post
      parameters:
      - in: query
        name: description
        description: Video description
      - in: query
        name: title
        description: Video title
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Videos
  /{video}:
    get:
      summary: Get Veo
      description: An individual video
      operationId: getVeo
      x-api-path-slug: video-get
      parameters:
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
  /{video}/comments:
    get:
      summary: Get Veo Comments
      description: All of the comments on this video.
      operationId: getVeoComments
      x-api-path-slug: videocomments-get
      parameters:
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
      - Comments
    post:
      summary: Post Veo Comments
      description: Posts a comment to this video.
      operationId: postVeoComments
      x-api-path-slug: videocomments-post
      parameters:
      - in: query
        name: message
        description: Comment text
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
      - Comments
  /{video}/likes:
    get:
      summary: Get Veo Likes
      description: Users who like this video.
      operationId: getVeoLikes
      x-api-path-slug: videolikes-get
      parameters:
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
      - Likes
    post:
      summary: Post Veo Likes
      description: Likes this video.
      operationId: postVeoLikes
      x-api-path-slug: videolikes-post
      parameters:
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
      - Likes
    delete:
      summary: Delete Veo Likes
      description: Unlikes this video.
      operationId: deleteVeoLikes
      x-api-path-slug: videolikes-delete
      parameters:
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
      - Likes
  /{video}/picture:
    get:
      summary: Get Veo Picture
      description: The image which represents the content of the video
      operationId: getVeoPicture
      x-api-path-slug: videopicture-get
      parameters:
      - in: path
        name: video
        description: Represents the ID of the video object
      responses:
        200:
          description: OK
      tags:
      - Video
      - Picture
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---