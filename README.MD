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

**To learn more about the dataset**: please refer to the [dataset paper](https://ojs.aaai.org/index.php/ICWSM/article/download/35909/38063).

## Participation

Join our Codabench competition here:

[Subtask A: Hate Speech Detection in Nepali-only Memes](https://www.codabench.org/competitions/12090/)
[Subtask B: Sentiment Analysis in Nepali-only Memes](https://www.codabench.org/competitions/12091/)

## Dataset

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the submission format is mentioned below.

| SubTask | Link |
|----------|----------|
| SubTask-A | [here](https://drive.google.com/drive/folders/1965Wf_dlQV5Z4Js8clQ66HQGr6BwV5sy?usp=sharing) |
| SubTask-B | [Link](https://drive.google.com/drive/folders/1y_pRejkzPIVtatbYwUl7vSs32-TUbHLp?usp=sharing) |

**Eval Data:**


| SubTask | Link |
|----------|----------|
| SubTask-A | [Link](https://drive.google.com/drive/folders/1EkUb1-sr52AEoNmXZSqcst9rMqDQKVXi?usp=sharing) | 
| SubTask-B | [Link](https://drive.google.com/drive/folders/1TI5e0tE8rvhk1i_fJAKO9MsOivSIx2Ny?usp=sharing) |


## OCR Extraction
Participants can use OCR extraction tools. We used [EasyOCR](https://github.com/JaidedAI/EasyOCR) in the project. [EasyOCR](https://github.com/JaidedAI/EasyOCR) is a simple and free tool for extracting text from images using Python. After installing it with pip, you create a reader that loads language models once, then call readtext() on an image to get detected words and their confidence scores. It supports multiple languages, including Nepali ('ne' argument in the function), works with file paths, NumPy arrays, or URLs, and can run on GPU or CPU. With just a few lines of code, you can perform OCR on scanned documents, signs, or screenshots and retrieve the text directly for further processing.

## Use of External Data

The use of external datasets is permitted. You should also mention your external data usage in your paper write-up. For code-mixed and low-resource settings, participants may find datasets like TamilMemes or Hindi code-mixed datasets useful for transfer learning experiments.

## Evaluation

All the images have a unique identifier called "index". The labels for training data are organized in the folder provided. For evaluation and testing, the script takes one prediction file as input. 

Your submission file must be a .csv file named ‘predictions.csv’ with columns 'index' and ‘label’. You must zip this file and submit the zipped archive file. Ensure that the zip does not have any sub-directories or any files besides the 'predictions.csv' file. The system only recognizes the first file in the zip folder. Ensure that the index order in the submission file is in ascending order. A sample submission file is available [here](https://github.com/therealthapa/chipsal26-memes/blob/main/sample_submission.csv).

| index | label |
|----------|----------|
|15001.jpg|	0|
|12345.jpg|	1|
|65102.jpg|	1|
|35231.jpg|	0|
|20524.jpg|	1|

**Hate Speech Detection (Subtask A)**

The Non-Hate label should be assigned '0', and the Hate label should be assigned '1'.

**Sentiment Analysis (Subtask B)**

The Negative label should be assigned '0', the Neutral label should be assigned '1', and the Positive label should be assigned '2'.

For all Subtasks, the performance will be ranked by **F1-score** (Macro).

## Sample Code

Sample code and the baseline framework (MemeNePAL) used for this dataset are available at our [GitHub Repository](https://github.com/therealthapa/chipsal26-memes).

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
* Shuvam Shiwakoti (Virginia Tech, USA)
* Siddhant Bikram Shah (Northeastern University, USA)
* Kritesh Rauniyar (Delhi Technological University, India)
* Surabhi Adhikari (Columbia University, USA)
* Kristina T. Johnson (Northeastern University, USA)
* Kengatharaiyer Sarveswaran (University of Jaffna, Sri Lanka)
* Bal Krishna Bal (Kathmandu University, Nepal)
* Usman Naseem (Macquarie University, Australia)

## Contact

If there are any questions related to the competition, please contact the organizers at rauniyark11@gmail.com. Participants in this shared task are encouraged to reach out with any concerns or questions to any of the shared task organizers.

## References

- *Thapa, S., Veeramani, H., Hu, L., Zhang, Q., Wang, W., & Naseem, U. (2025). NeMeme: A Multimodal Prompt-based Framework for Analyzing Code-Mixed and Low-Resource Memes. In *Proceedings of the Nineteenth International AAAI Conference on Web and Social Media (ICWSM 2025)*.
- *Thapa, S., Veeramani, H., Razzak, I., Lee, R. K. W., & Naseem, U. (2025, May). Cross Platform MultiModal Retrieval Augmented Distillation for Code-Switched Content Understanding. In Companion Proceedings of the ACM on Web Conference 2025 (pp. 2042-2051).*

