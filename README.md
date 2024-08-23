# Folder Contents

This folder contains three datasets and three language models (LLMs) related to medical audio transcription. Below is a detailed explanation of each dataset and model.

## Datasets

### 1. Audio_Medical3
- **Description:** Contains 200 rows with columns `Sentence` and `Audio`.
- **Details:** Sentences were generated using ChatGPT, focusing on the medical domain, varying sentence structures, and including medical terminology to challenge audio transcription models, especially with Indian accents.
- **Hugging Face Model ID:** [PradyumSomebody/Audio_Medical3](https://huggingface.co/PradyumSomebody/Audio_Medical3)

### 2. Audio_Medical4
- **Description:** Contains 200 rows with columns `Sentence` and `Audio`.
- **Details:** Similar to Audio_Medical3, these sentences were generated with a focus on medical terminology and challenging transcription in Indian accents.
- **Hugging Face Model ID:** [PradyumSomebody/Audio_Medical4](https://huggingface.co/PradyumSomebody/Audio_Medical4)

### 3. Audio_Medical5
- **Description:** Contains 50 rows with columns `Sentence` and `Audio`.
- **Details:** Sentences generated to focus on medical domain and transcription challenges, including medical terms.
- **Hugging Face Model ID:** [PradyumSomebody/Audio_Medical5](https://huggingface.co/PradyumSomebody/Audio_Medical5)

## Models

### 1. Whisper-Small
- **Description:** Base model used for fine-tuning on the above datasets.

### 2. Whisper-Small-HI-Custom4
- **Description:** Fine-tuned on datasets Audio_Medical3 and Audio_Medical4.
- **Hugging Face Model ID:** [PradyumSomebody/whisper-small-hi-custom4](https://huggingface.co/PradyumSomebody/whisper-small-hi-custom4)

### 3. Whisper-Small-HI-Custom5
- **Description:** Fine-tuned on datasets Audio_Medical3, Audio_Medical4, and Audio_Medical5.
- **Hugging Face Model ID:** [PradyumSomebody/whisper-small-hi-custom5](https://huggingface.co/PradyumSomebody/whisper-small-hi-custom5)

For details on the training results and procedures, please refer to the Hugging Face model pages linked above.
