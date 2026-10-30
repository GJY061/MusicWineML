**Local input data**

The notebook expects three CSV files in this directory:

| File | Required content |
| --- | --- |
| `music_genres.csv` | Labelled tracks, including numerical features and `music_genre`. |
| `music_unlabelled.csv` | Tracks with the same input schema, without `music_genre`. |
| `wine_features.csv` | Numerical wine measurements, including `Alcohol`, `Color_Intensity`, and `Hue`. |

The music columns are `instance_id`, `artist_name`, `track_name`, `popularity`, `acousticness`, `danceability`, `duration_ms`, `energy`, `instrumentalness`, `liveness`, `loudness`, `speechiness`, `tempo`, and `valence`. The labelled file also contains `music_genre`.

The wine dataset source is [Wine Dataset for Clustering](https://www.kaggle.com/datasets/harrywang/wine-dataset-for-clustering). The original music data's public distribution source has not been established in this repository; users must supply a compatible copy they are permitted to use.

Raw CSV files are kept out of version control by `.gitignore`. Their local presence allows rerunning the notebook without including them in the public source repository.
