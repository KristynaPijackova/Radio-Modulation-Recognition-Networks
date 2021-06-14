# Radio Modulation Classification Using Deep Learning Architectures

---

**Author: Kristyna Pijackova**

---


This notebook contains code for my [bachelor thesis](https://www.vutbr.cz/studenti/zav-prace/detail/133594) in the academic year 2020/2021. 

**Abstract**

*The bachelor thesis is focused on radio modulation classification with a deep learningapproach. There are four deep learning architectures presented in the thesis. Three ofthem use convolutional and recurrent neural networks, and the fourth uses a transformerarchitecture. The final number of parameters of each model was considered during thedesign phase, as it can have a big impact on a memory footprint of a deployed model.The architectures were written in Keras, which is a software library, which provides a Python interface for neural networks. The results of the architectures were additionally compared to results from other research papers on this topic.*

---

**The code structure is following:**


*   **Imports** - Import needed libraries
*   **Defined Functions** - Functions defined for an easier manipulation with the data later on
*   **Accessing the datasets** - you may skip this part and download the datasets elsewhere if you please
*   **Loading Data** - Load the data and divide them into training, validation and test sets
*   **Deep Learning Part** -Contains the architectures, which are prepared to be trained and evaluated
*   **Load Trained Model** - Optionaly you can download the CGDNN model and see how it does on the corresponding dataset
*   **Layer Visualization** - A part of code which was written to visualize the activation maps of the convolutional and recurrent layers
*   **Plotting** - You can plot the confusion matrices in this part 

---
This code was used in Google Colab enviroment utilizing its free GPU. If you'd like to see how it works feel free to get a copy from the GitHub repository and experiment on your own.

---

## Dataset used in the thesis

### RadioML Datasets
*  O'shea, Timothy J., and Nathan West. "Radio machine learning dataset generation with gnu radio." Proceedings of the GNU Radio Conference. Vol. 1. No. 1. 2016.

* The datasets are available at:  https://www.deepsig.ai/datasets  

*  All datasets provided by Deepsig Inc. are licensed under the Creative Commons Attribution -  [NonCommercial - ShareAlike 4.0 License (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Both datasets are left unchanged, however, the RadioML2016.10b version is not stored as the original data, but is already splitted into X and labels

### Migou-Mod Dataset


*  Utrilla, Ramiro (2020), “MIGOU-MOD: A dataset of modulated radio signals acquired with MIGOU, a low-power IoT experimental platform”, Mendeley Data, V1, doi: 10.17632/fkwr8mzndr.1

* The dataset is available at:  https://data.mendeley.com/datasets/fkwr8mzndr/1 

*  The dataset is licensed under the Creative Commons Attribution -  [NonCommercial - ShareAlike 4.0 License (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

The following version of the dataset contain only a fraction of the original samples (550,000 samples compared to 8.8 million samples in the original dataset)

### VUT Dataset

This dataset was generated in MATLAB with 1000 samples per SNR value and each modulation type. It includes three QAM modulation schemes and further OFDM, GFDM, and FBMC modulations which are not included in previous datasets. To mimic the RadioML dataset, the data are represented as 2x128 vectors of I/Q signals in the SNR range from -20 dB to 18 dB.

## DL Architectures

### CNN

![CNN](https://github.com/KristynaPijackova/Radio-Modulation-Recognition-Networks/blob/main/Imgs/CNN_architecture.png)


### CLDNN

![CLDNN](https://github.com/KristynaPijackova/Radio-Modulation-Recognition-Networks/blob/main/Imgs/CLDNN_architecture.png)


### CGDNN

![CGDNN](https://github.com/KristynaPijackova/Radio-Modulation-Recognition-Networks/blob/main/Imgs/CGDNN_architecture.png)


### MCTransformer

![MCTransformer](https://github.com/KristynaPijackova/Radio-Modulation-Recognition-Networks/blob/main/Imgs/Transformer_short_architecture.png)



Source: <a id="1">[2]</a>

## Confusion Matrices - Examples of CNN and CLDNN Matrices

![CMs](https://user-images.githubusercontent.com/49315845/112479895-c0c8b080-8d75-11eb-82f3-263b2ce4ebd7.png)

Source: <a id="1">[1]</a>


## References
<a id="1">[1]</a> 
Pijackova, Kristyna, and Tomas Gotthans. "Radio Modulation Classification Using Deep Learning Architectures." 2021 31st International Conference Radioelektronika (RADIOELEKTRONIKA). IEEE, 2021.

<!-- <a id="1">[2]</a> Pijackova, Kristyna, "Evaluation of CNN and CLDNN architectures on Radio Mod-ulation Datasets" 2021 In Proceedings of the 27th Conference STUDENT EEICT2021, 4 p., ISBN: 978-80-214-5942-7 -->

<a id="1">[2]</a> Pijackova, Kristýna "Radio  Modulation  Recognition  Networks" Brno: Brno Univer-sity of Technology, Faculty of Electrical Engineering and Communication, Departmentof Radio Electronics, 2021, 61 p.  Bachelor’s Thesis.  Advised by doc.  Ing. Tomas Gotthans, Ph.D, [ONLINE]  https://www.vutbr.cz/studenti/zav-prace/detail/133594

If you end up using some of the architectures, please, consider citing one of the above mentioned works :)
