<img width="150" height="150" align="right" style="float: right; margin: 0 10px 0 0;" alt="music_disc" src="public/imgs/logo2.png">

# discord-player version of Music Disc

<a href="https://github.com/hmes98318/Music-Disc-discord-player/releases"><img alt="GitHub package.json version" src="https://img.shields.io/github/package-json/v/hmes98318/Music-Disc-discord-player?style=for-the-badge"></a> 
<a href="https://discord.js.org/"><img src="https://img.shields.io/badge/Discord.JS-v14-blue?style=for-the-badge&logo=DISCORD" /></a> 
<a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.JS->=18.x-brightgreen?style=for-the-badge&logo=Node.js"></a> 
<a href="https://github.com/hmes98318/Music-Disc/blob/main/LICENSE"><img alt="GitHub" src="https://img.shields.io/github/license/hmes98318/Music-Disc?style=for-the-badge&color=brightgreen"></a>  

A discord music bot, supports **YouTube**, **Spotify**, **SoundCloud** streams.  
Developed based on [**discord.js v14**](https://discord.js.org/#/), [**discord-player**](https://github.com/Androz2091/discord-player).  


If you need the version of [**Lavalink**](https://github.com/lavalink-devs/Lavalink), please refer to this [**branch**](https://github.com/hmes98318/Music-Disc).  

If you encounter any issues or would like to contribute to the community, please join our [Discord server](https://discord.gg/7rQEx7SPGr).  



## Deploying with node.js

### Clone the latest version of the repository
```
git clone -b v1.4.3 https://github.com/hmes98318/Music-Disc-discord-player.git
```
or [**click here**](https://github.com/hmes98318/Music-Disc-discord-player/releases) to download  


### Install the dependencies
install all the dependencies from [`package.json`](./package.json)  
```
npm install
```

### Configure environment
[`.env`](./.env) 
```env
TOKEN = "your_token"
NAME = "Music Disc"
PREFIX = "+"
PLAYING = "+help | music"
EMBEDS_COLOR = "#FFFFFF"
DEFAULT_VOLUME = 50
MAX_VOLUME = 100
AUTO_LEAVE = true
AUTO_LEAVE_COOLDOWN = 5000
DISPLAY_VOICE_STATE = true
PORT = 33333

TEXT_QUERY_TYPE = "youtubeSearch"
URL_QUERY_TYPE = "auto"
DP_FORCE_YTDL_MOD = "play-dl"
```

<details> 
  <summary>Detailed description</summary>

  **`AUTO_LEAVE`** : After the music finished, can choose whether let the bot leave voice channel automatically or not.  
  **`AUTO_LEAVE_COOLDOWN`** : Timer for auto disconnect(ms).  
  **`DISPLAY_VOICE_STATE`** : Show voice channel status updates.   
  </br>
  
  **`TEXT_QUERY_TYPE`** : The default search engine for text search.  
  The following are the available options for **TEXT_QUERY_TYPE**:
    <pre>
      autoSearch, youtubeSearch, spotifySearch, soundcloudSearch, appleMusicSearch
    </pre>

  **`URL_QUERY_TYPE`** : The default search engine for links.  
  The following are the available options for **URL_QUERY_TYPE**:
    <pre>
      auto, youtube, spotifySong soundcloud, appleMusicSong
    </pre>

  **`DP_FORCE_YTDL_MOD`** : Streaming extractor settings. The default streaming library used is **play-dl**.  
  If you want to use another library, you can install one of the following libraries and change the `DP_FORCE_YTDL_MOD` setting.  
    <pre>
      $ npm install ytdl-core
      $ npm install @distube/ytdl-core
    </pre>
</details>


## Running the script 
```
npm run start
```


## Deploying with Docker Compose  
**image link** : https://hub.docker.com/r/hmes98318/music-disc  
### put your Token into [`docker-compose.yml`](./docker-compose.yml)
```yml
version: '3.8'
services:
  music-disc:
    image: hmes98318/music-disc:1.4.3
    container_name: music-disc
    restart: always
    ports:
      - 33333:33333
    environment:
      TOKEN: "your_token"
      PREFIX: "+"
      PLAYING: "+help | music"
      EMBEDS_COLOR: "#FFFFFF"
      DEFAULT_VOLUME: 50
      MAX_VOLUME: 100
      AUTO_LEAVE: "true"
      AUTO_LEAVE_COOLDOWN: 5000
      DISPLAY_VOICE_STATE: "true"
      TEXT_QUERY_TYPE: "youtubeSearch"
      URL_QUERY_TYPE: "auto"
      DP_FORCE_YTDL_MOD: "play-dl"
```

### Start the container  
```
docker-compose up -d
```


## Deploying with Replit  
Watch it by clicking on the image down below  
[![Music-Disc-with-Replit](https://img.youtube.com/vi/WH5aSHIebcc/0.jpg)](https://youtu.be/WH5aSHIebcc)  


