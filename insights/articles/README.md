# How to Add New Articles to Insights

Articles are displayed as beautiful HTML pages (not PDFs). Just write your content in simple text format!

## Step 1: Create Article Folder

Create a new folder inside `insights/articles/` with a unique name:

```
insights/articles/your-article-name/
```

## Step 2: Add Your Files

Inside your article folder, add exactly 2 files:

1. **content.txt** - Your article content (simple text with basic formatting)
2. **image.jpg** - Article thumbnail image (recommended 800x600px)

```
insights/articles/your-article-name/
├── content.txt
└── image.jpg
```

## Step 3: Write Your Article Content

Open `content.txt` and write your article using this simple format:

```
Your Article Title Here

Author: Your Name
Date: January 20, 2025

## Introduction

Your introduction text here. Write normally - paragraphs will be automatically formatted.

You can use **bold text** by wrapping it in double asterisks.

## Main Section

### Subsection Title

More content here.

- Bullet point 1
- Bullet point 2
- Bullet point 3

1. Numbered item
2. Another item
3. Final item

**Important Note**: You can make subsections bold like this.

---

Use three dashes for a horizontal line separator.
```

### Formatting Guide:

- `## Title` - Creates a main section heading (large, purple underline)
- `### Subtitle` - Creates a subsection heading (medium, purple)
- `**Bold Text**` or standalone `**Title**` - Makes text bold
- `*italic*` - Makes text italic
- `- item` - Creates bullet points
- `1. item` - Creates numbered lists
- `---` - Creates horizontal separator line
- Empty line - Creates paragraph break

## Step 4: Update articles.json

Open `insights/articles/articles.json` and add your article:

```json
[
  {
    "folder": "your-article-name",
    "title": "Your Article Title",
    "author": "Your Name",
    "date": "2025-01-20",
    "category": "Technical",
    "description": "Brief description shown on the card.",
    "image": "image.jpg",
    "pdf": "content.txt"
  }
]
```

### Field Descriptions:

- **folder**: Folder name (must match exactly, use hyphens not spaces)
- **title**: Article title (shown on card and article page)
- **author**: Author's name
- **date**: YYYY-MM-DD format
- **category**: Technical, Research, Tutorial, Case Study, etc.
- **description**: Short summary for the article card (1-2 sentences)
- **image**: Image filename (usually image.jpg)
- **pdf**: Keep as "content.txt" (legacy field name)

## Step 5: Done!

Refresh insights - your article appears with a "Read Article" button that opens a beautiful dedicated page!

## Example Article

See `insights/articles/article1/content.txt` for a complete example with all formatting options.

## Tips

- **Keep it simple**: Just write naturally with basic formatting
- **Image size**: 800x600px works great for thumbnails
- **Content length**: No limits - write as much as you need!
- **Multiple articles**: Add comma between entries in articles.json
- **Order**: Articles appear in the order listed (put newest first)

That's it! No PDF creation needed - just write in a text file! 🚀
