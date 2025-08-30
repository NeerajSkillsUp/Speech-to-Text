# 🎙️ Audio-to-Text Transcription with Python

Transform your audio files into readable text effortlessly! This project splits long audio recordings into manageable chunks, handles silence detection, and uses Google Speech Recognition to transcribe speech accurately.

## Features
- Automatic Chunking: Splits large audio files on silence for better accuracy.
- Speech Recognition: Converts spoken words to text using Google's API.
- Supports Multiple Formats: Works with MP3 and WAV files.
- Easy to Use: Minimal code and dependencies.

## Installation
pip install SpeechRecognition pydub

## Usage
1. Upload your audio file (MP3 or WAV).  
2. Convert to WAV if needed using ffmpeg:  
   subprocess.call(['ffmpeg', '-i', 'your_audio.mp3','wav_file.wav'])
3. Run the transcription:  
   print(get_large_audio_transcription('wav_file.wav'))

## Example Output
chunk1.wav : Hello there.  
chunk2.wav : Welcome to audio transcription.  
Full text: Hello there. Welcome to audio transcription.

## Notes
- Adjust `min_silence_len` and `silence_thresh` in the script for better results with different audio types.
- Longer audios are split automatically for optimal recognition.

Turn your speech into text seamlessly—perfect for lectures, podcasts, or personal notes!
