# Phase I Reflection on GenAI Assistance

**AI-aided pair**

| First and last name | Student ID |
|---|---|
| Youssef Hamad | K12453150 |
| Ahmed Bakkar | K12438432 |

We started Phase I by using ChatGPT to plan how to test a pretrained CNN on Fashion-MNIST. It helped us turn the idea into a short sequence of steps. First we would test the original images, then change blur and brightness separately on the same 10,000 test images.

We got stuck on repeated checkpoint-loading errors. After getting the supplied loader to work, we still only got 36.44% accuracy on the original images. We checked the model card and corrected the normalization to a mean of 0.2860 and a standard deviation of 0.3530. The baseline then matched the reported 94.76%.

Once the baseline worked, we ran the blur and brightness tests and made the plots. ChatGPT helped us choose what to look at. The accuracy curves showed that blur caused a much bigger drop across the settings we tested. The confusion matrices and image examples helped us see which mistakes were behind that drop.

The main lesson was to check AI suggestions against the model files and a baseline run before using them in the rest of the notebook. We kept the same test set and normalization for every run so we could compare the effects of the image changes.

The comparison with the human-only pair is pending because we did not have their results when writing this reflection.
