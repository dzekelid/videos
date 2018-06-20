---
swagger: "2.0"
x-collection-name: Viddler
x-complete: 1
info:
  title: Viddler  API
  description: the-viddler-api-exposes-viddleru2019s-key-features-to-those-that-would-like-to-build-custom-solutions-on-top-of-viddleru2019s-video-platform-
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
  viddler.videos.delClosedCaptioning:
    post:
      summary: Videos DelClosedCaptioning
      description: Remove an existing closed captioning file.
      operationId: videos-delclosedcaptioning
      x-api-path-slug: viddler-videos-delclosedcaptioning-post
      parameters:
      - in: query
        name: closed_captioning_id
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - DelClosedCaptioning
  viddler.videos.delete:
    post:
      summary: Videos Delete
      description: Delete a video.
      operationId: videos-delete
      x-api-path-slug: viddler-videos-delete-post
      parameters:
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
      - Delete
  viddler.videos.enableAds:
    post:
      summary: Videos EnableAds
      description: Turn ads off for specified videos.
      operationId: videos-enableads
      x-api-path-slug: viddler-videos-enableads-post
      parameters:
      - in: query
        name: sessionid
      - in: query
        name: video_ids
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - EnableAds
  viddler.videos.getAdsStatus:
    get:
      summary: Videos GetAdsStatus
      description: viddler.videos.getAdsStatusnGET
      operationId: videos-getadsstatus
      x-api-path-slug: viddler-videos-getadsstatus-get
      parameters:
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
      - GetAdsStatus
  viddler.videos.getEmbedCodeTypes:
    get:
      summary: Videos GetEmbedCodeTypes
      description: Return a list of the embed code types for your account.
      operationId: videos-getembedcodetypes
      x-api-path-slug: viddler-videos-getembedcodetypes-get
      parameters:
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - GetEmbedCodeTypes
  viddler.videos.getRecordToken:
    get:
      summary: Videos GetRecordToken
      description: Return a record token to use with Viddler&#8217;s Flash video recorder.
      operationId: videos-getrecordtoken
      x-api-path-slug: viddler-videos-getrecordtoken-get
      parameters:
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - GetRecordToken
  viddler.videos.prepareUpload:
    get:
      summary: Videos PrepareUpload
      description: Returns the end-point and token for a new upload session.
      operationId: videos-prepareupload
      x-api-path-slug: viddler-videos-prepareupload-get
      parameters:
      - in: query
        name: allow_replace
        description: Set to true if you are allowing the incoming upload to replace
          an already existing video
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - PrepareUpload
  viddler.videos.setClosedCaptioning:
    post:
      summary: Videos SetClosedCaptioning
      description: Update closed captioning details on a previously uploaded file.
      operationId: videos-setclosedcaptioning
      x-api-path-slug: viddler-videos-setclosedcaptioning-post
      parameters:
      - in: query
        name: closed_captioning_id
      - in: query
        name: default
      - in: query
        name: enabled
      - in: query
        name: language
        description: 'The language of the file (Max Characters: 50)'
      - in: query
        name: sessionid
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - SetClosedCaptioning
  viddler.videos.uploadProgress:
    get:
      summary: Videos UploadProgress
      description: Return the status of an upload.
      operationId: videos-uploadprogress
      x-api-path-slug: viddler-videos-uploadprogress-get
      parameters:
      - in: query
        name: sessionid
      - in: query
        name: token
      responses:
        200:
          description: OK
      tags:
      - Viddler
      - Videos
      - UploadProgress
---