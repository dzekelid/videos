---
swagger: "2.0"
info:
  title: Getty Images
  description: Build applications using the world's most powerful imagery
  version: 1.0.0
host: api.gettyimages.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/purchased-assets:
    get:
      summary: Get Purchased Images
      description: This endpoint returns a list of all assets purchased on gettyimages
      operationId: Purchases_GetPreviousAssetPurchases
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: header
        name: Authorization
        description: Provide access token in the format of 'Bearer {token}'
      - in: query
        name: end_date
        description: If specified, retrieves previous purchases on or before this
          date
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      - in: query
        name: start_date
        description: If specified, retrieves previous purchases on or after this date
      responses:
        200:
          description: OK
      tags:
      - images
      - purchases
definitions:
  AddBoardAssetsResult:
    properties:
      assets_added:
        description: This is a default description.
        type: get
      assets_not_added:
        description: This is a default description.
        type: get
  Asset:
    properties:
      asset_type:
        description: This is a default description.
        type: get
      date_added:
        description: This is a default description.
        type: get
      display_sizes:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
  AssetChanges:
    properties:
      change_set_id:
        description: This is a default description.
        type: get
      changed_assets:
        description: This is a default description.
        type: get
  BoardAsset:
    properties:
      asset_id:
        description: This is a default description.
        type: get
  BoardCommentPermissions:
    properties:
      can_add_comment:
        description: This is a default description.
        type: get
  BoardCreated:
    properties:
      id:
        description: This is a default description.
        type: get
  BoardDetail:
    properties:
      asset_count:
        description: This is a default description.
        type: get
      assets:
        description: This is a default description.
        type: get
      comment_count:
        description: This is a default description.
        type: get
      date_created:
        description: This is a default description.
        type: get
      date_last_updated:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  BoardInfo:
    properties:
      description:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  BoardList:
    properties:
      board_count:
        description: This is a default description.
        type: get
      boards:
        description: This is a default description.
        type: get
  BoardListBoard:
    properties:
      asset_count:
        description: This is a default description.
        type: get
      board_relationship:
        description: This is a default description.
        type: get
      date_created:
        description: This is a default description.
        type: get
      date_last_updated:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  BoardPermissions:
    properties:
      can_add_assets:
        description: This is a default description.
        type: get
      can_delete_board:
        description: This is a default description.
        type: get
      can_invite_to_board:
        description: This is a default description.
        type: get
      can_remove_assets:
        description: This is a default description.
        type: get
      can_update_description:
        description: This is a default description.
        type: get
      can_update_name:
        description: This is a default description.
        type: get
  ChangedAssetDetail:
    properties:
      asset_changed_utc_datetime:
        description: This is a default description.
        type: get
      asset_lifecycle:
        description: This is a default description.
        type: get
      asset_type:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  Collaborator:
    properties:
      first_name:
        description: This is a default description.
        type: get
      last_name:
        description: This is a default description.
        type: get
  Comment:
    properties:
      date_created:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      text:
        description: This is a default description.
        type: get
  CommentCreated:
    properties:
      id:
        description: This is a default description.
        type: get
  CommentPermissions:
    properties:
      can_delete_comment:
        description: This is a default description.
        type: get
  CommentRequest:
    properties:
      text:
        description: This is a default description.
        type: get
  CommentsList:
    properties:
      comments:
        description: This is a default description.
        type: get
  DisplaySize:
    properties:
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.AllowedUse:
    properties:
      how_can_i_use_it:
        description: This is a default description.
        type: get
      release_info:
        description: This is a default description.
        type: get
      usage_restrictions:
        description: This is a default description.
        type: get
  GettyImages.Models.Artists.DisplaySize:
    properties:
      aspect_ratio:
        description: This is a default description.
        type: get
      is_watermarked:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Artists.ImageSearchItem:
    properties:
      alternative_ids:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      asset_type:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      date_submitted:
        description: This is a default description.
        type: get
      display_sizes:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      keywords:
        description: This is a default description.
        type: get
  GettyImages.Models.Artists.ImageSearchResults:
    properties:
      images:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Artists.Keyword:
    properties:
      keyword_id:
        description: This is a default description.
        type: get
      text:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  GettyImages.Models.Artists.VideoSearchItem:
    properties:
      alternative_ids:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      asset_type:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      date_submitted:
        description: This is a default description.
        type: get
      display_sizes:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      keywords:
        description: This is a default description.
        type: get
  GettyImages.Models.Artists.VideoSearchResults:
    properties:
      result_count:
        description: This is a default description.
        type: get
      videos:
        description: This is a default description.
        type: get
  GettyImages.Models.Collections.Collection:
    properties:
      asset_family:
        description: This is a default description.
        type: get
      code:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      license_model:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      product_types:
        description: This is a default description.
        type: get
  GettyImages.Models.Collections.CollectionsList:
    properties:
      collections:
        description: This is a default description.
        type: get
  GettyImages.Models.Countries.CountriesList:
    properties:
      countries:
        description: This is a default description.
        type: get
  GettyImages.Models.Countries.Country:
    properties:
      iso_alpha_2:
        description: This is a default description.
        type: get
      iso_alpha_3:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  GettyImages.Models.CuratedSets.CuratedSet:
    properties:
      assets:
        description: This is a default description.
        type: get
      date_created:
        description: This is a default description.
        type: get
      date_last_updated:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      hero_image_uri:
        description: This is a default description.
        type: get
      keywords:
        description: This is a default description.
        type: get
      set_id:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  GettyImages.Models.Customers.CustomerInfoResponse:
    properties:
      email_address:
        description: This is a default description.
        type: get
      is_active:
        description: This is a default description.
        type: get
      user_name:
        description: This is a default description.
        type: get
  GettyImages.Models.Download:
    properties:
      agreement_name:
        description: This is a default description.
        type: get
      product_id:
        description: This is a default description.
        type: get
      product_type:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Downloads.GetDownloadsResponse:
    properties:
      downloads:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Downloads.GetDownloadsResponse.Download:
    properties:
      agreement_name:
        description: This is a default description.
        type: get
      asset_type:
        description: This is a default description.
        type: get
      date_downloaded:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      product_type:
        description: This is a default description.
        type: get
      size_name:
        description: This is a default description.
        type: get
      thumb_uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Downloads.GetDownloadsResponse.DownloadDetails:
    properties:
      download_notes:
        description: This is a default description.
        type: get
      project_code:
        description: This is a default description.
        type: get
  GettyImages.Models.Downloads.PremiumAccessDownloadData:
    properties:
      download_notes:
        description: This is a default description.
        type: get
      project_code:
        description: This is a default description.
        type: get
  GettyImages.Models.Downloads.User:
    properties:
      first_name:
        description: This is a default description.
        type: get
      last_name:
        description: This is a default description.
        type: get
      middle_name:
        description: This is a default description.
        type: get
      username:
        description: This is a default description.
        type: get
  GettyImages.Models.Events.Event:
    properties:
      child_event_count:
        description: This is a default description.
        type: get
      editorial_segments:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      image_count:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      start_date:
        description: This is a default description.
        type: get
  GettyImages.Models.Events.EventsResult:
    properties:
      events:
        description: This is a default description.
        type: get
      events_not_found:
        description: This is a default description.
        type: get
  GettyImages.Models.HeroImage:
    properties:
      display_sizes:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
  GettyImages.Models.HeroImageDisplaySize:
    properties:
      is_watermarked:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.IStockLicense:
    properties:
      credits:
        description: This is a default description.
        type: get
      license_type:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.EditorialSource:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.ImageDetail:
    properties:
      alternative_ids:
        description: This is a default description.
        type: get
      artist:
        description: This is a default description.
        type: get
      artist_title:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      asset_type:
        description: This is a default description.
        type: get
      call_for_image:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_id:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.ImageDetailDisplaySize:
    properties:
      height:
        description: This is a default description.
        type: get
      is_watermarked:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
      width:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.ImageDownloadAuthorization:
    properties:
      agreement_name:
        description: This is a default description.
        type: get
      product_id:
        description: This is a default description.
        type: get
      product_type:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.ImageDownloadSize:
    properties:
      bytes:
        description: This is a default description.
        type: get
      downloads:
        description: This is a default description.
        type: get
      height:
        description: This is a default description.
        type: get
      media_type:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      width:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.ImagesDetail:
    properties:
      images:
        description: This is a default description.
        type: get
      images_not_found:
        description: This is a default description.
        type: get
  GettyImages.Models.Images.Link:
    properties:
      rel:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Keyword:
    properties:
      entity_types:
        description: This is a default description.
        type: get
      entity_uris:
        description: This is a default description.
        type: get
      keyword_id:
        description: This is a default description.
        type: get
      relevance:
        description: This is a default description.
        type: get
      text:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  GettyImages.Models.LocationEvent:
    properties:
      city:
        description: This is a default description.
        type: get
      country:
        description: This is a default description.
        type: get
      state_province:
        description: This is a default description.
        type: get
      venue:
        description: This is a default description.
        type: get
  GettyImages.Models.MaxDimensions:
    properties:
      height:
        description: This is a default description.
        type: get
      width:
        description: This is a default description.
        type: get
  GettyImages.Models.Products.DownloadRequirements:
    properties:
      is_note_required:
        description: This is a default description.
        type: get
      is_project_code_required:
        description: This is a default description.
        type: get
      project_codes:
        description: This is a default description.
        type: get
  GettyImages.Models.Products.OverageDetails:
    properties:
      count:
        description: This is a default description.
        type: get
      limit:
        description: This is a default description.
        type: get
      overages_reached:
        description: This is a default description.
        type: get
      remaining:
        description: This is a default description.
        type: get
  GettyImages.Models.Products.Product:
    properties:
      agreement_name:
        description: This is a default description.
        type: get
      application_website:
        description: This is a default description.
        type: get
      credits_remaining:
        description: This is a default description.
        type: get
      download_limit:
        description: This is a default description.
        type: get
      download_limit_duration:
        description: This is a default description.
        type: get
      download_limit_reset_utc_date:
        description: This is a default description.
        type: get
      downloads_remaining:
        description: This is a default description.
        type: get
      expiration_utc_date:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      imagepack_resolution:
        description: This is a default description.
        type: get
  GettyImages.Models.Products.ProductsResult:
    properties:
      products:
        description: This is a default description.
        type: get
  GettyImages.Models.Purchases.PreviousAssetPurchase:
    properties:
      asset_id:
        description: This is a default description.
        type: get
      asset_type:
        description: This is a default description.
        type: get
      date_purchased:
        description: This is a default description.
        type: get
      download_uri:
        description: This is a default description.
        type: get
      file_size_in_bytes:
        description: This is a default description.
        type: get
      license_model:
        description: This is a default description.
        type: get
      order_id:
        description: This is a default description.
        type: get
      size_name:
        description: This is a default description.
        type: get
      thumb_uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Purchases.PreviousAssetPurchases:
    properties:
      previous_purchases:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Purchases.PreviousPurchase:
    properties:
      date_purchased:
        description: This is a default description.
        type: get
      image_id:
        description: This is a default description.
        type: get
      license_model:
        description: This is a default description.
        type: get
      order_id:
        description: This is a default description.
        type: get
      thumb_uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Purchases.PreviousPurchases:
    properties:
      previous_purchases:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.ReferralDestination:
    properties:
      site_name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.CreativeImageSearchLightResults:
    properties:
      images:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.CreativeImageSearchResults:
    properties:
      images:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.CreativeVideoSearchResults:
    properties:
      result_count:
        description: This is a default description.
        type: get
      videos:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.EditorialImageSearchResults:
    properties:
      images:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.EditorialSource:
    properties:
      id:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.EditorialVideoSearchResults:
    properties:
      result_count:
        description: This is a default description.
        type: get
      videos:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.EventsSearchResult:
    properties:
      events:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.ImageSearchItem:
    properties:
      alternative_ids:
        description: This is a default description.
        type: get
      artist:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      call_for_image:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_id:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      color_type:
        description: This is a default description.
        type: get
      copyright:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.ImageSearchItemCreative:
    properties:
      alternative_ids:
        description: This is a default description.
        type: get
      artist:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      call_for_image:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_id:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      color_type:
        description: This is a default description.
        type: get
      copyright:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.ImageSearchItemDisplaySize:
    properties:
      is_watermarked:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.ImageSearchItemEditorial:
    properties:
      alternative_ids:
        description: This is a default description.
        type: get
      artist:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      call_for_image:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_id:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      color_type:
        description: This is a default description.
        type: get
      copyright:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.ImageSearchLightItemCreative:
    properties:
      display_sizes:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.SearchResults[GettyImages.Models.Search.ImageSearchItem]:
    properties:
      images:
        description: This is a default description.
        type: get
      result_count:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.VideoSearchItem:
    properties:
      artist:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      clip_length:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_id:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      color_type:
        description: This is a default description.
        type: get
      copyright:
        description: This is a default description.
        type: get
      date_created:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.VideoSearchItemDisplaySize:
    properties:
      aspect_ratio:
        description: This is a default description.
        type: get
      is_watermarked:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Search.VideoSearchResults[GettyImages.Models.Artists.VideoSearchItem]:
    properties:
      result_count:
        description: This is a default description.
        type: get
      videos:
        description: This is a default description.
        type: get
  GettyImages.Models.Videos.VideoDetail:
    properties:
      artist:
        description: This is a default description.
        type: get
      asset_family:
        description: This is a default description.
        type: get
      caption:
        description: This is a default description.
        type: get
      clip_length:
        description: This is a default description.
        type: get
      collection_code:
        description: This is a default description.
        type: get
      collection_id:
        description: This is a default description.
        type: get
      collection_name:
        description: This is a default description.
        type: get
      color_type:
        description: This is a default description.
        type: get
      copyright:
        description: This is a default description.
        type: get
      date_created:
        description: This is a default description.
        type: get
  GettyImages.Models.Videos.VideoDetailDisplaySize:
    properties:
      aspect_ratio:
        description: This is a default description.
        type: get
      is_watermarked:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Videos.VideoDownloadAuthorization:
    properties:
      agreement_name:
        description: This is a default description.
        type: get
      product_id:
        description: This is a default description.
        type: get
      product_type:
        description: This is a default description.
        type: get
      uri:
        description: This is a default description.
        type: get
  GettyImages.Models.Videos.VideoDownloadSize:
    properties:
      bit_depth:
        description: This is a default description.
        type: get
      broadcast_video_standard:
        description: This is a default description.
        type: get
      compression:
        description: This is a default description.
        type: get
      content_type:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      downloads:
        description: This is a default description.
        type: get
      format:
        description: This is a default description.
        type: get
      frame_rate:
        description: This is a default description.
        type: get
      frame_size:
        description: This is a default description.
        type: get
      height:
        description: This is a default description.
        type: get
  GettyImages.Models.Videos.VideosDetail:
    properties:
      videos:
        description: This is a default description.
        type: get
      videos_not_found:
        description: This is a default description.
        type: get
  GettyImages.Services.Core.SecurityToken:
    properties:
      ActAsSystemId:
        description: This is a default description.
        type: get
      AdminId:
        description: This is a default description.
        type: get
      AuthId:
        description: This is a default description.
        type: get
      ClientIP:
        description: This is a default description.
        type: get
      ClientId:
        description: This is a default description.
        type: get
      Created:
        description: This is a default description.
        type: get
      Expires:
        description: This is a default description.
        type: get
      RememberedUser:
        description: This is a default description.
        type: get
      RenewalEnds:
        description: This is a default description.
        type: get
      SecureOnly:
        description: This is a default description.
        type: get
  Links:
    properties:
      invitation:
        description: This is a default description.
        type: get
      share:
        description: This is a default description.
        type: get
  Object:
    properties: []
  PartnerChannel:
    properties:
      asset_family:
        description: This is a default description.
        type: get
      channel_id:
        description: This is a default description.
        type: get
      channel_type:
        description: This is a default description.
        type: get
      notification_count:
        description: This is a default description.
        type: get
      start_date:
        description: This is a default description.
        type: get
  PartnerChannelList:
    properties:
      channels:
        description: This is a default description.
        type: get
  RegisterAssetsRequest:
    properties:
      asset_ids:
        description: This is a default description.
        type: get
  System.Object:
    properties: []
  asset_usage:
    properties:
      asset_id:
        description: This is a default description.
        type: get
      quantity:
        description: This is a default description.
        type: get
      usage_date:
        description: This is a default description.
        type: get
  report_usage_batch_request:
    properties:
      asset_usages:
        description: This is a default description.
        type: get
  report_usage_batch_response:
    properties:
      invalid_assets:
        description: This is a default description.
        type: get
      total_asset_usages_processed:
        description: This is a default description.
        type: get
x-collection-name: Getty Images
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