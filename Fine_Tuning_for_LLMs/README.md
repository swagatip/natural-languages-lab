### Project Overview

This project is based on tutorials on Prompt Engineering concepts, transfer learning, and fine-tuning LLMs.

### Reference

This project is loosely based on the LinkedIn Learning Tutorial: https://www.linkedin.com/learning/fine-tuning-for-llms-from-beginner-to-advanced/ by Instructor Axel Sirota: https://www.linkedin.com/learning/instructors/axel-sirota

### My Modifications

#### 1. Dependencies in requirements.txt
All the dependency libraries are kept in one place - `requirements.txt`
Run this command at the beginning of your jupyter notebook:

`% pip install -r ../requirements.txt -v`

The relative install path assumes the notebook runs with `src` as its working directory.

#### 2. Move from Tensorflow/Keras to PyTorch/Hugging Face's Seq2SeqTrainer

My initial TensorFlow/Keras attempt failed because `TFAutoModelForSeq2SeqLM` could not be imported from my installed version of Transformers. I switched to PyTorch for the fine-tuning workflow.

The `PromptEngg_*` notebooks retain most of the original code, while the other notebooks have been modified more substantially.

#### 3. Flag for running on CPU
In `TransferLearning_*` tutorial, I have set the flag `USE_CPU` to run in CPU on a smaller scale, if it detects that GPU is not available.