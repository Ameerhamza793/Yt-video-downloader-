## Guidence BY AH
unzip -l free-video-downloader
## Now run commands 1 by 1
cd ~/Yt-video-downloader-/free-video-downloader

source .venv/bin/activate

## Step 2 Check the installed versions

python -c "import fastapi, starlette, jinja2; print('FastAPI:', fastapi.__version__); print('Starlette:', starlette.__version__); print('Jinja2:', jinja2.__version__)"

## Step 3 — Fix the template call

return templates.TemplateResponse("index.html", {"request": request})

## Step 4 Replace that line with the current request-first form:

return templates.TemplateResponse(request=request, name="index.html")

## step 5 You can make this replacement automatically with:

python -c "from pathlib import Path; p=Path('app.py'); s=p.read_text(); old='return templates.TemplateResponse(\"index.html\", {\"request\": request})'; new='return templates.TemplateResponse(request=request, name=\"index.html\")'; assert old in s, 'Original line not found'; p.write_text(s.replace(old,new,1)); print('Template call updated')"

## step 6 Restart the app
Stop any running server with CTRL + C, then run:

python app.py


Open http://127.0.0.1:8080 in your browser.
