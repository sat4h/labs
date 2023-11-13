`Bilateral filtering on GPU`

![image](https://github.com/sat4h/labs/assets/146749026/58d94530-6748-4554-ac37-74f274e728ad)

![image](https://github.com/sat4h/labs/assets/146749026/e0ee5082-b054-4b4a-b59b-b45ea566ec77)

  2. Task definition
Given the image of size M×N, implement and apply a CUDA version of 9-point bilateral filter and store the
result to output image. Missing values for edge rows and columns are to be taken from nearest pixels. CUDA
implementation must make use of texture memory.
   3. Proposed method

The following method could be used to implement the bilateral filter:

1.Copy input data to device memory;

2.Bind input data to a texture link;

3.Extract each pixel together with its surrounding pixels via texture memory into 9-elements array;

4.Calculate the result pixel intensity using the formulas above;

5.Store the result into the array.

4.Implementation requirements

4.1. Input data

• Input grayscale image in BMP format, σ values;

4.2. Output data

• The time of image processing using GPU;
• The time of image processing using СPU;
• Resulting images in BMP format.

![image](https://github.com/sat4h/labs/assets/146749026/7118be51-b4c0-464f-a055-ffb4f5ffad22)

Лабораторная работа была выполнена в гугл коллаб. Выполнено на языке Python.

`1 Изображение `

![image](https://github.com/sat4h/labs/assets/146749026/6ad82b74-cdec-4324-9e0b-7565945176a3)
Размеры изображения:

Ширина: 1200, Высота: 600

Bilateral filtering on GPU

![image](https://github.com/sat4h/labs/assets/146749026/b7d3c7bd-18ee-4fee-9e50-033cfb1b92cc)
Время выполнения на GPU 0.04947

Bilateral filtering on CPU

![image](https://github.com/sat4h/labs/assets/146749026/c7ce6761-2893-4c73-904a-7226b73ec425)
Время выполнения на CPU 46.18258
Ускорение:  923.454347826087

`2 Изображение`

![image](https://github.com/sat4h/labs/assets/146749026/aa6125a0-d60a-490d-bd9f-b7a37d72e901)

Размеры изображения:

Ширина: 1600, Высота: 900

Bilateral filtering on GPU

![image](https://github.com/sat4h/labs/assets/146749026/1c71980c-7380-4467-887d-d11f73aa6869)

Время выполнения на GPU  0.10468

Bilateral filtering on СPU

![image](https://github.com/sat4h/labs/assets/146749026/1f36aea7-fb0c-4e35-a0af-86581f7693b2)

Время выполнения на CPU 89.73278

Ускорение: 857.2216037207269
