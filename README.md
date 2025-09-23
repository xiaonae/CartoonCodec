# CartoonCodec

## 1. Abstract

The rapid growth of video-based social applications has intensified the demand for efficient video transmission and personalized cartoon-style customization. Existing solutions typically apply talking face video codecs followed by cartoon-style control algorithms. However, the paradigm often leads to unsatisfactory compression performance and increased inference latency.
To address these limitations, we propose CartoonCodec, a novel generative framework that unifies face video coding and cartoon-style control into an end-to-end process. Our framework encodes facial video sequences into compact motion feature representations, which are then compressed and transmitted alongside text prompts to achieve low-bitrate communication. To embed control into the coding process while ensuring efficient compression, a text-guided adaptive layer selection mechanism relying on compact facial representations is introduced to dynamically select and optimize the most influential layers in the generators.  In addition, a self-supervised domain adaptation training strategy is proposed to construct both multimodal and unimodal data pairs for the computation of diverse loss functions. This enables domain adaptation across the decoupled space.
Extensive experimental results show that CartoonCodec outperforms baselines in compression efficiency across video reconstruction and cartoon-style control tasks while achieving the fastest encoding and decoding speeds. CartoonCodec provides key insights for advancing real-time face video communication with cartoon-style customization. 

## 2. Visual Comparisons on the Video Reconstruction and Cartoon-Style Control Tasks  (Similar Bitrate)

### 2.1 Visual Comparisons on the Video Reconstruction Task  (Similar Bitrate)

To assess subjective quality in video reconstruction, we conduct comparisons between our proposed CartoonCodec scheme, the latest hybrid video coding standard (VVC), and four generative compression schemes (FOMM, FV2V, CFTE, and CTTR) at similar bit rates. For clearer observation of the experimental results, the corresponding videos are provided in downloadable mp4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/dbd560be-8356-44a0-8dba-3dcd397406fd)](https://github.com/user-attachments/assets/dbd560be-8356-44a0-8dba-3dcd397406fd)

### 2.2 Visual Comparisons on the Cartoon-Style Control Task  (Similar Bitrate)

To assess subjective quality in video reconstruction, we conduct comparisons between our proposed CartoonCodec scheme, the latest hybrid video coding standard (VVC), and four generative compression schemes (FOMM, FV2V, CFTE, and CTTR) at similar bit rates. For clearer observation of the experimental results, the corresponding videos are provided in downloadable mp4 format.

Visual comparison among VVC+DiffCLIP~\cite{bross2021overview,kim2022diffusionclip}, VVC+NADA~\cite{bross2021overview,gal2022stylegan}, VVC+DeltaEdit~\cite{bross2021overview,lyu2023deltaedit}, VVC+FRESCO~\cite{bross2021overview,yang2024fresco}, and CartoonCodec (Ours) on the cartoon-style control task at similar bit rates. Note that, as stated in Section V-B of the initial manuscript, the cartoon-style control task includes five cases: Pixar, Disney Princess, Sketch, Zombie, and Anime Painting.

Disney Princess

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/07dc3be0-95d9-456f-9008-55a1ec6e45c8)](https://github.com/user-attachments/assets/07dc3be0-95d9-456f-9008-55a1ec6e45c8)

Pixar

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/39e7cf71-83b5-4759-bce2-0f530866f4c7)](https://github.com/user-attachments/assets/39e7cf71-83b5-4759-bce2-0f530866f4c7)

Sketch

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/ca7cf5fd-257e-4765-8d7c-5775b96544f4)](https://github.com/user-attachments/assets/ca7cf5fd-257e-4765-8d7c-5775b96544f4)

Zombie

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/28a2c243-ffd4-4ae0-9f39-d17022565eb6)](https://github.com/user-attachments/assets/28a2c243-ffd4-4ae0-9f39-d17022565eb6)

Anime Painting

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/173620ab-4d8d-4457-a4c1-e020055b4610)](https://github.com/user-attachments/assets/173620ab-4d8d-4457-a4c1-e020055b4610)








