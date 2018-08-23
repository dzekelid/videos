---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 1
info:
  title: Xibo API
  description: xibo-cms-api
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /playlist/widget/localVideo/{playlistId}:
    post:
      summary: Add a Local Video Widget
      description: Add a new Local Video Widget to the specified playlist
      operationId: WidgetLocalVideoAdd
      x-api-path-slug: playlistwidgetlocalvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: formData
        name: mute
        description: Flag (0, 1) Should the video be muted?
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: uri
        description: A local file path or URL to the video
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Local
      - Video
      - Widget
  /playlist/widget/video/{playlistId}:
    post:
      summary: Parameters for editing existing video on a layout
      description: Parameters for editing existing video on a layout, for adding new
        videos, please refer to POST /library documentation
      operationId: WidgetVideoEdit
      x-api-path-slug: playlistwidgetvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: loop
        description: Edit only - Flag (0, 1) Should the video loop (only for duration
          > 0 )?
      - in: formData
        name: mute
        description: Edit only - Flag (0, 1) Should the video be muted?
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Video
      - "On"
      - Layout
  /playlist/widget/videoin/{playlistId}:
    post:
      summary: Add a Video In Widget
      description: Add a new Video In Widget to the specified playlist
      operationId: WidgetVideoInAdd
      x-api-path-slug: playlistwidgetvideoinplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: The Widget Duration
      - in: path
        name: playlistId
        description: The playlist ID to add a Widget to
      - in: formData
        name: sourceId
        description: 'Which device input should be shown? available options: HDMI,
          RGB, DVI, DP, OPS'
      - in: formData
        name: useDuration
        description: Flag (0, 1) Select only if you will provide duration parameter
          as well
      responses:
        200:
          description: OK
      tags:
      - Video
      - In
      - Widget
---