swagger: "2.0"
x-collection-name: Entertainment Express
x-complete: 1
info:
  title: Entertainment Express
  description: your-gateway-to-building-incredible-movie-tv-and-game-content-discovery-experiences-
  version: "2.0"
host: ee.iva-api.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Videos/GetVideo/{Id}:
    get:
      summary: Returns a URL to a requested video.
      description: "Returns a URL to the requested video. [Video Format Specs](https://developer.iva-api.com/docs/v1/video-formats)\n\n**Formats:**
        MP4 = 4, HLS = 11, Dash = 14, HSS = 12, HDS = 13\n\n**MP4 KbRate:** 80, 212,
        450, 750, 1500, 2500(HD sources only), 5000 (sources >=  1080p)  \n\n**Adaptive
        Min/Max rate:** 212000, 350000, 600000, 1200000, 2000000, 2500000, 3500000
        \ \n\n `URLs requested with a Demo account will always return max 750 kbps
        video.  Full commercial account required for higher bitrates.`"
      operationId: GetVideo
      x-api-path-slug: videosgetvideoid-get
      parameters:
      - in: query
        name: end
        description: Position in seconds to end video playback
      - in: query
        name: Expires
        description: UTC Time to video link should expire
      - in: query
        name: Format
        description: Video format
      - in: path
        name: Id
        description: Id of the Video from either MovieVideo, ShowVideo, SeasonVideo,
          EpisodeVideo object
      - in: query
        name: KbRate
        description: Video bitrate required for MP4 content
      - in: query
        name: MaxRate
        description: Adaptive Minimum rate
      - in: query
        name: MinRate
        description: Adaptive Maximum rate
      - in: query
        name: ReportTag
        description: Report tag used in video analytics
      - in: query
        name: start
        description: Position in seconds to start video playback
      responses:
        200:
          description: OK
      tags:
      - Videos
      - Video
      - Id
  /Analytics/VideoLog/:
    get:
      summary: Get Views by Video.
      description: No required parameters, DateValue defaults to Today.
      operationId: GetAnalyticsViewsByVideoLog
      x-api-path-slug: analyticsvideolog-get
      parameters:
      - in: query
        name: DateValue
        description: Days spanned by report
      - in: query
        name: End
        description: Report end date
      - in: query
        name: Limit
        description: Number of records returned from top of response
      - in: query
        name: ReportTag
        description: Report Tag filter
      - in: query
        name: Start
        description: Report start date
      responses:
        200:
          description: OK
      tags:
      - Analytics
      - VideoLog