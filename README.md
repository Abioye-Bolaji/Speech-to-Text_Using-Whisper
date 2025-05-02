# 🗣️ **Speech To Text**


### 🛠 [Using Whisper by OpenAI](https://github.com/openai/whisper)
# Transcribe & Analyze Stakeholder Feedback with Whisper

This repository contains a project that leverages OpenAI's Whisper for speech-to-text transcription, with a focus on analyzing stakeholder feedback in the built environment. The primary goal is to automate the transcription of long audio files, break them into manageable segments, and set the stage for further analysis such as sentiment analysis or thematic categorization.

## Overview

In many built environment projects, stakeholder feedback is critical yet often recorded in lengthy audio formats. This project demonstrates:
- **Automated Transcription:** Utilizing Whisper to convert speech to text.
- **Segmented Processing:** Splitting long audio files into 10-minute segments to optimize performance and manage memory constraints.
- **Foundation for Analysis:** Providing a clean transcription pipeline that can be integrated with further analysis tools for insights into stakeholder feedback.

## Features

- **Google Colab Integration:** Code is tailored for easy execution on Google Colab with drive mounting and dependency management.
- **Dependency Control:** Specific versions for libraries (e.g., `numpy`, `torch`) are used to ensure reproducibility.
- **Robust Setup:** The notebook handles installation of critical packages like ffmpeg and Whisper.
- **Modularity & Clarity:** Code is structured into logical sections with markdown documentation to guide users through the process.

**Note:** Some library versions used in the Whisper model are currently out of date. Check the main file for further clarification

## Installation

To replicate this project, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Abioye-Bolaji/Speech-to-Text_Using-Whisper
   cd Speech-to-Text_Using-Whisper
   ```

2. **Set Up Your Environment:**
   - If using Google Colab, upload the notebook and run the cells sequentially.
   - For local setups, ensure you have Python 3.7+ installed.
   - Create a virtual environment and install required packages:
     ```bash
     python -m venv venv
     source venv/bin/activate  # On Windows use: venv\Scripts\activate
     pip install -r requirements.txt
     ```

3. **Dependencies:**
   The key dependencies include:
   - **Whisper:** Installed from OpenAI's GitHub repository.
   - **ffmpeg:** Required for audio processing.
   - **Torch & NumPy:** Specific versions are used for compatibility.
   - Other libraries such as `scipy`, `pydub`, and `deepl` are also required. Please refer to the notebook for the complete list.
### 🖥️ MacOS Installation Notes

If you're using macOS for local setup, follow these platform-specific steps in addition to the general setup:

1. **Ensure Homebrew is Installed:**
   If not already installed, you can install Homebrew with:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. **Install ffmpeg via Homebrew:**
   ```bash
   brew install ffmpeg
   ```

3. **Create and Activate Virtual Environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

4. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Mounting Google Drive (Colab Only):**
   - The notebook starts by mounting Google Drive for file access.
   
2. **Installing Dependencies:**
   - The first cell handles installing all necessary packages. Ensure you run this cell without interruption.

3. **Transcription Process:**
   - The notebook demonstrates how to split long audio files into smaller segments (10 minutes each) to facilitate efficient transcription.
   - Each segment is processed through Whisper to generate text output.

4. **Next Steps:**
   - The transcription output is the first step towards a comprehensive stakeholder feedback analysis. Future work will include:
     - **Sentiment Analysis:** Evaluating the tone and sentiment of stakeholder comments.
     - **Thematic Categorization:** Grouping feedback into key themes for easier decision-making.


## Contributing

Contributions are welcome! If you have improvements, additional features, or suggestions, please open an issue or submit a pull request. When contributing, please follow the coding conventions and document your changes appropriately.

## License

This project is licensed under the [MIT License](LICENSE).

If you find this repo useful don't hesitate to give it a star⭐
## Contact

For any questions or suggestions, please feel free to reach out via:
- Email: abioyebolaji18@gmail.com
- GitHub: [Bolaji Abioye](https://github.com/Abioye-Bolaji)


## Disclaimer

- Resource Constraints & GPU Limitations: Due to hardware limitations, training Whisper from scratch was not feasible. Instead, the project focuses on using pre-trained models and optimizing performance within the available computational resources.
- Library Version Conflicts: The Whisper model used in this project is based on an older version that does not support some of the latest Python libraries, such as updated versions of torch and numpy. To ensure compatibility, some libraries provided by Google Colab had to be downgraded to avoid conflicts (the main file would give more clarity).

