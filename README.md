# File Zipper

A lightweight, header-only C++ ZIP/UNZIP wrapper plus a polished browser demo for creating ZIP archives locally.

## What was improved

- Added a responsive Vercel-ready web interface under `web/`.
- Added drag-and-drop and multi-file selection.
- Added Fast, Balanced, and Maximum compression controls.
- Added client-side ZIP creation with no application server upload.
- Added file removal, clear-all, size summaries, status feedback, and light/dark mode.
- Added security-oriented response headers through `vercel.json`.
- Preserved the original C++ header-only library and example.

## Run the web demo locally

Because the demo is a static site, serve the `web` directory with any static HTTP server:

```bash
cd web
python -m http.server 8000
```

Then open `http://localhost:8000`.

## C++ library

The original library remains header-only and is based on MiniZip. It provides `zipper::Zip`, `zipper::UnZip`, and enumeration helpers. See `example/example.cpp` for usage.

## Deployment

The repository includes `vercel.json` and the web entrypoint lives in `web/`. In Vercel, set the project root to `web` (or deploy the repository as a static project using `web` as the output directory).

## Privacy

The demo performs file reading and ZIP generation in the browser. Files are not intentionally sent to an application backend.

## License

MIT License (© 2021 Yuji Hirose).
