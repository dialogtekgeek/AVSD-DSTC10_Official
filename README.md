# AVSD-DSTC10 Official
  Audio Visual Scene-Aware Dialog (AVSD) Challenge at the 10th Dialog System Technology Challenge (DSTC)
  [https://sites.google.com/dstc.community/dstc10](https://sites.google.com/dstc.community/dstc10)


## News
The challenge setup for AVSD-DSTC10 is available: https://github.com/ankitshah009/AVSD-DSTC10_baseline

#### System submission site is now open: 
    https://docs.google.com/forms/d/e/1FAIpQLSe6FNXNhpb-VjiILamx6EjR_ducdRLgnP9keh2fa-Q8WvrcJQ/viewform
    To upload your files, please use your google account.

#### The baseline system and the validation data for reasoning timing is now releasing:
After register DSTC10 and then get the baseline system from [HERE](https://docs.google.com/forms/d/e/1FAIpQLSeTQYoIz_caYHg59VAd18ypkI_9nfGvzrI6N6bq6wiT2c2SEw/viewform)

#### Please [Register HERE](https://docs.google.com/forms/d/e/1FAIpQLSe9CgrlygYciIZH_pK8133fbp1kqigTB6JIP7utfNFx_xSm6A/viewform) for participating in the DSTC10 challenge


## Goal: Reasoning for Audio Visual Scene-Aware Dialog

    The task setup for the previous challenges in DSTC7 and DSTC8 allowed the participants 
    to use human-created video captions to generate answers for the dialog questions. 
    However, such manual descriptions are not available in real-world applications, where the 
    system needs to learn to produce the answers without the captions. 
    To encourage progress towards this end, we propose a third challenge
    in DSTC10 under the video-based scene-aware dialog track. 
    In this challenge, we seek evidence from the system to support the generated answer 
    via detecting the temporal segments in the videos corresponding to the answer.
    
## Schedule

    June 14th, 2021: Answer generation data release
    June 30th, 2021: Answer reasoning temporal localization data and baseline release: 
       **Releasing  AVSD@DSTC10 registrants only**
  
    September 13th, 2021: Test Data release
    September 21st 2021: Test Submission due　-> 28th
    
    November 1st 2021: Challenge paper submission due
    January or February, 2022: Workshop

## Task definition
#### Task 1: Video QA dialog
    Goal: Answer generation without using manual descriptions for inference
    You can train models using manual descriptions but CANNOT use them for testing. 
    Video description capability needs to be embedded within the answer generation models.
    
    Data conditions:
    a. Use the provided video including audio and video features and localization information with answer reasoning, 
       the dialog history and manual video descriptions (scripts and summary) data for training for the Closed condition
        - text descriptions or scripts used by the actor to enact in the videos
        - summary generated by the questioners after holding 10 QAs.

    b. Publicly available external data and pre-trained models may also be used for training as a sub task for the Open condition

#### Task 2: Reasoning Video QA dialog
    Goal: Answer reasoning temporal Localization 

    To support answers, evidence is required to be shown without using manual descriptions. 
    For example, When a system generated answer is “A dog is barking.”, the sound of the dog’s barking and
    the dog must be grounded in the video as evidence.
    The localization of audiovisual evidence is required for each generated answer.
    To train reasoning localization, begin and end timing of the grounding/evidence will be additionally provided for the training data.

    Data conditions:
    Temporal localization information for answer reasoning is provided as begin and end timestamps showing evidence scenes
    a. Use the provided audio and video features with localization information with answer reasoning only for the Closed condition
    b. Any publicly available data and pre-trained models may also be used for training as a sub task for the Open condition
    
    
## Evaluation
    Likert scale by 5 humans + Similarity compared with single and multiple ground truths
    Intersection over Union (IoU) by comparing with “single” Evidence timing 

    
## Data Collection Method for Reasoning
![Data Collection for reasoning](https://github.com/dialogtekgeek/AVSD-DSTC10_Official/blob/main/InstructionForReasoning.png)

## Baseline system
The baseline system is based on Audio Visual Transformer for dialogue response sentence generation. <BR>
Information on gaining access to baseline is [HERE](https://github.com/ankitshah009/AVSD-DSTC10_baseline)
(Registration is required.)
  
    Output: 
    Answer generation considering dialog context 
    Evidence timing detection based on attention weights 
  
    Evaluation: 
    Validation data (1,787) was evaluated using “single” Answer and Evidence timing 
    Sentence similarity: BLEU, METEOR, CIDEr 
    Timing overlap: Intersection over Union (IoU)  
    Official evaluation: 
      - Likert scale by 5 humans 
      - Similarity compared with single and multiple ground truths 

    Additional Data:  
    Evidence timing for Training data (7,659) will be provided soon. 

### - Contact Information
#### Join the DSTC mailing list to get the latest updates about DSTC10
* To join the mailing list: visit https://groups.google.com/a/dstc.community/forum/#!forum/list/join
* To post a message: send your message to list@dstc.community
* To leave the mailing list: visit https://groups.google.com/a/dstc.community/forum/#!forum/list/unsubscribe

#### DSTC10 Task4 specific inquiries 
AVSD@DSTC10 Organizer: [Chiori Hori](mailto:chori@merl.com) & [Ankit Shah](mailto:aps1@andrew.cmu.edu)

### Task Organizers
Ankit Shah, Shijie Geng, Peng Gao, Anoop Cherian, Chiori Hori and Tim K. Marks
