# RLHF-Community-Session

## Dataset

[reddit_fine-tuning](https://huggingface.co/datasets/CarperAI/openai_summarize_tldr/viewer/default/train?row=1)

[reddit_comparison_dataset](https://huggingface.co/datasets/CarperAI/openai_summarize_comparisons/viewer/default/test?p=836)

### How the dataset will be used:
* train (92k) - for PPO
* test(83.6k) - for testing
* valid1(33k) - for fine tuning the base model
* valid2(50k) - for the rewards model

## Model

### Reference (supervised-fine-tuned)  model:
We will be using the [T5-base](https://huggingface.co/t5-base) model (220M params): Being an encoder-decoder, seems a better option for summarization.
Check the notebook on how we applied SFT on this model.

Here are the trained weights: 
- [4-bit model trained with QLoRA](https://huggingface.co/PanoEvJ/summarization_finetuned_t5_base_4bit)
- [full model](https://huggingface.co/PanoEvJ/T5_base_SFT_summarization)

### Policy (target) model

The target model we will be the same as the Base (fine-tuned): [T5-base](https://huggingface.co/t5-base) model (220M params): Being an encoder-decoder, seems a better option for summarization.

### Rewards model
  
The rewards model: We will be using Bert, as an encoder is more appropriate to produce a reward or a penalty based on the input.
Weights at: https://drive.google.com/drive/folders/1BKtlHKiv60unMdaXt5IEBnOgzF_6cSux?usp=sharing

Weights should be downloaded to your local computer from this link and once there they can be used from the notebook.  The notebook has a couple of lines to load the model:

model = AutoModelForSequenceClassification.from_pretrained("./model_bert_hf_experiment2/")

tokenizer = AutoTokenizer.from_pretrained("./model_bert_hf_experiment2/")


## References

[TRL_HuggingFace](https://huggingface.co/docs/trl/main/en/index)

[illustrated_RLHF](https://huggingface.co/blog/rlhf)

## Presentation stack

[canva_presentation](https://www.canva.com/design/DAFt45GUO8w/9mgzJR-LndkIkTJ767hcVw/edit?utm_content=DAFt45GUO8w&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
