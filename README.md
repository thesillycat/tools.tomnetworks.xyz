## 🛠️ api.tomsystems.org

All requests are made via simple `GET` parameters. Ensure your query strings are URL-encoded.

### 🔍 Search Metadata
Retrieve Spotify metadata for a specific song.

**Request:**
`GET https://api.tomsystems.org/api/search?title={song-title}&artist={song-artist}`

### 🎤 Get Lyrics
Fetch synchronized or plain-text lyrics with automatic fallback.

**Request:**
`GET https://api.tomsystems.org/api/lyrics?title={song-title}&artist={song-artist}`

---

## 💻 Example Integration (JavaScript)

```javascript
const getSongData = async (title, artist) => {
    const response = await fetch(`https://api.tomsystems.org/api/search?title=${encodeURIComponent(title)}&artist=${encodeURIComponent(artist)}`);
    const data = await response.json();
    console.log(data);
};
