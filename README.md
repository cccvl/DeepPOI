# DeepROI
A deep fake dataset for special person

The dataset is introduced in the submitted paper "Spatial-temporal transformer network for protecting person-of-interest from deepfake".

To ensure the diversity of the synthesized videos, we use three different methods including face swapping (SimSwap \cite{bib52}), lip-syncing (Wav2lip \cite{bib53}), and facial reenactment (FOMM \cite{bib54}) to create our dataset DeepPOI. For the real videos, we manually downloaded publicly available speeches of the POIs from the internet and standardized their length to 300 frames. We use MTCNN \cite{bib51} to crop the facial regions of POIs to facilitate the generation of fake videos.

For face swap deepfakes, we use the real videos from the FF++ dataset as the source to swap the POIs with the faces in these videos. For lip-sync deepfakes, we collect audio data from YouTube as the driver and synchronize the POI's lips with these reference voices. For facial reenactment deepfakes, the real videos in FF++ are used to drive the facial movements of the POI.

We compare our dataset with publicly available deepfake datasets, such as the FF++ dataset \cite{bib45}, DFDC dataset \cite{bib46}, Celeb-DF dataset \cite{bib47}, WildDeepfake dataset \cite{bib48}, DF TIMIT dataset \cite{bib49}, and DeeperForensics-1.0 dataset \cite{bib50}. In Tables~\ref{tab2} and~\ref{tab3}, we provide an overview of the fundamental details of these datasets and our dataset. Our dataset is unique in that it focuses specifically on POIs, and each video set comprises multiple types of deepfakes generated using different techniques.
|                                 | \multicolumn{2}{c@{}}{Real} | \multicolumn{2}{c@{}}{Fake} |
|---------------------------------|-----------------------------|-----------------------------|
| Dataset                         | Video                       | Frame                       | Video  | Frame     |
| DF-TIMIT\cite{bib49}            | 320                         | 34.0k                       | 320    | 34.0k     |
| FF++\cite{bib45}                | 1,000                       | 509.9k                      | 4,000  | 1,830.1k  |
| DFDC\cite{bib46}                | 1,131                       | 488.4k                      | 4,113  | 1783.3k   |
| Celeb-DF\cite{bib47}            | 590                         | 225.4k                      | 5,639  | 21,116.8k |
| WildDeepfake\cite{bib48}        | 3,805                       | 440.5k                      | 3,509  | 739.6k    |
| DeeperForensics-1.0\cite{bib50} | 50,000                      | 14,667k                     | 10,000 | 2,933k    |
| DeepPOI(Ours)                   | 27,000                      | 8,100k                      | 36,873 | 11,061.9k |



    
|         |          | \multicolumn{4}{c}{Fake} |
|---------|----------|--------------------------|--------------------|----------|----------|
| POI     | Real     | face swap                | facial reenactment | lip-sync | {Total}  |
| Putin   | 3,000    | 1,765                    | 1,054              | 1,206    | {7,025}  |
| Obama   | 6,000    | 2,466                    | 2,709              | 3,058    | {14,233} |
| Hillary | 6,000    | 2,289                    | 2,734              | 2,688    | {13,711} |
| Biden   | 6,000    | 2,423                    | 3,089              | 3,354    | {14,866} |
| Trump   | 6,000    | 2,367                    | 2,895              | 2,776    | {14,038} |
| {Total} | {27,000} | {11,310}                 | {12,481}           | {13,082} | {63,873} |
