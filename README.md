# Audioset-website
Professional Handpan Audio Dataset for AI &amp; Machine Learning. 255 high-fidelity samples (48kHz/24-bit) with rich JSON metadata, velocity layers, and pitch analysis. Optimized for Timbre Transfer and Sound Synthesis.
[README.md](https://github.com/user-attachments/files/25157164/README.md)
# 🎵 HANDPAN AI DATASET

**Professional-grade handpan sample library optimized for AI/ML applications**

[![License](https://img.shields.io/badge/License-Commercial%20Royalty--Free-blue.svg)](LICENSE.md)
[![Sample Rate](https://img.shields.io/badge/Sample%20Rate-48kHz-green.svg)]()
[![Bit Depth](https://img.shields.io/badge/Bit%20Depth-24bit-green.svg)]()
[![Format](https://img.shields.io/badge/Format-Stereo%20WAV-green.svg)]()

---

## 📊 Dataset Overview

This dataset contains **255 professionally recorded handpan samples** captured in a professional studio environment on February 7, 2026.

### Key Features
- **48kHz / 24-bit stereo WAV files** - Pristine audio quality
- **3 velocity layers** (Low, Medium, High) - Essential for realistic synthesis
- **Complete chromatic coverage** - C4 to C6 range
- **Organized taxonomy** - Notes, Major Chords, Minor Chords, Percussions
- **ML-ready metadata** - Comprehensive JSON annotations

---

## 📁 Dataset Structure
```
HANDPAN_AI_DATASET/
├── Audio/
│   ├── Notes/
│   │   ├── Notes_High/        (25 samples)
│   │   ├── Notes_Medium/      (25 samples)
│   │   └── Notes_Low/         (25 samples)
│   ├── Chords_Maj/
│   │   ├── Chords_High_Maj/   (25 samples)
│   │   ├── Chords_Medium_Maj/ (25 samples)
│   │   └── Chords_Low_Maj/    (25 samples)
│   ├── Chords_Min/
│   │   ├── Chords_High_Min/   (25 samples)
│   │   ├── Chords_Medium_Min/ (25 samples)
│   │   └── Chords_Low_Min/    (25 samples)
│   └── Percussions/
│       ├── Percussion_High/   (10 samples)
│       ├── Percussion_Medium/ (10 samples)
│       └── Percussion_Low/    (10 samples)
├── metadata.json
├── LICENSE.md
└── README.md
```

**Total: 255 samples** across 4 categories and 3 velocity layers

---

## 🎯 Use Cases

### Machine Learning Applications
- **Generative Models**: Train neural synthesis models (WaveNet, SampleRNN, Diffusion)
- **Timbre Transfer**: Style transfer and voice conversion systems
- **Audio Classification**: Instrument recognition and tagging
- **Music Information Retrieval**: Pitch detection, onset detection, harmonic analysis

### Production Applications
- **Virtual Instruments**: Sample-based or neural synthesis plugins
- **Game Audio**: Interactive music systems and procedural audio
- **Sound Design**: Unique percussive elements and atmospheric textures
- **Music Production**: High-quality handpan sounds for DAW integration

---

## 📋 Technical Specifications

| Specification | Value |
|--------------|-------|
| **Sample Rate** | 48,000 Hz |
| **Bit Depth** | 24-bit |
| **Channels** | Stereo |
| **Format** | WAV (uncompressed) |
| **Total Samples** | 255 |
| **Pitch Range** | C4 - C6 (25 chromatic notes) |
| **Velocity Layers** | 3 (Low ~40, Medium ~80, High ~120 MIDI velocity) |
| **Recording Date** | February 7, 2026 |
| **Recording Environment** | Professional Studio |

---

## 🤖 Metadata Structure

Each sample includes comprehensive metadata in `metadata.json`:
```json
{
  "filename": "HP_A4_high.wav",
  "file_path": "Audio/Notes/Notes_High/HP_A4_high.wav",
  "category": "note",
  "note": "A4",
  "midi_note": 69,
  "frequency": 440.0,
  "velocity_level": "high",
  "velocity_midi": 120,
  "dynamic_marking": "ff",
  "is_percussion": false,
  "chord_type": null,
  "playing_technique": "strike",
  "articulation": "normal"
}
```

### Metadata Fields
- **Audio identifiers**: filename, file_path, instrument
- **Musical attributes**: note, midi_note, frequency, octave, chord_type
- **Performance data**: velocity_level, velocity_midi, dynamic_marking
- **Taxonomy**: category, subcategory, is_percussion
- **Playing style**: playing_technique, articulation

---

## 💡 Quick Start

### Python Example
```python
import json
import librosa

# Load metadata
with open('metadata.json', 'r') as f:
    data = json.load(f)

# Access a specific sample
sample = data['samples'][0]
print(f"Loading: {sample['filename']}")
print(f"Note: {sample['note']} ({sample['frequency']} Hz)")

# Load audio
audio, sr = librosa.load(sample['file_path'], sr=48000, mono=False)
print(f"Shape: {audio.shape}, Duration: {len(audio[0])/sr:.2f}s")
```

### TensorFlow/PyTorch Integration
The metadata structure is designed to work seamlessly with standard ML frameworks:
- Direct mapping to tensor labels
- Easy filtering by category, velocity, or pitch range
- Ready for DataLoader/Dataset classes

---

## 📊 Dataset Statistics

| Category | Count | Velocity Layers |
|----------|-------|----------------|
| **Notes** | 75 | Low (25), Medium (25), High (25) |
| **Major Chords** | 75 | Low (25), Medium (25), High (25) |
| **Minor Chords** | 75 | Low (25), Medium (25), High (25) |
| **Percussions** | 30 | Low (10), Medium (10), High (10) |
| **TOTAL** | **255** | - |

---

## 🎓 Citation

If you use this dataset in academic research, please cite:
```bibtex
@dataset{handpan_ai_2026,
  title={HANDPAN AI DATASET: Professional Handpan Samples for Machine Learning},
  author={Chefi},
  year={2026},
  url={https://audioset.io},
  note={48kHz/24bit stereo, 255 samples with velocity layers}
}
```

---

## 📧 Contact & Support

- **Creator**: Chefi
- **Email**: Chefi.contact@gmail.com
- **Website**: [audioset.io](https://audioset.io)

For questions, custom licensing, or bulk dataset inquiries, please reach out via email.

---

## 🙏 Acknowledgments

Thank you for choosing the HANDPAN AI DATASET for your project. This dataset represents hours of careful recording, processing, and organization to ensure the highest quality for AI/ML applications.

We're excited to see what you create with these sounds!

---

## 📄 License

This dataset is licensed under a **Commercial Royalty-Free License** with **non-redistribution** terms.

See [LICENSE.md](LICENSE.md) for complete terms and conditions.

---

**Version**: 1.0.0  
**Last Updated**: February 7, 2026  
**Dataset ID**: HANDPAN_AI_DATASET_V1

---

*Made with ❤️ for the AI music community*
