# AVSD-DSTC10 Official
  Audio Visual Scene-Aware Dialog (AVSD) Challenge at the 10th Dialog System Technology Challenge (DSTC)
  [https://sites.google.com/dstc.community/dstc10](https://sites.google.com/dstc.community/dstc10)

## Goal: Reasoning for Audio Visual Scene-Aware Dialog

    The task setup for the previous challenges for DSTC7 and DSTC8 allowed the participants 
    to use human-created video captions to generate answers for the dialog questions. 
    However, such manual descriptions are not available in real-world applications, 
    the system needs to learn to produce the answers without the captions. 
    To encourage progress towards this end, we propose a third challenge
    in DSTC10 under the video-based scene-aware dialog track. 
    In this challenge, we seek evidence from the system to support the generated answer 
    via detecting the temporal segments in the videos corresponding to the answer.
    
## Challenge schedule

    June 14th, 2021: Answer generation data release
    June 30th, 2021: Answer reasoning temporal localization data and baseline release
   **Releasing answer reasoning to registrants only**
  
    September 13th, 2021: Test Data release
    September 21st 2021: Test Submission due
    November 1st 2021: Challenge paper submission due
    January or February, 2022: Workshop

## Task definition
#### Task 1: Video QA dialog
    Goal: Answer generation without using manual descripitions for inference
    You can train models using manual descriptions but CANNOT use them for testing. 
    Video description power needs to be emebedded in the answer generation models.
    
    Data conditions:
    a. Use the provided video including audio and video features, 
       the dialog history and manual video descriptions (scripts and summary) data for training
        - scripts used to instruct actions
        - summary generated by the questioners after holding 10 QAs.

    b. Publicly available external data and pre-trained models may also be used for training as a sub task

#### Task 2: Grounding Video QA dialog
    Goal: Answer reasoning temporal Localization 

    To support answers, evidence is required to be shown without using manual descriptions. 
    When a system answer is “A dog is barking.”, the sound of the dog’s barking and
    the image of the dog should be provided as evidence.
    The localization of audiovisual evidence is required for each generated answers.
    To train reasoning localization, begin and end timing of evidences will be additionally provided for the training data.

    Data conditions:
    a. Temporal localization information for answer reasoning is provided as begin and end timestamps showing evidence scenes
    b. Any publicly available data and pre-trained models may also be used for training as a sub task.
 
##### Data Collection Method for Reasoning
![Data Collection for reasoning](https://github.com/dialogtekgeek/AVSD-DSTC10_Official/blob/main/Instruction_for_Reasoning.png)

#### Validation data set:

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

### 1. Text files:

* **train_set4DSTC10-AVSD.json**
  Training text files (train_set4DSTC10-AVSD.json) - Contains summary, caption, question answer pairs, **action with its timestamps**. 
   
* **valid_set4DSTC10-AVSD_with_action.json**
  Validation text file (valid_set4DSTC10-AVSD_with_action.json) - contains question answer pairs, **action with its timestamps**.
 
* **valid_set4DSTC10-AVSD.json**
  Validation text file (valid_set4DSTC10-AVSD.json) - contains question answer pairs 
 
* **mock_test_set4DSTC10-AVSD_from_DSTC7.json**
  Mock Test text file from DSTC7 (mock_test_set4DSTC10-AVSD_from_DSTC7.json) - contains question answer pairs only from DSTC7-test set

* **mock_test_set4DSTC10-AVSD_from_DSTC8.json**
  Mock Test text file from DSTC8 (mock_test_set4DSTC10-AVSD_from_DSTC8.json) - contains question answer pairs only from DSTC8-test set
  
[Annotation Data Download here](https://github.com/dialogtekgeek/AVSD-DSTC10_Official/blob/main/AnswerGeneration_NoManualDescription_06_14_2021.zip) 

OR

```
You can do a git clone of this repository
git clone https://github.com/dialogtekgeek/AVSD-DSTC10_Official/ and then 
cd AVSD-DSTC10_Official/
unzip AnswerGeneration_NoManualDescription_06_14_2021.zip
```

### 2. Audio feature files:

[Download Audio features from DSTC7 Here](https://drive.google.com/drive/folders/12Ri617jeV1XfMjcDQf5camyRXGrVW5u3?usp=sharing)

* Training and validation data sets  
   * vggish.tgz 
* Test set:
   * vggish_testset.tgz: 

### 3. Visual feature files:

[Download Visual features from DSTC7 Here](https://drive.google.com/drive/folders/12R7OtjcXAgxZiFi2fOSG8miFiqi0ewL2?usp=sharing)

- Training and validation data sets:   
  - i3d_flow.tgz 
  - i3d_rgb.tgz
- Test set:
  - i3d_flow_testset.tgz
  - i3d_rgb_testset.tgz

### 4. DSTC10 evaluation setup

[Download DSTC7 Evaluation for mock test set Here](https://drive.google.com/file/d/19Jmm4HNXSwcg-sL7jktlCalakPCIhnxm/view?usp=sharing )

- dstc7avsd_eval.tgz

```
For the evaluation without caption using mock test set - the evaluation tool from DSTC7 and DSTC8 is provided here
```

Although a new baseline system will be released soon, the old one is available from the following link:
https://github.com/dialogtekgeek/AudioVisualSceneAwareDialog

You can find more information in the following DSTC7-AVSD overview paper:
http://workshop.colips.org/dstc7/papers/DSTC10_Task_3_overview_paper.pdf

You can find more information in the following DSTC10-AVSD overview paper:
https://drive.google.com/file/d/1Di_BbKZrigp3auma4qKtIgVsdgsniOrs/view

Links to the previous related AVSD track in DSTC7 and DSTC8 challenge: 

[AVSD DSTC7 GitHub link](https://github.com/hudaAlamri/DSTC7-Audio-Visual-Scene-Aware-Dialog-AVSD-Challenge)

[AVSD DSTC8 GitHub Link](https://github.com/dialogtekgeek/DSTC8-AVSD_official)


### - Contact Information
[Chiori Hori](mailto:chori@merl.com) & [Ankit Shah](mailto:aps1@andrew.cmu.edu)

### Task Organizers

Ankit Shah, Shijie Geng, Peng Gao, Anoop Cherian, Chiori Hori and Tim K. Marks
