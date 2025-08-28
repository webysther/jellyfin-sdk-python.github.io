## Documentation for API Endpoints Jellyfin 10.11

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ActivityLogApi* | [**get_log_entries**](ActivityLogApi.md#get_log_entries) | **GET** /System/ActivityLog/Entries | Gets activity log entries.
*ApiKeyApi* | [**create_key**](ApiKeyApi.md#create_key) | **POST** /Auth/Keys | Create a new api key.
*ApiKeyApi* | [**get_keys**](ApiKeyApi.md#get_keys) | **GET** /Auth/Keys | Get all keys.
*ApiKeyApi* | [**revoke_key**](ApiKeyApi.md#revoke_key) | **DELETE** /Auth/Keys/{key} | Remove an api key.
*ArtistsApi* | [**get_album_artists**](ArtistsApi.md#get_album_artists) | **GET** /Artists/AlbumArtists | Gets all album artists from a given item, folder, or the entire library.
*ArtistsApi* | [**get_artist_by_name**](ArtistsApi.md#get_artist_by_name) | **GET** /Artists/{name} | Gets an artist by name.
*ArtistsApi* | [**get_artists**](ArtistsApi.md#get_artists) | **GET** /Artists | Gets all artists from a given item, folder, or the entire library.
*AudioApi* | [**get_audio_stream**](AudioApi.md#get_audio_stream) | **GET** /Audio/{itemId}/stream | Gets an audio stream.
*AudioApi* | [**get_audio_stream_by_container**](AudioApi.md#get_audio_stream_by_container) | **GET** /Audio/{itemId}/stream.{container} | Gets an audio stream.
*AudioApi* | [**head_audio_stream**](AudioApi.md#head_audio_stream) | **HEAD** /Audio/{itemId}/stream | Gets an audio stream.
*AudioApi* | [**head_audio_stream_by_container**](AudioApi.md#head_audio_stream_by_container) | **HEAD** /Audio/{itemId}/stream.{container} | Gets an audio stream.
*BackupApi* | [**create_backup**](BackupApi.md#create_backup) | **POST** /Backup/Create | Creates a new Backup.
*BackupApi* | [**get_backup**](BackupApi.md#get_backup) | **GET** /Backup/Manifest | Gets the descriptor from an existing archive is present.
*BackupApi* | [**list_backups**](BackupApi.md#list_backups) | **GET** /Backup | Gets a list of all currently present backups in the backup directory.
*BackupApi* | [**start_restore_backup**](BackupApi.md#start_restore_backup) | **POST** /Backup/Restore | Restores to a backup by restarting the server and applying the backup.
*BrandingApi* | [**get_branding_css**](BrandingApi.md#get_branding_css) | **GET** /Branding/Css | Gets branding css.
*BrandingApi* | [**get_branding_css2**](BrandingApi.md#get_branding_css2) | **GET** /Branding/Css.css | Gets branding css.
*BrandingApi* | [**get_branding_options**](BrandingApi.md#get_branding_options) | **GET** /Branding/Configuration | Gets branding configuration.
*ChannelsApi* | [**get_all_channel_features**](ChannelsApi.md#get_all_channel_features) | **GET** /Channels/Features | Get all channel features.
*ChannelsApi* | [**get_channel_features**](ChannelsApi.md#get_channel_features) | **GET** /Channels/{channelId}/Features | Get channel features.
*ChannelsApi* | [**get_channel_items**](ChannelsApi.md#get_channel_items) | **GET** /Channels/{channelId}/Items | Get channel items.
*ChannelsApi* | [**get_channels**](ChannelsApi.md#get_channels) | **GET** /Channels | Gets available channels.
*ChannelsApi* | [**get_latest_channel_items**](ChannelsApi.md#get_latest_channel_items) | **GET** /Channels/Items/Latest | Gets latest channel items.
*ClientLogApi* | [**log_file**](ClientLogApi.md#log_file) | **POST** /ClientLog/Document | Upload a document.
*CollectionApi* | [**add_to_collection**](CollectionApi.md#add_to_collection) | **POST** /Collections/{collectionId}/Items | Adds items to a collection.
*CollectionApi* | [**create_collection**](CollectionApi.md#create_collection) | **POST** /Collections | Creates a new collection.
*CollectionApi* | [**remove_from_collection**](CollectionApi.md#remove_from_collection) | **DELETE** /Collections/{collectionId}/Items | Removes items from a collection.
*ConfigurationApi* | [**get_configuration**](ConfigurationApi.md#get_configuration) | **GET** /System/Configuration | Gets application configuration.
*ConfigurationApi* | [**get_default_metadata_options**](ConfigurationApi.md#get_default_metadata_options) | **GET** /System/Configuration/MetadataOptions/Default | Gets a default MetadataOptions object.
*ConfigurationApi* | [**get_named_configuration**](ConfigurationApi.md#get_named_configuration) | **GET** /System/Configuration/{key} | Gets a named configuration.
*ConfigurationApi* | [**update_branding_configuration**](ConfigurationApi.md#update_branding_configuration) | **POST** /System/Configuration/Branding | Updates branding configuration.
*ConfigurationApi* | [**update_configuration**](ConfigurationApi.md#update_configuration) | **POST** /System/Configuration | Updates application configuration.
*ConfigurationApi* | [**update_named_configuration**](ConfigurationApi.md#update_named_configuration) | **POST** /System/Configuration/{key} | Updates named configuration.
*DashboardApi* | [**get_configuration_pages**](DashboardApi.md#get_configuration_pages) | **GET** /web/ConfigurationPages | Gets the configuration pages.
*DashboardApi* | [**get_dashboard_configuration_page**](DashboardApi.md#get_dashboard_configuration_page) | **GET** /web/ConfigurationPage | Gets a dashboard configuration page.
*DevicesApi* | [**delete_device**](DevicesApi.md#delete_device) | **DELETE** /Devices | Deletes a device.
*DevicesApi* | [**get_device_info**](DevicesApi.md#get_device_info) | **GET** /Devices/Info | Get info for a device.
*DevicesApi* | [**get_device_options**](DevicesApi.md#get_device_options) | **GET** /Devices/Options | Get options for a device.
*DevicesApi* | [**get_devices**](DevicesApi.md#get_devices) | **GET** /Devices | Get Devices.
*DevicesApi* | [**update_device_options**](DevicesApi.md#update_device_options) | **POST** /Devices/Options | Update device options.
*DisplayPreferencesApi* | [**get_display_preferences**](DisplayPreferencesApi.md#get_display_preferences) | **GET** /DisplayPreferences/{displayPreferencesId} | Get Display Preferences.
*DisplayPreferencesApi* | [**update_display_preferences**](DisplayPreferencesApi.md#update_display_preferences) | **POST** /DisplayPreferences/{displayPreferencesId} | Update Display Preferences.
*DynamicHlsApi* | [**get_hls_audio_segment**](DynamicHlsApi.md#get_hls_audio_segment) | **GET** /Audio/{itemId}/hls1/{playlistId}/{segmentId}.{container} | Gets a video stream using HTTP live streaming.
*DynamicHlsApi* | [**get_hls_video_segment**](DynamicHlsApi.md#get_hls_video_segment) | **GET** /Videos/{itemId}/hls1/{playlistId}/{segmentId}.{container} | Gets a video stream using HTTP live streaming.
*DynamicHlsApi* | [**get_live_hls_stream**](DynamicHlsApi.md#get_live_hls_stream) | **GET** /Videos/{itemId}/live.m3u8 | Gets a hls live stream.
*DynamicHlsApi* | [**get_master_hls_audio_playlist**](DynamicHlsApi.md#get_master_hls_audio_playlist) | **GET** /Audio/{itemId}/master.m3u8 | Gets an audio hls playlist stream.
*DynamicHlsApi* | [**get_master_hls_video_playlist**](DynamicHlsApi.md#get_master_hls_video_playlist) | **GET** /Videos/{itemId}/master.m3u8 | Gets a video hls playlist stream.
*DynamicHlsApi* | [**get_variant_hls_audio_playlist**](DynamicHlsApi.md#get_variant_hls_audio_playlist) | **GET** /Audio/{itemId}/main.m3u8 | Gets an audio stream using HTTP live streaming.
*DynamicHlsApi* | [**get_variant_hls_video_playlist**](DynamicHlsApi.md#get_variant_hls_video_playlist) | **GET** /Videos/{itemId}/main.m3u8 | Gets a video stream using HTTP live streaming.
*DynamicHlsApi* | [**head_master_hls_audio_playlist**](DynamicHlsApi.md#head_master_hls_audio_playlist) | **HEAD** /Audio/{itemId}/master.m3u8 | Gets an audio hls playlist stream.
*DynamicHlsApi* | [**head_master_hls_video_playlist**](DynamicHlsApi.md#head_master_hls_video_playlist) | **HEAD** /Videos/{itemId}/master.m3u8 | Gets a video hls playlist stream.
*EnvironmentApi* | [**get_default_directory_browser**](EnvironmentApi.md#get_default_directory_browser) | **GET** /Environment/DefaultDirectoryBrowser | Get Default directory browser.
*EnvironmentApi* | [**get_directory_contents**](EnvironmentApi.md#get_directory_contents) | **GET** /Environment/DirectoryContents | Gets the contents of a given directory in the file system.
*EnvironmentApi* | [**get_drives**](EnvironmentApi.md#get_drives) | **GET** /Environment/Drives | Gets available drives from the server&#39;s file system.
*EnvironmentApi* | [**get_network_shares**](EnvironmentApi.md#get_network_shares) | **GET** /Environment/NetworkShares | Gets network paths.
*EnvironmentApi* | [**get_parent_path**](EnvironmentApi.md#get_parent_path) | **GET** /Environment/ParentPath | Gets the parent path of a given path.
*EnvironmentApi* | [**validate_path**](EnvironmentApi.md#validate_path) | **POST** /Environment/ValidatePath | Validates path.
*FilterApi* | [**get_query_filters**](FilterApi.md#get_query_filters) | **GET** /Items/Filters2 | Gets query filters.
*FilterApi* | [**get_query_filters_legacy**](FilterApi.md#get_query_filters_legacy) | **GET** /Items/Filters | Gets legacy query filters.
*GenresApi* | [**get_genre**](GenresApi.md#get_genre) | **GET** /Genres/{genreName} | Gets a genre, by name.
*GenresApi* | [**get_genres**](GenresApi.md#get_genres) | **GET** /Genres | Gets all genres from a given item, folder, or the entire library.
*HlsSegmentApi* | [**get_hls_audio_segment_legacy_aac**](HlsSegmentApi.md#get_hls_audio_segment_legacy_aac) | **GET** /Audio/{itemId}/hls/{segmentId}/stream.aac | Gets the specified audio segment for an audio item.
*HlsSegmentApi* | [**get_hls_audio_segment_legacy_mp3**](HlsSegmentApi.md#get_hls_audio_segment_legacy_mp3) | **GET** /Audio/{itemId}/hls/{segmentId}/stream.mp3 | Gets the specified audio segment for an audio item.
*HlsSegmentApi* | [**get_hls_playlist_legacy**](HlsSegmentApi.md#get_hls_playlist_legacy) | **GET** /Videos/{itemId}/hls/{playlistId}/stream.m3u8 | Gets a hls video playlist.
*HlsSegmentApi* | [**get_hls_video_segment_legacy**](HlsSegmentApi.md#get_hls_video_segment_legacy) | **GET** /Videos/{itemId}/hls/{playlistId}/{segmentId}.{segmentContainer} | Gets a hls video segment.
*HlsSegmentApi* | [**stop_encoding_process**](HlsSegmentApi.md#stop_encoding_process) | **DELETE** /Videos/ActiveEncodings | Stops an active encoding.
*ImageApi* | [**delete_custom_splashscreen**](ImageApi.md#delete_custom_splashscreen) | **DELETE** /Branding/Splashscreen | Delete a custom splashscreen.
*ImageApi* | [**delete_item_image**](ImageApi.md#delete_item_image) | **DELETE** /Items/{itemId}/Images/{imageType} | Delete an item&#39;s image.
*ImageApi* | [**delete_item_image_by_index**](ImageApi.md#delete_item_image_by_index) | **DELETE** /Items/{itemId}/Images/{imageType}/{imageIndex} | Delete an item&#39;s image.
*ImageApi* | [**delete_user_image**](ImageApi.md#delete_user_image) | **DELETE** /UserImage | Delete the user&#39;s image.
*ImageApi* | [**get_artist_image**](ImageApi.md#get_artist_image) | **GET** /Artists/{name}/Images/{imageType}/{imageIndex} | Get artist image by name.
*ImageApi* | [**get_genre_image**](ImageApi.md#get_genre_image) | **GET** /Genres/{name}/Images/{imageType} | Get genre image by name.
*ImageApi* | [**get_genre_image_by_index**](ImageApi.md#get_genre_image_by_index) | **GET** /Genres/{name}/Images/{imageType}/{imageIndex} | Get genre image by name.
*ImageApi* | [**get_item_image**](ImageApi.md#get_item_image) | **GET** /Items/{itemId}/Images/{imageType} | Gets the item&#39;s image.
*ImageApi* | [**get_item_image2**](ImageApi.md#get_item_image2) | **GET** /Items/{itemId}/Images/{imageType}/{imageIndex}/{tag}/{format}/{maxWidth}/{maxHeight}/{percentPlayed}/{unplayedCount} | Gets the item&#39;s image.
*ImageApi* | [**get_item_image_by_index**](ImageApi.md#get_item_image_by_index) | **GET** /Items/{itemId}/Images/{imageType}/{imageIndex} | Gets the item&#39;s image.
*ImageApi* | [**get_item_image_infos**](ImageApi.md#get_item_image_infos) | **GET** /Items/{itemId}/Images | Get item image infos.
*ImageApi* | [**get_music_genre_image**](ImageApi.md#get_music_genre_image) | **GET** /MusicGenres/{name}/Images/{imageType} | Get music genre image by name.
*ImageApi* | [**get_music_genre_image_by_index**](ImageApi.md#get_music_genre_image_by_index) | **GET** /MusicGenres/{name}/Images/{imageType}/{imageIndex} | Get music genre image by name.
*ImageApi* | [**get_person_image**](ImageApi.md#get_person_image) | **GET** /Persons/{name}/Images/{imageType} | Get person image by name.
*ImageApi* | [**get_person_image_by_index**](ImageApi.md#get_person_image_by_index) | **GET** /Persons/{name}/Images/{imageType}/{imageIndex} | Get person image by name.
*ImageApi* | [**get_splashscreen**](ImageApi.md#get_splashscreen) | **GET** /Branding/Splashscreen | Generates or gets the splashscreen.
*ImageApi* | [**get_studio_image**](ImageApi.md#get_studio_image) | **GET** /Studios/{name}/Images/{imageType} | Get studio image by name.
*ImageApi* | [**get_studio_image_by_index**](ImageApi.md#get_studio_image_by_index) | **GET** /Studios/{name}/Images/{imageType}/{imageIndex} | Get studio image by name.
*ImageApi* | [**get_user_image**](ImageApi.md#get_user_image) | **GET** /UserImage | Get user profile image.
*ImageApi* | [**head_artist_image**](ImageApi.md#head_artist_image) | **HEAD** /Artists/{name}/Images/{imageType}/{imageIndex} | Get artist image by name.
*ImageApi* | [**head_genre_image**](ImageApi.md#head_genre_image) | **HEAD** /Genres/{name}/Images/{imageType} | Get genre image by name.
*ImageApi* | [**head_genre_image_by_index**](ImageApi.md#head_genre_image_by_index) | **HEAD** /Genres/{name}/Images/{imageType}/{imageIndex} | Get genre image by name.
*ImageApi* | [**head_item_image**](ImageApi.md#head_item_image) | **HEAD** /Items/{itemId}/Images/{imageType} | Gets the item&#39;s image.
*ImageApi* | [**head_item_image2**](ImageApi.md#head_item_image2) | **HEAD** /Items/{itemId}/Images/{imageType}/{imageIndex}/{tag}/{format}/{maxWidth}/{maxHeight}/{percentPlayed}/{unplayedCount} | Gets the item&#39;s image.
*ImageApi* | [**head_item_image_by_index**](ImageApi.md#head_item_image_by_index) | **HEAD** /Items/{itemId}/Images/{imageType}/{imageIndex} | Gets the item&#39;s image.
*ImageApi* | [**head_music_genre_image**](ImageApi.md#head_music_genre_image) | **HEAD** /MusicGenres/{name}/Images/{imageType} | Get music genre image by name.
*ImageApi* | [**head_music_genre_image_by_index**](ImageApi.md#head_music_genre_image_by_index) | **HEAD** /MusicGenres/{name}/Images/{imageType}/{imageIndex} | Get music genre image by name.
*ImageApi* | [**head_person_image**](ImageApi.md#head_person_image) | **HEAD** /Persons/{name}/Images/{imageType} | Get person image by name.
*ImageApi* | [**head_person_image_by_index**](ImageApi.md#head_person_image_by_index) | **HEAD** /Persons/{name}/Images/{imageType}/{imageIndex} | Get person image by name.
*ImageApi* | [**head_studio_image**](ImageApi.md#head_studio_image) | **HEAD** /Studios/{name}/Images/{imageType} | Get studio image by name.
*ImageApi* | [**head_studio_image_by_index**](ImageApi.md#head_studio_image_by_index) | **HEAD** /Studios/{name}/Images/{imageType}/{imageIndex} | Get studio image by name.
*ImageApi* | [**head_user_image**](ImageApi.md#head_user_image) | **HEAD** /UserImage | Get user profile image.
*ImageApi* | [**post_user_image**](ImageApi.md#post_user_image) | **POST** /UserImage | Sets the user image.
*ImageApi* | [**set_item_image**](ImageApi.md#set_item_image) | **POST** /Items/{itemId}/Images/{imageType} | Set item image.
*ImageApi* | [**set_item_image_by_index**](ImageApi.md#set_item_image_by_index) | **POST** /Items/{itemId}/Images/{imageType}/{imageIndex} | Set item image.
*ImageApi* | [**update_item_image_index**](ImageApi.md#update_item_image_index) | **POST** /Items/{itemId}/Images/{imageType}/{imageIndex}/Index | Updates the index for an item image.
*ImageApi* | [**upload_custom_splashscreen**](ImageApi.md#upload_custom_splashscreen) | **POST** /Branding/Splashscreen | Uploads a custom splashscreen.  The body is expected to the image contents base64 encoded.
*InstantMixApi* | [**get_instant_mix_from_album**](InstantMixApi.md#get_instant_mix_from_album) | **GET** /Albums/{itemId}/InstantMix | Creates an instant playlist based on a given album.
*InstantMixApi* | [**get_instant_mix_from_artists**](InstantMixApi.md#get_instant_mix_from_artists) | **GET** /Artists/{itemId}/InstantMix | Creates an instant playlist based on a given artist.
*InstantMixApi* | [**get_instant_mix_from_artists2**](InstantMixApi.md#get_instant_mix_from_artists2) | **GET** /Artists/InstantMix | Creates an instant playlist based on a given artist.
*InstantMixApi* | [**get_instant_mix_from_item**](InstantMixApi.md#get_instant_mix_from_item) | **GET** /Items/{itemId}/InstantMix | Creates an instant playlist based on a given item.
*InstantMixApi* | [**get_instant_mix_from_music_genre_by_id**](InstantMixApi.md#get_instant_mix_from_music_genre_by_id) | **GET** /MusicGenres/InstantMix | Creates an instant playlist based on a given genre.
*InstantMixApi* | [**get_instant_mix_from_music_genre_by_name**](InstantMixApi.md#get_instant_mix_from_music_genre_by_name) | **GET** /MusicGenres/{name}/InstantMix | Creates an instant playlist based on a given genre.
*InstantMixApi* | [**get_instant_mix_from_playlist**](InstantMixApi.md#get_instant_mix_from_playlist) | **GET** /Playlists/{itemId}/InstantMix | Creates an instant playlist based on a given playlist.
*InstantMixApi* | [**get_instant_mix_from_song**](InstantMixApi.md#get_instant_mix_from_song) | **GET** /Songs/{itemId}/InstantMix | Creates an instant playlist based on a given song.
*ItemLookupApi* | [**apply_search_criteria**](ItemLookupApi.md#apply_search_criteria) | **POST** /Items/RemoteSearch/Apply/{itemId} | Applies search criteria to an item and refreshes metadata.
*ItemLookupApi* | [**get_book_remote_search_results**](ItemLookupApi.md#get_book_remote_search_results) | **POST** /Items/RemoteSearch/Book | Get book remote search.
*ItemLookupApi* | [**get_box_set_remote_search_results**](ItemLookupApi.md#get_box_set_remote_search_results) | **POST** /Items/RemoteSearch/BoxSet | Get box set remote search.
*ItemLookupApi* | [**get_external_id_infos**](ItemLookupApi.md#get_external_id_infos) | **GET** /Items/{itemId}/ExternalIdInfos | Get the item&#39;s external id info.
*ItemLookupApi* | [**get_movie_remote_search_results**](ItemLookupApi.md#get_movie_remote_search_results) | **POST** /Items/RemoteSearch/Movie | Get movie remote search.
*ItemLookupApi* | [**get_music_album_remote_search_results**](ItemLookupApi.md#get_music_album_remote_search_results) | **POST** /Items/RemoteSearch/MusicAlbum | Get music album remote search.
*ItemLookupApi* | [**get_music_artist_remote_search_results**](ItemLookupApi.md#get_music_artist_remote_search_results) | **POST** /Items/RemoteSearch/MusicArtist | Get music artist remote search.
*ItemLookupApi* | [**get_music_video_remote_search_results**](ItemLookupApi.md#get_music_video_remote_search_results) | **POST** /Items/RemoteSearch/MusicVideo | Get music video remote search.
*ItemLookupApi* | [**get_person_remote_search_results**](ItemLookupApi.md#get_person_remote_search_results) | **POST** /Items/RemoteSearch/Person | Get person remote search.
*ItemLookupApi* | [**get_series_remote_search_results**](ItemLookupApi.md#get_series_remote_search_results) | **POST** /Items/RemoteSearch/Series | Get series remote search.
*ItemLookupApi* | [**get_trailer_remote_search_results**](ItemLookupApi.md#get_trailer_remote_search_results) | **POST** /Items/RemoteSearch/Trailer | Get trailer remote search.
*ItemRefreshApi* | [**refresh_item**](ItemRefreshApi.md#refresh_item) | **POST** /Items/{itemId}/Refresh | Refreshes metadata for an item.
*ItemUpdateApi* | [**get_metadata_editor_info**](ItemUpdateApi.md#get_metadata_editor_info) | **GET** /Items/{itemId}/MetadataEditor | Gets metadata editor info for an item.
*ItemUpdateApi* | [**update_item**](ItemUpdateApi.md#update_item) | **POST** /Items/{itemId} | Updates an item.
*ItemUpdateApi* | [**update_item_content_type**](ItemUpdateApi.md#update_item_content_type) | **POST** /Items/{itemId}/ContentType | Updates an item&#39;s content type.
*ItemsApi* | [**get_item_user_data**](ItemsApi.md#get_item_user_data) | **GET** /UserItems/{itemId}/UserData | Get Item User Data.
*ItemsApi* | [**get_items**](ItemsApi.md#get_items) | **GET** /Items | Gets items based on a query.
*ItemsApi* | [**get_resume_items**](ItemsApi.md#get_resume_items) | **GET** /UserItems/Resume | Gets items based on a query.
*ItemsApi* | [**update_item_user_data**](ItemsApi.md#update_item_user_data) | **POST** /UserItems/{itemId}/UserData | Update Item User Data.
*LibraryApi* | [**delete_item**](LibraryApi.md#delete_item) | **DELETE** /Items/{itemId} | Deletes an item from the library and filesystem.
*LibraryApi* | [**delete_items**](LibraryApi.md#delete_items) | **DELETE** /Items | Deletes items from the library and filesystem.
*LibraryApi* | [**get_ancestors**](LibraryApi.md#get_ancestors) | **GET** /Items/{itemId}/Ancestors | Gets all parents of an item.
*LibraryApi* | [**get_critic_reviews**](LibraryApi.md#get_critic_reviews) | **GET** /Items/{itemId}/CriticReviews | Gets critic review for an item.
*LibraryApi* | [**get_download**](LibraryApi.md#get_download) | **GET** /Items/{itemId}/Download | Downloads item media.
*LibraryApi* | [**get_file**](LibraryApi.md#get_file) | **GET** /Items/{itemId}/File | Get the original file of an item.
*LibraryApi* | [**get_item_counts**](LibraryApi.md#get_item_counts) | **GET** /Items/Counts | Get item counts.
*LibraryApi* | [**get_library_options_info**](LibraryApi.md#get_library_options_info) | **GET** /Libraries/AvailableOptions | Gets the library options info.
*LibraryApi* | [**get_media_folders**](LibraryApi.md#get_media_folders) | **GET** /Library/MediaFolders | Gets all user media folders.
*LibraryApi* | [**get_physical_paths**](LibraryApi.md#get_physical_paths) | **GET** /Library/PhysicalPaths | Gets a list of physical paths from virtual folders.
*LibraryApi* | [**get_similar_albums**](LibraryApi.md#get_similar_albums) | **GET** /Albums/{itemId}/Similar | Gets similar items.
*LibraryApi* | [**get_similar_artists**](LibraryApi.md#get_similar_artists) | **GET** /Artists/{itemId}/Similar | Gets similar items.
*LibraryApi* | [**get_similar_items**](LibraryApi.md#get_similar_items) | **GET** /Items/{itemId}/Similar | Gets similar items.
*LibraryApi* | [**get_similar_movies**](LibraryApi.md#get_similar_movies) | **GET** /Movies/{itemId}/Similar | Gets similar items.
*LibraryApi* | [**get_similar_shows**](LibraryApi.md#get_similar_shows) | **GET** /Shows/{itemId}/Similar | Gets similar items.
*LibraryApi* | [**get_similar_trailers**](LibraryApi.md#get_similar_trailers) | **GET** /Trailers/{itemId}/Similar | Gets similar items.
*LibraryApi* | [**get_theme_media**](LibraryApi.md#get_theme_media) | **GET** /Items/{itemId}/ThemeMedia | Get theme songs and videos for an item.
*LibraryApi* | [**get_theme_songs**](LibraryApi.md#get_theme_songs) | **GET** /Items/{itemId}/ThemeSongs | Get theme songs for an item.
*LibraryApi* | [**get_theme_videos**](LibraryApi.md#get_theme_videos) | **GET** /Items/{itemId}/ThemeVideos | Get theme videos for an item.
*LibraryApi* | [**post_added_movies**](LibraryApi.md#post_added_movies) | **POST** /Library/Movies/Added | Reports that new movies have been added by an external source.
*LibraryApi* | [**post_added_series**](LibraryApi.md#post_added_series) | **POST** /Library/Series/Added | Reports that new episodes of a series have been added by an external source.
*LibraryApi* | [**post_updated_media**](LibraryApi.md#post_updated_media) | **POST** /Library/Media/Updated | Reports that new movies have been added by an external source.
*LibraryApi* | [**post_updated_movies**](LibraryApi.md#post_updated_movies) | **POST** /Library/Movies/Updated | Reports that new movies have been added by an external source.
*LibraryApi* | [**post_updated_series**](LibraryApi.md#post_updated_series) | **POST** /Library/Series/Updated | Reports that new episodes of a series have been added by an external source.
*LibraryApi* | [**refresh_library**](LibraryApi.md#refresh_library) | **POST** /Library/Refresh | Starts a library scan.
*LibraryStructureApi* | [**add_media_path**](LibraryStructureApi.md#add_media_path) | **POST** /Library/VirtualFolders/Paths | Add a media path to a library.
*LibraryStructureApi* | [**add_virtual_folder**](LibraryStructureApi.md#add_virtual_folder) | **POST** /Library/VirtualFolders | Adds a virtual folder.
*LibraryStructureApi* | [**get_virtual_folders**](LibraryStructureApi.md#get_virtual_folders) | **GET** /Library/VirtualFolders | Gets all virtual folders.
*LibraryStructureApi* | [**remove_media_path**](LibraryStructureApi.md#remove_media_path) | **DELETE** /Library/VirtualFolders/Paths | Remove a media path.
*LibraryStructureApi* | [**remove_virtual_folder**](LibraryStructureApi.md#remove_virtual_folder) | **DELETE** /Library/VirtualFolders | Removes a virtual folder.
*LibraryStructureApi* | [**rename_virtual_folder**](LibraryStructureApi.md#rename_virtual_folder) | **POST** /Library/VirtualFolders/Name | Renames a virtual folder.
*LibraryStructureApi* | [**update_library_options**](LibraryStructureApi.md#update_library_options) | **POST** /Library/VirtualFolders/LibraryOptions | Update library options.
*LibraryStructureApi* | [**update_media_path**](LibraryStructureApi.md#update_media_path) | **POST** /Library/VirtualFolders/Paths/Update | Updates a media path.
*LiveTvApi* | [**add_listing_provider**](LiveTvApi.md#add_listing_provider) | **POST** /LiveTv/ListingProviders | Adds a listings provider.
*LiveTvApi* | [**add_tuner_host**](LiveTvApi.md#add_tuner_host) | **POST** /LiveTv/TunerHosts | Adds a tuner host.
*LiveTvApi* | [**cancel_series_timer**](LiveTvApi.md#cancel_series_timer) | **DELETE** /LiveTv/SeriesTimers/{timerId} | Cancels a live tv series timer.
*LiveTvApi* | [**cancel_timer**](LiveTvApi.md#cancel_timer) | **DELETE** /LiveTv/Timers/{timerId} | Cancels a live tv timer.
*LiveTvApi* | [**create_series_timer**](LiveTvApi.md#create_series_timer) | **POST** /LiveTv/SeriesTimers | Creates a live tv series timer.
*LiveTvApi* | [**create_timer**](LiveTvApi.md#create_timer) | **POST** /LiveTv/Timers | Creates a live tv timer.
*LiveTvApi* | [**delete_listing_provider**](LiveTvApi.md#delete_listing_provider) | **DELETE** /LiveTv/ListingProviders | Delete listing provider.
*LiveTvApi* | [**delete_recording**](LiveTvApi.md#delete_recording) | **DELETE** /LiveTv/Recordings/{recordingId} | Deletes a live tv recording.
*LiveTvApi* | [**delete_tuner_host**](LiveTvApi.md#delete_tuner_host) | **DELETE** /LiveTv/TunerHosts | Deletes a tuner host.
*LiveTvApi* | [**discover_tuners**](LiveTvApi.md#discover_tuners) | **GET** /LiveTv/Tuners/Discover | Discover tuners.
*LiveTvApi* | [**discvover_tuners**](LiveTvApi.md#discvover_tuners) | **GET** /LiveTv/Tuners/Discvover | Discover tuners.
*LiveTvApi* | [**get_channel**](LiveTvApi.md#get_channel) | **GET** /LiveTv/Channels/{channelId} | Gets a live tv channel.
*LiveTvApi* | [**get_channel_mapping_options**](LiveTvApi.md#get_channel_mapping_options) | **GET** /LiveTv/ChannelMappingOptions | Get channel mapping options.
*LiveTvApi* | [**get_default_listing_provider**](LiveTvApi.md#get_default_listing_provider) | **GET** /LiveTv/ListingProviders/Default | Gets default listings provider info.
*LiveTvApi* | [**get_default_timer**](LiveTvApi.md#get_default_timer) | **GET** /LiveTv/Timers/Defaults | Gets the default values for a new timer.
*LiveTvApi* | [**get_guide_info**](LiveTvApi.md#get_guide_info) | **GET** /LiveTv/GuideInfo | Get guide info.
*LiveTvApi* | [**get_lineups**](LiveTvApi.md#get_lineups) | **GET** /LiveTv/ListingProviders/Lineups | Gets available lineups.
*LiveTvApi* | [**get_live_recording_file**](LiveTvApi.md#get_live_recording_file) | **GET** /LiveTv/LiveRecordings/{recordingId}/stream | Gets a live tv recording stream.
*LiveTvApi* | [**get_live_stream_file**](LiveTvApi.md#get_live_stream_file) | **GET** /LiveTv/LiveStreamFiles/{streamId}/stream.{container} | Gets a live tv channel stream.
*LiveTvApi* | [**get_live_tv_channels**](LiveTvApi.md#get_live_tv_channels) | **GET** /LiveTv/Channels | Gets available live tv channels.
*LiveTvApi* | [**get_live_tv_info**](LiveTvApi.md#get_live_tv_info) | **GET** /LiveTv/Info | Gets available live tv services.
*LiveTvApi* | [**get_live_tv_programs**](LiveTvApi.md#get_live_tv_programs) | **GET** /LiveTv/Programs | Gets available live tv epgs.
*LiveTvApi* | [**get_program**](LiveTvApi.md#get_program) | **GET** /LiveTv/Programs/{programId} | Gets a live tv program.
*LiveTvApi* | [**get_programs**](LiveTvApi.md#get_programs) | **POST** /LiveTv/Programs | Gets available live tv epgs.
*LiveTvApi* | [**get_recommended_programs**](LiveTvApi.md#get_recommended_programs) | **GET** /LiveTv/Programs/Recommended | Gets recommended live tv epgs.
*LiveTvApi* | [**get_recording**](LiveTvApi.md#get_recording) | **GET** /LiveTv/Recordings/{recordingId} | Gets a live tv recording.
*LiveTvApi* | [**get_recording_folders**](LiveTvApi.md#get_recording_folders) | **GET** /LiveTv/Recordings/Folders | Gets recording folders.
*LiveTvApi* | [**get_recording_group**](LiveTvApi.md#get_recording_group) | **GET** /LiveTv/Recordings/Groups/{groupId} | Get recording group.
*LiveTvApi* | [**get_recording_groups**](LiveTvApi.md#get_recording_groups) | **GET** /LiveTv/Recordings/Groups | Gets live tv recording groups.
*LiveTvApi* | [**get_recordings**](LiveTvApi.md#get_recordings) | **GET** /LiveTv/Recordings | Gets live tv recordings.
*LiveTvApi* | [**get_recordings_series**](LiveTvApi.md#get_recordings_series) | **GET** /LiveTv/Recordings/Series | Gets live tv recording series.
*LiveTvApi* | [**get_schedules_direct_countries**](LiveTvApi.md#get_schedules_direct_countries) | **GET** /LiveTv/ListingProviders/SchedulesDirect/Countries | Gets available countries.
*LiveTvApi* | [**get_series_timer**](LiveTvApi.md#get_series_timer) | **GET** /LiveTv/SeriesTimers/{timerId} | Gets a live tv series timer.
*LiveTvApi* | [**get_series_timers**](LiveTvApi.md#get_series_timers) | **GET** /LiveTv/SeriesTimers | Gets live tv series timers.
*LiveTvApi* | [**get_timer**](LiveTvApi.md#get_timer) | **GET** /LiveTv/Timers/{timerId} | Gets a timer.
*LiveTvApi* | [**get_timers**](LiveTvApi.md#get_timers) | **GET** /LiveTv/Timers | Gets the live tv timers.
*LiveTvApi* | [**get_tuner_host_types**](LiveTvApi.md#get_tuner_host_types) | **GET** /LiveTv/TunerHosts/Types | Get tuner host types.
*LiveTvApi* | [**reset_tuner**](LiveTvApi.md#reset_tuner) | **POST** /LiveTv/Tuners/{tunerId}/Reset | Resets a tv tuner.
*LiveTvApi* | [**set_channel_mapping**](LiveTvApi.md#set_channel_mapping) | **POST** /LiveTv/ChannelMappings | Set channel mappings.
*LiveTvApi* | [**update_series_timer**](LiveTvApi.md#update_series_timer) | **POST** /LiveTv/SeriesTimers/{timerId} | Updates a live tv series timer.
*LiveTvApi* | [**update_timer**](LiveTvApi.md#update_timer) | **POST** /LiveTv/Timers/{timerId} | Updates a live tv timer.
*LocalizationApi* | [**get_countries**](LocalizationApi.md#get_countries) | **GET** /Localization/Countries | Gets known countries.
*LocalizationApi* | [**get_cultures**](LocalizationApi.md#get_cultures) | **GET** /Localization/Cultures | Gets known cultures.
*LocalizationApi* | [**get_localization_options**](LocalizationApi.md#get_localization_options) | **GET** /Localization/Options | Gets localization options.
*LocalizationApi* | [**get_parental_ratings**](LocalizationApi.md#get_parental_ratings) | **GET** /Localization/ParentalRatings | Gets known parental ratings.
*LyricsApi* | [**delete_lyrics**](LyricsApi.md#delete_lyrics) | **DELETE** /Audio/{itemId}/Lyrics | Deletes an external lyric file.
*LyricsApi* | [**download_remote_lyrics**](LyricsApi.md#download_remote_lyrics) | **POST** /Audio/{itemId}/RemoteSearch/Lyrics/{lyricId} | Downloads a remote lyric.
*LyricsApi* | [**get_lyrics**](LyricsApi.md#get_lyrics) | **GET** /Audio/{itemId}/Lyrics | Gets an item&#39;s lyrics.
*LyricsApi* | [**get_remote_lyrics**](LyricsApi.md#get_remote_lyrics) | **GET** /Providers/Lyrics/{lyricId} | Gets the remote lyrics.
*LyricsApi* | [**search_remote_lyrics**](LyricsApi.md#search_remote_lyrics) | **GET** /Audio/{itemId}/RemoteSearch/Lyrics | Search remote lyrics.
*LyricsApi* | [**upload_lyrics**](LyricsApi.md#upload_lyrics) | **POST** /Audio/{itemId}/Lyrics | Upload an external lyric file.
*MediaInfoApi* | [**close_live_stream**](MediaInfoApi.md#close_live_stream) | **POST** /LiveStreams/Close | Closes a media source.
*MediaInfoApi* | [**get_bitrate_test_bytes**](MediaInfoApi.md#get_bitrate_test_bytes) | **GET** /Playback/BitrateTest | Tests the network with a request with the size of the bitrate.
*MediaInfoApi* | [**get_playback_info**](MediaInfoApi.md#get_playback_info) | **GET** /Items/{itemId}/PlaybackInfo | Gets live playback media info for an item.
*MediaInfoApi* | [**get_posted_playback_info**](MediaInfoApi.md#get_posted_playback_info) | **POST** /Items/{itemId}/PlaybackInfo | Gets live playback media info for an item.
*MediaInfoApi* | [**open_live_stream**](MediaInfoApi.md#open_live_stream) | **POST** /LiveStreams/Open | Opens a media source.
*MediaSegmentsApi* | [**get_item_segments**](MediaSegmentsApi.md#get_item_segments) | **GET** /MediaSegments/{itemId} | Gets all media segments based on an itemId.
*MoviesApi* | [**get_movie_recommendations**](MoviesApi.md#get_movie_recommendations) | **GET** /Movies/Recommendations | Gets movie recommendations.
*MusicGenresApi* | [**get_music_genre**](MusicGenresApi.md#get_music_genre) | **GET** /MusicGenres/{genreName} | Gets a music genre, by name.
*MusicGenresApi* | [**get_music_genres**](MusicGenresApi.md#get_music_genres) | **GET** /MusicGenres | Gets all music genres from a given item, folder, or the entire library.
*PackageApi* | [**cancel_package_installation**](PackageApi.md#cancel_package_installation) | **DELETE** /Packages/Installing/{packageId} | Cancels a package installation.
*PackageApi* | [**get_package_info**](PackageApi.md#get_package_info) | **GET** /Packages/{name} | Gets a package by name or assembly GUID.
*PackageApi* | [**get_packages**](PackageApi.md#get_packages) | **GET** /Packages | Gets available packages.
*PackageApi* | [**get_repositories**](PackageApi.md#get_repositories) | **GET** /Repositories | Gets all package repositories.
*PackageApi* | [**install_package**](PackageApi.md#install_package) | **POST** /Packages/Installed/{name} | Installs a package.
*PackageApi* | [**set_repositories**](PackageApi.md#set_repositories) | **POST** /Repositories | Sets the enabled and existing package repositories.
*PersonsApi* | [**get_person**](PersonsApi.md#get_person) | **GET** /Persons/{name} | Get person by name.
*PersonsApi* | [**get_persons**](PersonsApi.md#get_persons) | **GET** /Persons | Gets all persons.
*PlaylistsApi* | [**add_item_to_playlist**](PlaylistsApi.md#add_item_to_playlist) | **POST** /Playlists/{playlistId}/Items | Adds items to a playlist.
*PlaylistsApi* | [**create_playlist**](PlaylistsApi.md#create_playlist) | **POST** /Playlists | Creates a new playlist.
*PlaylistsApi* | [**get_playlist**](PlaylistsApi.md#get_playlist) | **GET** /Playlists/{playlistId} | Get a playlist.
*PlaylistsApi* | [**get_playlist_items**](PlaylistsApi.md#get_playlist_items) | **GET** /Playlists/{playlistId}/Items | Gets the original items of a playlist.
*PlaylistsApi* | [**get_playlist_user**](PlaylistsApi.md#get_playlist_user) | **GET** /Playlists/{playlistId}/Users/{userId} | Get a playlist user.
*PlaylistsApi* | [**get_playlist_users**](PlaylistsApi.md#get_playlist_users) | **GET** /Playlists/{playlistId}/Users | Get a playlist&#39;s users.
*PlaylistsApi* | [**move_item**](PlaylistsApi.md#move_item) | **POST** /Playlists/{playlistId}/Items/{itemId}/Move/{newIndex} | Moves a playlist item.
*PlaylistsApi* | [**remove_item_from_playlist**](PlaylistsApi.md#remove_item_from_playlist) | **DELETE** /Playlists/{playlistId}/Items | Removes items from a playlist.
*PlaylistsApi* | [**remove_user_from_playlist**](PlaylistsApi.md#remove_user_from_playlist) | **DELETE** /Playlists/{playlistId}/Users/{userId} | Remove a user from a playlist&#39;s users.
*PlaylistsApi* | [**update_playlist**](PlaylistsApi.md#update_playlist) | **POST** /Playlists/{playlistId} | Updates a playlist.
*PlaylistsApi* | [**update_playlist_user**](PlaylistsApi.md#update_playlist_user) | **POST** /Playlists/{playlistId}/Users/{userId} | Modify a user of a playlist&#39;s users.
*PlaystateApi* | [**mark_played_item**](PlaystateApi.md#mark_played_item) | **POST** /UserPlayedItems/{itemId} | Marks an item as played for user.
*PlaystateApi* | [**mark_unplayed_item**](PlaystateApi.md#mark_unplayed_item) | **DELETE** /UserPlayedItems/{itemId} | Marks an item as unplayed for user.
*PlaystateApi* | [**on_playback_progress**](PlaystateApi.md#on_playback_progress) | **POST** /PlayingItems/{itemId}/Progress | Reports a session&#39;s playback progress.
*PlaystateApi* | [**on_playback_start**](PlaystateApi.md#on_playback_start) | **POST** /PlayingItems/{itemId} | Reports that a session has begun playing an item.
*PlaystateApi* | [**on_playback_stopped**](PlaystateApi.md#on_playback_stopped) | **DELETE** /PlayingItems/{itemId} | Reports that a session has stopped playing an item.
*PlaystateApi* | [**ping_playback_session**](PlaystateApi.md#ping_playback_session) | **POST** /Sessions/Playing/Ping | Pings a playback session.
*PlaystateApi* | [**report_playback_progress**](PlaystateApi.md#report_playback_progress) | **POST** /Sessions/Playing/Progress | Reports playback progress within a session.
*PlaystateApi* | [**report_playback_start**](PlaystateApi.md#report_playback_start) | **POST** /Sessions/Playing | Reports playback has started within a session.
*PlaystateApi* | [**report_playback_stopped**](PlaystateApi.md#report_playback_stopped) | **POST** /Sessions/Playing/Stopped | Reports playback has stopped within a session.
*PluginsApi* | [**disable_plugin**](PluginsApi.md#disable_plugin) | **POST** /Plugins/{pluginId}/{version}/Disable | Disable a plugin.
*PluginsApi* | [**enable_plugin**](PluginsApi.md#enable_plugin) | **POST** /Plugins/{pluginId}/{version}/Enable | Enables a disabled plugin.
*PluginsApi* | [**get_plugin_configuration**](PluginsApi.md#get_plugin_configuration) | **GET** /Plugins/{pluginId}/Configuration | Gets plugin configuration.
*PluginsApi* | [**get_plugin_image**](PluginsApi.md#get_plugin_image) | **GET** /Plugins/{pluginId}/{version}/Image | Gets a plugin&#39;s image.
*PluginsApi* | [**get_plugin_manifest**](PluginsApi.md#get_plugin_manifest) | **POST** /Plugins/{pluginId}/Manifest | Gets a plugin&#39;s manifest.
*PluginsApi* | [**get_plugins**](PluginsApi.md#get_plugins) | **GET** /Plugins | Gets a list of currently installed plugins.
*PluginsApi* | [**uninstall_plugin**](PluginsApi.md#uninstall_plugin) | **DELETE** /Plugins/{pluginId} | Uninstalls a plugin.
*PluginsApi* | [**uninstall_plugin_by_version**](PluginsApi.md#uninstall_plugin_by_version) | **DELETE** /Plugins/{pluginId}/{version} | Uninstalls a plugin by version.
*PluginsApi* | [**update_plugin_configuration**](PluginsApi.md#update_plugin_configuration) | **POST** /Plugins/{pluginId}/Configuration | Updates plugin configuration.
*QuickConnectApi* | [**authorize_quick_connect**](QuickConnectApi.md#authorize_quick_connect) | **POST** /QuickConnect/Authorize | Authorizes a pending quick connect request.
*QuickConnectApi* | [**get_quick_connect_enabled**](QuickConnectApi.md#get_quick_connect_enabled) | **GET** /QuickConnect/Enabled | Gets the current quick connect state.
*QuickConnectApi* | [**get_quick_connect_state**](QuickConnectApi.md#get_quick_connect_state) | **GET** /QuickConnect/Connect | Attempts to retrieve authentication information.
*QuickConnectApi* | [**initiate_quick_connect**](QuickConnectApi.md#initiate_quick_connect) | **POST** /QuickConnect/Initiate | Initiate a new quick connect request.
*RemoteImageApi* | [**download_remote_image**](RemoteImageApi.md#download_remote_image) | **POST** /Items/{itemId}/RemoteImages/Download | Downloads a remote image for an item.
*RemoteImageApi* | [**get_remote_image_providers**](RemoteImageApi.md#get_remote_image_providers) | **GET** /Items/{itemId}/RemoteImages/Providers | Gets available remote image providers for an item.
*RemoteImageApi* | [**get_remote_images**](RemoteImageApi.md#get_remote_images) | **GET** /Items/{itemId}/RemoteImages | Gets available remote images for an item.
*ScheduledTasksApi* | [**get_task**](ScheduledTasksApi.md#get_task) | **GET** /ScheduledTasks/{taskId} | Get task by id.
*ScheduledTasksApi* | [**get_tasks**](ScheduledTasksApi.md#get_tasks) | **GET** /ScheduledTasks | Get tasks.
*ScheduledTasksApi* | [**start_task**](ScheduledTasksApi.md#start_task) | **POST** /ScheduledTasks/Running/{taskId} | Start specified task.
*ScheduledTasksApi* | [**stop_task**](ScheduledTasksApi.md#stop_task) | **DELETE** /ScheduledTasks/Running/{taskId} | Stop specified task.
*ScheduledTasksApi* | [**update_task**](ScheduledTasksApi.md#update_task) | **POST** /ScheduledTasks/{taskId}/Triggers | Update specified task triggers.
*SearchApi* | [**get_search_hints**](SearchApi.md#get_search_hints) | **GET** /Search/Hints | Gets the search hint result.
*SessionApi* | [**add_user_to_session**](SessionApi.md#add_user_to_session) | **POST** /Sessions/{sessionId}/User/{userId} | Adds an additional user to a session.
*SessionApi* | [**display_content**](SessionApi.md#display_content) | **POST** /Sessions/{sessionId}/Viewing | Instructs a session to browse to an item or view.
*SessionApi* | [**get_auth_providers**](SessionApi.md#get_auth_providers) | **GET** /Auth/Providers | Get all auth providers.
*SessionApi* | [**get_password_reset_providers**](SessionApi.md#get_password_reset_providers) | **GET** /Auth/PasswordResetProviders | Get all password reset providers.
*SessionApi* | [**get_sessions**](SessionApi.md#get_sessions) | **GET** /Sessions | Gets a list of sessions.
*SessionApi* | [**play**](SessionApi.md#play) | **POST** /Sessions/{sessionId}/Playing | Instructs a session to play an item.
*SessionApi* | [**post_capabilities**](SessionApi.md#post_capabilities) | **POST** /Sessions/Capabilities | Updates capabilities for a device.
*SessionApi* | [**post_full_capabilities**](SessionApi.md#post_full_capabilities) | **POST** /Sessions/Capabilities/Full | Updates capabilities for a device.
*SessionApi* | [**remove_user_from_session**](SessionApi.md#remove_user_from_session) | **DELETE** /Sessions/{sessionId}/User/{userId} | Removes an additional user from a session.
*SessionApi* | [**report_session_ended**](SessionApi.md#report_session_ended) | **POST** /Sessions/Logout | Reports that a session has ended.
*SessionApi* | [**report_viewing**](SessionApi.md#report_viewing) | **POST** /Sessions/Viewing | Reports that a session is viewing an item.
*SessionApi* | [**send_full_general_command**](SessionApi.md#send_full_general_command) | **POST** /Sessions/{sessionId}/Command | Issues a full general command to a client.
*SessionApi* | [**send_general_command**](SessionApi.md#send_general_command) | **POST** /Sessions/{sessionId}/Command/{command} | Issues a general command to a client.
*SessionApi* | [**send_message_command**](SessionApi.md#send_message_command) | **POST** /Sessions/{sessionId}/Message | Issues a command to a client to display a message to the user.
*SessionApi* | [**send_playstate_command**](SessionApi.md#send_playstate_command) | **POST** /Sessions/{sessionId}/Playing/{command} | Issues a playstate command to a client.
*SessionApi* | [**send_system_command**](SessionApi.md#send_system_command) | **POST** /Sessions/{sessionId}/System/{command} | Issues a system command to a client.
*StartupApi* | [**complete_wizard**](StartupApi.md#complete_wizard) | **POST** /Startup/Complete | Completes the startup wizard.
*StartupApi* | [**get_first_user**](StartupApi.md#get_first_user) | **GET** /Startup/User | Gets the first user.
*StartupApi* | [**get_first_user2**](StartupApi.md#get_first_user2) | **GET** /Startup/FirstUser | Gets the first user.
*StartupApi* | [**get_startup_configuration**](StartupApi.md#get_startup_configuration) | **GET** /Startup/Configuration | Gets the initial startup wizard configuration.
*StartupApi* | [**set_remote_access**](StartupApi.md#set_remote_access) | **POST** /Startup/RemoteAccess | Sets remote access and UPnP.
*StartupApi* | [**update_initial_configuration**](StartupApi.md#update_initial_configuration) | **POST** /Startup/Configuration | Sets the initial startup wizard configuration.
*StartupApi* | [**update_startup_user**](StartupApi.md#update_startup_user) | **POST** /Startup/User | Sets the user name and password.
*StudiosApi* | [**get_studio**](StudiosApi.md#get_studio) | **GET** /Studios/{name} | Gets a studio by name.
*StudiosApi* | [**get_studios**](StudiosApi.md#get_studios) | **GET** /Studios | Gets all studios from a given item, folder, or the entire library.
*SubtitleApi* | [**delete_subtitle**](SubtitleApi.md#delete_subtitle) | **DELETE** /Videos/{itemId}/Subtitles/{index} | Deletes an external subtitle file.
*SubtitleApi* | [**download_remote_subtitles**](SubtitleApi.md#download_remote_subtitles) | **POST** /Items/{itemId}/RemoteSearch/Subtitles/{subtitleId} | Downloads a remote subtitle.
*SubtitleApi* | [**get_fallback_font**](SubtitleApi.md#get_fallback_font) | **GET** /FallbackFont/Fonts/{name} | Gets a fallback font file.
*SubtitleApi* | [**get_fallback_font_list**](SubtitleApi.md#get_fallback_font_list) | **GET** /FallbackFont/Fonts | Gets a list of available fallback font files.
*SubtitleApi* | [**get_remote_subtitles**](SubtitleApi.md#get_remote_subtitles) | **GET** /Providers/Subtitles/Subtitles/{subtitleId} | Gets the remote subtitles.
*SubtitleApi* | [**get_subtitle**](SubtitleApi.md#get_subtitle) | **GET** /Videos/{routeItemId}/{routeMediaSourceId}/Subtitles/{routeIndex}/Stream.{routeFormat} | Gets subtitles in a specified format.
*SubtitleApi* | [**get_subtitle_playlist**](SubtitleApi.md#get_subtitle_playlist) | **GET** /Videos/{itemId}/{mediaSourceId}/Subtitles/{index}/subtitles.m3u8 | Gets an HLS subtitle playlist.
*SubtitleApi* | [**get_subtitle_with_ticks**](SubtitleApi.md#get_subtitle_with_ticks) | **GET** /Videos/{routeItemId}/{routeMediaSourceId}/Subtitles/{routeIndex}/{routeStartPositionTicks}/Stream.{routeFormat} | Gets subtitles in a specified format.
*SubtitleApi* | [**search_remote_subtitles**](SubtitleApi.md#search_remote_subtitles) | **GET** /Items/{itemId}/RemoteSearch/Subtitles/{language} | Search remote subtitles.
*SubtitleApi* | [**upload_subtitle**](SubtitleApi.md#upload_subtitle) | **POST** /Videos/{itemId}/Subtitles | Upload an external subtitle file.
*SuggestionsApi* | [**get_suggestions**](SuggestionsApi.md#get_suggestions) | **GET** /Items/Suggestions | Gets suggestions.
*SyncPlayApi* | [**sync_play_buffering**](SyncPlayApi.md#sync_play_buffering) | **POST** /SyncPlay/Buffering | Notify SyncPlay group that member is buffering.
*SyncPlayApi* | [**sync_play_create_group**](SyncPlayApi.md#sync_play_create_group) | **POST** /SyncPlay/New | Create a new SyncPlay group.
*SyncPlayApi* | [**sync_play_get_group**](SyncPlayApi.md#sync_play_get_group) | **GET** /SyncPlay/{id} | Gets a SyncPlay group by id.
*SyncPlayApi* | [**sync_play_get_groups**](SyncPlayApi.md#sync_play_get_groups) | **GET** /SyncPlay/List | Gets all SyncPlay groups.
*SyncPlayApi* | [**sync_play_join_group**](SyncPlayApi.md#sync_play_join_group) | **POST** /SyncPlay/Join | Join an existing SyncPlay group.
*SyncPlayApi* | [**sync_play_leave_group**](SyncPlayApi.md#sync_play_leave_group) | **POST** /SyncPlay/Leave | Leave the joined SyncPlay group.
*SyncPlayApi* | [**sync_play_move_playlist_item**](SyncPlayApi.md#sync_play_move_playlist_item) | **POST** /SyncPlay/MovePlaylistItem | Request to move an item in the playlist in SyncPlay group.
*SyncPlayApi* | [**sync_play_next_item**](SyncPlayApi.md#sync_play_next_item) | **POST** /SyncPlay/NextItem | Request next item in SyncPlay group.
*SyncPlayApi* | [**sync_play_pause**](SyncPlayApi.md#sync_play_pause) | **POST** /SyncPlay/Pause | Request pause in SyncPlay group.
*SyncPlayApi* | [**sync_play_ping**](SyncPlayApi.md#sync_play_ping) | **POST** /SyncPlay/Ping | Update session ping.
*SyncPlayApi* | [**sync_play_previous_item**](SyncPlayApi.md#sync_play_previous_item) | **POST** /SyncPlay/PreviousItem | Request previous item in SyncPlay group.
*SyncPlayApi* | [**sync_play_queue**](SyncPlayApi.md#sync_play_queue) | **POST** /SyncPlay/Queue | Request to queue items to the playlist of a SyncPlay group.
*SyncPlayApi* | [**sync_play_ready**](SyncPlayApi.md#sync_play_ready) | **POST** /SyncPlay/Ready | Notify SyncPlay group that member is ready for playback.
*SyncPlayApi* | [**sync_play_remove_from_playlist**](SyncPlayApi.md#sync_play_remove_from_playlist) | **POST** /SyncPlay/RemoveFromPlaylist | Request to remove items from the playlist in SyncPlay group.
*SyncPlayApi* | [**sync_play_seek**](SyncPlayApi.md#sync_play_seek) | **POST** /SyncPlay/Seek | Request seek in SyncPlay group.
*SyncPlayApi* | [**sync_play_set_ignore_wait**](SyncPlayApi.md#sync_play_set_ignore_wait) | **POST** /SyncPlay/SetIgnoreWait | Request SyncPlay group to ignore member during group-wait.
*SyncPlayApi* | [**sync_play_set_new_queue**](SyncPlayApi.md#sync_play_set_new_queue) | **POST** /SyncPlay/SetNewQueue | Request to set new playlist in SyncPlay group.
*SyncPlayApi* | [**sync_play_set_playlist_item**](SyncPlayApi.md#sync_play_set_playlist_item) | **POST** /SyncPlay/SetPlaylistItem | Request to change playlist item in SyncPlay group.
*SyncPlayApi* | [**sync_play_set_repeat_mode**](SyncPlayApi.md#sync_play_set_repeat_mode) | **POST** /SyncPlay/SetRepeatMode | Request to set repeat mode in SyncPlay group.
*SyncPlayApi* | [**sync_play_set_shuffle_mode**](SyncPlayApi.md#sync_play_set_shuffle_mode) | **POST** /SyncPlay/SetShuffleMode | Request to set shuffle mode in SyncPlay group.
*SyncPlayApi* | [**sync_play_stop**](SyncPlayApi.md#sync_play_stop) | **POST** /SyncPlay/Stop | Request stop in SyncPlay group.
*SyncPlayApi* | [**sync_play_unpause**](SyncPlayApi.md#sync_play_unpause) | **POST** /SyncPlay/Unpause | Request unpause in SyncPlay group.
*SystemApi* | [**get_endpoint_info**](SystemApi.md#get_endpoint_info) | **GET** /System/Endpoint | Gets information about the request endpoint.
*SystemApi* | [**get_log_file**](SystemApi.md#get_log_file) | **GET** /System/Logs/Log | Gets a log file.
*SystemApi* | [**get_ping_system**](SystemApi.md#get_ping_system) | **GET** /System/Ping | Pings the system.
*SystemApi* | [**get_public_system_info**](SystemApi.md#get_public_system_info) | **GET** /System/Info/Public | Gets public information about the server.
*SystemApi* | [**get_server_logs**](SystemApi.md#get_server_logs) | **GET** /System/Logs | Gets a list of available server log files.
*SystemApi* | [**get_system_info**](SystemApi.md#get_system_info) | **GET** /System/Info | Gets information about the server.
*SystemApi* | [**get_system_storage**](SystemApi.md#get_system_storage) | **GET** /System/Info/Storage | Gets information about the server.
*SystemApi* | [**post_ping_system**](SystemApi.md#post_ping_system) | **POST** /System/Ping | Pings the system.
*SystemApi* | [**restart_application**](SystemApi.md#restart_application) | **POST** /System/Restart | Restarts the application.
*SystemApi* | [**shutdown_application**](SystemApi.md#shutdown_application) | **POST** /System/Shutdown | Shuts down the application.
*TimeSyncApi* | [**get_utc_time**](TimeSyncApi.md#get_utc_time) | **GET** /GetUtcTime | Gets the current UTC time.
*TmdbApi* | [**tmdb_client_configuration**](TmdbApi.md#tmdb_client_configuration) | **GET** /Tmdb/ClientConfiguration | Gets the TMDb image configuration options.
*TrailersApi* | [**get_trailers**](TrailersApi.md#get_trailers) | **GET** /Trailers | Finds movies and trailers similar to a given trailer.
*TrickplayApi* | [**get_trickplay_hls_playlist**](TrickplayApi.md#get_trickplay_hls_playlist) | **GET** /Videos/{itemId}/Trickplay/{width}/tiles.m3u8 | Gets an image tiles playlist for trickplay.
*TrickplayApi* | [**get_trickplay_tile_image**](TrickplayApi.md#get_trickplay_tile_image) | **GET** /Videos/{itemId}/Trickplay/{width}/{index}.jpg | Gets a trickplay tile image.
*TvShowsApi* | [**get_episodes**](TvShowsApi.md#get_episodes) | **GET** /Shows/{seriesId}/Episodes | Gets episodes for a tv season.
*TvShowsApi* | [**get_next_up**](TvShowsApi.md#get_next_up) | **GET** /Shows/NextUp | Gets a list of next up episodes.
*TvShowsApi* | [**get_seasons**](TvShowsApi.md#get_seasons) | **GET** /Shows/{seriesId}/Seasons | Gets seasons for a tv series.
*TvShowsApi* | [**get_upcoming_episodes**](TvShowsApi.md#get_upcoming_episodes) | **GET** /Shows/Upcoming | Gets a list of upcoming episodes.
*UniversalAudioApi* | [**get_universal_audio_stream**](UniversalAudioApi.md#get_universal_audio_stream) | **GET** /Audio/{itemId}/universal | Gets an audio stream.
*UniversalAudioApi* | [**head_universal_audio_stream**](UniversalAudioApi.md#head_universal_audio_stream) | **HEAD** /Audio/{itemId}/universal | Gets an audio stream.
*UserApi* | [**authenticate_user_by_name**](UserApi.md#authenticate_user_by_name) | **POST** /Users/AuthenticateByName | Authenticates a user by name.
*UserApi* | [**authenticate_with_quick_connect**](UserApi.md#authenticate_with_quick_connect) | **POST** /Users/AuthenticateWithQuickConnect | Authenticates a user with quick connect.
*UserApi* | [**create_user_by_name**](UserApi.md#create_user_by_name) | **POST** /Users/New | Creates a user.
*UserApi* | [**delete_user**](UserApi.md#delete_user) | **DELETE** /Users/{userId} | Deletes a user.
*UserApi* | [**forgot_password**](UserApi.md#forgot_password) | **POST** /Users/ForgotPassword | Initiates the forgot password process for a local user.
*UserApi* | [**forgot_password_pin**](UserApi.md#forgot_password_pin) | **POST** /Users/ForgotPassword/Pin | Redeems a forgot password pin.
*UserApi* | [**get_current_user**](UserApi.md#get_current_user) | **GET** /Users/Me | Gets the user based on auth token.
*UserApi* | [**get_public_users**](UserApi.md#get_public_users) | **GET** /Users/Public | Gets a list of publicly visible users for display on a login screen.
*UserApi* | [**get_user_by_id**](UserApi.md#get_user_by_id) | **GET** /Users/{userId} | Gets a user by Id.
*UserApi* | [**get_users**](UserApi.md#get_users) | **GET** /Users | Gets a list of users.
*UserApi* | [**update_user**](UserApi.md#update_user) | **POST** /Users | Updates a user.
*UserApi* | [**update_user_configuration**](UserApi.md#update_user_configuration) | **POST** /Users/Configuration | Updates a user configuration.
*UserApi* | [**update_user_password**](UserApi.md#update_user_password) | **POST** /Users/Password | Updates a user&#39;s password.
*UserApi* | [**update_user_policy**](UserApi.md#update_user_policy) | **POST** /Users/{userId}/Policy | Updates a user policy.
*UserLibraryApi* | [**delete_user_item_rating**](UserLibraryApi.md#delete_user_item_rating) | **DELETE** /UserItems/{itemId}/Rating | Deletes a user&#39;s saved personal rating for an item.
*UserLibraryApi* | [**get_intros**](UserLibraryApi.md#get_intros) | **GET** /Items/{itemId}/Intros | Gets intros to play before the main media item plays.
*UserLibraryApi* | [**get_item**](UserLibraryApi.md#get_item) | **GET** /Items/{itemId} | Gets an item from a user&#39;s library.
*UserLibraryApi* | [**get_latest_media**](UserLibraryApi.md#get_latest_media) | **GET** /Items/Latest | Gets latest media.
*UserLibraryApi* | [**get_local_trailers**](UserLibraryApi.md#get_local_trailers) | **GET** /Items/{itemId}/LocalTrailers | Gets local trailers for an item.
*UserLibraryApi* | [**get_root_folder**](UserLibraryApi.md#get_root_folder) | **GET** /Items/Root | Gets the root folder from a user&#39;s library.
*UserLibraryApi* | [**get_special_features**](UserLibraryApi.md#get_special_features) | **GET** /Items/{itemId}/SpecialFeatures | Gets special features for an item.
*UserLibraryApi* | [**mark_favorite_item**](UserLibraryApi.md#mark_favorite_item) | **POST** /UserFavoriteItems/{itemId} | Marks an item as a favorite.
*UserLibraryApi* | [**unmark_favorite_item**](UserLibraryApi.md#unmark_favorite_item) | **DELETE** /UserFavoriteItems/{itemId} | Unmarks item as a favorite.
*UserLibraryApi* | [**update_user_item_rating**](UserLibraryApi.md#update_user_item_rating) | **POST** /UserItems/{itemId}/Rating | Updates a user&#39;s rating for an item.
*UserViewsApi* | [**get_grouping_options**](UserViewsApi.md#get_grouping_options) | **GET** /UserViews/GroupingOptions | Get user view grouping options.
*UserViewsApi* | [**get_user_views**](UserViewsApi.md#get_user_views) | **GET** /UserViews | Get user views.
*VideoAttachmentsApi* | [**get_attachment**](VideoAttachmentsApi.md#get_attachment) | **GET** /Videos/{videoId}/{mediaSourceId}/Attachments/{index} | Get video attachment.
*VideosApi* | [**delete_alternate_sources**](VideosApi.md#delete_alternate_sources) | **DELETE** /Videos/{itemId}/AlternateSources | Removes alternate video sources.
*VideosApi* | [**get_additional_part**](VideosApi.md#get_additional_part) | **GET** /Videos/{itemId}/AdditionalParts | Gets additional parts for a video.
*VideosApi* | [**get_video_stream**](VideosApi.md#get_video_stream) | **GET** /Videos/{itemId}/stream | Gets a video stream.
*VideosApi* | [**get_video_stream_by_container**](VideosApi.md#get_video_stream_by_container) | **GET** /Videos/{itemId}/stream.{container} | Gets a video stream.
*VideosApi* | [**head_video_stream**](VideosApi.md#head_video_stream) | **HEAD** /Videos/{itemId}/stream | Gets a video stream.
*VideosApi* | [**head_video_stream_by_container**](VideosApi.md#head_video_stream_by_container) | **HEAD** /Videos/{itemId}/stream.{container} | Gets a video stream.
*VideosApi* | [**merge_versions**](VideosApi.md#merge_versions) | **POST** /Videos/MergeVersions | Merges videos into a single record.
*YearsApi* | [**get_year**](YearsApi.md#get_year) | **GET** /Years/{year} | Gets a year.
*YearsApi* | [**get_years**](YearsApi.md#get_years) | **GET** /Years | Get years.


## Documentation For Models

 - [AccessSchedule](AccessSchedule.md)
 - [ActivityLogEntry](ActivityLogEntry.md)
 - [ActivityLogEntryMessage](ActivityLogEntryMessage.md)
 - [ActivityLogEntryQueryResult](ActivityLogEntryQueryResult.md)
 - [ActivityLogEntryStartMessage](ActivityLogEntryStartMessage.md)
 - [ActivityLogEntryStopMessage](ActivityLogEntryStopMessage.md)
 - [AddVirtualFolderDto](AddVirtualFolderDto.md)
 - [AlbumInfo](AlbumInfo.md)
 - [AlbumInfoRemoteSearchQuery](AlbumInfoRemoteSearchQuery.md)
 - [AllThemeMediaResult](AllThemeMediaResult.md)
 - [ArtistInfo](ArtistInfo.md)
 - [ArtistInfoRemoteSearchQuery](ArtistInfoRemoteSearchQuery.md)
 - [AudioSpatialFormat](AudioSpatialFormat.md)
 - [AuthenticateUserByName](AuthenticateUserByName.md)
 - [AuthenticationInfo](AuthenticationInfo.md)
 - [AuthenticationInfoQueryResult](AuthenticationInfoQueryResult.md)
 - [AuthenticationResult](AuthenticationResult.md)
 - [BackupManifestDto](BackupManifestDto.md)
 - [BackupOptionsDto](BackupOptionsDto.md)
 - [BackupRestoreRequestDto](BackupRestoreRequestDto.md)
 - [BaseItemDto](BaseItemDto.md)
 - [BaseItemDtoImageBlurHashes](BaseItemDtoImageBlurHashes.md)
 - [BaseItemDtoQueryResult](BaseItemDtoQueryResult.md)
 - [BaseItemKind](BaseItemKind.md)
 - [BaseItemPerson](BaseItemPerson.md)
 - [BaseItemPersonImageBlurHashes](BaseItemPersonImageBlurHashes.md)
 - [BookInfo](BookInfo.md)
 - [BookInfoRemoteSearchQuery](BookInfoRemoteSearchQuery.md)
 - [BoxSetInfo](BoxSetInfo.md)
 - [BoxSetInfoRemoteSearchQuery](BoxSetInfoRemoteSearchQuery.md)
 - [BrandingOptionsDto](BrandingOptionsDto.md)
 - [BufferRequestDto](BufferRequestDto.md)
 - [CastReceiverApplication](CastReceiverApplication.md)
 - [ChannelFeatures](ChannelFeatures.md)
 - [ChannelItemSortField](ChannelItemSortField.md)
 - [ChannelMappingOptionsDto](ChannelMappingOptionsDto.md)
 - [ChannelMediaContentType](ChannelMediaContentType.md)
 - [ChannelMediaType](ChannelMediaType.md)
 - [ChannelType](ChannelType.md)
 - [ChapterInfo](ChapterInfo.md)
 - [ClientCapabilitiesDto](ClientCapabilitiesDto.md)
 - [ClientLogDocumentResponseDto](ClientLogDocumentResponseDto.md)
 - [CodecProfile](CodecProfile.md)
 - [CodecType](CodecType.md)
 - [CollectionCreationResult](CollectionCreationResult.md)
 - [CollectionType](CollectionType.md)
 - [CollectionTypeOptions](CollectionTypeOptions.md)
 - [ConfigImageTypes](ConfigImageTypes.md)
 - [ConfigurationPageInfo](ConfigurationPageInfo.md)
 - [ContainerProfile](ContainerProfile.md)
 - [CountryInfo](CountryInfo.md)
 - [CreatePlaylistDto](CreatePlaylistDto.md)
 - [CreateUserByName](CreateUserByName.md)
 - [CultureDto](CultureDto.md)
 - [CustomDatabaseOption](CustomDatabaseOption.md)
 - [CustomDatabaseOptions](CustomDatabaseOptions.md)
 - [DatabaseConfigurationOptions](DatabaseConfigurationOptions.md)
 - [DatabaseLockingBehaviorTypes](DatabaseLockingBehaviorTypes.md)
 - [DayOfWeek](DayOfWeek.md)
 - [DayPattern](DayPattern.md)
 - [DefaultDirectoryBrowserInfoDto](DefaultDirectoryBrowserInfoDto.md)
 - [DeinterlaceMethod](DeinterlaceMethod.md)
 - [DeviceInfoDto](DeviceInfoDto.md)
 - [DeviceInfoDtoQueryResult](DeviceInfoDtoQueryResult.md)
 - [DeviceOptionsDto](DeviceOptionsDto.md)
 - [DeviceProfile](DeviceProfile.md)
 - [DirectPlayProfile](DirectPlayProfile.md)
 - [DisplayPreferencesDto](DisplayPreferencesDto.md)
 - [DlnaProfileType](DlnaProfileType.md)
 - [DownMixStereoAlgorithms](DownMixStereoAlgorithms.md)
 - [DynamicDayOfWeek](DynamicDayOfWeek.md)
 - [EmbeddedSubtitleOptions](EmbeddedSubtitleOptions.md)
 - [EncoderPreset](EncoderPreset.md)
 - [EncodingContext](EncodingContext.md)
 - [EncodingOptions](EncodingOptions.md)
 - [EndPointInfo](EndPointInfo.md)
 - [ExternalIdInfo](ExternalIdInfo.md)
 - [ExternalIdMediaType](ExternalIdMediaType.md)
 - [ExternalUrl](ExternalUrl.md)
 - [ExtraType](ExtraType.md)
 - [FileSystemEntryInfo](FileSystemEntryInfo.md)
 - [FileSystemEntryType](FileSystemEntryType.md)
 - [FolderStorageDto](FolderStorageDto.md)
 - [FontFile](FontFile.md)
 - [ForceKeepAliveMessage](ForceKeepAliveMessage.md)
 - [ForgotPasswordAction](ForgotPasswordAction.md)
 - [ForgotPasswordDto](ForgotPasswordDto.md)
 - [ForgotPasswordPinDto](ForgotPasswordPinDto.md)
 - [ForgotPasswordResult](ForgotPasswordResult.md)
 - [GeneralCommand](GeneralCommand.md)
 - [GeneralCommandMessage](GeneralCommandMessage.md)
 - [GeneralCommandType](GeneralCommandType.md)
 - [GetProgramsDto](GetProgramsDto.md)
 - [GroupInfoDto](GroupInfoDto.md)
 - [GroupQueueMode](GroupQueueMode.md)
 - [GroupRepeatMode](GroupRepeatMode.md)
 - [GroupShuffleMode](GroupShuffleMode.md)
 - [GroupStateType](GroupStateType.md)
 - [GroupStateUpdate](GroupStateUpdate.md)
 - [GroupUpdate](GroupUpdate.md)
 - [GroupUpdateType](GroupUpdateType.md)
 - [GuideInfo](GuideInfo.md)
 - [HardwareAccelerationType](HardwareAccelerationType.md)
 - [IPlugin](IPlugin.md)
 - [IgnoreWaitRequestDto](IgnoreWaitRequestDto.md)
 - [ImageFormat](ImageFormat.md)
 - [ImageInfo](ImageInfo.md)
 - [ImageOption](ImageOption.md)
 - [ImageOrientation](ImageOrientation.md)
 - [ImageProviderInfo](ImageProviderInfo.md)
 - [ImageResolution](ImageResolution.md)
 - [ImageSavingConvention](ImageSavingConvention.md)
 - [ImageType](ImageType.md)
 - [InboundKeepAliveMessage](InboundKeepAliveMessage.md)
 - [InboundWebSocketMessage](InboundWebSocketMessage.md)
 - [InstallationInfo](InstallationInfo.md)
 - [IsoType](IsoType.md)
 - [ItemCounts](ItemCounts.md)
 - [ItemFields](ItemFields.md)
 - [ItemFilter](ItemFilter.md)
 - [ItemSortBy](ItemSortBy.md)
 - [JoinGroupRequestDto](JoinGroupRequestDto.md)
 - [KeepUntil](KeepUntil.md)
 - [LibraryChangedMessage](LibraryChangedMessage.md)
 - [LibraryOptionInfoDto](LibraryOptionInfoDto.md)
 - [LibraryOptions](LibraryOptions.md)
 - [LibraryOptionsResultDto](LibraryOptionsResultDto.md)
 - [LibraryStorageDto](LibraryStorageDto.md)
 - [LibraryTypeOptionsDto](LibraryTypeOptionsDto.md)
 - [LibraryUpdateInfo](LibraryUpdateInfo.md)
 - [ListingsProviderInfo](ListingsProviderInfo.md)
 - [LiveStreamResponse](LiveStreamResponse.md)
 - [LiveTvInfo](LiveTvInfo.md)
 - [LiveTvOptions](LiveTvOptions.md)
 - [LiveTvServiceInfo](LiveTvServiceInfo.md)
 - [LiveTvServiceStatus](LiveTvServiceStatus.md)
 - [LocalizationOption](LocalizationOption.md)
 - [LocationType](LocationType.md)
 - [LogFile](LogFile.md)
 - [LogLevel](LogLevel.md)
 - [LyricDto](LyricDto.md)
 - [LyricLine](LyricLine.md)
 - [LyricLineCue](LyricLineCue.md)
 - [LyricMetadata](LyricMetadata.md)
 - [MediaAttachment](MediaAttachment.md)
 - [MediaPathDto](MediaPathDto.md)
 - [MediaPathInfo](MediaPathInfo.md)
 - [MediaProtocol](MediaProtocol.md)
 - [MediaSegmentDto](MediaSegmentDto.md)
 - [MediaSegmentDtoQueryResult](MediaSegmentDtoQueryResult.md)
 - [MediaSegmentType](MediaSegmentType.md)
 - [MediaSourceInfo](MediaSourceInfo.md)
 - [MediaSourceType](MediaSourceType.md)
 - [MediaStream](MediaStream.md)
 - [MediaStreamProtocol](MediaStreamProtocol.md)
 - [MediaStreamType](MediaStreamType.md)
 - [MediaType](MediaType.md)
 - [MediaUpdateInfoDto](MediaUpdateInfoDto.md)
 - [MediaUpdateInfoPathDto](MediaUpdateInfoPathDto.md)
 - [MediaUrl](MediaUrl.md)
 - [MessageCommand](MessageCommand.md)
 - [MetadataConfiguration](MetadataConfiguration.md)
 - [MetadataEditorInfo](MetadataEditorInfo.md)
 - [MetadataField](MetadataField.md)
 - [MetadataOptions](MetadataOptions.md)
 - [MetadataRefreshMode](MetadataRefreshMode.md)
 - [MovePlaylistItemRequestDto](MovePlaylistItemRequestDto.md)
 - [MovieInfo](MovieInfo.md)
 - [MovieInfoRemoteSearchQuery](MovieInfoRemoteSearchQuery.md)
 - [MusicVideoInfo](MusicVideoInfo.md)
 - [MusicVideoInfoRemoteSearchQuery](MusicVideoInfoRemoteSearchQuery.md)
 - [NameGuidPair](NameGuidPair.md)
 - [NameIdPair](NameIdPair.md)
 - [NameValuePair](NameValuePair.md)
 - [NetworkConfiguration](NetworkConfiguration.md)
 - [NewGroupRequestDto](NewGroupRequestDto.md)
 - [NextItemRequestDto](NextItemRequestDto.md)
 - [OpenLiveStreamDto](OpenLiveStreamDto.md)
 - [OutboundKeepAliveMessage](OutboundKeepAliveMessage.md)
 - [OutboundWebSocketMessage](OutboundWebSocketMessage.md)
 - [PackageInfo](PackageInfo.md)
 - [ParentalRating](ParentalRating.md)
 - [ParentalRatingScore](ParentalRatingScore.md)
 - [PathSubstitution](PathSubstitution.md)
 - [PersonKind](PersonKind.md)
 - [PersonLookupInfo](PersonLookupInfo.md)
 - [PersonLookupInfoRemoteSearchQuery](PersonLookupInfoRemoteSearchQuery.md)
 - [PinRedeemResult](PinRedeemResult.md)
 - [PingRequestDto](PingRequestDto.md)
 - [PlayAccess](PlayAccess.md)
 - [PlayCommand](PlayCommand.md)
 - [PlayMessage](PlayMessage.md)
 - [PlayMethod](PlayMethod.md)
 - [PlayQueueUpdate](PlayQueueUpdate.md)
 - [PlayQueueUpdateReason](PlayQueueUpdateReason.md)
 - [PlayRequest](PlayRequest.md)
 - [PlayRequestDto](PlayRequestDto.md)
 - [PlaybackErrorCode](PlaybackErrorCode.md)
 - [PlaybackInfoDto](PlaybackInfoDto.md)
 - [PlaybackInfoResponse](PlaybackInfoResponse.md)
 - [PlaybackOrder](PlaybackOrder.md)
 - [PlaybackProgressInfo](PlaybackProgressInfo.md)
 - [PlaybackRequestType](PlaybackRequestType.md)
 - [PlaybackStartInfo](PlaybackStartInfo.md)
 - [PlaybackStopInfo](PlaybackStopInfo.md)
 - [PlayerStateInfo](PlayerStateInfo.md)
 - [PlaylistCreationResult](PlaylistCreationResult.md)
 - [PlaylistDto](PlaylistDto.md)
 - [PlaylistUserPermissions](PlaylistUserPermissions.md)
 - [PlaystateCommand](PlaystateCommand.md)
 - [PlaystateMessage](PlaystateMessage.md)
 - [PlaystateRequest](PlaystateRequest.md)
 - [PluginInfo](PluginInfo.md)
 - [PluginInstallationCancelledMessage](PluginInstallationCancelledMessage.md)
 - [PluginInstallationCompletedMessage](PluginInstallationCompletedMessage.md)
 - [PluginInstallationFailedMessage](PluginInstallationFailedMessage.md)
 - [PluginInstallingMessage](PluginInstallingMessage.md)
 - [PluginStatus](PluginStatus.md)
 - [PluginUninstalledMessage](PluginUninstalledMessage.md)
 - [PreviousItemRequestDto](PreviousItemRequestDto.md)
 - [ProblemDetails](ProblemDetails.md)
 - [ProcessPriorityClass](ProcessPriorityClass.md)
 - [ProfileCondition](ProfileCondition.md)
 - [ProfileConditionType](ProfileConditionType.md)
 - [ProfileConditionValue](ProfileConditionValue.md)
 - [ProgramAudio](ProgramAudio.md)
 - [PublicSystemInfo](PublicSystemInfo.md)
 - [QueryFilters](QueryFilters.md)
 - [QueryFiltersLegacy](QueryFiltersLegacy.md)
 - [QueueItem](QueueItem.md)
 - [QueueRequestDto](QueueRequestDto.md)
 - [QuickConnectDto](QuickConnectDto.md)
 - [QuickConnectResult](QuickConnectResult.md)
 - [RatingType](RatingType.md)
 - [ReadyRequestDto](ReadyRequestDto.md)
 - [RecommendationDto](RecommendationDto.md)
 - [RecommendationType](RecommendationType.md)
 - [RecordingStatus](RecordingStatus.md)
 - [RefreshProgressMessage](RefreshProgressMessage.md)
 - [RemoteImageInfo](RemoteImageInfo.md)
 - [RemoteImageResult](RemoteImageResult.md)
 - [RemoteLyricInfoDto](RemoteLyricInfoDto.md)
 - [RemoteSearchResult](RemoteSearchResult.md)
 - [RemoteSubtitleInfo](RemoteSubtitleInfo.md)
 - [RemoveFromPlaylistRequestDto](RemoveFromPlaylistRequestDto.md)
 - [RepeatMode](RepeatMode.md)
 - [RepositoryInfo](RepositoryInfo.md)
 - [RestartRequiredMessage](RestartRequiredMessage.md)
 - [ScheduledTaskEndedMessage](ScheduledTaskEndedMessage.md)
 - [ScheduledTasksInfoMessage](ScheduledTasksInfoMessage.md)
 - [ScheduledTasksInfoStartMessage](ScheduledTasksInfoStartMessage.md)
 - [ScheduledTasksInfoStopMessage](ScheduledTasksInfoStopMessage.md)
 - [ScrollDirection](ScrollDirection.md)
 - [SearchHint](SearchHint.md)
 - [SearchHintResult](SearchHintResult.md)
 - [SeekRequestDto](SeekRequestDto.md)
 - [SendCommand](SendCommand.md)
 - [SendCommandType](SendCommandType.md)
 - [SeriesInfo](SeriesInfo.md)
 - [SeriesInfoRemoteSearchQuery](SeriesInfoRemoteSearchQuery.md)
 - [SeriesStatus](SeriesStatus.md)
 - [SeriesTimerCancelledMessage](SeriesTimerCancelledMessage.md)
 - [SeriesTimerCreatedMessage](SeriesTimerCreatedMessage.md)
 - [SeriesTimerInfoDto](SeriesTimerInfoDto.md)
 - [SeriesTimerInfoDtoQueryResult](SeriesTimerInfoDtoQueryResult.md)
 - [ServerConfiguration](ServerConfiguration.md)
 - [ServerDiscoveryInfo](ServerDiscoveryInfo.md)
 - [ServerRestartingMessage](ServerRestartingMessage.md)
 - [ServerShuttingDownMessage](ServerShuttingDownMessage.md)
 - [SessionInfoDto](SessionInfoDto.md)
 - [SessionMessageType](SessionMessageType.md)
 - [SessionUserInfo](SessionUserInfo.md)
 - [SessionsMessage](SessionsMessage.md)
 - [SessionsStartMessage](SessionsStartMessage.md)
 - [SessionsStopMessage](SessionsStopMessage.md)
 - [SetChannelMappingDto](SetChannelMappingDto.md)
 - [SetPlaylistItemRequestDto](SetPlaylistItemRequestDto.md)
 - [SetRepeatModeRequestDto](SetRepeatModeRequestDto.md)
 - [SetShuffleModeRequestDto](SetShuffleModeRequestDto.md)
 - [SongInfo](SongInfo.md)
 - [SortOrder](SortOrder.md)
 - [SpecialViewOptionDto](SpecialViewOptionDto.md)
 - [StartupConfigurationDto](StartupConfigurationDto.md)
 - [StartupRemoteAccessDto](StartupRemoteAccessDto.md)
 - [StartupUserDto](StartupUserDto.md)
 - [SubtitleDeliveryMethod](SubtitleDeliveryMethod.md)
 - [SubtitleOptions](SubtitleOptions.md)
 - [SubtitlePlaybackMode](SubtitlePlaybackMode.md)
 - [SubtitleProfile](SubtitleProfile.md)
 - [SyncPlayCommandMessage](SyncPlayCommandMessage.md)
 - [SyncPlayGroupDoesNotExistUpdate](SyncPlayGroupDoesNotExistUpdate.md)
 - [SyncPlayGroupJoinedUpdate](SyncPlayGroupJoinedUpdate.md)
 - [SyncPlayGroupLeftUpdate](SyncPlayGroupLeftUpdate.md)
 - [SyncPlayGroupUpdateMessage](SyncPlayGroupUpdateMessage.md)
 - [SyncPlayLibraryAccessDeniedUpdate](SyncPlayLibraryAccessDeniedUpdate.md)
 - [SyncPlayNotInGroupUpdate](SyncPlayNotInGroupUpdate.md)
 - [SyncPlayPlayQueueUpdate](SyncPlayPlayQueueUpdate.md)
 - [SyncPlayQueueItem](SyncPlayQueueItem.md)
 - [SyncPlayStateUpdate](SyncPlayStateUpdate.md)
 - [SyncPlayUserAccessType](SyncPlayUserAccessType.md)
 - [SyncPlayUserJoinedUpdate](SyncPlayUserJoinedUpdate.md)
 - [SyncPlayUserLeftUpdate](SyncPlayUserLeftUpdate.md)
 - [SystemInfo](SystemInfo.md)
 - [SystemStorageDto](SystemStorageDto.md)
 - [TaskCompletionStatus](TaskCompletionStatus.md)
 - [TaskInfo](TaskInfo.md)
 - [TaskResult](TaskResult.md)
 - [TaskState](TaskState.md)
 - [TaskTriggerInfo](TaskTriggerInfo.md)
 - [TaskTriggerInfoType](TaskTriggerInfoType.md)
 - [ThemeMediaResult](ThemeMediaResult.md)
 - [TimerCancelledMessage](TimerCancelledMessage.md)
 - [TimerCreatedMessage](TimerCreatedMessage.md)
 - [TimerEventInfo](TimerEventInfo.md)
 - [TimerInfoDto](TimerInfoDto.md)
 - [TimerInfoDtoQueryResult](TimerInfoDtoQueryResult.md)
 - [TonemappingAlgorithm](TonemappingAlgorithm.md)
 - [TonemappingMode](TonemappingMode.md)
 - [TonemappingRange](TonemappingRange.md)
 - [TrailerInfo](TrailerInfo.md)
 - [TrailerInfoRemoteSearchQuery](TrailerInfoRemoteSearchQuery.md)
 - [TranscodeReason](TranscodeReason.md)
 - [TranscodeSeekInfo](TranscodeSeekInfo.md)
 - [TranscodingInfo](TranscodingInfo.md)
 - [TranscodingProfile](TranscodingProfile.md)
 - [TransportStreamTimestamp](TransportStreamTimestamp.md)
 - [TrickplayInfoDto](TrickplayInfoDto.md)
 - [TrickplayOptions](TrickplayOptions.md)
 - [TrickplayScanBehavior](TrickplayScanBehavior.md)
 - [TunerChannelMapping](TunerChannelMapping.md)
 - [TunerHostInfo](TunerHostInfo.md)
 - [TypeOptions](TypeOptions.md)
 - [UnratedItem](UnratedItem.md)
 - [UpdateLibraryOptionsDto](UpdateLibraryOptionsDto.md)
 - [UpdateMediaPathRequestDto](UpdateMediaPathRequestDto.md)
 - [UpdatePlaylistDto](UpdatePlaylistDto.md)
 - [UpdatePlaylistUserDto](UpdatePlaylistUserDto.md)
 - [UpdateUserItemDataDto](UpdateUserItemDataDto.md)
 - [UpdateUserPassword](UpdateUserPassword.md)
 - [UploadSubtitleDto](UploadSubtitleDto.md)
 - [UserConfiguration](UserConfiguration.md)
 - [UserDataChangeInfo](UserDataChangeInfo.md)
 - [UserDataChangedMessage](UserDataChangedMessage.md)
 - [UserDeletedMessage](UserDeletedMessage.md)
 - [UserDto](UserDto.md)
 - [UserItemDataDto](UserItemDataDto.md)
 - [UserPolicy](UserPolicy.md)
 - [UserUpdatedMessage](UserUpdatedMessage.md)
 - [UtcTimeResponse](UtcTimeResponse.md)
 - [ValidatePathDto](ValidatePathDto.md)
 - [VersionInfo](VersionInfo.md)
 - [Video3DFormat](Video3DFormat.md)
 - [VideoRange](VideoRange.md)
 - [VideoRangeType](VideoRangeType.md)
 - [VideoType](VideoType.md)
 - [VirtualFolderInfo](VirtualFolderInfo.md)
 - [WebSocketMessage](WebSocketMessage.md)
 - [XbmcMetadataOptions](XbmcMetadataOptions.md)