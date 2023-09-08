# RLHF-Community-Session

## Dataset

[reddit_fine-tuning](https://huggingface.co/datasets/CarperAI/openai_summarize_tldr/viewer/default/train?row=1)

[reddit_comparison_dataset](https://huggingface.co/datasets/CarperAI/openai_summarize_comparisons/viewer/default/test?p=836)

### How the dataset will be used:
train (92k) - for PPO; 
test(83.6k) - for testing; 
valid1(33k) - for fine tuning the base model; 
valid2(50k) - for the rewards model

## References

[TRL_HuggingFace](https://huggingface.co/docs/trl/main/en/index)

[illustrated_RLHF](https://huggingface.co/blog/rlhf)

