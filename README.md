# prostate_segmentation
Prostate Cancer segmentation and explainability decision support system

Segmentation using efficientnet.
Use a expert system to provide decision support based on segmented result.


Introduction 

Automated prostate cancer stratification has seen high-performing yet impractical solutions. While automating this diagnosis sector can help settle borderline classification decisions (e.g. a 3+4 tumor and its 4+3 counterpart contain minute, but critical differences), state-of-the-art solutions fail to address key aspects. Merely regurgitating a single Gleason leaves no room for doctors to assess confidence metrics and predict treatment paths. To combat these shortcomings, a four-pipeline deliverable GleasonNet was to achieve a 75% baseline Jaccard Distance with recall emphasis.

Protocol 

Four pipelines were created using pathologic data from Radboud and Karolinska Institutes. (1) A Preprocessing segment downpooled images to an accessible size and filtered an ISUP/Gleason CSV to Radboud. (2) The Semantic Segmentation Pipeline was trained to categorize 6 distinct pixel types. (3) The Prediction Pipeline was trained using Google Cloud TPU as a quantification mechanism from marked masks to corresponding ISUP. (4) A novel decision support algorithm was devised with a GU oncologist.

Discussion 

After relevant testing, the Semantic Segmentation Pipeline achieved an average IOU/Jaccard Distance (overlap between target/predicted mask) of 85%. Pipelines 3-4 (quantification of usable metrics) achieved validation accuracy and recall of both 79%. Using the oncologist-defined algorithm, “percentage involvement” was explainably calculated. A TPU helped overcome  computational complexity caused by dataset size. 

Not only does GleasonNet achieve competitive results; it enables vital aspects of explainability, confidence, and decision support. Large-scope implementation may serve to reduce missed early-onset precancerous lesions and resolve difficulties of borderline diagnoses.


