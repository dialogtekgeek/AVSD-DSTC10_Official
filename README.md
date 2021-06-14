# AVSD-DSTC10 Official
Audio Visual Scene-Aware Dialog (AVSD) Challenge at the 10th Dialog System Technology Challenge (DSTC)
https://sites.google.com/dstc.community/dstc10

# Challenge schedule
    June 14th, 2021: Answer generation data release
    June 30th, 2021: Answer reasoning temporal localization data and baseline release
                     ## *releasing to registrants only*
    September 13th, 2021: Test Data release
    September 21st 2021: Test Submission due
    November 1st 2021: Challenge paper submission due
    January or February, 2022: Workshop

# Task definition
#### Task 1: Answer generation without using manual descripitions for inference
    You can train models using manual descriptions but CANNOT use them for testing. 
    Video description power needs to be emebedded in the answer generation models.
    
    Data conditions:
    a. Use the provided video (including audio and videa features), 
       the dialog history and manual video descriptions (scripts and summary) data for training
        - scripts used to instruct actions
        - summary generated by the questioners after holding 10 QAs.
    b. Publicly available external data and pre-trained models may also be used for training as a sub task

#### Task 2: Reasoning temoporal Localization 
    a. Temporal localization information for reasoning is given as "begin:end" timestamps showing evidence scenes 
    b. Any publicly available data and pre-trained models may also be used for training as a sub task.
    
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

You can download the full official data set and the references for AVSD@DSTC10 from here:
https://drive.google.com/drive/folders/1SlZTySJAk_2tiMG5F8ivxCfOl_OWwd_Q?usp=sharing

### 1. Text files:
* train_set4DSTC10-AVSD.json
* valid_set4DSTC10-AVSD.json
* test_set4DSTC10-AVSD.json

Training text files - Contains summary, caption, question answer pairs, action with its timestamps. 

Validation text files - contains question answer pairs

Test text files - contains question answer pairs

### 2. Audio feature files:**
* Training and validation data sets  
   * vggish.tgz 
* DSTC10 test set:
   * vggish_testset.tgz: 

3. **Visual feature files:**
   - Training and validation data sets:
     
     - i3d_flow.tgz 
     
     - i3d_rgb.tgz
   
   - DSTC10 test set:
   
     - i3d_flow_testset.tgz
     
     - i3d_rgb_testset.tgz

4. **DSTC10 evaluation setup**
   - dstc10avsd_eval.tgz


Although a new baseline system will be released soon, the old one is available from the following link:
https://github.com/dialogtekgeek/AudioVisualSceneAwareDialog

You can find more information in the following DSTC7-AVSD overview paper:
http://workshop.colips.org/dstc7/papers/DSTC10_Task_3_overview_paper.pdf

You can find more information in the following DSTC10-AVSD overview paper:
https://drive.google.com/file/d/1Di_BbKZrigp3auma4qKtIgVsdgsniOrs/view

### - Contact Information
chori@merl.com & aps1@andrew.cmu.edu
