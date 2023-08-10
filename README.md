# MPL-Summer23
This repository contains work done during the summer of 2023 at Multimodal Perception Lab, IIIT - Bangalore.

## Project Description and Goal
- The project as a whole aims to predict if a child has Autism or not based on recorded sessions of them performing certain activities.
- We worked on a specific sub-problem of this project which involved detecting the presence of a child or an adult within an image.
- To accomplish this task, we made use of, and trained the YOLOv8 model on our custom dataset.

## Work Done
### Data Collection and Training - 1
- Our first task was to collect images of children and adults from the internet on which we would train our model. This was an important step as our mentor informed us of how existing datasets have images of people of primarily white ethnicity, which would not be suitable for our usecase.
- We collected around 250 images and annotated them with bounding boxes. To do this, we used a web-based tool called `Roboflow` which allowed us to annotate, preprocess, augment, and export the dataset.
- We then trained the model on this data and did some experimentation too, but the results obtained were not as desired.
- We felt that this was due to having a wide variety of images (pertaining to different scenarios) but not enough samples (number of images).

### Data Collection and Training - 2
- Upon discussing this issue with our mentor, she shared a larger dataset of short videos with us. We were able to extract 1013 images from this dataset which were relevant to our usecase.
- Data Split:

| `Category` | `Number of Images` |
| ---------- | ------------------ |
| Train | 710 |
| Test | 153 |
| Validate | 150 |
| Total | 1013 |

- Now, we trained the model on this new dataset and the results obtained were definitely an improvement over the previous ones.

### Training - 3
- We were instructed by our mentor to now try using the images we collected (from the internet, `Data Collection and Training - 1`) to test the model which was trained on the larger dataset (from `Data Collection and Training - 2`).
- This led to a decrease in how good the model performed earlier. We suspected that over-fitting might be the reason and looked at how we could make our model generalise better.
- We discussed this issue with our professor and came to the conclusion that in some situations when we know beforehand that our model will be used only in specific scenarios (where the model performed relatively well), over-fitting would not be a huge drawback.

## Results and Summary

## Key Learnings
- During the course of the internship, we explored how CNNs function and went through lectures from CS231n, Stanford University (available on Youtube) which introduced us to image classification.

## Other Takeaways
- We also had a chance to understand some basic machine learning models and their use through Tensorflow and Pytorch.
- Our mentor shared the following papers with us for reading:
    * Multi-Modal Classifiers for Open-Vocabulary Object Detection
    * InternImage: Exploring Large-Scale Vision Foundation Models with Deformable Convolutions
- We read these papers and prepared slides for discussing the same.

## People Involved
- Prof. Dinesh Babu Jayagopi
- Ms. Jeba Berlin (Mentor)
- Vidhish Trivedi (Intern)
- Deepkumar Patel (Intern)
