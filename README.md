# qlora-fine-tune

My data & modified qlora.py from [mzbacc/qlora-fine-tune](https://github.com/mzbac/qlora-fine-tune).

output.json data manually created from information pertaining to Gigabyte Motherboards.

QLoRA trained with 1000 optimizer steps using an input-output format for training. 

Each json object is passed into the ALPACA dataset format:
```
### Instruction: {input}
### Response: {output}
```
The input gives context for the task that the LLM is trying to achieve, while the output is the answer to the instruction given. 

Base model used is [TheBloke's WizsardLM 7B](https://huggingface.co/TheBloke/wizardLM-7B-HF). This model was chosen because originally we were going to use the WizardLM 13B model which ranks highly on several different metrics such as Alpaca Eval & MT-Bench. However, for the sake of managing resources, I decided to fine tune on a 7B model instead. The original model is based on Llama 2 and fine tuned by using a method called Evol-Instruct to create complex instruction data.
