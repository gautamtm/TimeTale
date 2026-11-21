# TimeTale

Local photo-to-video tool (Canvas collage + Create video). Runs on your PC — nothing is uploaded.

## Project layout

```
.
├── Start_Web_UI.bat      # double-click: browser UI
├── Start_UI.bat          # double-click: desktop UI
├── requirements.txt
├── README.md
│
├── timetale/             # Python package (application code)
│   ├── __main__.py       # python -m timetale web|desktop
│   ├── paths.py          # project root + config/cache paths
│   ├── web_app.py        # browser server
│   ├── app.py            # desktop (Tk) UI
│   ├── photo_to_video.py # render engine
│   ├── ui_common.py      # shared settings / validation
│   └── vehicles.py
│
├── web_ui/               # front-end (HTML / JS)
├── config/               # settings JSON (ui_settings.json)
├── scripts/              # launch scripts (.bat)
├── cache/                # analysis cache
│
├── music/                # built-in tracks + library.json
├── sounds/               # shutter samples
├── vehicles/             # travel icons (+ optional .json metadata)
├── projects/             # saved trip project JSON
├── input_photos/         # default sample / input folder
└── output/               # generated videos
```

## Run

```bat
Start_Web_UI.bat
```

or:

```bat
pip install -r requirements.txt
set PYTHONPATH=%CD%
python -m timetale web
python -m timetale desktop
```

Browser UI: [http://127.0.0.1:8765](http://127.0.0.1:8765)

## Conventions

| Kind | Location |
|------|----------|
| Python modules | `timetale/` |
| App settings JSON | `config/` |
| Launch scripts | `scripts/` (+ root stubs for convenience) |
| Front-end | `web_ui/` |
| Media assets | `music/`, `sounds/`, `vehicles/` |
| User projects / output | `projects/`, `output/` |
