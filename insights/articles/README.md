# How to Add New Articles to Insights

Articles are displayed as beautiful HTML pages with markdown support. Each article lives in its own folder with markdown content, images, and optional PDF files.

## Step 1: Create Article Folder

Create a new folder inside `insights/articles/` with a unique name (use hyphens, not spaces):

```bash
insights/articles/your-article-name/
```

## Step 2: Add Your Files

Inside your article folder, add these files:

1. **article.md** - Your article content in markdown format (required)
2. **image.jpg** - Article thumbnail image for the card (required, recommended 800x600px)
3. **article.pdf** - PDF version of the article (optional)

```
insights/articles/your-article-name/
├── article.md          # Article content (markdown)
├── image.jpg           # Thumbnail image
└── article.pdf         # Optional PDF version
```

## Step 3: Write Your Article Content

Create `article.md` and write your article using markdown format:

```markdown
Your Article Title Here

Author: Your Name
Date: January 20, 2025

## Introduction

Your introduction text here. Write normally - paragraphs will be automatically formatted.

You can use **bold text** and *italic text*.

## Main Section

### Subsection Title

More content here.

- Bullet point 1
- Bullet point 2
- Bullet point 3

1. Numbered item
2. Another item
3. Final item

**Important Note**: You can emphasize important points like this.

---

Use three dashes for a horizontal separator line.
```

### Markdown Formatting Guide:

- `## Title` - Creates a main section heading (large, with purple underline)
- `### Subtitle` - Creates a subsection heading (medium, purple)
- `**Bold Text**` - Makes text bold
- `*italic*` - Makes text italic
- `- item` - Creates bullet points (unordered list)
- `1. item` - Creates numbered lists (ordered list)
- `---` - Creates horizontal separator line
- Empty line - Creates paragraph break

## Step 4: Update articles.js

Open `insights/articles/articles.js` and add your article metadata to the array:

```javascript
window.articlesData = [
  {
    "folder": "your-article-name",
    "title": "Your Article Title",
    "author": "Your Name",
    "date": "2025-01-20",
    "category": "Technical",
    "description": "Brief description shown on the article card (1-2 sentences).",
    "image": "image.jpg",
    "pdf": "article.pdf"
  }
];
```

### Field Descriptions:

- **folder**: Folder name (must match your folder exactly, use hyphens not spaces)
- **title**: Article title (displayed on card and article page)
- **author**: Author's full name
- **date**: Date in YYYY-MM-DD format
- **category**: Category tag (e.g., "Technical", "Research", "Tutorial", "Case Study")
- **description**: Short summary for the article card (1-2 sentences, shown on insights page)
- **image**: Image filename (e.g., "image.jpg")
- **pdf**: PDF filename if you have one (e.g., "article.pdf"), or omit if none

### Multiple Articles

When adding multiple articles, separate them with commas:

```javascript
window.articlesData = [
  {
    "folder": "article1",
    "title": "First Article",
    ...
  },
  {
    "folder": "article2",
    "title": "Second Article",
    ...
  }
];
```

**Tip**: Put newest articles first - they appear in the order listed.

## Step 5: Done!

Refresh the insights page and your article will appear automatically! Click "Read Article" to view it on its own dedicated page.

## Example Article

See `insights/articles/article1/` for a complete example:
- `article.md` - Full article with all formatting options
- `image.jpg` - Example thumbnail image
- `article.pdf` - Example PDF (optional)

## Tips

- **Markdown is powerful**: Use standard markdown syntax for rich formatting
- **Image size**: 800x600px or larger works great for thumbnails
- **Content length**: No limits - write as much as you need
- **File naming**: Use hyphens in folder names (e.g., `rf-interference-analysis`)
- **Order matters**: Articles display in the order listed in `articles.js` (newest first recommended)
- **Testing**: Always check your article renders correctly on the live page

## Architecture

The article system works as follows:
1. **articles.js** - Contains metadata for all articles
2. **insights.html** - Lists all articles as cards using metadata
3. **article-template.html** - Dynamically loads and renders individual articles
4. **article.md** - Markdown content fetched and parsed at runtime

That's it! Write in markdown, add metadata, and you're done! 🚀
