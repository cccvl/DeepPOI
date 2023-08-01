# DeepPOI
A deep fake dataset for particular person

The dataset is introduced in the submitted paper "Spatial-temporal transformer network for protecting person-of-interest from deepfake".

To ensure the diversity of the synthesized videos, we use three different methods including face swapping (SimSwap, lip-syncing (Wav2lip ), and facial reenactment (FOMM ) to create our dataset DeepPOI. For the real videos, we manually downloaded publicly available speeches of the POIs from the internet and standardized their length to 300 frames. We use MTCNN to crop the facial regions of POIs to facilitate the generation of fake videos.

For face swap deepfakes, we use the real videos from the FF++ dataset as the source to swap the POIs with the faces in these videos. For lip-sync deepfakes, we collect audio data from YouTube as the driver and synchronize the POI's lips with these reference voices. For facial reenactment deepfakes, the real videos in FF++ are used to drive the facial movements of the POI.

We compare our dataset with publicly available deepfake datasets, such as the FF++ dataset, DFDC dataset, Celeb-DF dataset, WildDeepfake dataset, DF TIMIT dataset, and DeeperForensics-1.0 dataset . In Table 1 and Table 2, we provide an overview of the fundamental details of these datasets and our dataset. Our dataset is unique in that it focuses specifically on POIs, and each video set comprises multiple types of deepfakes generated using different techniques.

Table 1 Comparison of our dataset with existing deepfake datasets
<table>
    <tr>
        <td></td>
        <td colspan="2">Real</td>
        <td colspan="2">Fake</td>        
    </tr>
    <tr>
        <td>Dataset</td>
        <td>Video</td>
        <td>Frame</td>
        <td>Video</td>
        <td>Frame</td>
    </tr>
    <tr>
        <td>DF-TIMIT</td>
        <td>320</td>
        <td>34.0k</td>
        <td>320</td>
        <td>34.0k</td>
    </tr>
    <tr>
        <td>FF++</td>
        <td>1,000</td>
        <td>509.9k</td>
        <td>4,000</td>
        <td>1,830.1k</td>
    </tr>
    <tr>
        <td>DFDC</td>
        <td>1,131</td>
        <td>488.4k</td>
        <td>4,113</td>
        <td>1783.3k</td>
    </tr>
    <tr>
        <td>Celeb-DF</td>
        <td>590</td>
        <td>225.4k</td>
        <td>5,639</td>
        <td>21,116.8k</td>
    </tr>
    <tr>
        <td>WildDeepfake</td>
        <td>3,805</td>
        <td>440.5k</td>
        <td>3,509</td>
        <td>739.6k</td>
    </tr>
    <tr>
        <td>DeeperForensics-1.0</td>
        <td>50,000</td>
        <td>14,667k</td>
        <td>10,000</td>
        <td>2,933k</td>
    </tr>
    <tr>
        <td>DeepPOI(Ours)</td>
        <td>27,000</td>
        <td>8,100k</td>
        <td>36,873</td>
        <td>11,061.9k</td>
    </tr>
</table>

Table 2 Total number of videos per POI in DeepPOI
<table>
    <tr>
        <td></td>
        <td></td>        
        <td colspan="3">Fake</td>     
    </tr>
    <tr>
        <td>POI</td>
        <td>Real</td>
        <td>face swap</td>
        <td>facial reenactment</td>
        <td>lip-sync</td>
        <td>Total</td>
    </tr>
    <tr>
        <td>Putin</td>
        <td>3,000</td>
        <td>1,765</td>
        <td>1,054</td>
        <td>1,206</td>
        <td>7,025</td>
    </tr>
    <tr>
        <td>Obama</td>
        <td>6,000</td>
        <td>2,466</td>
        <td>2,709</td>
        <td>3,058</td>
        <td>14,233</td>
    </tr>
    <tr>
        <td>Hillary</td>
        <td>6,000</td>
        <td>2,289</td>
        <td>2,734</td>
        <td>2,688</td>
        <td>13,711</td>
    </tr>
    <tr>
        <td>Biden</td>
        <td>6,000</td>
        <td>2,423</td>
        <td>3,089</td>
        <td>3,354</td>
        <td>14,866</td>
    </tr>
    <tr>
        <td>Trump</td>
        <td>6,000</td>
        <td>2,367</td>
        <td>2,895</td>
        <td>2,776</td>
        <td>14,038</td>
    </tr>
    <tr>
        <td>Total</td>
        <td>27,000</td>
        <td>11,310</td>
        <td>12,481</td>
        <td>13,082</td>
        <td>63,873</td>
    </tr>
</table>

Download DeepPOI from https://pan.baidu.com/s/1NziUZPEmG98nB3_OhMx7ig with code:lgg8 
