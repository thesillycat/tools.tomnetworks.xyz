## 🛠️ tools.tomsystems.xyz

All requests are made via simple `GET` parameters. Ensure your query strings are URL-encoded.

### 🔍 Search Metadata
Retrieve Spotify metadata for a specific song.

**Request:**
`GET https://tools.tomnetworks.xyz/api/search?title={song-title}&artist={song-artist}`

### 🎤 Get Lyrics
Fetch synchronized or plain-text lyrics with automatic fallback.

**Request:**
`GET https://tools.tomnetworks.xyz/api/lyrics?title={song-title}&artist={song-artist}`

---

## 💻 Example Integration (JavaScript)

```javascript
const getSongData = async (title, artist) => {
    const response = await fetch(`https://tools.tomnetworks.xyz/api/search?title=${encodeURIComponent(title)}&artist=${encodeURIComponent(artist)}`);
    const data = await response.json();
    console.log(data);
};
