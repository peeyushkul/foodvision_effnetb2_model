# foodvision_effnetb2_model

An [EfficientNetB2 feature extractor](https://pytorch.org/vision/stable/models/generated/torchvision.models.efficientnet_b2.html#torchvision.models.efficientnet_b2) computer vision model to classify images.

Deployed Model at Hugging Face - https://huggingface.co/spaces/peeyushkul/foodvision_effnetb2_model_full


**Broad Steps:**
1. Create an EffNetB2 feature extractor (transfer learning model that has its base layers frozen and output layers customized for current problem)
2. Get the input transform needed from model weights
3. Get [Food101 dataset](https://pytorch.org/vision/main/generated/torchvision.datasets.Food101.html)
4. Turn Food101 datasets into DataLoaders
5. Train Foodvision model
6. Inspect loss curves
7. Save model if accuracy is satisfactory
8. Use Gradio to create a deployable app
9. Deploy on [Hugging Face](https://huggingface.co/spaces/peeyushkul/foodvision_effnetb2_model_full)


**Details of files:**
* `data_setup.py` - a file to prepare and download data if needed.
* `engine.py` - a file containing various training functions.
* `model_builder.py` - a file to create a PyTorch TinyVGG model.
* `train.py` - a file to leverage all other files and train a target PyTorch model.
* `utils.py` - a file dedicated to helpful utility functions.
* `predictions.py` - a file for making predictions with a trained PyTorch model and input image
