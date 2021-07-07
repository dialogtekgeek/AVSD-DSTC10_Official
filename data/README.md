
# Data set: Video Data from Charades dataset
    Video dat: CHARADES for human action recognition datasets.
        https://allenai.org/plato/charades/
   
        *The original videos of the test sets of the official Charades Challenge
          https://ai2-public-datasets.s3-us-west-2.amazonaws.com/charades/Charades_vu17_test.tar [13Gb]
          https://ai2-public-datasets.s3-us-west-2.amazonaws.com/charades/Charades_vu17_test_480.tar [2Gb]

# Validation data set:
Please train models using the training data set only.
You can tune the parameters using the validation set and confirm the performance of your systems using the DSTC10 test sets.
Notes: The official challenge doesn't allow you to use the DSTC10 test set to tune your models.

|               |    Training    |  Validation   |   DSTC10 Test  |
| ------------- | -------------- | ------------- | ------------- |
| # of Dialogs  |       7,659    |      1,787    |      1,710    |   
| # of Turns    |     153,180    |     35,740    |     13,490    |
| # of Words    |   1,450,754    |    339,006    |    110,252    |

*The number of turns for the test set is smaller than the validation
because they are not always full dialogs.

Please review the following information on how to download annotations set, feature representations and evaluation setup for AVSD@DSTC10.


# Data release
## 1. Text files:

* **train_set4DSTC10-AVSD.json**
  Training text files (train_set4DSTC10-AVSD.json) - Contains summary, caption, question answer pairs, **action with its timestamps**. 
   
* **valid_set4DSTC10-AVSD_with_action.json**
  Validation text file (valid_set4DSTC10-AVSD_with_action.json) - contains question answer pairs, **action with its timestamps**.
 
* **valid_set4DSTC10-AVSD.json**
  Validation text file (valid_set4DSTC10-AVSD.json) - contains question answer pairs 
 
* **mock_test_set4DSTC10-AVSD_from_DSTC7_singref.json**
  Mock Test text file from DSTC7 (mock_test_set4DSTC10-AVSD_from_DSTC7_singref.json) - contains question answer pairs only from DSTC7-test set

* **mock_test_set4DSTC10-AVSD_from_DSTC8_singref.json**
  Mock Test text file from DSTC8 (mock_test_set4DSTC10-AVSD_from_DSTC8_singref.json) - contains question answer pairs only from DSTC8-test set
  
[Annotation Data Download here](https://github.com/dialogtekgeek/AVSD-DSTC10_Official/blob/main/AnswerGeneration_NoManualDescription_06_14_2021.zip) 

OR

```
You can do a git clone of this repository
git clone https://github.com/dialogtekgeek/AVSD-DSTC10_Official/ and then 
cd AVSD-DSTC10_Official/
unzip AnswerGeneration_NoManualDescription_06_14_2021.zip
```

## 2. Audio feature files:

[Download Audio features from DSTC7 Here](https://drive.google.com/drive/folders/12Ri617jeV1XfMjcDQf5camyRXGrVW5u3?usp=sharing)

* Training and validation data sets  
   * vggish.tgz 
* Test set:
   * vggish_testset.tgz: 

## 3. Visual feature files:

[Download Visual features from DSTC7 Here](https://drive.google.com/drive/folders/12R7OtjcXAgxZiFi2fOSG8miFiqi0ewL2?usp=sharing)

- Training and validation data sets:   
  - i3d_flow.tgz 
  - i3d_rgb.tgz
- Test set:
  - i3d_flow_testset.tgz
  - i3d_rgb_testset.tgz

## 4. DSTC10 evaluation setup for Mock

### DSTC10 official baseline system
Download DSTC10 baseline system from here:
GitHub_Link:

### Task 1. Video QA dialog: Answer generation evaluation using single ground truth
[Download DSTC7 Evaluation for mock test set here](https://drive.google.com/file/d/19Jmm4HNXSwcg-sL7jktlCalakPCIhnxm/view?usp=sharing)
- dstc7avsd_eval.tgz

[Download DSTC8 Evaluation for mock test set here](https://drive.google.com/file/d/1EKfPtrNBQ5ciKRl6XggImweGRP84XuPi/view?usp=sharing)
- dstc8avsd_eval.tgz

   ```
   For the evaluation using mock test set where the "__UNDISCLOSED__" needs to be replaced by your system answers
   - the evaluation tool from DSTC7 and DSTC8 is provided here
   ```
   The baseline system for DSTC7 and DSTC8 is available from the following link:
   https://github.com/dialogtekgeek/AudioVisualSceneAwareDialog

   You can find more information in the following DSTC7-AVSD overview paper:
   http://workshop.colips.org/dstc7/papers/DSTC10_Task_3_overview_paper.pdf

   Links to the previous related AVSD track in DSTC7 and DSTC8 challenge: 
   
   [AVSD DSTC7 GitHub link](https://github.com/hudaAlamri/DSTC7-Audio-Visual-Scene-Aware-Dialog-AVSD-Challenge)
   
   [AVSD DSTC8 GitHub Link](https://github.com/dialogtekgeek/DSTC8-AVSD_official)

### Task 2. Reasoning Video QA dialog: Answer generation with reasoning timing using single answer
Please use the evaluation package in the DSTC10 official baseline system.

##### Data Collection Method for Reasoning
![Data Collection for reasoning](https://github.com/dialogtekgeek/AVSD-DSTC10_Official/blob/main/InstructionForReasoning.png)

