# Docent-Research

## text classification
[jupyter notebook](https://github.com/Docent-Inc/Docent-Research/blob/main/text_classification.ipynb)

![](https://kr.object.ncloudstorage.com/docent/Screenshot%202024-01-25%20at%203.08.44%20PM.png)

### 목적
기록의 편리함을 위해 대화형으로 기록하는 서비스를 제작했습니다. 그 과정에서 사용자의 텍스트를 분류하기 위해 기존 gpt-4-turbo 모델을 사용했습니다.

하지만 기존 모델은 사용자의 텍스트를 분류하는데에 있어서 정확도가 떨어지고 높은 비용이 발생했습니다. 이를 해결하기 위해 사용자의 텍스트를 분류하는 모델을 제작했습니다.

### 성과
기존 방식에 비해 매우 저렴한 비용으로 더 높은 정확도(f1-score기준: 1.4배)를 얻을 수 있습니다.
- 기존 f1-score: 0.673
- 개선된 f1-score: 0.952

### 개발환경
    gpu: NVIDIA GeForce RTX 4090 24GB
    torch: 1.13.0
    transformers: 4.31.0
    scikit-learn: 1.3.0
    cuda: 12.3

## image prompt generator
[jupyter notebook](https://github.com/Docent-Inc/Docent-Research/blob/main/%08image_prompt_generator.ipynb)

![](https://kr.object.ncloudstorage.com/docent/Group%2088.png)

### 목적
꿈, 일기, 한 주 돌아보기 보고서에서 사용자의 텍스트를 분석해서 이미지를 생성해주는 기능을 제공합니다. dalle-3가 나오기 전까지는 gpt-3.5로 사용자의 텍스트로 이미지를 생성할 수 있는 prompt를 생성한 후 dalle-2에게 이미지를 생성하도록 요청했습니다. 하지만 dalle-3가 나오면서 그 과정이 생략돼서 사용자의 텍스트로 바로 이미지를 생성할 수 있게 됐습니다.

하지만 높은 비용이 발생했습니다. 따라서 무료로 제공하는 서비스에서는 사용할 수 없었습니다. 이를 해결하기 위해 사용자의 텍스트로 이미지의 prompt를 생성하는 모델을 제작했습니다.

### 성과
꿈, 일기, 한 주 돌아보기 보고서에 대해 사용자의 텍스트로 이미지의 prompt를 생성하는 모델을 제작했습니다. 각 분야에 대한 분위기, 특징, 성별을 반영하는 prompt를 생성할 수 있습니다.

### 개발환경
    gpu: NVIDIA GeForce RTX 4090 24GB
    torch: 1.13.0
    transformers: 4.33.3
    diffusers: 0.21.4
    compel: 2.0.2
    peft: 0.7.2
    accelerate: 0.27.0