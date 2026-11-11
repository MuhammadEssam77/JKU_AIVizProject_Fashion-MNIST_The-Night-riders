# Phase I AI Interaction Log

These three prompts are paraphrases of how we used ChatGPT during Phase I.

## 1. Experiment Setup

> How should we set up an experiment to see what blur and brightness changes do to our Fashion-MNIST model?

ChatGPT suggested testing the original images first, then varying blur and brightness separately. Having one baseline made the results easier to compare. Accuracy fell from 94.76% to 42.54% at the strongest blur we tested, while it stayed between 87.01% and 94.76% across the brightness settings.

## 2. Checkpoint Loading and Preprocessing

> The checkpoint keeps giving me errors, and when I get it running the accuracy is only 36.44%. What should I check?

We used the supplied loader for the checkpoint and checked the preprocessing against the model card. Once we used the right mean and standard deviation, accuracy went up to 94.76%. Getting the model to load was only half the job. The baseline told us whether we were feeding it the images correctly.

## 3. Visualizing Errors and Confidence

> What can we plot to see which classes the model mixes up when the images get blurry, and how sure it is when it gets them wrong?

ChatGPT suggested per-class accuracy plots, confusion matrices and a confidence comparison. We also put original and blurred images side by side. At the strongest blur, the model called 476 sandals ankle boots, and its wrong predictions still had an average confidence of 48.68%.
