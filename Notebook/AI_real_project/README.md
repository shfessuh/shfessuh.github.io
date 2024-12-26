# Abstract
The ability of AI to create and generate realistic images has significant implications for authenticity and reliability in the digital era. With misinformation competing for attention on social platforms, tools to decode images and determine their source are invaluable for maintaining truth in information dissemination. This project explores the use of machine learning to classify images as either "Real" (human-made) or "AI-Generated." Using a Random Forest model and a Convolutional Neural Network (CNN), we compared their performance in detecting AI-generated content. Through this project, I was able to focus on model development, data preprocessing, hyperparameter tuning, and evaluation metrics.

## Dataset

The dataset, originally published on Kaggle by Cash Bowman, contains AI-generated and human-made artworks in categories such as people, animals, portraits, scenery, and psychedelics.
* The dataset was reduced to 970 valid images (originally 975).
* Images were resized to 224x224 pixels and converted to RGB without normalization to preserve original color schemes.

The dataset holds potential real-world applications, such as tagging computer-generated images on social media to prevent the spread of misinformation.

Link: https://www.kaggle.com/datasets/cashbowman/ai-generated-images-vs-real-images


## Method #1: Random Forest
* Random Forest was chosen for its robustness against noise and its ability to handle complex features, such as pixel values and textures.
* Data was split 70/30 for training and testing.
### Key Findings:
* After tuning hyperparameters, the optimal model achieved a testing accuracy of 68.04% .
* The model often misclassified real images as AI-generated, with a 38% misclassification rate for real images versus 28% for AI-generated images.
* Efforts to prune and fine-tune the model reduced overfitting but only marginally improved accuracy.


## Method #2: Convolutional Neural Network
A CNN model was mainly developed and analyzed by a project partner, achieving the highest accuracy of 71.9%. This method was particularly effective due to the CNN's capability for high-level feature extraction, making it well-suited for the image classification task.

* Tested different image dimensions (e.g., 64x64, 128x128, 256x256).
* Varied learning rates, identifying 0.0005 as optimal.
Adjusted the number of full layers, concluding that 5 layers provided the best results.
### Key Findings:
* Images with larger dimensions (256x256) performed better than smaller ones.
* Achieved a highest testing accuracy of 71.9%, outperforming the Random Forest model.

## Limitations and Future Work
**Dataset Size:** The dataset was limited to 970 images, which may restrict the models' generalizability to broader contexts.
**Overfitting:** The Random Forest model struggled with overfitting, reducing its performance on unseen data.
**Future Improvements:** Implementing advanced CNN architectures like ResNet or expanding the dataset with more diverse examples could significantly improve accuracy and applicability.

## Libraries 
 NumPy, pandas, matplotlib, torchvision, torch, and scikit-learn
