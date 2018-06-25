---
name: Viddler
x-slug: viddler
description: www.viddler.com
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
x-kinRank: "8"
x-alexaRank: "81111"
tags: Videos
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/apis.md
specificationVersion: "0.14"
apis:
- name: Viddler  API Videos AddClosedCaptioning
  x-api-slug: viddler--api
  description: Add new closed captioning file for a specific video. All uploaded closed
    captioning files are enabled by default. The first uploaded file is default for
    a video.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.addClosedCaptioning
  tags: Viddler,Videos,AddClosedCaptioning
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-addclosedcaptioning-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-addclosedcaptioning-post-openapi.md
- name: Viddler  API Videos Comments Get
  x-api-slug: viddler--api
  description: Get comments for a video. If logged in and querying comments for own
    video &#8211; all comments with any moderation status will be returned. If quering
    comments as logged out or for not owned video &#8211; only approved comments will
    be returned if the video itself is public.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.comments.get
  tags: Viddler,Videos,Comments,Get
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-comments-get-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-comments-get-get-openapi.md
- name: Viddler  API Videos DelClosedCaptioning
  x-api-slug: viddler--api
  description: Remove an existing closed captioning file.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.delClosedCaptioning
  tags: Viddler,Videos,DelClosedCaptioning
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-delclosedcaptioning-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-delclosedcaptioning-post-openapi.md
- name: Viddler  API Videos Delete
  x-api-slug: viddler--api
  description: Delete a video.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.delete
  tags: Viddler,Videos,Delete
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-delete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-delete-post-openapi.md
- name: Viddler  API Videos EnableAds
  x-api-slug: viddler--api
  description: Turn ads off for specified videos.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.enableAds
  tags: Viddler,Videos,EnableAds
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-enableads-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-enableads-post-openapi.md
- name: Viddler  API Videos GetAdsStatus
  x-api-slug: viddler--api
  description: viddler.videos.getAdsStatusnGET
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.getAdsStatus
  tags: Viddler,Videos,GetAdsStatus
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-getadsstatus-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-getadsstatus-get-openapi.md
- name: Viddler  API Videos GetEmbedCodeTypes
  x-api-slug: viddler--api
  description: Return a list of the embed code types for your account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.getEmbedCodeTypes
  tags: Viddler,Videos,GetEmbedCodeTypes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-getembedcodetypes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-getembedcodetypes-get-openapi.md
- name: Viddler  API Videos GetRecordToken
  x-api-slug: viddler--api
  description: Return a record token to use with Viddler&#8217;s Flash video recorder.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.getRecordToken
  tags: Viddler,Videos,GetRecordToken
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-getrecordtoken-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-getrecordtoken-get-openapi.md
- name: Viddler  API Videos PrepareUpload
  x-api-slug: viddler--api
  description: Returns the end-point and token for a new upload session.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.prepareUpload
  tags: Viddler,Videos,PrepareUpload
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-prepareupload-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-prepareupload-get-openapi.md
- name: Viddler  API Videos SetClosedCaptioning
  x-api-slug: viddler--api
  description: Update closed captioning details on a previously uploaded file.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.setClosedCaptioning
  tags: Viddler,Videos,SetClosedCaptioning
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-setclosedcaptioning-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-setclosedcaptioning-post-openapi.md
- name: Viddler  API Videos UploadProgress
  x-api-slug: viddler--api
  description: Return the status of an upload.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2/viddler.videos.uploadProgress
  tags: Viddler,Videos,UploadProgress
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-uploadprogress-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/viddler-videos-uploadprogress-get-openapi.md
- name: Viddler  API
  x-api-slug: viddler--api
  description: The Viddler API exposes Viddler&rsquo;s key features to those that
    would like to build custom solutionson topof Viddler&rsquo;s video platform.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/274-viddler.jpg
  humanURL: http://www.viddler.com/
  baseURL: https://api.viddler.com//api/v2
  tags: Videos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/videos/master/_listings/viddler/openapi.md
x-common:
- type: x-base
  url: http://api.viddler.com/api/
- type: x-blog
  url: http://blog.viddler.com/
- type: x-blog-rss
  url: http://blog.viddler.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/viddler
- type: x-crunchbase
  url: https://crunchbase.com/organization/viddler
- type: x-developer
  url: http://developers.viddler.com/
- type: x-email
  url: sales@viddler.com
- type: x-email
  url: privacy@viddler.com
- type: x-email
  url: support@viddler.com
- type: x-email
  url: copyright@viddler.com
- type: x-faq
  url: http://www.viddler.com/help/
- type: x-github
  url: https://github.com/viddler
- type: x-google-plus
  url: https://plus.google.com/+viddler
- type: x-privacy
  url: http://www.viddler.com/privacy-policy/
- type: x-terms-of-service
  url: http://www.viddler.com/terms-of-use/
- type: x-twitter
  url: https://twitter.com/viddler
- type: x-website
  url: http://www.viddler.com/
- type: x-website
  url: http://viddler.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---