## song_recommender repo:
This Python repository will output a given number of recommended songs based on an inputted song by a given artist. 
If desired, it will also send you a text message (via Amazon SNS) with your recommended songs.

## Why this was created:
Like many other people, I have a select few songs I listen to on repeat until they get old. When this happens, typically Spotify recommends other similar artists. Sometimes, these new playlists have a couple new songs I enjoy, but most of the time, I forget about these recommended songs within a few minutes or skip the songs completely. I wanted to write code that ONLY gave me recommended songs based on a singular song that I know I love rather than an entire artist's collection of music. Hopefully, this repository will also benefit other avid music-lovers who want to expand their libraries to include songs that are extremely similar to the songs they love!

## Steps to use:
1. Clone to this repository to your local machine.
2. Install the `requirements.txt` file. This does not contain any 'funky' packages.
3. Open your machine's CLI and navigate to the location of this repository.
4. Run the following command within the CLI:
`python3 song_recommendation.py "Name of Song" "Name of Artist" number_of_songs_to_output phone_number`

    -**NOTE**: If you want to send a text, ensure `phone_number` is formatted as follows:
      `"+11234567890"` where +1 is your country code, the next three digits are the area code, and the remaining is the actual phone number. Ensure it is a string.

    -**NOTE**: `number_of_songs_to_output` must be an integer. The default value is 10 but it cannot exceed 15.
  
    -**NOTE**: `"Name of Song"` and `"Name of Artist"` MUST be string values. Ensure spelling is correct before submitting.
  
5. An example of running this within a CLI would be:
`python3 song_recommendation.py "God's Plan" "Drake" 5 "+11234567890"`
6. This will output an assortment of song names by particular artists based on your inputs. If you specified a phone number to send a text with these recommendations to, you will see an additional print statement within your CLI stating that the text was sent.
