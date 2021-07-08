
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
  
[Download text files from Here](https://drive.google.com/drive/folders/13UgQz0cUkLrqOQt225PrivjmgdjUPLY8?usp=sharing )


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

# Data Collection Method for Reasoning
![Data Collection for reasoning](https://github.com/dialogtekgeek/AVSD-DSTC10_Official/blob/main/InstructionForReasoning.png)

