# CantTalkAboutThis Dataset - Teaching LLMs to stay on topic in Dialogues

Dataset for the [paper](https://aclanthology.org/2024.findings-emnlp.713/) "CantTalkAboutThis: Aligning Language Models to Stay on Topic in Dialogues" published at EMNLP 2024.

## Dataset
The data can be found under the `data` folder. We provide two versions of the dataset - one generated using `OpenAI gpt-4-turbo` and one using [`Mixtral-8x7B-Instruct`](https://huggingface.co/mistralai/Mixtral-8x7B-Instruct-v0.1). The data generated with `gpt-4-turbo` is released under `cc-by-nc-4.0` license and the data generated with `Mixtral-8x7B-Instruct` is released under `cc-by-4.0` license.

* The 'domains' folder contains the data split into various domains and can be easily analyzed to understand the structure of the dataset.
* Each sample in the dataset contains a system instruction, a scenario, a conversation with ~10 turns and a set of 5 distractors.
* The scenarios and system instructions for the various domains can be found in the `system_instructions.json` file.
* The data contains dialogues along with distractors for 9 different domains - 'banking', 'computer troubleshooting', 'education', 'health', 'insurance', 'legal', 'real estate', 'taxes', 'travel'.
* The 'processed' folder contains the processed data that can be directly used for training and evaluation.
* The human annotated test set for the banking domain can be found in the 'data/human_test_set.jsonl' file. This file contains more realistic and difficult distractors that can be used to evaluate the model's ability to stay on topic.

## Code and Model Checkpoints

We will be releasing the code for training and evaluation soon. Model checkpoints using Llama-3.1-8B-Instruct will also be released.

## How to cite

If you find this work useful, please cite the accompanying paper

```bibtex
@inproceedings{sreedhar-etal-2024-canttalkaboutthis,
    title = "{C}ant{T}alk{A}bout{T}his: Aligning Language Models to Stay on Topic in Dialogues",
    author = "Sreedhar, Makesh Narsimhan  and
      Rebedea, Traian  and
      Ghosh, Shaona  and
      Zeng, Jiaqi  and
      Parisien, Christopher",
    editor = "Al-Onaizan, Yaser  and
      Bansal, Mohit  and
      Chen, Yun-Nung",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2024",
    month = nov,
    year = "2024",
    address = "Miami, Florida, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.findings-emnlp.713",
    pages = "12232--12252"
}
```