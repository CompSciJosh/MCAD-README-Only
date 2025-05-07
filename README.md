# 🌓 MCAD - Multi-scale Crater Analysis and Detection

**MCAD** is a command-line tool for detecting lunar craters in satellite imagery using a custom-trained YOLOv8 model. 
It supports single-image, full directory and recursive batch directory processing. MCAD also provides an interactive shell
for repeated use. Built for lunar research and detection tasks, MCAD simplifies AI-based crater detection into a 
user-friendly CLI.

---

## 📁 Project Structure
```bash
jams/
├── app/
│   ├── backend/
│   │   └── system/
│   │       ├── best.pt
│   │       └── YOLOv8MCAD.py
│   └── frontend/
│       ├── ascii_image.py
│       ├── cli.py
│       ├── mcad_nasa.png
│       ├── mcad_nasa_colored.txt
│       ├── nasa_logo.png
│       └── nasa_logo_colored.txt
├── requirements.txt
└── README.md
```

---

## ⚙️ Box.com Installation

### 1. Download the project
- Download the zipped MCAD project folder
- Extract the contents to a location of your choice (e.g., `~/PycharmProjects/jams`)

### 2. Navigate to the project directory
```bash
cd ~/PycharmProjects/jams
```

### 3. Create and activate the virtual environment
```bash
python3 -m venv .venv
````
```bash
source .venv/bin/activate
```

### 4. Install dependencies
```bash
pip install -r requirements.txt
```

---
## Activate virtual environment if needed, example:
```bash
source ~/PycharmProjects/jams/app/.venv/bin/activate
```

## 🚀 Usage in main CLI
### ➤ Run the main CLI
```bash
python cli.py
```

### ➤ Detect a single image
```bash
python cli.py detect /path/to/image.png --output custom_folder_name
```

### ➤ Batch detect with recursive mode
```bash
python cli.py batch_detect /path/to/folder/ --recursive --output custom_folder_name
```
## 🚀 Usage in interactive shell
### ➤ Run the interactive shell
```bash
python cli.py shell
```

### ➤ Detect a single image
```bash
detect /path/to/image.png --output custom_folder_name
```

### ➤ Batch detect with recursive mode
```bash
batch_detect /path/to/folder/ --recursive --output custom_folder_name
```

> By default, detection results (annotated images and YOLO `.txt` files) are 
> saved to a folder named `Yolo Results` unless `--output` is specified in which you 
> can customize the output folder name.

---

## 🧪 Commands and Flags

| Command        | Description                                  |
|----------------|----------------------------------------------|
| `detect`       | Detect craters in a single image or folder   |
| `batch_detect` | Detect craters recursively in subdirectories |
| `shell`        | Launch interactive CLI shell                 |
| `exit`, `quit` | Exit the CLI shell                           |

**Available Flags:**
- `--output`: Set output folder (default: `Yolo Results`)
- `--model`: Use custom YOLO model (default: `best.pt`)
- `--recursive`: Enable recursive search (for `batch_detect` only)

> By default, the crater detection model is set to `best.pt` but can be customized by including the flag `--model` followed by the crater detection model name.
> Such as `detect /path/to/folder/ --model newModel.pt` or omit the `--model` flag to use the default crater detection model.

---

## 🧠 Crater Detection Model

MCAD uses a custom YOLOv8 model (`best.pt`) trained to detect craters across various lighting conditions and scales in lunar surface images. 
This file is stored at:

```
jams/app/backend/system/best.pt
```

---

## 📸 Screenshots

![Crater Detection 000/image3](_Users_joshuajackson_Downloads_mcad_moon_data_000_image_3_visualized.jpg)

![Crater Detection 000/image4](_Users_joshuajackson_Downloads_mcad_moon_data_000_image_4_visualized.jpg)

![Crater Detection 000/image5](_Users_joshuajackson_Downloads_mcad_moon_data_000_image_5_visualized.jpg)

![Crater Detection 000/image6](_Users_joshuajackson_Downloads_mcad_moon_data_000_image_6_visualized.jpg)

---

## 📜 License

This project is part of a senior design collaboration with NASA and may be subject to intellectual property or licensing policies from NASA or Prairie View A&M University.

Please contact the project lead or university representative before using or redistributing this code.

---
## 👤 Documentation Author

**Joshua Jackson**

### 💻 Project By

**Team JAMS**  
*Joshua Jackson, Anthony Pham, Marc Mata, Sukhraj Singh*  
Senior Design Project 2024 - 2025 · Prairie View A&M University



