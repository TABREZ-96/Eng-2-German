# Eng-2-German
Eng 2 German is a user-friendly and efficient English to German translator powered by Intel's pre-trained machine translation model. Simplifying the language barrier, this tool provides quick and accurate translations from English to German. Whether you're a language enthusiast, traveler, or someone exploring German content.

# English to German Translator using OpenVINO and Streamlit

This demo utilizes Intel's pre-trained machine translation model to translate English sentences into German. The model is powered by OpenVINO and presented through an interactive Streamlit interface.

## Output
![image](https://github.com/TABREZ-96/Eng-2-German/assets/114156392/3e6cb3dc-acc0-4ff5-980b-551b19cd6d9f)

## Model Information

The translation model encodes sentences using the SentencePieceBPETokenizer from HuggingFace. The tokenizer vocabulary is automatically downloaded with the OMZ tool.

### Inputs and Outputs

- **Inputs:** The model's input is a sequence of up to 150 tokens. It has the following structure: `<s>` + tokenized sentence + `<s>` + `<pad>` (to pad remaining blank spaces).

- **Output:** After inference, the output is a sequence of up to 200 tokens with a similar structure as the input.

## Getting Started

Follow these steps to run the English to German translator:

1. Download the model to the current directory. Make sure you have run `pip install openvino-dev` beforehand.

    ```bash
    omz_downloader --name machine-translation-nar-en-de-0002
    ```

2. Install the required dependencies:

    ```bash
    pip install -q 'openvino-dev>=2023.0.0' streamlit tokenizers
    ```

3. Run the Streamlit app:

    ```bash
    streamlit run main.py
    ```

Replace `your_script_name.py` with the actual name of your Python script containing the Streamlit app.

## Usage

1. Launch the Streamlit app using the provided command.
2. Select the desired device from the dropdown list for running inference using OpenVINO.
3. Enter an English sentence in the text input.
4. Click the "Translate" button to see the German translation.
5. The translated sentence and the time spent during inference will be displayed.


## Additional Information

For more details about the translation model, refer to the [Open Model Zoo (OMZ) documentation](https://github.com/openvinotoolkit/open_model_zoo/blob/main/models/intel/machine-translation-nar-en-de-0002/README.md).

Feel free to contribute, report issues, or suggest improvements by creating GitHub issues or pull requests.

Happy translating!

