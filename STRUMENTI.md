# Strumenti

| Strumento | A cosa serve | Installazione |
|---|---|---|
| **Remotion** | Comporre video e animazioni con codice React | `npx create-video@latest` |
| **HyperFrames** (HeyGen) | Alternativa a Remotion: video scritti in HTML e renderizzati in MP4 | `npm i hyperframes` |
| **FFmpeg** | Tagli, conversioni, export | `apt-get install -y ffmpeg` |
| **Whisper** (faster-whisper) | Trascrizione con tempi, da cui creare i sottotitoli (.srt) | `pip install faster-whisper` |
| **yt-dlp** | Recupero dei riferimenti accessibili | `pip install yt-dlp` |

## Note
- **Remotion / HyperFrames:** se ne usa uno per progetto, non entrambi. Remotion è gratuito per privati e aziende piccole; le aziende più grandi hanno bisogno di una licenza.
- **Whisper:** al primo uso scarica il modello da huggingface.co (serve accesso a quel sito).
- **yt-dlp:** un link pubblico non garantisce che il video sia scaricabile. Scarica solo contenuti che hai il diritto di usare. I riferimenti scaricati vanno in `riferimenti/`.

## Flusso tipico
1. Video originale in `girato/`
2. Whisper → trascrizione con tempi → sottotitoli `.srt`
3. FFmpeg → tagli di pause ed errori (regole in `STILE.md`)
4. Remotion o HyperFrames → grafiche, testi animati, sottotitoli stilizzati
5. FFmpeg → export finale in `export/`
