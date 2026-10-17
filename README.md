# Neuro_Forge
## 🎬 Demo

![Project Demo](demo.gif)

## 📸 Screenshots

### Screenshot 1
![Screenshot 1](Screenshot1.png)

### Screenshot 2
![Screenshot 2](Screenshot2.png)

### Screenshot 3
![Screenshot 3](Screenshot3.png)



C++ neural network
## 🚀 How to Run the App

NeuroForge's Streamlit app (`app.py`) only works when the **entire project folder is open in VS Code** and launched from that folder's terminal. It will not run on its own from a hosted link, because it relies on the C++ executables and data files that sit next to it.

### Requirements

- [Python 3.9+](https://www.python.org/downloads/)
- [Visual Studio Code](https://code.visualstudio.com/)
- Windows (the included `.exe` files are Windows builds; on macOS/Linux, build from source with CMake, see below)

### Step 1: Download the project

Clone the repo:

```bash
git clone https://github.com/amnafatimaa6-ops/Neuro_Forge.git
```

or click **Code → Download ZIP** on GitHub and extract it.

### Step 2: Download the NASA Exoplanet data

The dataset is too large to store in this repository, so you need to download it yourself:

1. Go to the [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/) and download the exoplanet table as a CSV.
2. Move the downloaded file into the project's **`data/`** folder, so it sits at `Neuro_Forge/data/<your-file>.csv`.
3. Make sure the filename matches what the code expects (check `app.py` / `src/` for the expected file name, and rename your download if needed).

### Step 3: Open the folder in VS Code

1. Open VS Code.
2. Go to **File → Open Folder…** and select the **`Neuro_Forge`** folder itself (the one containing `app.py`, not its parent folder).
3. Open a terminal inside VS Code: **Terminal → New Terminal**. It should start inside `Neuro_Forge`.

### Step 4: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 5: Run the app

```bash
python -m streamlit run app.py
```

Your browser will open automatically at `http://localhost:8501`. If it doesn't, paste that address into your browser.

### Troubleshooting

| Problem | Fix |
|---|---|
| `streamlit` is not recognized | Always use `python -m streamlit run app.py` (not just `streamlit run`). |
| File or data not found | Make sure VS Code has the `Neuro_Forge` folder open directly, and that the NASA CSV is inside `data/`. |
| `.exe` won't start / not on Windows | Rebuild the C++ code with CMake: `cmake -S . -B build` then `cmake --build build --config Release`. |
| Port already in use | Run with another port: `python -m streamlit run app.py --server.port 8502` |

To stop the app, press `Ctrl + C` in the terminal.
