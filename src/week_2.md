# Week 2

> 2022/10/03 - 2022/10/09

## Acceleration Ratio

The distributed square attack can reduce the attack time from ~15h to ~4h.

**Source Code**: [https://github.com/wuhanstudio/adversarial-classification](https://github.com/wuhanstudio/adversarial-classification)



## Common Mistakes

While implementing distributed black-box attacks, I noticed that some prior research made several common mistakes in their code. Their methods outperformed state-of-the-art partly because these mistakes gave them access to extra information that should not be available for black-box attacks. For example:

- They apply the perturbation after image resizing, assuming they know the input image size of a black-box model.
- The bandit attack does not clip the image while estimating gradients, assuming they can send invalid images (pixel value > 255 or < 0) to the black-box model.

Besides these mistakes, some methods are less effective while attacking real-world image classification APIs:

- They assume they can perturb a pixel value from 105 to 105.45 (float), while real-world input images are 8-bit integers, thus some perturbations are mitigated after data type conversion: int(105.45) == 105.

- Cloud APIs accept JPEG or PNG images (lossy compression) as input, while prior research assumes they can add perturbations to the raw pixels.   After JPEG encoding, some adversarial perturbation gets lost.

As a result, some prior research compared their methods with others under on unfair settings. To prevent making these mistakes, I designed my own image classification cloud service for further research, so that we have a fair comparison.



## Why they made these mistakes

They tested their attacks against local models on their computers (they have access to the file model.h5), and **rely on themselves to restrain access to model information**. Intentionally or unintentionally, they exploit extra information to improve their methods. For example:

- A Pytorch / Tensorflow model makes predictions using the function `model.predict(X)`, and the function only accepts input images `X` as arrays. We can't stack images of different shapes to be an array, thus they resize the images to be the same size so that the function won't give errors, which is a mistake.
- The function `model.predict(X)` won't give errors even if the image `X` contains negative values. Thus they are unaware that their methods generate invalid images.
- The function `model.predict(X)` accepts float numbers, thus they did not convert their input images to be integers. 
- The function `model.predict(X)` accepts raw images, thus they did not encode their inputs.



## Plan

**Week 1**:

- Local Search

  [●] SimBA (2019)
  
  [●] Square Attack (2020)

**Week 2**:

- Gradient Estimation

  [ &nbsp;] Limited Query (2018) (NES Gradient Estimation)

  [●] Bandits (2019) (The Data and Time priors)


- Cloud Service APIs

  [●]  Cloud Vision (Google)

  [●]  Imagga

  [●]  Deep API (ours)

- The Draft for MLSys 2023. (Introduction)

