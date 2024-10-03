# DiP-ASR Dataset

## Introduction
The DiP-ASR dataset is designed to facilitate research in cross-lingual proper noun recognition in automatic speech recognition (ASR) systems. This dataset includes recordings from multiple languages and is focused on proper noun recognition within different linguistic contexts.

## Dataset Description
This dataset contains utterances in Hindi, Tamil, Telugu, Chinese, and Russian. The utterances are categorized into simple and complex commands, particularly focusing on user requests directed at personal assistants, predominantly for playing songs and other specific instructions.

### Dataset Structure
- **Languages:** Hindi, Tamil, Telugu, Chinese, Russian
- **Total Utterances:** 2711
- **Training Set:** 200 utterances from three speakers in each language
- **Test Set:** 100 utterances per language divided into:
  - 50 simple utterances (X_S)
  - 50 complex utterances (X_C)

### Utterance Types
- **Simple Utterances (X_S):** Command and song name, typically containing one or two cross-lingual proper nouns.
- **Complex Utterances (X_C):** Command, song name, and platform name, containing more than two cross-lingual proper nouns.

## Data Collection
The dataset was created by three contributors:
- **S. Ganesh Janakiraman**
- **Abhiram Naidu**
- **Swaroop R. Ghag**

All contributors followed detailed instructions to ensure consistent and high-quality recordings. Utterances were recorded in controlled environments to minimize background noise and ensure clarity.

## Usage
The dataset is provided in a structured format to facilitate easy integration into ASR systems. Each utterance is labeled with its corresponding language, type (simple or complex), and the intended transcription.

### Example Usage
```python
# Example code to load and use the dataset
import json

with open('dip_asr_dataset.json', 'r') as f:
    data = json.load(f)

# Iterate through the dataset
for entry in data:
    print(f"Language: {entry['language']}, Utterance: {entry['utterance']}, Type: {entry['type']}")

