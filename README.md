# Ying Yang Twins For All Seasons

## Project Description:

Ying Yang Twings For All Seasons provides you with four playlists generated by the Spotify API filtering the entire Ying Yang Twins library of non-stop hits by three qualities: danceability, energy, and valence. In the Spotify API these qualities are represented by a value from 0.0-1.0, so the seasonal playlists will be generated with the following parameters: Winter - 0.0-0.25, Fall - 0.25-0.5, Spring - 0.5-0.75, Summer - 0.75-1.0. I hope to sort the playlists in season-value order from low to high for Fall and Winter and high to low for Spring and Summer. I have no idea what the results will be (do the Ying Yang Twins even have a song in the 0.0-0.25 range?!?!), but I do know that no matter what it will provide at least one (1) chuckle to every viewer.

## Wireframe:

- https://docs.google.com/document/d/1dRWyjigrgYdyX_zYfLplsNtNjLfDrbbQl8FpaRJgGQ0/edit?usp=sharing

## MVP User Stories:
- as a User, I just want to listen to the Ying Yang Twins entire catalog sorted by associated season (Create Playlists with Spotify API)
- as a User, I just want to know what I'm looking at. (Home component with app description linking to each Playlist)
- as a User, I want to know what I'm listening to. (in Playlist Component, have song title)
- as a User, I want to be able to navigate through the Playlist and listen the way I want (volume and time controls, with skip and previous buttons/playlist display)

## Stretch:
- Playlist Component details - adding as much info about current song as possible onto the page (potentially using a second API - TheAudioDB)
- Save playlists to your Spotify account
- Curate playlists for potential accuracy (might have to save playlists to my own account and edit, then link to playlists on website.)
- Ying Yang Twins and Friends - be able to input artist or genre, playlist length, and season to generate playlist. 
- STYLE
- Spotify API's Playback feature might improve the audio control
- Use Spotify's Recommendations to extend playlist length

## API:

### Spotify (https://developer.spotify.com/documentation/web-api/):
- [Use GET](https://api.spotify.com/v1/search?q=artist:ying+yang+twins&type=track) to get all tracks by the Ying Yang Twins
- [Use GET](https://api.spotify.com/v1/audio-features) to obtain danceability, energy, and valence values for all tracks and filter songs into four arrays (also sort by popularity perhaps?)
- [Use POST](https://api.spotify.com/v1/users/{user_id}/playlists) to create Playlists
- [Use POST](https://api.spotify.com/v1/playlists/{playlist_id}/)tracks add tracks to playlists

## Component Heirarchy
- App
    - Home
        - About/Description
        - PlaylistDisplay
            - PlaylistFull (x4)
                - Playlist
                - SongInfo
        - Create Your Own (stretch)
