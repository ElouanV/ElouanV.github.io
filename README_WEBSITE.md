# Academic Homepage with JSON Data Management

This is a modern, organized academic homepage that uses JSON files for data management, making it easy to update content without editing HTML directly.

## 📁 Project Structure

```
├── index.html              # Homepage with news section
├── papers.html             # Publications page
├── conferences.html        # Conferences & presentations page
├── admin.html              # Content management interface
├── style.css               # All styles
├── data/                   # JSON data files
│   ├── news.json          # News items and updates
│   ├── papers.json        # Publications data
│   ├── conferences.json   # Conference presentations
│   └── profile.json       # Personal information
└── js/                     # JavaScript modules
    ├── main.js            # Core functionality
    ├── news.js            # News section handler
    ├── papers.js          # Papers page functionality
    └── conferences.js     # Conferences page functionality
```

## 🚀 Features

### Dynamic Content Loading
- **JSON-based data management** - All content is stored in structured JSON files
- **JavaScript rendering** - Content is dynamically loaded and displayed
- **No HTML editing required** - Update content by editing JSON files

### Interactive Features
- **Search functionality** on papers page
- **Filter options** for papers (by status) and conferences (by year/type)
- **News filtering** by category (publications, presentations, awards, etc.)
- **Responsive design** - Works on desktop and mobile

### Easy Content Management
- **Admin interface** (`admin.html`) for creating new news items
- **Structured data format** - Consistent JSON schema
- **Copy-paste workflow** - Generate JSON and add to data files

## 📝 How to Update Content

### Method 1: Using the Admin Interface
1. Open `admin.html` in your browser
2. Fill out the form to create new news items
3. Copy the generated JSON
4. Add it to the appropriate data file

### Method 2: Direct JSON Editing

#### Adding News Items
Edit `data/news.json` and add new items to the "news" array:

```json
{
  "id": 6,
  "date": "Sep 2025",
  "title": "Your News Title",
  "content": "Description of the news item.",
  "type": "publication",
  "links": [
    {
      "text": "Paper",
      "url": "https://example.com/paper.pdf"
    }
  ]
}
```

#### Adding Papers
Edit `data/papers.json` and add to the appropriate section (journal, conference, preprint, thesis):

```json
{
  "id": 9,
  "title": "Your Paper Title",
  "authors": ["Elouan V.", "Co-Author"],
  "venue": "Conference/Journal Name",
  "year": 2025,
  "abstract": "Brief description of the paper.",
  "links": [
    {
      "text": "PDF",
      "url": "https://example.com/paper.pdf"
    }
  ],
  "status": "published"
}
```

#### Adding Conferences
Edit `data/conferences.json` and add to upcoming/past sections:

```json
{
  "id": 7,
  "name": "Conference Name",
  "location": "City, Country",
  "date": {
    "month": "Oct",
    "year": "2025"
  },
  "presentation_type": "Oral Presentation",
  "title": "Your Presentation Title",
  "description": "Brief description.",
  "links": [
    {
      "text": "Slides",
      "url": "https://example.com/slides.pdf"
    }
  ]
}
```

## 🎨 Customization

### Profile Information
Edit `data/profile.json` to update:
- Contact information
- Bio and research interests
- Social media links

### Styling
- Modify `style.css` to change colors, fonts, or layout
- All CSS is in one file for easy customization

### Adding New Features
- Create new JavaScript modules in the `js/` folder
- Add new data structures to existing JSON files
- Extend the admin interface for new content types

## 🌐 Deployment to GitHub Pages

1. **Commit and push** all files to your `ElouanV.github.io` repository
2. **Enable GitHub Pages** in repository settings:
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: main
3. Your site will be available at `https://ElouanV.github.io`

## 🔧 Development

### Local Development
1. Serve the files using a local web server (required for JSON loading):
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```
2. Open `http://localhost:8000` in your browser

### File Organization Benefits
- **Separation of concerns** - Content, presentation, and behavior are separated
- **Easy maintenance** - Update content without touching HTML/CSS
- **Version control friendly** - JSON changes are easy to track
- **Scalable** - Easy to add new content types or features
- **Collaborative** - Multiple people can update content easily

## 📊 Content Types

### News Types
- `publication` - Paper acceptances, publications
- `presentation` - Conference talks, posters
- `collaboration` - New research collaborations
- `award` - Awards and recognition
- `service` - Conference service, reviewing

### Paper Statuses
- `published` - Published papers
- `under-review` - Papers under peer review
- `preprint` - Preprints and working papers
- `in-progress` - Work in progress

### Presentation Types
- `Oral Presentation` - Conference talks
- `Poster Presentation` - Poster sessions
- `Workshop Presentation` - Workshop talks
- `Invited Talk` - Invited seminars

## 🤝 Contributing

To add new features or fix issues:
1. Fork the repository
2. Create a new branch for your changes
3. Test your changes locally
4. Submit a pull request

## 📄 License

This project is open source and available under the MIT License.
