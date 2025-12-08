# Shared Task on Multimodal Hate and Sentiment Understanding in Low-Resource Memes at CHiPSAL 2026

Competition Links:

[Subtask A: Hate Speech Detection in Nepali-only Memes](https://www.codabench.org/competitions/12090/)

[Subtask B: Sentiment Analysis in Nepali-only Memes](https://www.codabench.org/competitions/12091/)

**Multimodal content moderation in low-resource languages**

This shared task focuses on multimodal content moderation in low-resource languages, with a particular emphasis on Nepali memes. The objective is to develop systems that can automatically determine whether a meme is hateful or not, as well as classify its sentiment into positive, negative, or neutral categories. The task will include two subtasks: (i) hate speech detection in Nepali-only memes and (ii) sentiment analysis in Nepali-only memes. The competition will be hosted on Codabench. A dataset for this task has already been published in ICWSM 2025 (Thapa et al., 2025).

## Subtask A

**Hate Speech Detection in Nepali-only Memes:** The aim is to detect the presence of hate speech in monolingual Nepali memes. The dataset for this task will have binary labels: *Non-Hate* and *Hate*.

## Subtask B

**Sentiment Analysis in Nepali-only Memes:** The goal is to classify the sentiment of monolingual Nepali memes. The dataset will have three labels: *Negative*, *Neutral*, and *Positive*.

**To know more about the dataset**: please refer to the [dataset paper](https://ojs.aaai.org/index.php/ICWSM/article/download/35909/38063).

## Participation

Join our Codabench competition here:

[Subtask A: Hate Speech Detection in Nepali-only Memes](https://www.codabench.org/competitions/12090/)
[Subtask B: Sentiment Analysis in Nepali-only Memes](https://www.codabench.org/competitions/12091/)

## Dataset

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the submission format is mentioned below.

**Subtask A**

  * [Training Data](https://drive.google.com/drive/folders/1965Wf_dlQV5Z4Js8clQ66HQGr6BwV5sy?usp=drive_link)
  * [Evaluation Data (Without Labels)](https://drive.google.com/drive/folders/1IYyaBb9Skj6iG6EXZhMl1LzkPt953u1g?usp=drive_link)
  * [Test Data](https://drive.google.com/drive/folders/1CDYZn0wEitU7ZS8bLShHx1gCJ78i1h56?usp=drive_link)

**Subtask B**

  * [Training Data](https://drive.google.com/drive/folders/1y_pRejkzPIVtatbYwUl7vSs32-TUbHLp?usp=drive_link)
  * [Evaluation Data (Without Labels)](https://drive.google.com/drive/folders/1zUyIjCJq9K6CoqM7HZDgs14nagU96Hyp?usp=drive_link)
  * [Test Data](https://drive.google.com/drive/folders/1RgLzy3tkZ9HVk296kVpZzO79svvTaUzr?usp=drive_link)

## Instructions for OCR Extraction

If you want to extract OCR, you can use Google Vision API, Tesseract, EasyOCR, etc. In the benchmark paper (Thapa et al., 2025), Google Vision API was used to extract OCR for training the models. As many participants may not have access to the Vision API, we have provided the extracted text used in our benchmark paper.

Extracted Text for Train Data: [Link Placeholder]
Extracted Text for Evaluation Data: [Link Placeholder]

## Use of External Data

The use of external datasets is permitted. You should also mention your external data usage in your paper write-up. For code-mixed and low-resource settings, participants may find datasets like TamilMemes or Hindi code-mixed datasets useful for transfer learning experiments.

## Evaluation

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the script takes one prediction file as input. 

Your submission file must be a .csv file named ‘predictions.csv’ with columns 'index' and ‘label’. You must zip this file and submit the zipped archive file. Ensure that the zip does not have any sub-directories or any files besides the 'predictions.csv' file. The system only recognizes the first file in the zip folder. Ensure that the index order in the submission file is in ascending order.

**Hate Speech Detection (Subtask A)**

The Non-Hate label should be assigned '0', and the Hate label should be assigned '1'.

**Sentiment Analysis (Subtask B)**

The Negative label should be assigned '0', the Neutral label should be assigned '1', and the Positive label should be assigned '2'.

For all Subtasks, the performance will be ranked by **F1-score** (Macro).

## Sample Code

Sample code and the baseline framework (MemeNePAL) used for this dataset are available at [GitHub Repository](https://github.com/therealthapa/chipsal26-memes).

## Publication

Participants in the Shared Task are expected to submit a paper to the CHiPSAL 2026 workshop. Submitting a paper is not mandatory to participate in the shared task. Papers must follow the workshop submission instructions and will undergo regular peer review. Their acceptance will not depend on the results obtained in the shared task but on the quality of the paper. All the accepted papers will be published in LREC's workshop proceedings.

## Timeline of the Events

 * Start of the Competition: Dec 8, 2025
 * Eval Phase Start: Dec 8, 2025
 * Test Phase Start: Dec 25, 2025
 * Test Phase End: Feb 14, 2026
 * Paper Submission Deadline: Feb 20, 2026
 * Notification of acceptance: March 20, 2026
 * Camera Ready due: March 30, 2026


## Organizers

  * Surendrabikram Thapa (Virginia Tech, USA)
  * Kritesh Rauniyar (Macquarie University, Australia)
  * Shuvam Shiwakoti (Virginia Tech, USA)
  * Siddhant Bikram Shah (Northeastern University, USA)
  * Kristina T. Johnson (Northeastern University, USA)
  

## Contact

If there are any questions related to the competition, please contact the organizers at rauniyark11@gmail.com. Participants in this shared task are encouraged to reach out with any concerns or questions to any of the shared task organizers.

## References

  * Thapa, S., Veeramani, H., Hu, L., Zhang, Q., Wang, W., & Naseem, U. (2025). NeMeme: A Multimodal Prompt-based Framework for Analyzing Code-Mixed and Low-Resource Memes. In *Proceedings of the Nineteenth International AAAI Conference on Web and Social Media (ICWSM 2025)*.

