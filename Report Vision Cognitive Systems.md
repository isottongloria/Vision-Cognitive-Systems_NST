**Introduction** 

Neural style transfer is an artificial system based on a Deep Neural Network that creates artistic images of high perceptual quality. Starting with two images, a content image, and a style image, this algorithm creates a new picture that combines the content of the content image with the style of the style image. While the global arrangement of the original photograph is preserved, the colors and local structures that compose the overall scenery are provided by the artwork. 
The system uses neural representations of the fed images (feature maps) to separate and recombine the content and style of pictures.

The importance of this study is to take a step closer to an algorithmic comprehension of the mechanisms underlying human creation and perception of artistic imagery.
aggiungere altro sulle impliazioni biologiche ?? tipo:
*`The style representations simply compute the correlations between*`
`*different types of neurons in the network. Extracting correlations between neurons is a biologically plausible computation that is, for example, implemented by so-called complex cells in the primary visual system (V1).21 Our results suggest that performing a complex-cell like computation at different processing stages along the ventral stream would be a possible way to obtain a content-independent representation of the appearance of a visual input.All in all it is truly fascinating that a neural system, which is trained to perform one of the*`
`*core computational tasks of biological vision, automatically learns image representations that*`
`*allow the separation of image content from style. The explanation could be that when learning*`
`*object recognition, the network has to become invariant to all image variation that preserves*`
`*object identity. Representations that factorise the variation in the content of an image and the*`
`*variation in its appearance would be extremely practical for this task. Thus, our ability to*`
`*abstract content from style and therefore our ability to create and enjoy art might be primarily a*`
`*preeminent signature of the powerful inference capabilities of our visual system.*`


Add the main results ... 


**Related Work**
==Since the mid-1990s, the  art theories behind the appealing artworks have been attracting  interest not only among artists but also among numerous researchers in the field of computer science. A plethora of studies and methodologies have emerged, exploring how to automatically turn images into synthetic artworks== [@article{article,
author = {Jing, Yongcheng and Yang, Yezhou and Feng, Zunlei and Ye, Jingwen and Yu, Yizhou and Song, Mingli},
year = {2020},
month = {11},
pages = {3365-3385},
title = {Neural Style Transfer: A Review},
volume = {26},
journal = {IEEE Transactions on Visualization and Computer Graphics},
doi = {10.1109/TVCG.2019.2921336}
}].

==Within the computer vision community, style transfer is usually studied as a generalised problem of texture synthesis, which is to extract and transfer the texture from the source to target== [[5] A. A. Efros and W. T. Freeman, “Image quilting for texture
synthesis and transfer,” in Proceedings of the 28th annual conference
on Computer graphics and interactive techniques. ACM, 2001, pp.
341–346.
[6] I. Drori, D. Cohen-Or, and H. Yeshurun, “Example-based style
synthesis,” in Proceedings of the IEEE Conference on Computer Vision
and Pattern Recognition, vol. 2. IEEE, 2003, pp. II–143.
[7] O. Frigo, N. Sabater, J. Delon, and P. Hellier, “Split and match:
Example-based adaptive patch sampling for unsupervised style
transfer,” in Proceedings of the IEEE Conference on Computer Vision
and Pattern Recognition, 2016, pp. 553–561.
[8] M. Elad and P. Milanfar, “Style transfer via texture synthesis,”
IEEE Transactions on Image Processing, vol. 26, no. 5, pp. 2338–
2351, 2017.]]

==In the late 2000's Hertzmann and colleagues ==[@article{article,
author = {Hertzmann, Aaron and Jacobs, Charles and Oliver, Nuria and Curless, Brian and Salesin, David},
year = {2001},
month = {06},
pages = {},
title = {Image Analogies},
volume = {2001},
journal = {Proceedings of ACM SIGGRAPH},
doi = {10.1145/383259.383295}
}] ==introduced a framework called "image analogies" to execute a generalized style transfer, acquiring knowledge from analogous transformations observed in pairs of unstylized and stylized images. Nevertheless, a shared constraint among these approaches is their reliance on low-level image features, frequently resulting in inadequate capture of image structures.==

==In recent times, drawing inspiration from the power of Convolutional Neural Networks (CNNs), Gatys and collaborators [10] first studied how to  employ a CNN forn creating artistic imagery by separating and recombining image content and style. This work is usually regarded as a gold standard in style transfer algorithms. 
The application of CNNs to transform a content image into diverse styles, commonly referred to as Neural Style Transfer (NST), has gained significant prominence over time in both academic discourse and industrial applications, attracting growing interest. Numerous approaches have been put forth to enhance or broaden the original NST algorithm.

Previous work on separating content from style was evaluated on sensory inputs of much lesser complexity, such as characters in different handwriting or images of faces or small figures in different poses.12, 13 

In our demonstration, we render a given photograph in the style of a range of well-known
artworks. This problem is usually approached in a branch of computer vision called non-
photorealistic rendering (for recent review see14). Conceptually most closely related are methods using texture transfer to achieve artistic style transfer.15–19 However, these previous approaches mainly rely on non-parametric techniques to directly manipulate the pixel representation of an image. 

In contrast, by using Deep Neural Networks trained on object recognition, we carry out manipulations in feature spaces that explicitly represent the high level content of an image.



**Dataset** 

In this particular scenario, the need for an extensive training set is avoided, as we leverage the pre-trained VGGNet19, which has been trained on ImageNet. Therefore, there is no substantial training involved for this neural network; rather, the emphasis lies in refining the initialized image.

For our experiments, we considered a total of ** style images and ** content images, sourcing them from rawpixels.com. A selection of these images will be showcased in the analysis section.The following provides illustrative glimpses of both the content and style images that were curated for this purpose.

Before subjecting these images to the model, it is important to undergo a preprocessing stage. This involved converting the images into the appropriate tensor format to ensure compatibility with deep learning models. Additionally, image dimensions were standardized to facilitate efficient computation of the loss function during the subsequent training phase. 



**Method**

















**Further improvements**

evaluation method : In our experiment, each stylised
image is rated by 8 different raters (4 males and 4 females)
with the same occupation and age. As depicted in Figure 13,
given the same stylised result, different observers with the
same occupation and age still have quite different ratings.
Nevertheless, there is currently no gold standard evaluation
method for assessing NPR and NST algorithms. This chal-
lenge of aesthetic evaluation will continue to be an open
question in both NPR and NST communities, the solution
of which might require the collaboration with professional
artists and the efforts in the identification of underlying
aesthetic principles.
