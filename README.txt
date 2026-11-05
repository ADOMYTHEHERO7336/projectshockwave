FLASH ARCADE – how to use

1. Drop your .swf files into the /games folder.
2. (Optional) add preview images (png/jpg) to /thumbs.
3. Add one line per game in games.js.
4. Upload the whole folder to any static host (GitHub Pages, Netlify, Cloudflare Pages, etc.).

Testing locally: browsers block SWF loading from file://, so run a tiny server in this folder:
    python3 -m http.server 8000
then open http://localhost:8000

Notes
- Games run through Ruffle (a Flash emulator in WebAssembly). Most ActionScript 1/2 games work well;
  many ActionScript 3 games work, some don't.
- For reliability, download Ruffle's "selfhosted" build from ruffle.rs, put it in a /ruffle folder,
  and change the <script src> in index.html to "ruffle/ruffle.js".
