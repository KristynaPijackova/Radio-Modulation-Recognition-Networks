# Radio Modulation Classification Using Deep Learning Architectures

---

**Author: Kristyna Pijackova**

---

This notebook contains code, which is a part of solution for semestral thesis in the academic year 2020/2021. 

---

**This code contains 4 main parts:**


*   **Imports** - Import needed libraries, dataset and define some functions for later
*   **Data Pre-Processing**
*   **Deep Learning Part** - Architecture's design, training the designed models
*   **Results** - Evaluation of the Network, Graphs and Confusion Matrices

---
This code was used in Google Colab enviroment utilizing its free GPU. If you'd like to see how it works feel free to get a copy from the GitHub repository and experiment on your own.

---

## Dataset

The dataset has an open-source licension and is avaible at this page [DEEPSIG Dataset](https://www.deepsig.ai/datasets), which is provided open source under the Create Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) Licence https://creativecommons.org/licenses/by-nc/4.0/ 

The version **RadioML2016.10b** contains 10 different modulation types stored as I/Q data in the form of a 128x2 vectors with signal-to-noise ratio in the range from -20 to 18 dB. 

Note: !wget commands won't work anymore on downloading the dataset as deepsig.ai was forced to screen http requests due abuse issues. The downloading now requests registration and email verification before downloading.

## DL Architectures

### CNN

![CNN](https://user-images.githubusercontent.com/49315845/112479656-8bbc5e00-8d75-11eb-9adf-b9d33bb255de.png)

Source: <a id="1">[2]</a> 

### CLDNN

![CLDNN](https://user-images.githubusercontent.com/49315845/112479402-4bf57680-8d75-11eb-91de-5b231dff0609.png)

Source: <a id="1">[2]</a>

## Confusion Matrices 

![CMs](https://user-images.githubusercontent.com/49315845/112479895-c0c8b080-8d75-11eb-82f3-263b2ce4ebd7.png)

Source: <a id="1">[1]</a>

## References
<a id="1">[1]</a> 
K. Pijackova, T. Gotthans, “Radio Modulation Classification Using Deep Learning Architectures,” 2021 31st International Conference Radioelektronika (RADIOELEKTRONIKA), Brno,
Czech Republic, 2021

<a id="1">[2]</a> K.Pijackova, “Evaluation of CNN and CLDNN architectures on radio modulation datasets,“ 27th Conference STUDENT EEICT 2019. Brno: Vysoké učení technické v Brně, Fakulta elektrotechniky a komunikačních technologií, 2021
