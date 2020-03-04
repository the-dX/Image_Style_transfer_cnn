# Image_Style_transfer_cnn

5.1 Workflow
5. DESIGN METHODOLOGY
Following is the methodology involved for the real-life implementation of the project[5][6]:
1. Take an input image (image in which style is to be applied).
2. Take a style image (image’s style is to be applied to the previous image).
3. Resize them into the same size and shape.
4. Load a Convolutional Neural Network (CNN).
5. Distinguish between the layers that represent the style (basic shapes, colour etc.), and content (image specific features) of the images respectively and separate them.
6. Implement A Neural Algorithm of Artistic Style to extract and store the content and style representations and then transfer the style of the second image onto the first one.
7. Also calculate and optimize content loss (because content is to be preserved), style loss (because style has to be transferred), and total variation loss (because output image has to be de-noised).
The project uses the Iterative Waterfall Model for software development because it is a small project and there’s no uncertainty of requirements, Also, its sequential design process which leads to no overlapping of different phases which ensures proper departmentalization and control.[4]
The illustration below shows the different phases of the Waterfall Model:
1. Start with VGG with average pooling (they saw better gradient flow compared to max pooling).
2. Take a content image, a style image, and a target image initialized to random pixel values.
3. Define a content loss (MSE of the feature activations for the content image and the target image)
4. And a style loss (MSE of the Gram matrices of the style image and the target image).
5. Run SGD, optimizing a linear combination of the losses by modifying the pixel values of the target image.
