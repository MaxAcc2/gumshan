# gumshan.com

Static site. No build step. Upload this folder as-is to any static host.

Swap the trailer: edit the `<source src="...">` inside the `<video>` in index.html. The player is the browser's native HTML5 player; any public MP4 (H.264 video, AAC audio) works. For S3, the object must be publicly readable and served with Content-Type video/mp4.

Swap the hero: replace assets/hero.jpg and assets/hero.webp (2000px wide, 2.39:1). Regenerate assets/og.jpg (1200x630) from the same still.

Add laurels: uncomment the `.laurels` CSS block and the `<div class="laurels">` in the hero, drop SVG or PNG laurels in assets/.

Deploy (Cloudflare Pages, free): create a project, upload this folder (or connect a git repo), then add the custom domain gumshan.com in the Pages project. Cloudflare gives you the exact records to add at your registrar; typically a CNAME for www pointing to your pages.dev hostname and either a CNAME-flattened apex or nameserver change. Netlify and Vercel work the same way: drag the folder in, add the domain, follow their DNS instructions.
