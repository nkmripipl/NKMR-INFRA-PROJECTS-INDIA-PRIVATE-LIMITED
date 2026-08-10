# NKMR INFRA - Python Web Server Setup

## Quick Start

### Option 1: Run Locally (Development)

```bash
# Navigate to the project directory
cd NKMR-INFRA-PROJECTS-INDIA-PRIVATE-LIMITED

# Run the web server
python3 app.py
```

Then open your browser and visit: **http://localhost:8000**

### Option 2: Using Python's Built-in Server (Alternative)

```bash
python3 -m http.server 8000
```

## Files Overview

- **app.py** - Main Python web server script
- **index.html** - Homepage with styling and content
- **requirements.txt** - Python dependencies (currently none required for basic server)

## Features

✅ Simple HTTP server (no frameworks needed)
✅ Serves HTML/CSS/JavaScript files
✅ CORS headers enabled for API requests
✅ Automatic index.html routing
✅ Easy to extend

## Deployment

### For Production (Using Gunicorn)

1. Install Gunicorn:
```bash
pip install gunicorn
```

2. Run with Gunicorn:
```bash
gunicorn -w 4 -b 0.0.0.0:8000 app:run_server
```

### Environment Variables

You can set the port via environment variable:
```bash
export PORT=8080
python3 app.py
```

## Troubleshooting

**Port already in use?**
```bash
# Use a different port
python3 -m http.server 8001
```

**Permission denied?**
```bash
# Make script executable
chmod +x app.py
```

**Module not found?**
```bash
# Ensure you're using Python 3
python3 --version
```

## Next Steps

- Add CSS styling to `index.html`
- Create additional `.html` pages in the project root
- Add JavaScript for interactivity
- Consider migrating to Flask or Django for more complex needs

---

**Server Ready!** 🚀 Your website is set up and ready to run.
