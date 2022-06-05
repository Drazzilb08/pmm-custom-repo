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

Thank you so much to everybody who has made this possible especially Sohjiro for PMM.

---
Below you can see my current config file. The key notes you should take away from it is each of the collection files are called using the `- repo:` tag this is different from the `- git:` tag that is in the offical PMM config, the reason for this is I'm using a `custom_repo`. Which you can see near the bottom.
---
Note: If you're going to use `chart/myanimelist` then you'll need to fill in all your myanimelist information. Info for this can be fhound [here](https://metamanager.wiki/en/latest/config/myanimelist.html) 
Most of these lists require mdblist to operate. Fill in your information for this [here](https://metamanager.wiki/en/latest/config/mdblist.html)
**Example:**

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
          use_separator: false
          collection_mode: hide
      - repo: streaming
        template_variables:
          use_separator: false
          collection_mode: hide
    settings:
      asset_directory: config/assets/series/animated-series/
    operations:
      delete_unmanaged_collections: true
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
      delete_unmanaged_collections: true
      assets_for_all: true
  Kids Series:
    metadata_path:
      - repo: show/network
        template_variables:
          use_separator: false
          collection_mode: hide
      - repo: streaming
        template_variables:
          use_separator: false
          collection_mode: hide
    settings:
      asset_directory: config/assets/series/kids-series/
    operations:
      delete_unmanaged_collections: true
      assets_for_all: true
    overlay_path:
      - repo: overlays/streaming
        template_variables:
          vertical_offset: 15
  Documentary Series:
    metadata_path:
      - repo: show/network
        template_variables:
          use_separator: false
          collection_mode: hide
      - repo: streaming
        template_variables:
          collection_mode: hide
          use_separator: false
    settings:
      asset_directory: config/assets/series/documentary-series/
    operations:
      delete_unmanaged_collections: true
      assets_for_all: true
    overlay_path:
      - repo: overlays/streaming
        template_variables:
          vertical_offset: 15
  Reality Series:
    metadata_path:
      - repo: show/network
        template_variables:
          use_separator: false
          collection_mode: hide
      - repo: streaming
        template_variables:
          collection_mode: hide
          use_separator: false
    settings:
      asset_directory: config/assets/series/reality-series/
    operations:
      delete_unmanaged_collections: true
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
          use_separator: false
          collection_mode: hide
      - repo: streaming
        template_variables:
          use_separator: false
          collection_mode: hide
    settings:
      asset_directory: config/assets/series/live-action-series
    operations:
      delete_unmanaged_collections: true
      assets_for_all: true
    overlay_path:
      - repo: overlays/streaming
        template_variables:
          vertical_offset: 15
  Anime Movies:
    metadata_path:
      - repo: anime/anime_movie_collection
    settings:
      asset_directory: config/assets/films/anime-movies
      show_missing_assets: false
      delete_unmanaged_collections: true
    operations:
      delete_unmanaged_collections: true
      assets_for_all: true
  Documentary Movies:
    metadata_path:
      - repo: streaming
        template_variables:
          use_separator: false
          collection_mode: hide
          visible_library_amazon: true
    settings:
      asset_directory: config/assets/films/documentary-movies
    operations:
      delete_unmanaged_collections: true
      assets_for_all: true
    overlay_path:
      - repo: overlays/imdb_top_250
      - repo: overlays/streaming
        template_variables:
          vertical_offset: 15
  Movies:
    metadata_path:
      - repo: streaming
        template_variables:
          collection_mode: hide
          use_separator: false
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
        template_variables:
          collection_mode: hide
          use_separator: false
      - repo: movie/universe
        template_variables:
          collection_mode: hide
          use_separator: false
    settings:
      asset_directory: config/assets/films/movies
    operations:
      delete_unmanaged_collections: true
      assets_for_all: true
    overlay_path:
      - repo: overlays/imdb_top_250
      - repo: overlays/streaming
        template_variables:
          vertical_offset: 15
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

Finally **Use at your own risk**, I take no responsability if you screw up your Plex instance. Always remember the golden rule **Back up, Back up, Back up**.

Cheers
