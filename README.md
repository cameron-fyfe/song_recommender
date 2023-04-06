## song_recommender repository:
This Python repository will output a given number of recommended songs based on an inputted song by a given artist. 
If desired, it will also send you a text message (via Amazon SNS) with your recommended songs.

## Why this was created:
Like many other people, I have a select few songs I listen to on repeat until they get old. When this happens, Spotify typically recommends songs (within a playlist) from similar-sounding artists. Sometimes, these new playlists have a couple new songs I enjoy, but most of the time, I forget about these recommended songs within a few minutes or skip the songs completely because I do not like them. Also, these recommended playlists are created based on your larger listening history rather than one particular song. Instead of finding similar-sounding artists or creaing recommendations based on the larger listening history, I was more interested in finding similar-sounding songs *regardless* of the artist that created them, so I wrote code that ONLY gave me recommended songs based on a particular song that I know I love rather than song recommendations based numerous songs I have listened to. Sometimes, you just want similar songs to match whatever vibe you are looking for. Hopefully this repository will also benefit other avid music-lovers who want to expand their libraries to include songs that are extremely similar to the songs they love!

## Steps to use:
1. Clone to this repository to your local machine.
2. Open your machine's CLI and navigate to the location of this repository.
3. Install the `requirements.txt` file. By using the following command: `pip install requirements.txt` 
4. Run the following command within the CLI:
`python3 song_recommendation.py "Name of Song" "Name of Artist" number_of_songs_to_output phone_number`

    -**NOTE**: If you want to send a text, ensure `phone_number` is formatted as follows:
      `"+11234567890"` where +1 is your country code, the next three digits are the area code, and the remaining is the actual phone number. Ensure it is a string. However it is an **optional argument** so if you just want to populate the output in the CLI, then you can skip this argument.

    -**NOTE**: `number_of_songs_to_output` must be an integer. The default value is 10 but it cannot exceed 15.
  
    -**NOTE**: `"Name of Song"` and `"Name of Artist"` MUST be string values. Ensure spelling is correct before submitting.
  
5. An example of running this within a CLI would be:
`python3 song_recommendation.py "God's Plan" "Drake" 5 "+11234567890"`
6. This will output an assortment of song names by particular artists based on your inputs. If you specified a phone number to send a text with these recommendations to, you will see an additional print statement within your CLI stating that the text was sent.



## Future iterations:
- Instead of using the recommendation feature from the `spotipy` library, create my own recommendation model.
- Incorporate the ability to input a list of songs rather than just one
- And more as more ideas pop into my head :)
