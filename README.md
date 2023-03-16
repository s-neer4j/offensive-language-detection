---
license: mit
datasets:
- badmatr11x/hate-offensive-speech
language:
- en
metrics:
- accuracy
library_name: adapter-transformers
pipeline_tag: text-classification
tags:
- code
widget:
- text: "People are fun to talk."
  example_title: "Neither Speech"
- text: "Black people are good at running."
  example_title: "Hate Speech"
- text: "And I'm goin back to school, only for the hoes and a class or two."
  example_title: "Offensive Speech"
---


This is the **Offensive and Hateful Speech Detection** mode fine-tuned on the **distilroberta-base** model available on the huggingface pre-trained models. This model is trained with the [dataset](https://huggingface.co/datasets/badmatr11x/hate-offensive-speech/) which contains around 55K annotated tweets; classified into three different categories, Hateful, Offensive and Neither.

This is the example of the dataset instance:
```
{
  "label": {
    0: "Hate Speech",
    1: "Offensive Speech",
    2: "Neither"
  }
  "tweet": <string>
}
```

Model is fine-tuned on epochs number 5 with over than 15500 rounds of training. The self-verified evaluation accuracy of the models is **95.60%** with the evaluation lost **17.02%**. The testing accuracy of the model is recored **95.04%**, self stated.