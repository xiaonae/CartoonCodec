# CartoonCodec: Generative Talking Face Video Coding with Cartoon-Style Customization

## 1. Abstract

The rapid growth of video-based social applications has intensified the demand for efficient transmission and personalized cartoon-style customization. Existing solutions typically apply talking face video and text codecs, followed by cartoon-style control algorithms, which often result in unsatisfactory compression performance and high inference latency. In this paper, we propose CartoonCodec, an efficient generative framework that unifies face video coding and cartoon-style control into an end-to-end process. Our framework encodes facial video sequences into compact motion feature representations, which are transmitted together with compressed text prompts. To integrate control into the coding process while ensuring efficient compression, a text-guided adaptive layer selection mechanism relying on the compact representations is introduced to dynamically select and optimize the most influential layers in the generators. Furthermore, to facilitate adaptation to cartoon-style domains across the decoupled spaces, we propose a self-supervised domain adaptation strategy that constructs both multimodal and unimodal data pairs, enabling the use of diverse loss functions. Extensive experiments demonstrate that CartoonCodec outperforms baselines in compression efficiency for video reconstruction and cartoon-style control tasks while maintaining competitive inference efficiency. CartoonCodec provides key insights for advancing face video communication with cartoon-style customization.

## 2. Visual Comparisons on the Video Reconstruction and Cartoon-Style Control Tasks  (Similar Bit rates)

### 2.1 Visual Comparisons on the Video Reconstruction Task  (Similar Bit Rates)

To assess subjective quality in video reconstruction, we conduct comparisons between our proposed CartoonCodec scheme, the latest hybrid video coding standard (VVC), and four generative compression schemes (FOMM, FV2V, CFTE, and CTTR) at similar bit rates. For clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/eb4b915a-6d00-41fa-bfe7-9989a007616c)](https://github.com/user-attachments/assets/eb4b915a-6d00-41fa-bfe7-9989a007616c)


### 2.2 Visual Comparisons on the Cartoon-Style Control Task  (Similar Bit Rates)

To assess subjective quality in Cartoon-Style Control, we conduct comparisons between our proposed CartoonCodec scheme, VVC+DiffCLIP, VVC+NADA, VVC+DeltaEdit, and VVC+FRESCO at similar bit rates. Note that the cartoon-style control task includes five cases: Disney Princess, Pixar, Sketch, Zombie, and Anime Painting. For clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

#### Pixar Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/7db62fdf-8b01-4eca-9082-460d289872ac)](https://github.com/user-attachments/assets/7db62fdf-8b01-4eca-9082-460d289872ac)

#### Sketch Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/746051e4-6379-420e-82c9-f8148c9ffa9d)](https://github.com/user-attachments/assets/746051e4-6379-420e-82c9-f8148c9ffa9d)

#### Zombie Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/167aa752-aa88-448e-b0b4-752edbab766f)](https://github.com/user-attachments/assets/167aa752-aa88-448e-b0b4-752edbab766f)

#### Anime Painting Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/173620ab-4d8d-4457-a4c1-e020055b4610)](https://github.com/user-attachments/assets/173620ab-4d8d-4457-a4c1-e020055b4610)

## 3. Visual results on the VoxCeleb testing dataset (Similar Bit Rates)

To assess our CartoonCodec scheme in more realistic scenarios, we selected testing sequences from the VoxCeleb dataset, an in-the-wild dataset that naturally includes complex background conditions. Specifically, we compare our CartoonCodec with VVC on the video reconstruction task at similar bit rates. In addition, we evaluate our CartoonCodec on the cartoon-style control task at similar bit rates. To facilitate clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/6270b9ee-d3b6-4712-ae28-e669cbc68648)](https://github.com/user-attachments/assets/6270b9ee-d3b6-4712-ae28-e669cbc68648)

## 4. Video demonstration of our CartoonCodec’s runtime performance

We provide a demonstration video of our CartoonCodec running on an NVIDIA A40 GPU with 48 GB of memory, showcasing the measurement process of encoding and decoding time of CartoonCodec. The video is available for download at https://github.com/xiaonae/CartoonCodec/releases/download/V1/A40_latest.mp4. The video includes the encoding and decoding of 10 testing sequences (108 frames each). The average encoding and decoding time per video is presented, which is consistent with the results in Table III of our response letter. That is, the total runtime on the encoding side is 5.86734 s, and the total runtime on the decoding side is 3.09567 s. In addition, three decompressed videos are randomly selected for playback. For this demonstration, Pixar is used as the target cartoon style. 

## 5. Visual results of our CartoonCodec on the cartoon-style control task (Fig. 10 of the initial manuscript)

To facilitate clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/2b86f149-3054-4f40-a83c-42c60dc46b0b)](https://github.com/user-attachments/assets/2b86f149-3054-4f40-a83c-42c60dc46b0b)

## 6. Visual results of the Ablation study (Fig. 11 of the initial manuscript)

To analyze (1) the visual examples of three variants of our CartoonCodec scheme and (2) the disentangled poses and expressions of these variants on the Pixar control case, we present the following results. For clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/bb4d0a57-627b-4d36-968e-2bdce0d6a2d3)](https://github.com/user-attachments/assets/bb4d0a57-627b-4d36-968e-2bdce0d6a2d3)




