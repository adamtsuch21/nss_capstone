# nss_capstone

READ ME

Adam Tsuchiyama's Final NSS Capstone Project: Do Digital Audio Remaster's Change the "Character" of a Song?

 For my NSS final Capstone Project, I set out to answer the question of whether digital audio remasters changed the character of the original master. To answer this  question, I collected data from the Spotify Web API on 40 songs (20 masters and 20 remasters of the same songs). The 20 songs used were:
 
 Aretha Franklin - Respect
 Beastie Boys - Ch-Check It Out
 The Clash - London Calling
 Curtis Blow - Christmas Rappin'
 Eurythmics - Sweet Dreams (Are Made of This)
 Hootie & The Blowfish - Only Wanna Be With You
 Ice Cube - It Was A Good Day
 Interpol - PDA
 Maze - Before I Let Go
 Matchbox 20 - Unwell
 Michael Jackson - P.Y.T. (Pretty Young Thing)
 Nine Inch Nails - Head Like A Hole
 The Notorious B.I.G. - Big Poppa
 Oasis - Wonderwall
 Postal Service - Such Great Heights
 Queen - Another One Bites The Dust
 Frank Sinatra - Come Fly With Me
 The Rolling Stones - Wild Horses
 Talking Heads - Psycho Killer
 Yellow Magic Orchestra - Firecracker
 Led Zeppelin - Immigrant Song
 
Originally had these songs as well, but discovered through my analysis that the versions I had were not "remasters", but were in fact exactly the same as the original master:
 
 Alanis Morrissette - Hand In My Pocket (Acoustic)
 Santana - Smooth (feat. Rob Thomas)
 
I selected songs across a veriety of different genres (Hip Hop, R&B/Soul, Electronic/EDM, Hard Rock, Alt. Rock/Punk) and decades (1950s-2000s). For each song, I had 3 different datasets from the Spotify Web API:

1. Audio Features Data - High-level data for the song. Measures loudness, energy, etc. across the song as a whole.
2. Audio Analysis Data - Low-level data for the song. Measures loudness, timbre, pitch, etc. during different moments in time.
3. Artist Data - Has the genre breakdown for the artist of the song. Used to merge with the other two datasets.

I cleaned and analyzed the data using Python, and visualized the data using Tableau.

How I Collected the Data (for Audio Features and Audio Analysis):

1. Put the songs (masters and remasters) used for this project into a Spotify playlist.
2. Create an application that connects and authenticates with the Spotify Web API through Terminal. An explanation of how to set this up can be found at this GitHub repository: https://github.com/markkohdev/spotify-api-starter
3. Within the application, connect to your Spotify account and to the Spotify playlist containing the songs.
4. For Audio Features: Select all the songs, and then select Audio Features.
5. Copy the data for each song, paste into a .txt file, format as a Python dictionary, and save.
6. For Audio Analysis: Select 1st song (dataset is too large to select all at once). Select Audio Analysis.
7. Copy the data, paste into a .txt file, and save.
8. Repeat steps 6 and 7 for each song.

How I Collected the Data (for Artist Data):

1. Go to the Spotify webpage for the artist of the 1st song. Copy everything in the url after "artist/".
2. Go to the Spotify Web API artist data page (https://developer.spotify.com/documentation/web-api/reference/artists/get-artist/) and click "Try It".
3. Paste what you just copied into the "id" field and click "Try It".
4. Copy the "genres" and "id" data that appears on the right side and paste into a .txt file.
5. Format the id and genre as a Python dictionary.
6. Repeat steps 1-5 for each song, and save the .txt file.

Python notebooks for my data cleaning and analysis can be found within the "notebooks" folder of this repository.

My Tableau visualizations can be found at this link: https://public.tableau.com/profile/adam.tsuchiyama#!/vizhome/nss_capstone/capstone_presentation
