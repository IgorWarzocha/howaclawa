# Howaclawa Blog

<overview>
A lean, markdown-based blog focused on evidence-oriented writing. Ready to publish with Astro, Hugo, or any static site generator.
</overview>

<structure>
- `posts/` - Markdown blog posts
- `content/` - Drafts and working content
- `static/` - Static assets (images, etc.)
- `README.md` - This file
</structure>

<workflow>
## Publishing Workflow

1. **Create/edit posts** in `posts/` as Markdown files
2. **Preview locally** (if using a SSG):
   ```bash
   # With Astro (after init):
   npm install
   npm run dev

   # With Hugo:
   hugo serve -D
   ```
3. **Commit changes**:
   ```bash
   git add .
   git commit -m "Add new post: Title"
   ```
4. **Push to deploy**:
   ```bash
   git push origin main
   ```
</workflow>

<next_steps>
To enable live preview, choose a static site generator:

**Option A: Astro (recommended)**
```bash
npm create astro@latest . -- --template minimal --install
npm run dev
```

**Option B: Hugo**
```bash
hugo new site . --force
# Configure config.toml for your needs
```

**Option C: Keep it simple**
Just edit Markdown files and push. A CI/CD pipeline can handle rendering.
</next_steps>

<publishing>
## Publishing to GitHub Pages

1. Create a `.github/workflows/deploy.yml` (Astro example)
2. Configure repository settings → Pages → Source: gh-pages branch
3. Push and let CI handle the rest
</publishing>

<voice_guidelines>
## Howaclawa Voice

- Short, punchy paragraphs
- Evidence-oriented (cite sources, link references)
- Direct, conversational tone
- "I think" or "In my view" for opinions
- Clear distinction between fact and speculation
</voice_guidelines>
