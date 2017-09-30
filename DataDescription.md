# File description

train_final.csv - the training set of interactions
tracks_final.csv - supplementary information about the items
playlists_final.csv - supplementary information about the users
target_playlists.csv - the set of target playlists that will receive recommendations
target_tracks.csv - the set of target items (tracks) to be recommended
sample_submission.csv - a sample submission file in the correct format: [playlist], [ordered list of recommended items]
PS: all files are given with '\t' as separator, with the exception of the sample_submission which has ',' as separator. This means you have to use ',' as separator for the submission file.

## Attribute description

### train_final

playlist_id - ID of the playlist
track_id - ID of the track

### tracks_final

track_id - ID of the track
artist_id - ID of the artist
duration - duration of the track in seconds
album - ID of the album in which the track is contained
tags - list of significant keywords related to the track; each keyword is coded with a numerical ID

### playlists_final

created_at - timestamp of playlist creation
playlist_id - ID of the playlist
owner - ID of the user who created the playlist
title - encoding of the words in the title of the playlist (each word is coded with a unique ID)
duration - total duration of the playlist in seconds

### target_playlists

playlist_id - ID of the playlists that will receive recommendations

### target_tracks

track_id - ID of the tracks to be recommended

### sample_submission

playlist_id - ID of the playlist that is receiving recommendations
track_ids - IDs of the recommended tracks
