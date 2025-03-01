# DG-Hybrid
Discriminative/Generative joint approach for CNNs  

## Pixel distributions  
For every pixel position in the images of class 1 (e.g., all images labeled as the digit 1 in MNIST), you can form an empirical distribution by gathering the intensity value at that pixel across all samples. Consider the samples 'unrolled', then they are arrays. Thusly, pixel 1 of each image is in a distribution of values for that position, which captures how that pixel varies (or remains constant) across the class. Similarly for th 2nd pixel of each class, and so on. There are 784 distributions for each class, and we can then consider 'a distribution of distributions', of which there would be 10.  

## Alternative  
Alternatively, consider taking the average of pixel values for a given position across samples of a class. An image can be formed by using the 784 averages, and this can be used to find an initial mean and variance for each class. This can (but is not required to) be used in conjunction with the above mentioned approach.  

## 
The 784 pixel distributions for a given class may capture fine-grained variations, while the 'distribution of distributions' may cover top level information.