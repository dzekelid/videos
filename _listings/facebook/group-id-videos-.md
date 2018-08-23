---
swagger: "2.0"
info:
  title: Facebook
  description: Facebook is an online social networking service that allows its users
    to connect with friends and family as well as make new connections. It provides
    its users with the ability to create a profile, update information, add images,
    send friend requests, and accept requests from other users. Its features include
    status update, photo tagging and sharing, and more.
  termsOfService: https://www.facebook.com/policies/
  version: 1.0.0
host: graph.facebook.com
basePath: v2.9/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{group-id}/videos:
    "":
      summary: Videos
      description: Videos for a Facebook Group
      operationId: videos
      parameters:
      - in: path
        name: group-id
        type: string
      responses:
        200:
          description: Successful Response
          schema:
            type: array
            items:
              $ref: '#/definitions/Videos'
      tags:
      - videos
definitions:
  Canvas_Button:
    properties:
      action:
        description: The action associated with the button
        type: string
      button_color:
        description: Color of the button
        type: string
      button_style:
        description: The style of the button
        type: string
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      deep_link:
        description: Deep link destination only for mobile apps          (used for
          mobile install or engagement ads, and app link is supported)
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      font_family:
        description: The font family
        type: string
      font_size:
        description: The size of the font for the text
        type: string
      line_height:
        description: The line height of the text
        type: string
  Achievement:
    properties:
      id:
        description: ID of this particular achievement.
        type: string
      from:
        description: The user who achieved this.
        type: string
      publish_time:
        description: Time at which this was achieved.
        type: string
      application:
        description: The app in which the user achieved this.
        type: string
      data:
        description: Information about the achievement type this instance is connected
          with.
        type: string
      achievement:
        description: The achievement type that the user achieved.
        type: string
      importance:
        description: A weighting given to each achievement type by the app.
        type: string
      type:
        description: Always game.achievement.
        type: string
      no_feed_story:
        description: Indicates whether gaining the achievement published a feed story
          for the user.
        type: string
  Comments:
    properties:
      order:
        description: 'Order in which comments were returned.ranked: The most interesting
          comments are sorted first.chronological: Comments sorted by the oldest comments
          first. reverse_chronological: Comments sorted by the newest comments first.'
        type: string
      total_count:
        description: 'The count of comments on this node. It is important to note
          that this value is changed depending on the filter modifier being used (where
          comment replies are available):if filter is stream then total_count will
          be a count of all comments (including replies) on the node.if filter is
          toplevel then total_count will be a count of all top-level comments on the
          node.Note: total_count can be greater than or equal to the actual number
          of comments returned due to comment privacy or deletion.'
        type: string
      message:
        description: The comment text. One of attachment_url, attachment_id, message
          or source must be provided when publishing.When a Page is publishing the
          comment, this message parameter can contain mentions of other Facebook Pages
          using the following syntax:&#064;[page-id]For example the following message
          would mention the Facebook Developers page inline:Test message &#064;[19292868552]
          tagUsage of this feature is subject to review but by using Pages you are
          an admin of (both to make the API call, and to be used in a mention), and
          an app you are a developer of, you can test it for yourself before review.
        type: string
      attachment_id:
        description: An optional ID of a unpublished photo (see no_story field in
          /&#123;user-id&#125;/photos) uploaded to Facebook to include as a photo
          comment. One of attachment_url, attachment_id, message or source must be
          provided when publishing.
        type: string
      attachment_url:
        description: The URL of an image to include as a photo comment. One of attachment_url,
          attachment_id, message or source must be provided when publishing.
        type: string
      source:
        description: A photo, encoded as form data, to use as a photo comment. One
          of attachment_url, attachment_id, message or source must be provided when
          publishing.
        type: string
  Likes:
    properties:
      total_count:
        description: Total number of people who liked. This is only returned when
          the flag summary=true is set.
        type: string
  Achievement_Type:
    properties:
      id:
        description: ID of the achievement type
        type: string
      type:
        description: The value will be games.achievement
        type: string
      title:
        description: Title of achievement
        type: string
      url:
        description: Unique URL of the achievement
        type: string
      description:
        description: Description of the achievement
        type: string
      image:
        description: Image for the achievement
        type: string
      width:
        description: Pixel width of the image
        type: string
      height:
        description: Pixel height of the image
        type: string
      data:
        description: An object containing the points this achievement is worth.
        type: string
      points:
        description: Number of points that this achievement is worth. Total points
          per game may not exceed 1000 points limit, which is enforced
        type: string
  Album:
    properties:
      id:
        description: The album ID.
        type: string
      can_upload:
        description: Whether the viewer can upload photos to this album.
        type: string
      count:
        description: The approximate number of photos in the album. This is not necessarily
          an exact count
        type: string
      cover_photo:
        description: The ID of the album&#039;s cover photo.
        type: string
      created_time:
        description: The time the album was initially created.
        type: string
      description:
        description: The description of the album.
        type: string
      event:
        description: The event associated with this album.
        type: string
      from:
        description: The profile that created the album.
        type: string
      link:
        description: A link to this album on Facebook.
        type: string
      location:
        description: The textual location of the album.
        type: string
  Photos:
    properties:
      source:
        description: The photo, encoded as form data. Either this or url field is
          required, but both should not be used together.
        type: string
      url:
        description: The URL of a photo that is already uploaded to the internet.
          Either this or source is required, but both should not be used together.
        type: string
      message:
        description: The description of the photo, used as the accompanying status
          message in any feed story.
        type: string
      place:
        description: Page ID of a place associated with the Photo.
        type: string
      no_story:
        description: If set to true, this will suppress the feed story that is automatically
          generated on a person&#039;s profile when they upload a photo using your
          app.
        type: string
  App_Link_Host:
    properties:
      id:
        description: The app link host IDDefault
        type: string
      android:
        description: The app links defined for the Android platform
        type: string
      application:
        description: The application that created this app link host
        type: string
      canonical_url:
        description: The Facebook URL that hosts the app link meta tags.Default
        type: string
      ios:
        description: The app links defined for the iOS platform
        type: string
      ipad:
        description: The app links defined for the iPad device
        type: string
      iphone:
        description: The app links defined for the iPhone device
        type: string
      name:
        description: The name of the app link host
        type: string
      web:
        description: The web redirect when the canonical url is loaded in a browser
        type: string
      windows:
        description: The app links defined for the Windows platform
        type: string
  App_Request:
    properties:
      id:
        description: The ID of an individual requestCore
        type: string
      action_type:
        description: Request action type for structured request
        type: string
      application:
        description: The app used to send the requestCoreDefault
        type: string
      created_time:
        description: Timestamp when the request was sentCoreDefault
        type: string
      data:
        description: Optional data passed with the request for tracking purposesDefault
        type: string
      from:
        description: The user who sent the request. This is not present for app-to-user
          requests made with the Graph APICoreDefault
        type: string
      message:
        description: The message included with the requestCoreDefault
        type: string
      object:
        description: Open Graph object for structured request. Note the type of object
          should belong to this app
        type: string
      to:
        description: The user who received the requestCoreDefault
        type: string
  Application:
    properties:
      id:
        description: The app IDCore
        type: string
      an_platforms:
        description: The platforms associated with the app in the Audience Network
          product. Not enforced, but when present, it can be used to provide the user
          with platform specific information for the app and its placements
        type: string
      app_ad_debug_info:
        description: App ad related information to help debugging.
        type: string
      app_domains:
        description: Domains and subdomains this app can use
        type: string
      app_install_tracked:
        description: Whether the app install is trackable or not
        type: string
      app_name:
        description: App name
        type: string
      app_type:
        description: App type
        type: string
      auth_dialog_data_help_url:
        description: The URL of a special landing page that helps people who are using
          an app begin publishing Open Graph activity
        type: string
      auth_dialog_headline:
        description: One line description of an app that appears in the Login Dialog
        type: string
      auth_dialog_perms_explanation:
        description: The text to explain why an app needs additional permissions.  This
          appears in the Login Dialog
        type: string
  Application_Context:
    properties:
      id:
        description: The token representing the social context
        type: string
  Audience_Insights_Rule:
    properties:
      id:
        description: IDDefault
        type: string
      description:
        description: Description of the study rule.Default
        type: string
      name:
        description: Name of the study rule. If no name was provided at the creation,
          we autogenerated one.Default
        type: string
      rule_components:
        description: Rule componentsDefault
        type: string
  Canvas_Carousel:
    properties:
      child_elements:
        description: The child elements of the carousel
        type: string
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      name:
        description: The name of the elementDefault
        type: string
      style:
        description: The presentation style of the carousel
        type: string
      top_padding:
        description: The padding above the element
        type: string
  Canvas_Footer:
    properties:
      child_elements:
        description: The child elements inside a footer
        type: string
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      name:
        description: The name of the elementDefault
        type: string
      top_padding:
        description: The padding above the element
        type: string
  Canvas_Header:
    properties:
      background_color:
        description: The background color of the header
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      child_elements:
        description: The child elements (typically a photo) inside the header
        type: string
      id:
        description: The id of the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      name:
        description: The name of the elementDefault
        type: string
      top_padding:
        description: The padding above the element
        type: string
  Canvas_Photo:
    properties:
      action:
        description: The action associated with the photo
        type: string
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      deep_link:
        description: Deep link destination only for mobile apps          (used for
          mobile install or engagement ads, and app link is supported)
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      name:
        description: The name of the elementDefault
        type: string
      photo:
        description: The facebook photo node
        type: string
      style:
        description: The presentation style of the photo node
        type: string
      top_padding:
        description: The padding above the element
        type: string
      open_url_action:
        description: The action associated with the photo
        type: string
  Canvas_Product_Set:
    properties:
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      max_products:
        description: Maximum number of products to show
        type: string
      name:
        description: The name of the elementDefault
        type: string
      product_set_id:
        description: The product set id which contains a subset of products within
          a product catalog
        type: string
      top_padding:
        description: The padding above the element
        type: string
      max_items:
        description: Maximum number of products to show
        type: string
  Canvas_Store_Locator:
    properties:
      header_background_color:
        description: Header background color for the store locator
        type: string
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      name:
        description: The name of the elementDefault
        type: string
      top_padding:
        description: The padding above the element
        type: string
      typeface:
        description: Font used to display info about the store
        type: string
      page_set_id:
        description: The page set id used for the store locator
        type: string
  Canvas_Text:
    properties:
      background_color:
        description: The color of the background for the element
        type: string
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      font_family:
        description: The font family
        type: string
      font_size:
        description: The size of the font for the text
        type: string
      line_height:
        description: The line height of the text
        type: string
      name:
        description: The name of the elementDefault
        type: string
      rich_text:
        description: The text content of the element
        type: string
      text_alignment:
        description: The alignment of the text
        type: string
  Canvas_Video:
    properties:
      id:
        description: The id of the element
        type: string
      bottom_padding:
        description: The padding below the element
        type: string
      element_type:
        description: The type of the elementDefault
        type: string
      name:
        description: The name of the elementDefault
        type: string
      style:
        description: The presentation style of the video
        type: string
      top_padding:
        description: The padding above the element
        type: string
      video:
        description: The facebook video node
        type: string
      video_id:
        description: ID of Facebook video used in the video element
        type: string
  Comment:
    properties:
      id:
        description: The comment ID
        type: string
      attachment:
        description: Link or photo attached to the comment
        type: string
      can_comment:
        description: Whether the viewer can reply to this comment
        type: string
      can_remove:
        description: Whether the viewer can remove this comment
        type: string
      can_hide:
        description: Whether the viewer can hide this comment.  Only visible to a
          page admin
        type: string
      can_like:
        description: Whether the viewer can like this comment
        type: string
      can_reply_privately:
        description: Whether the viewer can send a private reply to this comment (Page
          viewers only)
        type: string
      comment_count:
        description: Number of replies to this comment
        type: string
      created_time:
        description: The time this comment was made
        type: string
      from:
        description: The person that made this comment
        type: string
  Private_replies:
    properties:
      message:
        description: The text of the reply. This field is required.
        type: string
  Conversation:
    properties:
      id:
        description: The ID of a conversation, in a format similar to t_id.000000000000000.
        type: string
      snippet:
        description: The snippet of the most recent message in a conversation.
        type: string
      updated_time:
        description: Last update time.
        type: string
      message_count:
        description: The number of messages.
        type: string
      unread_count:
        description: The number of unread messages.
        type: string
      tags:
        description: A set of tags indicating the message folder and source of the
          conversation.
        type: string
      name:
        description: The name of the message folder or source.
        type: string
      participants:
        description: People and Pages who are on this conversation.
        type: string
      senders:
        description: People who have sent a message.
        type: string
      can_reply:
        description: Whether the Page is able to reply.
        type: string
  Messages:
    properties:
      tags:
        description: A set of tags indicating the message folder and source of the
          message.
        type: string
      name:
        description: The name of the message folder or source.
        type: string
      message:
        description: The text of reply. This field is required.
        type: string
  Crisis:
    properties:
      id:
        description: The id of the object
        type: string
      creation_time:
        description: When this Safety Check instance was created, which is not necessarily
          the time when the actual event happened. It is best to use the date of this
          time, not the specific hour
        type: string
      geo_area:
        description: The crisis geo area that this crisis affects
        type: string
      main_location_page:
        description: The actual geographic area that encompasses a Safety Check instance
          can be cities, regions, or countries. However we use one main location page
          to name the crisis, and usually to center the map
        type: string
      name:
        description: The name of the Safety Check instance, like &quot;the Flooding
          in West Virginia&quot;. This name is localized to each locale based on the
          viewer locale
        type: string
      permalink_uri:
        description: The absolute permalink URI of the Safety Check instance, where
          users can go to check on their friends or interact with other features
        type: string
  Crisis_Listing:
    properties:
      id:
        description: The id of the object
        type: string
      author:
        description: The person who posted this listing
        type: string
      creation_time:
        description: Time when the post was created
        type: string
      for_num_people:
        description: The number of people this request is for, omitted from certain
          categories (like pet supplies)
        type: string
      latitude:
        description: The approximate latitude GPS location of this listing; the real
          location is not provided due to privacy concerns. Useful for plotting on
          a map
        type: string
      listing_category:
        description: The category that this offer or request is for
        type: string
      listing_type:
        description: The listing type represents whether this post is requesting help
          or offering help; however, it also has two other states, a &quot;closed
          request&quot; and a &quot;closed offer&quot; which represents the user closed
          this post out. Posts with the latter types should no longer be shown on
          the map
        type: string
      longitude:
        description: The approximate longitude GPS location of this listing; the real
          location is not provided due to privacy concerns. Useful for plotting on
          a map
        type: string
      message:
        description: An associated message with the offer or request, optional
        type: string
      permalink_uri:
        description: The uri of this Community Help post, where users can like, comment
          on, or share the post
        type: string
  Debug_Token:
    properties:
      data:
        description: Data wrapper around the result.
        type: string
      app_id:
        description: The ID of the application this access token is for.
        type: string
      application:
        description: Name of the application this access token is for.
        type: string
      error:
        description: Any error that a request to the graph api would return due to
          the access token.
        type: string
      code:
        description: The error code for the error.
        type: string
      message:
        description: The error message for the error.
        type: string
      subcode:
        description: The error subcode for the error.
        type: string
      expires_at:
        description: Timestamp when this access token expires.
        type: string
      is_valid:
        description: Whether the access token is still valid or not.
        type: string
      issued_at:
        description: Timestamp when this access token was issued.
        type: string
  Doc:
    properties:
      id:
        description: The document ID
        type: string
      can_delete:
        description: Boolean, can document be deleted by viewerDefault
        type: string
      can_edit:
        description: Boolean, can document be edited by viewerDefault
        type: string
      created_time:
        description: Timestamp of when the document was createdDefault
        type: string
      from:
        description: Author of the documentDefault
        type: string
      icon:
        description: Image file for document iconDefault
        type: string
      link:
        description: URL for the documentDefault
        type: string
      message:
        description: Content of the documentDefault
        type: string
      revision:
        description: Current revision IDDefault
        type: string
      subject:
        description: Title of the documentDefault
        type: string
  Domain:
    properties:
      id:
        description: The ID of the domain.
        type: string
      name:
        description: The name of the domain.
        type: string
  Education_Experience:
    properties:
      id:
        description: id
        type: string
      classes:
        description: Classes takenDefault
        type: string
      concentration:
        description: Facebook Pages representing subjects studiedDefault
        type: string
      degree:
        description: The Facebook Page for the degree obtainedDefault
        type: string
      school:
        description: The Facebook Page for this schoolDefault
        type: string
      type:
        description: The type of educational institutionDefault
        type: string
      with:
        description: People tagged who went to school with this personDefault
        type: string
      year:
        description: Facebook Page for the year this person graduatedDefault
        type: string
  Event:
    properties:
      id:
        description: The event ID
        type: string
      attending_count:
        description: Number of people attending the event
        type: string
      can_guests_invite:
        description: Can guests invite friends
        type: string
      can_viewer_post:
        description: Whether a user has permission to post on the event timeline
        type: string
      category:
        description: The category of the event
        type: string
      cover:
        description: Cover picture
        type: string
      declined_count:
        description: Number of people who declined the event
        type: string
      description:
        description: Long-form descriptionDefault
        type: string
      end_time:
        description: End time, if one has been setDefault
        type: string
      guest_list_enabled:
        description: Can see guest list
        type: string
  Friends:
    properties:
      id:
        description: The friend list IDDefault
        type: string
      list_type:
        description: The type of the friend listDefault
        type: string
      name:
        description: The name of the friend listDefault
        type: string
      owner:
        description: The owner of the friend list
        type: string
  Group:
    properties:
      id:
        description: The group ID
        type: string
      cover:
        description: Information about the group&#039;s cover photo.
        type: string
      source:
        description: URL to the Photo that represents this cover photo.
        type: string
      offset_y:
        description: The vertical offset in pixels of the photo from the bottom.
        type: string
      offset_x:
        description: The horizontal offset in pixels of the photo from the left.
        type: string
      description:
        description: A brief description of the group.
        type: string
      email:
        description: The email address to upload content to the group. Only current
          members of the group can use this.
        type: string
      icon:
        description: The URL for the group&#039;s icon.
        type: string
      member_request_count:
        description: The number of pending member requests. If the token is for an
          administrator, this is the total number of outstanding requests.  If the
          token is for a group member, this will return the number of friends who
          have requested membership and also use the same app that is making the request.
        type: string
      name:
        description: The name of the group.
        type: string
  Admins:
    properties:
      member:
        description: The user to make an admin. They must be a member of the group
          and user of the app. This is required.
        type: string
      uid:
        description: The admin to remove. This is required.
        type: string
  Albums:
    properties:
      name:
        description: The name given to the album. This field is required.
        type: string
      message:
        description: The description of the album, which will show up in news feed
          stories as the status message.
        type: string
      privacy:
        description: Privacy settings for the album. If not supplied, this defaults
          to the privacy level granted to the app in the Login Dialog. This field
          cannot be used to set a more open privacy setting than the one granted.
        type: string
      value:
        description: The value of the privacy setting.
        type: string
      allow:
        description: When value is CUSTOM, this is a comma-separated list of user
          IDs and friend list IDs that can see the post. This can also be ALL_FRIENDS
          or FRIENDS_OF_FRIENDS to include all members of those sets.
        type: string
      deny:
        description: When value is CUSTOM, this is a comma-separated list of user
          IDs and friend list IDs that cannot see the post.
        type: string
  Feed:
    properties:
      message:
        description: The main body of the post, otherwise called the status message.
          Either link or message must be supplied.
        type: string
      link:
        description: The URL of a link to attach to the post. Either link or message
          must be supplied. Additional fields associated with link are shown below.
        type: string
  Files:
    properties:
      id:
        description: The ID of the file. Note that you cannot request each file individually
          by its ID, only through this edge.
        type: string
      from:
        description: The person who uploaded the file.
        type: string
      group:
        description: The group the file is uploaded to (the same group as in the request).
        type: string
      download_link:
        description: URL to download the file.
        type: string
      updated_time:
        description: The last time the file was changed.
        type: string
  Members:
    properties:
      administrator:
        description: Whether or not the person is a group admin.
        type: string
      member:
        description: The user to invite. They must have a role in the app such as
          admin, developer, or tester. This is required.
        type: string
      from:
        description: The user ID of someone that can appear as the sender of the group
          invite. If this field is used, the two people must be friends on Facebook
          for the invite to send. This field is optional.
        type: string
  Videos:
    properties:
      id:
        description: The target ID where the video is posted to.
        type: string
      title:
        description: The title of the video.
        type: string
      description:
        description: The description of the video, used as the accompanying status
          message in any feed story. This parameter can contain mentions of other
          Facebook Pages using the following syntax:&#064;[page-id]For example the
          following description would mention the Facebook Developers page inline:Test
          message &#064;[19292868552] tagUsage of this feature is subject to review
          but by using Pages you are an admin of (both to make the API call, and to
          be used in a mention), and an app you are a developer of, you can test it
          for yourself before review.
        type: string
      source:
        description: The video, encoded as form data. This field is required.
        type: string
      file_url:
        description: Accessible URL of a video file. Cannot be used with upload_phase.
        type: string
      thumb:
        description: The video thumbnail raw data to be uploaded and associated with
          a video.
        type: string
      upload_phase:
        description: Type of chunked upload request.
        type: string
      file_size:
        description: The size of the entire video file in bytes.
        type: string
      start_offset:
        description: Start byte position of the file chunk.
        type: string
      video_file_chunk:
        description: The video file chunk, encoded as form data. This field is required
          during transfer upload phase.
        type: string
  Group_Doc:
    properties:
      id:
        description: The group doc ID.
        type: string
      from:
        description: The profile that created this doc.
        type: string
      subject:
        description: The title of the doc.
        type: string
      message:
        description: The body of the doc. This string will contain HTML for any formatting
          in the doc, and will be HTML encoded.
        type: string
      icon:
        description: The URL for the doc&#039;s icon
        type: string
      created_time:
        description: When the doc was created.
        type: string
      updated_time:
        description: The last time the doc was changed.
        type: string
      revision:
        description: An ID representing the current doc revision.
        type: string
      can_edit:
        description: Whether the session user can edit this doc.
        type: string
      can_delete:
        description: Whether the session user can delete this doc (on Facebook.com).
        type: string
  Instagram_Carousel:
    properties:
      id:
        description: ID of the Instagram carousel
        type: string
      caption_text:
        description: Caption text
        type: string
      comment_count:
        description: Number of comments
        type: string
      content_type:
        description: 0 for photo, 1 for video
        type: string
      display_url:
        description: URL of the photo or cover frame
        type: string
      like_count:
        description: Number of likes
        type: string
      owner_instagram_user:
        description: The Instagram user that owns this carousel
        type: string
      permalink:
        description: Instagram permalink of the first asset
        type: string
      taken_at:
        description: When the media was created
        type: string
      video_url:
        description: URL of the video
        type: string
  Instagram_Comment:
    properties:
      comment_type:
        description: Enum indicating the type of comment &#123;CAPTION, NORMAL, UNKNOWN&#125;
        type: string
      created_at:
        description: Creation time of the comment in milliseconds
        type: string
      id:
        description: Base 64 encoded string of instagram_media_id and instagram_comment_id
        type: string
      instagram_comment_id:
        description: Id of the comment in instagram
        type: string
      instagram_user:
        description: Instagram user who made the comment
        type: string
      mentioned_instagram_users:
        description: Instagram users that are mentioned in the comment
        type: string
      message:
        description: Textual message content of the Instagram comment
        type: string
      ad_id:
        description: Ad id associated to this Instagram MediaRequired
        type: string
      hide:
        description: Boolean denoting whether the comment is to be hidden or unhiddenRequired
        type: string
  Instagram_Media:
    properties:
      id:
        description: ID of the Instagram media
        type: string
      caption_text:
        description: Caption text
        type: string
      comment_count:
        description: Number of comments
        type: string
      content_type:
        description: 0 for photo, 1 for video
        type: string
      display_url:
        description: URL of the photo or cover frame
        type: string
      filter_name:
        description: Name of filter
        type: string
      latitude:
        description: Latitude of the location
        type: string
      like_count:
        description: Number of likes
        type: string
      location:
        description: Location data
        type: string
      location_name:
        description: Name of location for location tag
        type: string
  Instagram_User:
    properties:
      id:
        description: ID of the Instagram user
        type: string
      follow_count:
        description: Number of Instagram users that this Instagram user follows
        type: string
      followed_by_count:
        description: Number of Instagram users that follow this Instagram user
        type: string
      has_profile_picture:
        description: Indicates whether Instagram Account has a profile picture
        type: string
      is_private:
        description: Whether the Instagram user is private
        type: string
      is_published:
        description: Whether the Instagram user is published
        type: string
      media_count:
        description: Number of active media posted by this Instagram user
        type: string
      profile_pic:
        description: URI to user&#039;s Instagram profile picture
        type: string
      username:
        description: Instagram username
        type: string
  Life_Event:
    properties:
      created_time:
        description: The time when this milestone was publishedDefault
        type: string
      description:
        description: Description of the milestoneDefault
        type: string
      end_time:
        description: The time when this milestone came to an endDefault
        type: string
      from:
        description: The information of the Page that ownes the milestoneDefault
        type: string
      id:
        description: The milestone IDDefault
        type: string
      is_hidden:
        description: Whether the milestone is hidden or notDefault
        type: string
      start_time:
        description: The time when this milestone was startedDefault
        type: string
      title:
        description: The title of the milestoneDefault
        type: string
      updated_time:
        description: The time when this milestone was updatedDefault
        type: string
  Link:
    properties:
      id:
        description: The link ID.
        type: string
      created_time:
        description: The time the message was published.
        type: string
      description:
        description: A description of the link (appears beneath the link caption).
        type: string
      from:
        description: The user that created the link.
        type: string
      icon:
        description: A URL to the link icon that Facebook displays in the news feed.
        type: string
      link:
        description: The URL that was shared.
        type: string
      message:
        description: The optional message from the user about this link.
        type: string
      name:
        description: The name of the link.
        type: string
      picture:
        description: A URL to the thumbnail image used in the link post
        type: string
  Live_Video:
    properties:
      id:
        description: The live video ID
        type: string
      broadcast_start_time:
        description: The time the video was initially published
        type: string
      copyright:
        description: The copyright information for the live video
        type: string
      creation_time:
        description: The creation time of the live video
        type: string
      dash_preview_url:
        description: Preview URL for dash player
        type: string
      description:
        description: The description of the live video
        type: string
      embed_html:
        description: The embed html of the live videoDefault
        type: string
      from:
        description: The originator of the live video
        type: string
      is_manual_mode:
        description: Whether schedule live is in manual mode, in which live video
          will start manually instead of on schedled time
        type: string
      is_reference_only:
        description: Whether the live video is exclusively used for copyright monitoring
        type: string
  Mailing_Address:
    properties:
      id:
        description: The mailing address IDDefault
        type: string
      city:
        description: Address city nameDefault
        type: string
      city_page:
        description: Page representing the address city
        type: string
      country:
        description: Country of the addressDefault
        type: string
      postal_code:
        description: Postal code of the addressDefault
        type: string
      region:
        description: Region or state of the addressDefault
        type: string
      street1:
        description: Street addressDefault
        type: string
      street2:
        description: Second part of the street address - apt, suite, etcDefault
        type: string
  Media_Fingerprint:
    properties:
      id:
        description: Media fingerprint IDDefault
        type: string
      duration_in_sec:
        description: The length of the fingerprinted content, in secondsDefault
        type: string
      fingerprint_content_type:
        description: Media fingerprint content typeDefault
        type: string
      fingerprint_type:
        description: The fingerprint typeDefault
        type: string
      metadata:
        description: The metadata associated with the fingerprinted content
        type: string
      title:
        description: The title of the fingerprinted content
        type: string
      universal_content_id:
        description: 'A unique code user can use to manage fingerprint. For example:
          International Standard Recording Code for songtracks. This is for your own
          use; Facebook will not use this data.'
        type: string
      album:
        description: Album name of a songtrack. This is a required metadata field
          for SONGTRACK content type.
        type: string
      artist:
        description: Artist name of a songtrack. This is a required metadata field
          for SONGTRACK content type.
        type: string
      episode:
        description: Episode name of an episode. This is a required metadata field
          for EPISODE content type.
        type: string
  Message:
    properties:
      created_time:
        description: A timestamp of when this message was created
        type: string
      from:
        description: The sender of this message.
        type: string
      id:
        description: The unique ID for this message.
        type: string
      message:
        description: The text of the message.
        type: string
      subject:
        description: The subject of the message.
        type: string
      tags:
        description: A set of tags indicating the message folder and source of the
          message.
        type: string
      to:
        description: A list of recipients of the message.
        type: string
  Attachments:
    properties:
      id:
        description: The attachment ID.
        type: string
      mime_type:
        description: The file MIME type.
        type: string
      name:
        description: The filename of the attachment.
        type: string
      size:
        description: The file size in bytes.
        type: string
      description:
        description: Text accompanying the attachment
        type: string
      description_tags:
        description: Profiles tagged in the text accompanying the attachment
        type: string
      media:
        description: Media object (photo, link etc.) contained in the attachment
        type: string
      image:
        description: An image in the attachment
        type: string
      height:
        description: Height of the image
        type: string
      src:
        description: URI of the image
        type: string
  Shares:
    properties:
      description:
        description: The description of the shared item.
        type: string
      link:
        description: The URL to the shared item.
        type: string
      id:
        description: The shared item ID.
        type: string
      name:
        description: The title of the shared item.
        type: string
  Milestone:
    properties:
      id:
        description: The ID of a milestone event
        type: string
      title:
        description: The title of the milestone
        type: string
      from:
        description: The Page that posted the milestone.
        type: string
      description:
        description: The description of the milestone
        type: string
      created_time:
        description: The creation time of the milestone
        type: string
      updated_time:
        description: The update time of the milestone
        type: string
      start_time:
        description: The start time of the milestone
        type: string
      end_time:
        description: The end time of the milestone. Page milestones have the same
          start and end time
        type: string
  Native_Offer:
    properties:
      id:
        description: The id of the native offer.Default
        type: string
      barcode_photo:
        description: Barcode image ID for in-store redemption.
        type: string
      barcode_photo_uri:
        description: Barcode image URI for in-store redemption.
        type: string
      barcode_type:
        description: Barcode type for in-store redemption.
        type: string
      barcode_value:
        description: Barcode value for in-store redemption.
        type: string
      details:
        description: Additional primary text describing the native offer.
        type: string
      disable_location:
        description: Whether or not the location features, such as the map and nearby
          notification, are disabled.
        type: string
      discounts:
        description: A structured representation of each part of the deal.
        type: string
      expiration_time:
        description: The time when the native offer expires, as a UNIX timestamp.
          After this time, the native offer will not be available for users to save.
        type: string
      instore_code:
        description: The code used to redeem the native offer in-store.
        type: string
  Notification:
    properties:
      id:
        description: The notification&#039;s id.
        type: string
      from:
        description: The entity (user, page, app, etc.) that &#039;sent&#039;, or
          is the source of the notification.
        type: string
      to:
        description: The entity that received the notification.
        type: string
      created_time:
        description: When the notification was created.
        type: string
      updated_time:
        description: When the notification was last updated.
        type: string
      title:
        description: The message text in the notification.
        type: string
      link:
        description: The URL that clicking on the notification would take someone.
        type: string
      application:
        description: The app responsible for generating the notification. Some of
          the core Facebook features have their own app that shows up here, such as
          likes when someone likes another person&#039;s content.
        type: string
      unread:
        description: Indicates that the notification is unread. Note that &#039;read&#039;
          notifications will not be accessible.
        type: string
      object:
        description: The object (this can be a post, a photo, a comment, etc.) that
          was the subject of the notification.
        type: string
  Object_Comments:
    properties:
      order:
        description: 'Order in which comments were returned.ranked: The most interesting
          comments are sorted first.chronological: Comments sorted by the oldest comments
          first. reverse_chronological: Comments sorted by the newest comments first.'
        type: string
      total_count:
        description: 'The count of comments on this node. It is important to note
          that this value is changed depending on the filter modifier being used (where
          comment replies are available):if filter is stream then total_count will
          be a count of all comments (including replies) on the node.if filter is
          toplevel then total_count will be a count of all top-level comments on the
          node.Note: total_count can be greater than or equal to the actual number
          of comments returned due to comment privacy or deletion.'
        type: string
      message:
        description: The comment text. One of attachment_url, attachment_id, message
          or source must be provided when publishing.When a Page is publishing the
          comment, this message parameter can contain mentions of other Facebook Pages
          using the following syntax:&#064;[page-id]For example the following message
          would mention the Facebook Developers page inline:Test message &#064;[19292868552]
          tagUsage of this feature is subject to review but by using Pages you are
          an admin of (both to make the API call, and to be used in a mention), and
          an app you are a developer of, you can test it for yourself before review.
        type: string
      attachment_id:
        description: An optional ID of a unpublished photo (see no_story field in
          /&#123;user-id&#125;/photos) uploaded to Facebook to include as a photo
          comment. One of attachment_url, attachment_id, message or source must be
          provided when publishing.
        type: string
      attachment_url:
        description: The URL of an image to include as a photo comment. One of attachment_url,
          attachment_id, message or source must be provided when publishing.
        type: string
      source:
        description: A photo, encoded as form data, to use as a photo comment. One
          of attachment_url, attachment_id, message or source must be provided when
          publishing.
        type: string
  Object_Likes:
    properties:
      total_count:
        description: Total number of people who liked. This is only returned when
          the flag summary=true is set.
        type: string
  Open_Graph_Action_Type:
    properties:
      id:
        description: ID
        type: string
      allow_multiple_references:
        description: Whether multiple objects can be referenced by the action
        type: string
      app_preposition:
        description: The preposition used to address the app
        type: string
      button_text:
        description: Button text
        type: string
      description:
        description: Description
        type: string
      is_app_secret_required:
        description: Whether the app secret is required for API calls related to actions
          of this type
        type: string
      name:
        description: NameDefault
        type: string
      object_types:
        description: Object types associated with this action type
        type: string
      plural_past:
        description: The plural past form of the action
        type: string
      plural_present:
        description: The plural present form of the action
        type: string
  Open_Graph_Context:
    properties:
      id:
        description: The token representing the social context
        type: string
  Open_Graph_Object_Type:
    properties:
      id:
        description: ID
        type: string
      article:
        description: An article for the type name
        type: string
      name:
        description: A noun representing the typeDefault
        type: string
      plural:
        description: The plural form of the object
        type: string
      property_config:
        description: Per-property config
        type: string
      singular:
        description: The singular form of the object
        type: string
      type:
        description: Type nameDefault
        type: string
  Page:
    properties:
      id:
        description: Page ID. No access token is required to access this fieldCore
        type: string
      about:
        description: Information about the Page
        type: string
      access_token:
        description: The access token you can use to act as the Page. Only visible
          to Page Admins. If your business requires two-factor authentication, and
          the person hasn&#039;t authenticated, this field may not be returned
        type: string
      ad_campaign:
        description: The Page&#039;s currently running promotion campaign
        type: string
      affiliation:
        description: Affiliation of this person. Applicable to Pages representing
          people
        type: string
      app_id:
        description: App ID for app-owned Pages and app Pages
        type: string
      app_links:
        description: AppLinks data associated with the Page&#039;s URL
        type: string
      artists_we_like:
        description: Artists the band likes. Applicable to Bands
        type: string
      attire:
        description: Dress code of the business. Applicable to Restaurants or Nightlife.
          Can be one of Casual, Dressy or Unspecified
        type: string
      awards:
        description: The awards information of the film. Applicable to Films
        type: string
  Page_Admin_Note:
    properties:
      body:
        description: Content of this note
        type: string
      from:
        description: Page that owns the note
        type: string
      id:
        description: ID of the tagDefault
        type: string
      user:
        description: The user that this note is attached to
        type: string
      user_id:
        description: ID of the user that this note is associate with.Required
        type: string
  Page_Call_To_Action:
    properties:
      android_app:
        description: App that stores the destination info on Android
        type: string
      android_deeplink:
        description: Destination deeplink for the call-to-action on Android
        type: string
      android_destination_type:
        description: Destination type for the call-to-action on Android
        type: string
      android_package_name:
        description: Destination app for the call-to-action on Android
        type: string
      android_url:
        description: Destination url for the call-to-action on Android
        type: string
      created_time:
        description: Time when the call-to-action was created
        type: string
      email_address:
        description: Email address that can be contacted by a user
        type: string
      id:
        description: ID of the call-to-actionDefault
        type: string
      from:
        description: Page that owns the call-to-action
        type: string
      intl_number_with_plus:
        description: International phone number with plus that can be called by a
          phone
        type: string
  Page_Label:
    properties:
      creation_time:
        description: Time when the label was created
        type: string
      creator_id:
        description: Admin who created the label
        type: string
      from:
        description: Page that owns the label
        type: string
      id:
        description: ID of the labelDefault
        type: string
      name:
        description: Name of the labelDefault
        type: string
  Page/insights:
    properties:
      period:
        description: The aggregation period
        type: string
      metric:
        description: The list of metrics that needs to be fetched
        type: string
      since:
        description: Lower bound of the time range to consider
        type: string
      until:
        description: Upper bound of the time range to consider
        type: string
      page_stories:
        description: The number of stories created about your Page (Stories).
        type: string
      page_storytellers*:
        description: The number of people sharing stories about your page (&#039;People
          Talking About This&#039; / PTAT). These stories include liking your Page,
          posting to your Page&#039;s Timeline, liking, commenting on or sharing one
          of your Page posts, answering a Question you posted, RSVPing to one of your
          events, mentioning your Page, phototagging your Page or checking in at your
          Place. Note that currently only the weekly value is in real-time if you
          set `until=now` in the request. This metric is deprecated after the `deprecate_PTAT`
          migration.
        type: string
      page_stories_by_story_type:
        description: The number of stories about your Page&#039;s stories, by Page
          story type. (See possible types)
        type: string
      page_storytellers_by_story_type:
        description: The number of people talking about your Page&#039;s stories,
          by Page story type. (See possible types)
        type: string
      page_storytellers_by_age_gender:
        description: The number of People Talking About the Page by user age and gender.
        type: string
      page_storytellers_by_city:
        description: The number of People Talking About the Page by user city.
        type: string
  Pages_Platform_Component_Flow_Service_Config:
    properties:
      id:
        description: Id
        type: string
      deeplink:
        description: The deeplink to open the flow. It will switch to native apps
          in mobileDefault
        type: string
      flow_category:
        description: The category of the flow
        type: string
      label:
        description: The label of the entry point that enters the flow
        type: string
  Payment:
    properties:
      id:
        description: The payment ID
        type: string
      user:
        description: The consumer&#039;s first and last name along with their user
          id. May be omitted in some cases.
        type: string
      request_id:
        description: The unique, optional app-created identifier passed into the JS
          function (255 character maximum)
        type: string
      application:
        description: The app associated with this payment
        type: string
      actions:
        description: The list of different action types that have occurred in this
          payment.
        type: string
      type:
        description: 'The type of this particular action. type can be:charge: This
          designates the type of action that was taken on this payment was a charge.
          If the charge has a status of completed, then you should fulfill the order.refund:
          The refund type designates the payment has been refunded and the item sold
          to the consumer should be retracted if possible as you will no longer be
          paid out for this transaction.chargeback: A chargeback is initiated by a
          consumer with their bank disputing the payment in question. When a chargeback
          occurs, you should retract the in-game item from the costumer where possible
          as you will not be paid out for this order.chargeback_reversal: A chargeback_reversal
          occurs when a chargeback is retroactively reversed. In this case, you should
          reinstate the consumer&#039;s in-game item if possible as you will now be
          paid out for this payment.decline: A decline occurs when a funding source
          used to create a bundled transaction is declined at the moment of processing
          the payment. You should retract the in-game item from the consumer where
          possible as you will not be paid out for this order. More information on
          bundled transactions and declines can be found in Handling Disputes and
          Refunds.'
        type: string
      status:
        description: 'The status for this particular action. status can be:initiated:
          An initiated payment designates the payment was only initiated but not yet
          fully completed. You should not fulfill an order of this type with the consumer
          and you should not receive a real time update for a payment with this status.
          You will however get a real time update when the corresponding transaction
          is completed. Developers may see initiated state for certain payment methods
          which requires long time to settle, for example, certain methods require
          the costumer to fill-in a form online, print out a receipt and go to the
          bank offline to pay.completed: A completed status means the action was successfully
          completed. If the type was a charge you will want to fulfill the order to
          the consumer at this time. Similarly, if the action type was a refund you
          will want to retract the item from the consumer.failed: This designates
          a failed action for the underlying type. This value can be present for both
          a charge action type as well as a refund action type.'
        type: string
      amount:
        description: The amount of money covered by this action.
        type: string
      currency:
        description: The currency of the above amount in this action.
        type: string
      time_created:
        description: When this action occurred.
        type: string
  Dispute:
    properties:
      reason:
        description: The reason you are settling this dispute. This is required.
        type: string
  Refunds:
    properties:
      currency:
        description: The three-letter ISO code of the currency in which the refund
          amount is specified; it must be the same as the currency in which the original
          purchase was denominated. This is required.
        type: string
      amount:
        description: The amount to refund. This is required. It must be less than
          or equal to the refundable_amount field on the parent Payment object.
        type: string
      reason:
        description: The reason you are refunding this order.
        type: string
  Photo:
    properties:
      id:
        description: The photo ID
        type: string
      album:
        description: The album this photo is in
        type: string
      backdated_time:
        description: A user-specified time for when this object was created
        type: string
      backdated_time_granularity:
        description: How accurate the backdated time is
        type: string
      can_backdate:
        description: Indicates whether the viewer can backdate the photo
        type: string
      can_delete:
        description: Indicates whether the viewer can delete the photo
        type: string
      can_tag:
        description: Indicates whether the viewer can tag the photo
        type: string
      created_time:
        description: The time this photo was publishedDefault
        type: string
      event:
        description: If this object has a place, the event associated with the place
        type: string
      from:
        description: The profile (user or page) that uploaded this photo
        type: string
  Place:
    properties:
      id:
        description: ID
        type: string
      location:
        description: Location of PlaceDefault
        type: string
      name:
        description: NameDefault
        type: string
      overall_rating:
        description: Overall Rating of Place, on a 5-star scale. 0 means not enough
          data to get a combined rating.
        type: string
  Place_Tag:
    properties:
      id:
        description: IDDefault
        type: string
      created_time:
        description: Time when the place was visitedDefault
        type: string
      place:
        description: The place that was visitedDefault
        type: string
  Place_Topic:
    properties:
      id:
        description: The topic ID
        type: string
      count:
        description: How many Pages have this category
        type: string
      has_children:
        description: Whether there are subcategories of this category
        type: string
      icon_url:
        description: The URL for the icon representing this category
        type: string
      name:
        description: Localized name of the categoryDefault
        type: string
      parent_ids:
        description: IDs of any parent categories that this is a subcategory of
        type: string
      plural_name:
        description: Localized plural name of the category
        type: string
      top_subtopic_names:
        description: Names of the subtopics associated with the most pages
        type: string
  Post:
    properties:
      id:
        description: The post ID
        type: string
      admin_creator:
        description: ID of admin, app or business that created the post.  Applies
          to pages only
        type: string
      name:
        description: Name of the person, app or business
        type: string
      application:
        description: Information about the app this post was published by.
        type: string
      call_to_action:
        description: The call to action type used in any Page posts for mobile app
          engagement ads.
        type: string
      context:
        description: The call to action type used in any Page posts for mobile app
          engagement ads.
        type: string
      caption:
        description: Link caption in post that appears below name. The caption must
          be an actual URLs and should accurately reflect the URL and associated advertiser
          or business someone visits when they click on it.
        type: string
      created_time:
        description: The time the post was initially published. For a post about a
          life event, this will be the date and time of the life event
        type: string
      description:
        description: A description of a link in the post (appears beneath the caption).
        type: string
      feed_targeting:
        description: Object that controls news feed targeting for this post. Anyone
          in these groups will be more likely to see this post, others will be less
          likely, but may still see it anyway. Any of the targeting fields shown here
          can be used, none are required (applies to Pages only).
        type: string
  Insights:
    properties:
      period:
        description: The aggregation period
        type: string
      metric:
        description: The list of metrics that needs to be fetched
        type: string
      since:
        description: Lower bound of the time range to consider
        type: string
      until:
        description: Upper bound of the time range to consider
        type: string
      page_stories:
        description: The number of stories created about your Page (Stories).
        type: string
      page_storytellers*:
        description: The number of people sharing stories about your page (&#039;People
          Talking About This&#039; / PTAT). These stories include liking your Page,
          posting to your Page&#039;s Timeline, liking, commenting on or sharing one
          of your Page posts, answering a Question you posted, RSVPing to one of your
          events, mentioning your Page, phototagging your Page or checking in at your
          Place. Note that currently only the weekly value is in real-time if you
          set `until=now` in the request. This metric is deprecated after the `deprecate_PTAT`
          migration.
        type: string
      page_stories_by_story_type:
        description: The number of stories about your Page&#039;s stories, by Page
          story type. (See possible types)
        type: string
      page_storytellers_by_story_type:
        description: The number of people talking about your Page&#039;s stories,
          by Page story type. (See possible types)
        type: string
      page_storytellers_by_age_gender:
        description: The number of People Talking About the Page by user age and gender.
        type: string
      page_storytellers_by_city:
        description: The number of People Talking About the Page by user city.
        type: string
  Promotion_Info:
    properties:
      budget:
        description: The budget for the promoted post
        type: string
      currency:
        description: The currency used for the promotion
        type: string
      spent:
        description: The amount spent promoting this post so far
        type: string
  RTBDynamic_Post:
    properties:
      child_attachments:
        description: List of child cards for carousel posts
        type: string
      created:
        description: The time this post was made
        type: string
      description:
        description: The link description
        type: string
      id:
        description: The dynamic post IDDefault
        type: string
      image_url:
        description: The dynamic post image
        type: string
      link:
        description: The dynamic post link
        type: string
      message:
        description: The post text
        type: string
      owner_id:
        description: The ID of the owner of this post
        type: string
      place_id:
        description: The place page ID of the dynamic post
        type: string
      product_id:
        description: The product ID
        type: string
  Request:
    properties:
      id:
        description: The request object ID.
        type: string
      application:
        description: App associated with the request.
        type: string
      to:
        description: The recipient of the request.
        type: string
      from:
        description: The sender associated with the request. This is only included
          for user to user requests.
        type: string
      message:
        description: A string describing the request.
        type: string
      created_time:
        description: Timestamp when the request was created.
        type: string
  Saved_Message_Response:
    properties:
      id:
        description: The ID of the saved responseDefault
        type: string
      category:
        description: The message category of the saved response,Default
        type: string
      image:
        description: The image attached to this save response
        type: string
      is_enabled:
        description: Toggle whether to enable the messageDefault
        type: string
      message:
        description: The message body of the saved responseDefault
        type: string
      title:
        description: The title of the saved response
        type: string
      remove_image:
        description: 'Default value: falseSet to true to remove the response image'
        type: string
  Status:
    properties:
      id:
        description: The status message ID.
        type: string
      event:
        description: Event associated with this status, if any.
        type: string
      from:
        description: The user who posted the message.
        type: string
      name:
        description: The name of the Profile, e.g. the Person&#039;s full name
        type: string
      message:
        description: The status message content.
        type: string
      place:
        description: Location associated with this status, if any.
        type: string
      updated_time:
        description: The time the message was published.
        type: string
  Test_User:
    properties:
      name:
        description: New name for the test user.
        type: string
      password:
        description: A new password for the test user.
        type: string
  Thread:
    properties:
      id:
        description: The unique ID for this message thread.
        type: string
      comments:
        description: The messages in this thread.
        type: string
      to:
        description: Profiles that are subscribed to the thread.
        type: string
      unread:
        description: The amount of messages that are unread by the session profile.
        type: string
      unseen:
        description: The amount of messages that are unseen by the session profile.
        type: string
      updated_time:
        description: When the thread was last updated.
        type: string
  URL:
    properties:
      id:
        description: The URL itself.
        type: string
      og_object:
        description: The Open Graph object that is canonically associated with this
          URL.
        type: string
      description:
        description: The description of the object.
        type: string
      title:
        description: The title of the object.
        type: string
      type:
        description: The object type.
        type: string
      updated_time:
        description: When the object was last updated.
        type: string
      app_links:
        description: AppLinks data associated with this URL.
        type: string
      engagement:
        description: Engagements associated with this URL.
        type: string
      reaction_count:
        description: The sum of reactions across all posts containing the URL on Facebook.
        type: string
      comment_count:
        description: The sum of comments on posts containing this URL on Facebook.
        type: string
  User:
    properties:
      id:
        description: The id of this person&#039;s user account. This ID is unique
          to each app and cannot be used across different apps. Our upgrade guide
          provides more information about app-specific IDsCore
        type: string
      about:
        description: Equivalent to the bio field
        type: string
      admin_notes:
        description: Notes added by viewing page on this person
        type: string
      age_range:
        description: The age segment for this person expressed as a minimum and maximum
          age. For example, more than 18, less than 21.Core
        type: string
      birthday:
        description: The person&#039;s birthday.  This is a fixed format string, like
          MM/DD/YYYY.  However, people can control who can see the year they were
          born separately from the month and day so this string can be only the year
          (YYYY) or the month + day (MM/DD)Core
        type: string
      context:
        description: Social context for this person
        type: string
      cover:
        description: The person&#039;s cover photo
        type: string
      currency:
        description: The person&#039;s local currency information
        type: string
      devices:
        description: The list of devices the person is using. This will return only
          iOS and Android devices
        type: string
      education:
        description: The person&#039;s education
        type: string
  User_Context:
    properties:
      id:
        description: The token representing the social context
        type: string
  Video:
    properties:
      backdated_time_granularity:
        description: Accuracy of the backdated time.
        type: string
      id:
        description: The video ID.
        type: string
      backdated_time:
        description: The time when the video post was created.
        type: string
      content_category:
        description: The content category of this video.
        type: string
      content_tags:
        description: Tags that describe the contents of the video.
        type: string
      created_time:
        description: The time the video was initially published.
        type: string
      description:
        description: The description of the video.Default
        type: string
      embed_html:
        description: The HTML element that may be embedded in a Web page to play the
          video.
        type: string
      embeddable:
        description: Whether the video is embeddable.
        type: string
      event:
        description: If this object has a place, the event associated with the place
        type: string
  Video_Copyright:
    properties:
      id:
        description: The video copyright IDDefault
        type: string
      copyright_content_id:
        description: The copyright content IDDefault
        type: string
      creator:
        description: The account that created the copyrightDefault
        type: string
      in_conflict:
        description: Whether the video copyright is in active conflict with another
          rights owner&#039;s video copyright.Default
        type: string
      monitoring_status:
        description: Whether the video is monitored successfully for copyright. The
          status could be NOT_EXAMED, COPYRIGHTED, and ERROR.Default
        type: string
      monitoring_type:
        description: Whether the video is monitored for video, audio, or bothDefault
        type: string
      ops_override_monitoring_type:
        description: Whether ops changed the monitoring type to video, audio or bothDefault
        type: string
      ownership_countries:
        description: A string array of ISO 3166 format country codes, where the owner
          owns the rights of the contentDefault
        type: string
      reference_file_disabled_by_ops:
        description: Whether the reference file has been disabled by ops.Default
        type: string
      reference_owner_id:
        description: The ID of the reference video ownerDefault
        type: string
  Video_Copyright_Rule:
    properties:
      id:
        description: The id of video copyright rules objectDefault
        type: string
      condition_groups:
        description: Groups of conditions on the rules objectDefault
        type: string
      copyrights:
        description: Copyrights associated with this copyright rules object
        type: string
      created_date:
        description: The date on which the rule was created
        type: string
      creator:
        description: The person who created the match rule
        type: string
      is_in_migration:
        description: Wether or not the rule is in migration
        type: string
      name:
        description: Name of the video copyright rules objectDefault
        type: string
      action:
        description: The action to be performed on a match if any of the conditions
          pass.Required
        type: string
      conditions:
        description: A list of conditions to be evaluated.
        type: string
      type:
        description: The type of condition to be evaluated.Required
        type: string
  Video_List:
    properties:
      id:
        description: Video playlist IDDefault
        type: string
      creation_time:
        description: The time when the playlist was created
        type: string
      description:
        description: Description of the playlist
        type: string
      last_modified:
        description: The time when the contents of the playlist was last changed
        type: string
      owner:
        description: Owner of the playlist
        type: string
      season_number:
        description: Number of Season which this episode belongs to
        type: string
      thumbnail:
        description: Thumbnail of the playlist
        type: string
      title:
        description: Title of the playlistDefault
        type: string
      videos_count:
        description: Number of Videos in the playlist
        type: string
      video_ids:
        description: IDs of videos to be added into the video listRequired
        type: string
  Work_Experience:
    properties:
      id:
        description: id
        type: string
      description:
        description: DescriptionDefault
        type: string
      employer:
        description: EmployerDefault
        type: string
      end_date:
        description: End dateDefault
        type: string
      from:
        description: Tagged byDefault
        type: string
      location:
        description: LocationDefault
        type: string
      position:
        description: PositionDefault
        type: string
      projects:
        description: ProjectsDefault
        type: string
      start_date:
        description: Start dateDefault
        type: string
      with:
        description: Tagged usersDefault
        type: string
x-collection-name: Facebook
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