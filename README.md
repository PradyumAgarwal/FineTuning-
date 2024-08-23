# Audio and Text Fine-Tuning Project

This repository contains notebooks for creating datasets, fine-tuning audio transcription models, managing storage during training, and fine-tuning text generation models.

## Table of Contents

- [Notebooks](#notebooks)
  - [MakaDataset.ipynb](#makadatasetipynb)
  - [AudioTranscriptionFineTuning.ipynb](#audiotranscriptionfinetuningipynb)
  - [ClearTrash.ipynb](#cleartrashipynb)
  - [finetuninText.ipynb](#finetunintextipynb)
- [Usage Instructions](#usage-instructions)
- [Contributing](#contributing)
- [Contact](#contact)

## Notebooks

### MakaDataset.ipynb

This notebook generates a dataset for fine-tuning models. It requires access to a drive containing:

- `dataset.csv`: A CSV file with two columns: `Serial number` and `Sentence`.
- `AudioFiles` folder: Contains audio files corresponding to the sentences named as `audio1.mp3`, `audio2.mp3`, etc.

### AudioTranscriptionFineTuning.ipynb

This notebook fine-tunes an audio transcription model using the provided audio data. Key points:

- Loads a base audio transcription model and fine-tunes it.
- Requires the dataset to have `Sentence` and `Audio` columns.
- Needs access to a drive to store training checkpoints. Only the three latest checkpoints are kept to manage memory usage.
- It is recommended to run the `ClearTrash.ipynb` notebook alongside to avoid memory clogging.

### ClearTrash.ipynb

This notebook requires drive authentication and clears the trash folder of the drive every 2 minutes. This helps manage storage by ensuring that the deleted checkpoints during training do not fill up the drive space.

### finetuninText.ipynb

This notebook fine-tunes a text generation model on a provided dataset and uploads the fine-tuned model to Hugging Face. Key points:

- The data preparation steps are currently tailored for LLaMA 3 model variants.
- Parameters for quantization, LoRA, and training arguments can be adjusted based on requirements and available resources.
- Default settings are optimized for the limited resources of free Colab GPU.

## Usage Instructions

1. **MakaDataset.ipynb**:
   - Ensure you have a `dataset.csv` file and an `AudioFiles` folder in your drive.
   - Run the notebook to prepare your dataset.

2. **AudioTranscriptionFineTuning.ipynb**:
   - Load the notebook and set the base model, dataset, and training arguments.
   - Authenticate the drive to store checkpoints.
   - Run the notebook for fine-tuning the model.
   - Optionally, run the `ClearTrash.ipynb` notebook simultaneously.

3. **ClearTrash.ipynb**:
   - Authenticate your drive.
   - Run the notebook to periodically clear the trash folder.

4. **finetuninText.ipynb**:
   - Load the notebook and set the text generation model, dataset, and training arguments.
   - Adjust the data processing stage if changing the base model.
   - Run the notebook to fine-tune the model and upload it to Hugging Face.

## Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a pull request

## Contact

For questions or support, contact:

- **Name**: Pradyum Agarwal
- **Email**: pradyumagarwal2004@gmail.com
- **GitHub**: [PradyumSomebody](https://github.com/PradyumSomebody)
)

For details on the training results and procedures, please refer to the Hugging Face model pages linked above.
