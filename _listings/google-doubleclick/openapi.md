---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 1
info:
  title: Google Doubleclick Merged API
  version: 1.0.0
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
---