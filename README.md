# MangaBaka Stats Card

A dynamic SVG stats card for your MangaBaka library, deployable on Vercel and embeddable in AniList profiles.

## Deploy to Vercel

1. **Fork/clone this repo**
2. **Set environment variable** in Vercel:
   - `MANGABAKA_API_KEY` = your MangaBaka API key
3. **Deploy**

## Usage in AniList Bio

After deploying, your card will be available at:
```
https://your-project.vercel.app/api/card
```

Add this to your AniList bio:
```markdown
![MangaBaka Stats](https://your-project.vercel.app/api/card)
```

## Features

- Total library entries
- Chapters & volumes read
- Average rating
- Status distribution (Reading, Completed, Paused, Dropped, Plan to Read)
- Media type breakdown (Manga, Manhwa, Manhua, Novel)
- Top 5 genres & tags
- Auto-updates every 5 minutes

## API

| Endpoint | Description |
|----------|-------------|
| `/api/card` | Returns SVG image with your stats |

## Cache

The card is cached for 5 minutes (`max-age=300`) to avoid rate limiting.
