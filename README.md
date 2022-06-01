This is my custom repo for PMM (Plex-Meta-Manager), this is heavily influenced by the official PMM configuration found [Here](https://github.com/meisnate12/Plex-Meta-Manager-Configs/tree/master/PMM). Thanks to Yozora, Bullmoose20, & Sohjiro for all of that.

Finally the images that I'm using are modified versions of the official images found [here](https://github.com/meisnate12/Plex-Meta-Manager-Images).
Thanks Bullmoose20 for support on modifying these images. 

The Anime Genre images were sourced from [jjjonesjr23](https://theposterdb.com/user/jjjonesjr33) on ThePosterDb's website.

The studio albums were sourced from [musikmann2000](https://theposterdb.com/user/musikmann2000) on ThePosterDb's website
<br>
**Movies Screenshot**
![movies](screenshots/movies.jpg)
**Shows Screenshot**
![Shows](screenshots/series.jpg)
Lists are from [mdblist.com](https://mdblist.com)

Thank you so much to everybody who has made this possible esepcially Sohjiro for PMM.


___
Below you can see my current config file. The key notes you should take away from it is each of the collection files are called using the `- repo:` tag this is different from the `- git:` tag that is in the offical PMM config, the reason for this is I'm using a `custom_repo`. Which you can see near the bottom. 
___
```yaml
####################################
#            Libraries             #
####################################
libraries:
  Animated Series:
    metadata_path:
    - repo: chart/other
      template_variables:
        collection_mode: hide
        use_stevenlu: false
        use_anidb: false
        use_pirated: false
        use_trending_movies: false
        use_popular_movies: false
        use_trending_animated: true
        visible_library_trending_animated: true
        visible_home_trending_animated: true
        visible_shared_trending_animated: true
        use_popular_series: false
        use_trending_series: false
    - repo: show/network
      template_variables:
        use_separator: true
        collection_mode: hide
    - repo: show/streaming
      template_variables:
        use_separator: true
        collection_mode: hide
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/series/animated-series/
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/streaming
      template_variables:
        vertical_offset: 15
  Anime Series:
    metadata_path:
    - repo: chart/myanimelist
      template_variables:
        collection_mode: hide
        visible_library_popular: true
        visible_shared_popular: true
        visible_library_top: true
        visible_shared_top: true
        visible_library_trending: true
        visible_shared_trending: true
        visible_library_season: true
        visible_shared_season: true
    - repo: anime/anime_genre
      template_variables:
        collection_mode: hide
    settings:
      asset_directory: config/assets/series/anime-series/
    operations:
      assets_for_all: true
  Kids Series:
    metadata_path:
    - repo: show/network
      template_variables:
        use_separator: true
        collection_mode: hide
    - repo: show/streaming
      template_variables:
        use_separator: false
        collection_mode: hide
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/series/kids-series/
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/streaming
      template_variables:
        vertical_offset: 15
  Documentary Series:
    metadata_path:
    - repo: show/network
      template_variables:
        use_separator: true
        collection_mode: hide
    - repo: show/streaming
      template_variables:
        collection_mode: hide
        use_separator: false
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/series/documentary-series/
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/streaming
      template_variables:
        vertical_offset: 15
  Reality Series:
    metadata_path:
    - repo: show/network
      template_variables:
        use_separator: true
        collection_mode: hide
    - repo: show/streaming
      template_variables:
        collection_mode: hide
        use_separator: false
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/series/reality-series/
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/streaming
      template_variables:
        vertical_offset: 15
  Series:
    metadata_path:
    - repo: chart/other
      template_variables:
        collection_mode: hide
        use_stevenlu: false
        use_anidb: false
        use_pirated: false
        use_trending_movies: false
        use_popular_movies: false
        use_trending_animated: false
        visible_library_trending_animated: true
        visible_home_trending_animated: true
        visible_shared_trending_animated: true
        use_popular_series: true
        visible_library_popular_series: true
        visible_home_popular_series: true
        visible_shared_popular_series: true
        use_trending_series: true
        visible_library_trending_series: true
        visible_home_trending_series: true
        visible_shared_trending_series: true
    - repo: show/network
      template_variables:
        use_separator: true
        collection_mode: hide
    - repo: show/streaming
      template_variables:
        use_separator: false
        collection_mode: hide
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/series/live-action-series
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/streaming
      template_variables:
        vertical_offset: 15
  Anime Movies:
    metadata_path:
    - repo: anime/anime_movie_collection
    - repo: movie/streaming
      template_variables:
        collection_mode: hide
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/films/anime-movies
      show_missing_assets: false
    operations:
      assets_for_all: true
  Documentary Movies:
    metadata_path:
    - repo: movie/streaming
      template_variables:
        use_separator: false
        collection_mode: hide
        visible_home_all4: false
        visible_home_appletv: false
        visible_home_bet: false
        visible_home_britbox: false
        visible_home_disney: false
        visible_home_hayu: false
        visible_home_hbomax: false
        visible_home_hulu: false
        visible_home_netflix: false
        visible_home_paramount: false
        visible_home_peacock: false
        visible_home_amazon: false
        visible_library_appletv: true
        visible_library_bet: true
        visible_library_britbox: true
        visible_library_disney: true
        visible_library_hbomax: true
        visible_library_hulu: true
        visible_library_netflix: true
        visible_library_paramount: true
        visible_library_peacock: true
        visible_library_amazon: true
    settings:
      asset_directory: config/assets/films/documentary-movies
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/imdb_top_250
  Movies:
    metadata_path:
      - repo: movie/streaming
        template_variables:
          collection_mode: hide
          visible_home_all4: false
          visible_home_appletv: false
          visible_home_bet: false
          visible_home_britbox: false
          visible_home_disney: false
          visible_home_hayu: false
          visible_home_hbomax: false
          visible_home_hulu: false
          visible_home_netflix: false
          visible_home_paramount: false
          visible_home_peacock: false
          visible_home_amazon: false
          visible_library_appletv: true
          visible_library_bet: true
          visible_library_britbox: true
          visible_library_disney: true
          visible_library_hbomax: true
          visible_library_hulu: true
          visible_library_netflix: true
          visible_library_paramount: true
          visible_library_peacock: true
          visible_library_amazon: true
      - repo: chart/other
        template_variables:
          collection_mode: hide
          use_stevenlu: false
          use_anidb: false
          use_pirated: false
          use_trending_movies: true
          use_popular_movies: true
          use_trending_animated: false
          visible_library_popular_movies: true
          visible_home_popular_movies: true
          visible_shared_popular_movies: true
          visible_library_trending_movies: true
          visible_home_trending_movies: true
          visible_shared_trending_movies: true
      - repo: movie/metadata
      - repo: movie/collections
      - repo: studio
      - repo: movie/universe
    settings:
      asset_directory: config/assets/films/movies
    operations:
      assets_for_all: true
    overlay_path:
    - repo: overlays/imdb_top_250
playlist_files:
- repo: playlist
  template_variables:
    libraries: Movies, Series, Animated Series
settings:
  cache: true
  cache_expiration: 60
  asset_folders: true
  asset_depth: 0
  dimensional_asset_rename: true
  show_missing_season_assets: false
  sync_mode: sync
  delete_below_minimum: false
  delete_not_scheduled: false
  run_again_delay: 0
  missing_only_released: true
  only_filter_missing: false
  show_unmanaged: true
  show_filtered: false
  show_options: false
  show_missing: false
  show_missing_assets: false
  tvdb_language: default
  ignore_ids:
  ignore_imdb_ids:
  minimum_items: 2
  default_collection_order:
  create_asset_folders: true
  download_url_assets: false
  verify_ssl: true
  item_refresh_delay: 0
  playlist_sync_to_users: all
  show_missing_episode_assets: false
  show_asset_not_needed: false
  custom_repo: https://github.com/Drazzilb08/pmm-custom-repo/tree/master/
  save_missing: false
  prioritize_assets: false
  playlist_report: false
  check_nightly: false
  asset_directory:
```

Drop me a line if you have questions or any issues. I spent a bit of time to get this to work on my setup without any problems. However if you do please let me know.

PRs are welcome to update and improve the configs. 

Screenshots []

Finally **Use at your own risk**, I take no responsability if you screw up your Plex instance. Always remember the golden rule **Back up, Back up, Back up**.

Cheers