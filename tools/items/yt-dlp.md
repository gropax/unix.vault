```bash
# Télécharger la meilleure qualité vidéo+audio
yt-dlp <URL>

# Extraire audio seulement, convertir en mp3
yt-dlp -x --audio-format mp3 <URL>

# Télécharger les sous-titres anglais (texte) sans vidéo
yt-dlp --skip-download --write-subs --sub-lang en <URL>

# Télécharger une playlist complète, éviter les doublons
yt-dlp --download-archive archive.txt <PLAYLIST_URL>

# Télécharger un flux livestream HLS (avec MPEG-TS pour tolérer interruption)
yt-dlp --hls-use-mpegts <LIVE_URL>

# Forcer format : vidéo 720p max + format mp4
yt-dlp -f "best[height<=720][ext=mp4]" <URL>

# Limiter la vitesse de téléchargement
yt-dlp --limit-rate 500K <URL>

# Utiliser un proxy SOCKS5
yt-dlp --proxy socks5://127.0.0.1:9050 <URL>

# Embedding miniature + métadonnées + sous-titres
yt-dlp --embed-thumbnail --embed-metadata --write-subs --sub-lang en <URL>

```
