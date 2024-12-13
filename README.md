# LGCL_IMG_CAP
Implementation of Language Guidance into an Image Captioning model (combination of Vit_base_224_16 and GPT2), to mitigate cathastrophic forgetting during continual learning.


Abstract

This thesis explores prompt-based continual learning as a solution to catastrophic forgetting in image captioning. Continual learning models must learn incrementally across tasks without losing previously acquired knowledge. However, most continual learning research has focused on simpler tasks, like image classification, while image captioning remains mostly underexplored. Common continual learning strategies, such as regularization, rehearsal, and architecture-based methods, each have limitations like scalability issues and increased model complexity, particularly when applied to complex tasks like image captioning.
Our research builds on recent advances in prompt-based continual learning, notably the Language Guidance for Prompt-based Continual Learning (LGCL) framework, which uses language as a stable semantic space to retain and transfer knowledge across tasks. LGCL aligns visual representations with language prompts, creating a shared semantic structure that helps mitigate forgetting. Inspired by this, we propose two novel prompt-based strategies with a pretrained Image Captioning model: the use of structured string prompts and a contrastive learning technique involving positive and negative prompts. The structured string prompt, applied at the beginning of each caption, consistently anchors the model’s focus, while contrastive learning differentiates between relevant and irrelevant visual features using a triplet loss function.
Our approach introduces language guidance in a memory-efficient way, applying prompt-based methods only during training to avoid inference overhead. During training, the model uses positive prompts derived from target nouns and negative prompts sampled from unrelated tasks to reinforce attention on task-relevant information. Our approach, tested across a sequence of captioning tasks, shows promising results in retention.
Our findings also reveal some trade-offs, such as a slight decrease in task-specific accuracy in favour of retention. Future work could address these challenges.
In essence, this thesis highlights the potential of prompt-based continual learning as an effective method for mitigating forgetting in image captioning. By leveraging structured, language-guided prompts, our work provides a framework that preserves model performance over sequential tasks without adding computational burden during inference. 



Keywords: Image Captioning, Continual Learning, Prompt-Based Continual Learning, LGCL. 



Steps to run the code:



