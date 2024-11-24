<div align="center">

# AI Video Caption & Generation System


[![Gradio](https://img.shields.io/badge/Gradio-FF6B6B?style=for-the-badge&logo=gradio&logoColor=white)](https://gradio.app/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org/)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org/)

An intelligent system that extracts frames from videos, generates captions using BLIP, and creates new AI-generated videos using diffusion models.

</div>

## 📑 Table of Contents
- [Features](#-features)
- [Installation](#-installation)
- [Usage](#-usage)
- [Technical Details](#-technical-details)
- [Project Structure](#-project-structure)
- [Dependencies](#-dependencies)
- [Troubleshooting](#-troubleshooting)

## ⚡ Features

- Frame extraction from videos at customizable frame rates
- Advanced video captioning using BLIP model
- AI video generation using AnimateDiff diffusion model
- User-friendly Gradio interface
- Real-time processing and status updates
- Support for multiple video formats

## 🔧 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-video-generator.git
cd ai-video-generator

# Install required packages
pip install gradio
pip install transformers
pip install opencv-python-headless
pip install diffusers
pip install torch
```

## 🚀 Usage

```python
# Start the Gradio interface
python app.py
```

## 💻 Technical Details

### Video Processing Pipeline
```python
# Extract frames
frames = extract_frames(video_path, frame_rate=1)

# Generate captions
captions = generate_captions(frames)

# Create AI-generated video
generate_video_from_captions('captions.txt', 'output_video.mp4')
```

## 📁 Project Structure

```
ai-video-generator/
├── app.py              # Main Gradio application
├── modules/
│   ├── extractor.py    # Frame extraction utilities
│   ├── caption.py      # BLIP captioning system
│   └── generator.py    # Video generation code
├── models/
│   └── weights/        # Pre-trained model weights
├── requirements.txt
└── README.md
```

## 📦 Dependencies

- Python 3.8+
- gradio
- transformers==4.30.0+
- opencv-python-headless
- diffusers
- torch>=2.0.0
- Pillow
- numpy

## Model Details

| Component | Model | Source |
|-----------|-------|---------|
| Captioning | BLIP | `Salesforce/blip-image-captioning-base` |
| Video Generation | Latte-1 | `maxin-cn/Latte-1` |

## 🛠️ Configuration

```python
# Frame extraction settings
FRAME_RATE = 1  # Frames per second
FRAME_SIZE = (1920, 1080)
FPS = 24

# Video output settings
VIDEO_FORMAT = 'mp4v'
```

## ⚠️ Troubleshooting

Common Issues:
```
1. CUDA Out of Memory
   Solution: Reduce batch size or frame rate

2. Video Loading Error
   Solution: Ensure video format is supported (mp4, avi)

3. Model Loading Issues
   Solution: Check internet connection and HuggingFace login
```

## 🔄 Processing Pipeline

1. Video Input → Frame Extraction
2. Frames → BLIP Captioning
3. Captions → Latte-1 Generation
4. Generated Frames → Final Video

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
