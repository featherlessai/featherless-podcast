# PDF to Podcast pipeline with Open-models

![PDF to Podcast Pipeline](assets/podcastbanner.jpeg)

A comprehensive pipeline for converting PDF documents into engaging podcast content using AI. This project uses Featherless.ai's API to transform technical content into natural-sounding conversations, complete with text-to-speech generation. This series of notebooks was inspired by the [Llama Cookbook](https://github.com/meta-llama/llama-cookbook)

## Pipeline Overview

The process consists of four main stages, each handled by a separate notebook:

1. **Text Extraction** (`featherless_podcast.ipynb`)
   - Extracts and cleans text from PDF documents
   - Uses PyMuPDF for efficient text extraction
   - Handles document validation and metadata
   - Chunks text for processing

2. **Script Generation** (`featherless_podcast2.ipynb`)
   - Transforms extracted text into conversational dialogue
   - Creates natural-sounding exchanges between two speakers
   - Adds personality and engagement through questions and responses
   - Includes realistic speech patterns and interjections

3. **TTS Optimization** (`featherless_podcast3.ipynb`)
   - Refines dialogue for text-to-speech compatibility
   - Structures output as speaker-attributed segments
   - Enhances script with proper pacing and expressions
   - Prepares content in a TTS-friendly format

4. **Audio Generation** (`featherless_podcast4.ipynb`)
   - Converts script to audio using Kokoro TTS
   - Handles voice selection for different speakers
   - Manages audio timing and transitions
   - Exports podcast in multiple formats

## Requirements

- Python 3.12+
- PyMuPDF
- Torch/Torchaudio
- Kokoro TTS
- FFmpeg (for audio processing)
- Featherless.ai API key

## Installation

1. Clone the repository
2. Install required packages:
pip install PyPDF2 rich ipywidgets pymupdf4llm torch torchaudio pydub soundfile kokoro>=0.7.11

3. Set up your Featherless.ai API key in the configuration cells

## Usage

1. Place your PDF file in the `pdf` directory
2. Run the notebooks in sequence:
   ```bash
   jupyter notebook notebooks/featherless_podcast.ipynb
   jupyter notebook notebooks/featherless_podcast2.ipynb
   jupyter notebook notebooks/featherless_podcast3.ipynb
   jupyter notebook notebooks/featherless_podcast4.ipynb
   ```

3. Find your generated podcast audio in the `podcast_export` directory

## Features

- **Intelligent Text Extraction**: Handles complex PDF layouts and formatting
- **Natural Dialogue Generation**: Creates engaging conversations from technical content
- **Multiple Voice Support**: Distinct voices for different speakers
- **Format Options**: Exports in MP3, WAV, and OGG formats
- **Progress Tracking**: Visual feedback during processing
- **Error Handling**: Robust error management throughout the pipeline

## Configuration

Key configuration parameters can be adjusted in each notebook:

- PDF processing settings (chunk size, max chars)
- API model selection and parameters
- Voice characteristics and speaker styles
- Audio output format and quality settings

## License

MIT License

## Acknowledgments

- [Llama Cookbook](https://github.com/meta-llama/llama-cookbook) for the inspiration on the notebooks
- [Kokoro](https://github.com/hexgrad/kokoro) for TTS capabilities
- [PyMuPDF](https://github.com/pymupdf/PyMuPDF) for PDF processing

## Contributing

Contributions welcome! Please read the contributing guidelines before submitting pull requests.