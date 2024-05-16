# CK3 DNA predictor
The code by Akime [published](https://forum.paradoxplaza.com/forum/threads/ck3-image-to-portrait-modeling.1519240/) in Paradox Plaza forums.
It can predict character's face features by the photo supplied.

This fork has been made for [Vladislav](https://www.instagram.com/vladislav1706/) to describe usage and fix possible bugs and typos.

## Dataset
The [dataset](https://drive.google.com/file/d/1qeUAL9Cumoxv9Z1mpe1ySjbpRSQhzrHE/view?usp=sharing) is published separately since it's 3.1 Gb in size.

## Training details
This network has been trained on the torngasuk_dataset, which contains approximately 23k data samples of 8900 unique characters. Due to an error of mine every dna file was parsed as male, so the network saw all those characters as males, which may be the reason it is not as performing when inputting female pictures. I then proceeded to retrain the model with the corrected dataset. Surprisingly, it worsened the performance of the network by a lot. This may be due to the fact that recognizing gender added another layer of complexity to the problem, gender recognition also, is more of a categorical classification problem, telling if someone is male or female, rather than a regression problem where you have to output values. I have quite a few ideas on how to tackle this problem so that will take some testing. But even as it is, purely scaling up the dataset should do the trick, performance scale up with the quantity of data fed into it. But as the dataset scale it will cost more and more to train it. So I don't really have the most freedom when testing.

## Usage
TBD


## Related projects
 - [Face predictor](https://colab.research.google.com/drive/1tbwgCMt7XlEnbnGO7huSX75-YuAzUP22?usp=sharing) from [CK subreddit](https://www.reddit.com/r/CrusaderKings/comments/u7w3el/comment/i5h5txz/)

