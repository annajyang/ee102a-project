# EE102A Final Project
Anna Yang & David Hu

## Concepts:
- Continuous & discrete signals
- Fourier Transform
- Convolution
- High pass, low pass, band pass filtering
- Sampling & interpolation

## Deliverables:
- One program that takes in 3 user drawings and converts them from 2-D drawings into an audio file that encodes oscilloscope cursor position into L and R channels. The three drawings will also be frequency multiplexed in the frequency domain. The program uses sampling and interpolation to generate the audio file. If time, we will add a slider for the user to customize sampling rate & options for interpolation method (nearest neighbor, linear, quadratic, cubic, etc).
- A second program that takes in an audio file and filters out the three images contained within the frequency domain, shifts them accordingly and displays them on an oscilloscope.
- Video demo of both programs working

## Methods:
Both programs will be written in python, audio files will be stereo .wav format.

## Project structure

```text
drawings-to-audio/
  main.py              # Drawing-to-audio entry point
  drawing_input.py     # Collect three 2-D drawings
  sampling.py          # Sampling and interpolation
  multiplexing.py      # Frequency multiplexing and L/R encoding
  wav_output.py        # Stereo WAV export
audio-to-oscilloscope/
  main.py              # Audio-to-oscilloscope entry point
  wav_input.py         # Stereo WAV input
  filtering.py         # Band separation and frequency shifting
  display.py           # XY oscilloscope display
requirements.txt       # Python dependencies
```

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

Run the placeholder entry points from the project root:

```bash
python drawings-to-audio/main.py
python audio-to-oscilloscope/main.py
```