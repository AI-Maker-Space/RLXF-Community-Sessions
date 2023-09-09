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
* The target model: We will be using the [T5-base](https://huggingface.co/t5-base) model (220M params): Being an encoder-decoder, seems a better option for summarization.
* The rewards model: We will be using Bert, as an encoder is more appropriate to produce a reward or a penalty based on the input.

## References

[TRL_HuggingFace](https://huggingface.co/docs/trl/main/en/index)

[illustrated_RLHF](https://huggingface.co/blog/rlhf)

## Presentation stack

[canva_presentation](https://www.canva.com/design/DAFt45GUO8w/9mgzJR-LndkIkTJ767hcVw/edit?utm_content=DAFt45GUO8w&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## Reward Model
Weights at: https://drive.google.com/drive/folders/1BKtlHKiv60unMdaXt5IEBnOgzF_6cSux?usp=sharing
