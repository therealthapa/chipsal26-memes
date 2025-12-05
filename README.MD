# Shared Task on Multimodal Hate and Sentiment Understanding in Low-Resource Memes at CHiPSAL 2026

[Competition Link](https://www.google.com)

**Multimodal content moderation in low-resource languages**
This shared task focuses on multimodal content moderation in low-resource languages, with a particular emphasis on Nepali memes. The objective is to develop systems that can automatically determine whether a meme is hateful or not, as well as classify its sentiment into positive, negative, or neutral categories. The task will include six subtasks: (i) hate speech detection in Nepali-only memes, (ii) sentiment analysis in Nepali-only memes, (iii) hate speech detection in code-mixed Nepali memes, (iv) sentiment analysis in code-mixed Nepali memes, (v) hate speech detection in code-switched Nepali memes, and (vi) sentiment analysis in code-switched Nepali memes. The competition will be hosted on CodaLab. A dataset for this task has already been published in ICWSM 2025 (Thapa et al., 2025).

## Subtask A

**Hate Speech Detection in Nepali-only Memes:** The aim is to detect the presence of hate speech in monolingual Nepali memes. The dataset for this task will have binary labels: *Non-Hate* and *Hate*.

## Subtask B

**Sentiment Analysis in Nepali-only Memes:** The goal is to classify the sentiment of monolingual Nepali memes. The dataset will have three labels: *Negative*, *Neutral*, and *Positive*.

## Subtask C

**Hate Speech Detection in Code-Mixed Nepali Memes:** The aim is to detect the presence of hate speech in memes containing both Nepali and English text (code-mixed). The dataset for this task will have binary labels: *Non-Hate* and *Hate*.

## Subtask D

**Sentiment Analysis in Code-Mixed Nepali Memes:** The goal is to classify the sentiment of code-mixed Nepali-English memes. The dataset will have three labels: *Negative*, *Neutral*, and *Positive*.

## Subtask E

**Hate Speech Detection in Code-Switched Nepali Memes:** Similar to Subtask C, this task focuses on detecting hate speech in code-switched environments. The dataset will have binary labels: *Non-Hate* and *Hate*.

## Subtask F

**Sentiment Analysis in Code-Switched Nepali Memes:** Similar to Subtask D, this task focuses on sentiment classification in code-switched environments. The dataset will have three labels: *Negative*, *Neutral*, and *Positive*.

**To know more about the dataset**: please refer to the [dataset paper](https://ojs.aaai.org/index.php/ICWSM/article/download/35909/38063).

## Participation

Join our CodaLab competition [here](https://www.google.com).

## Dataset

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the submission format is mentioned below.

**Training Data**

  * Subtask A (Hate - Nepali): [Link Placeholder]
  * Subtask B (Sentiment - Nepali): [Link Placeholder]
  * Subtask C (Hate - Code-Mixed): [Link Placeholder]
  * Subtask D (Sentiment - Code-Mixed): [Link Placeholder]
  * Subtask E (Hate - Code-Switched): [Link Placeholder]
  * Subtask F (Sentiment - Code-Switched): [Link Placeholder]

**Evaluation Data (Without Labels)**

  * Subtask A: [Link Placeholder]
  * Subtask B: [Link Placeholder]
  * Subtask C: [Link Placeholder]
  * Subtask D: [Link Placeholder]
  * Subtask E: [Link Placeholder]
  * Subtask F: [Link Placeholder]

**Test Data**

  * Subtask A: [Link Placeholder]
  * Subtask B: [Link Placeholder]
  * Subtask C: [Link Placeholder]
  * Subtask D: [Link Placeholder]
  * Subtask E: [Link Placeholder]
  * Subtask F: [Link Placeholder]

## Instructions for OCR Extraction

If you want to extract OCR, you can use Google Vision API, Tesseract, EasyOCR, etc. In the benchmark paper (Thapa et al., 2025), Google Vision API was used to extract OCR for training the models. As many participants may not have access to the Vision API, we have provided the extracted text used in our benchmark paper.

Extracted Text for Train Data: [Link Placeholder]
Extracted Text for Evaluation Data: [Link Placeholder]

## Use of External Data

The use of external datasets is permitted. You should also mention your external data usage in your paper write-up. For code-mixed and low-resource settings, participants may find datasets like TamilMemes or Hindi code-mixed datasets useful for transfer learning experiments.

## Evaluation

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the script takes one prediction file as input. Your submission file must be a JSON file inside a zipped archive. To submit the files, name your JSON file `submission.json` and zip it with the file name `ref.zip`. Ensure that the zip does not have any sub-directories. The system only recognizes the first file in the zip folder.

IMPORTANT: Ensure that the index order in the submission file in JSON is in ascending order.

**Hate Speech Detection (Subtasks A, C, E)**

The Non-Hate label should be assigned '0', and the Hate label should be assigned '1'.

For example:

```python
{"index": "meme_20568.jpg", "prediction": 1}
{"index": "meme_30987.jpg", "prediction": 0}
{"index": "meme_45805.jpg", "prediction": 0}
```

**Sentiment Analysis (Subtasks B, D, F)**

The Negative label should be assigned '0', the Neutral label should be assigned '1', and the Positive label should be assigned '2'.

For example:

```python
{"index": "meme_20568.jpg", "prediction": 2}
{"index": "meme_30987.jpg", "prediction": 0}
{"index": "meme_45805.jpg", "prediction": 1}
```

For all Subtasks, the performance will be ranked by **F1-score** (Macro).

## Sample Code

Sample code and the baseline framework (MemeNePAL) used for this dataset are available at [GitHub Repository](https://github.com/therealthapa/chipsal26-memes).

## Publication

Participants in the Shared Task are expected to submit a paper to the CHiPSAL 2026 workshop. Submitting a paper is not mandatory to participate in the shared task. Papers must follow the workshop submission instructions and will undergo regular peer review. Their acceptance will not depend on the results obtained in the shared task but on the quality of the paper. All the accepted papers will be published in the ACL Anthology.

## Timeline of the Events

 * Start of the Competition: Dec 5, 2025
 * Eval Phase Start: Dec 5, 2025
 * Test Phase Start: Dec 20, 2025
 * Test Phase End: Feb 14, 2026
 * Paper Submission Deadline: Feb 20, 2026
 * Notification of acceptance: March 1, 2026
 * Camera Ready due: March 6, 2026


## Organizers

  * Surendrabikram Thapa (Virginia Tech, USA)
  * Siddhant Bikram Shah (Northeastern University, USA)
  * Hariram Veeramani (University of California Los Angeles, USA)
  * Liang Hu (DeepBlue Academy of Sciences, China)
  * Qi Zhang (Tongji University, China)
  * Wei Wang (Shenzhen MSU-BIT University, China)
  * Usman Naseem (Macquarie University, Australia)

## Contact

If there are any questions related to the competition, please contact the organizers at rauniyark11@gmail.com. Participants in this shared task are encouraged to reach out with any concerns or questions to any of the shared task organizers.

## References

  * Thapa, S., Veeramani, H., Hu, L., Zhang, Q., Wang, W., & Naseem, U. (2025). NeMeme: A Multimodal Prompt-based Framework for Analyzing Code-Mixed and Low-Resource Memes. In *Proceedings of the Nineteenth International AAAI Conference on Web and Social Media (ICWSM 2025)*.

