# Artificial Neural Network and Deep Learning Challenges

<p align="center">
  <a href="#image-classification">Image Classification</a> •
  <a href="#image-segmentation">Image Segmentation</a> •
  <a href="#visual-question-answering">VQA</a>
</p>

## Image Classification
[![Kaggle](https://img.shields.io/badge/open-Kaggle-4791CD.svg)](https://www.kaggle.com/c/artificial-neural-networks-and-deep-learning-2020)

The goal is to classify images depicting groups of people based on the number of masked people. In the specific, the solution must discriminate between images depending on the following cases:

1. All the people in the image are wearing a mask
2. No person in the image is wearing a mask
3. Someone in the image is not wearing a mask

The following images are taken from the dataset and each one is of a different class (Up-Left (3), Up-Right (1), Bottom (2)).

<p align="center">
  <img src="https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F3311561%2Fbbb25e67374ea55c2f15f575b2989746%2F11056.jpg?generation=1604834938309207&alt=media" width="300" alt="Mask image 1"/>
  <img src="https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F3311561%2Fef05c005aa712dae1fd71351f2c5b3f7%2F10405.jpg?generation=1604835094952941&alt=media" width="300" alt="Mask image 2"/>
  <br>
  <img src="https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F3311561%2F2a987afcb01c2f48e296c30924ad51a7%2F11172.jpg?generation=1604835052572395&alt=media" width="200" alt="Mask image 3"/>
</p>

Dataset Details:
- Image size: variable
- File Format: JPG
- Number of classes: 3
- Training: 5614 images
- Test: 450 images

Classes:
- 0: "NO PERSON in the image is wearing a mask", 1900 images
- 1: "ALL THE PEOPLE in the image are wearing a mask", 1897 images
- 2: "SOMEONE in the image is not wearing a mask", 1817 images

Result: 92.2% accuracy on testset.

## Image Segmentation
### 1st ACRE Cascade Competition!
[![Kaggle](https://img.shields.io/badge/open-CodaLab-4791CD.svg)](https://competitions.codalab.org/competitions/27176)

ACRE is the Agri-food Competition for Robot Evaluation, part of the METRICS project funded by the European Union’s Horizon 2020 research and innovation program under grant agreement No 871252. Autonomous robots compete to demonstrate their ability to perform agricultural tasks (such as removing weeds or surveying crops down to individual-plant resolution). At field campaigns, participants collect data that are then made available for online competitions (Cascade Campaigns) like the one you are seeing. For more information about ACRE and METRICS visit the official website.

After years of decline, the number of undernourished people began to slowly increase again in 2015. Food Security requires that everyone can have enough food produced in a sustainable manner. The topic is increasingly gaining attention as food scarcity is worsened by a continuously growing population. Also, food production is threatened by climate change. The topic is so relevant that is part of one of the 17 Sustainable Development Goals of the UN 2030 Agenda. In particular, Food Security is a pillar of SDG number 2, Zero Hunger.

In this context, the agricultural sector is going under a process of revolution by the introduction of digital technologies. The Digital Agricultural Revolution can help to reduce the use of resources (water, fertilizers, and pesticides), thus diminishing the environmental contamination and the costs for the farmers. Also, it could increase the climate resilience of crops and their productivity.

Automatic crop and weed segmentation can be a driver of innovations to optimize the agricultural processes. Indeed, automatic weed detection can be exploited by a ground robot for mechanical weeding. Thus, pesticides could even be completely avoided.

Submissions are evaluated on the mean Intersection over Union (IoU) obtained on the two classes, crop and weed. IoU is typically used in segmentation tasks and it essentially quantifies the percentage of overlap between predicted and target segmentations.

<p align="center">
  <img src="https://i.ibb.co/4mmz110/Bipbip-haricot-im-00321.jpg" width="400" alt="Plants"/>
  <img src="https://i.ibb.co/7y542N2/Bipbip-haricot-im-00321.png" width="400" alt="Mask"/>
</p>

Dataset Details:
- Color space: RGB
- Number of Training images (per team per crop): 90
- Number of Test_Dev images (per team per crop): 15
- Number of Test images (per team per crop): 20

Classes: 
- Crop
- Weed
- Other vegetation
- Soil

Result: 0.6443 IoU on testset.

## Visual Question Answering
[![Kaggle](https://img.shields.io/badge/open-Kaggle-4791CD.svg)](https://www.kaggle.com/c/anndl-2020-vqa)

This competition is a visual question answering (VQA) problem on the proposed dataset. The dataset is composed by synthetic scenes, in which people and objects interact, and by corresponding questions, which are about the content of the images. Given an image and a question, the goal is to provide the correct answer. Answers belong to 3 possible categories: 'yes/no', 'counting' (from 0 to 5) and 'other' (e.g. colors, location, ecc.) answers.

<p align="center">
  <div align="center">
    <img src="https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F3311561%2F180591568512ee55bba8b82cd743b7e0%2F11654.png?generation=1608673500821556&alt=media" width="400" alt="VQA image 1"/><br>
    <h5>Q: Is the man's shirt blue?</h3>
    <h6>A: yes</h6>
  </div>
  <div align="center">
    <img src="https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F3311561%2Fd2cd106fefb32cdc2b80018b7e2106f0%2F19312.png?generation=1608673712874472&alt=media" width="400" alt="VQA image 2"/><br>
    <h5>Q: How many bikes?!</h3>
    <h6>A: 1</h6>
  </div>
</p>


Dataset Details:
- Image size: 400x700 pixels
- Color space: RGB
- File Format: png
- Total number of images: 29333

Questions:
- Number of training questions: 58832
- Number of test questions: 6372

Answers (targets):

58 possible answers belonging to 3 possible categories: 'yes/no' answers, 'counting' answers (from 0 to 5) and 'other' (e.g., colors, objects, ecc.). In the following the labels associated to each answer:

```python
labels_dict = {
  '0': 0,
  '1': 1,
  '2': 2,
  '3': 3,
  '4': 4,
  '5': 5,
  'apple': 6,
  'baseball': 7,
  'bench': 8,
  'bike': 9,
  'bird': 10,
  'black': 11,
  'blanket': 12,
  'blue': 13,
  'bone': 14,
  'book': 15,
  'boy': 16,
  'brown': 17,
  'cat': 18,
  'chair': 19,
  'couch': 20,
  'dog': 21,
  'floor': 22,
  'food': 23,
  'football': 24,
  'girl': 25,
  'grass': 26,
  'gray': 27,
  'green': 28,
  'left': 29,
  'log': 30,
  'man': 31,
  'monkey bars': 32,
  'no': 33,
  'nothing': 34,
  'orange': 35,
  'pie': 36,
  'plant': 37,
  'playing': 38,
  'red': 39,
  'right': 40,
  'rug': 41,
  'sandbox': 42,
  'sitting': 43,
  'sleeping': 44,
  'soccer': 45,
  'squirrel': 46,
  'standing': 47,
  'stool': 48,
  'sunny': 49,
  'table': 50,
  'tree': 51,
  'watermelon': 52,
  'white': 53,
  'wine': 54,
  'woman': 55,
  'yellow': 56,
  'yes': 57
}
```

*Best result*: 63.496% accuracy on testset.
