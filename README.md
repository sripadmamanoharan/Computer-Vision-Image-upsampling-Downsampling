# Computer-Vision-Image Upsampling-Downsampling

 
• Normalize a grayscale image such that its pixel intensities range between [0, 1].
• Implement a custom downsampling function to reduce the image size by half in both x and y
directions.
• Perform downsampling twice on the image ‘lena.png’ and compare the result with the original image in the same size, making low-resolution images visually larger.
• Perform upsampling by inserting an empty pixel between every adjacent pixel and repeat the process to get the image back to its original size. Analyze how the upsampled images look.

Analysis
Image Normalization
The image is normalized so that pixel values range between [0, 1]. This step ensures that the image is in a format suitable for further processing. Normalizing the image helps avoid intensity scaling issues, especially when applying filters or performing mathematical operations on the pixel values.

Downsampling
By reducing the image size through downsampling, we can see the effects of losing resolution. In each downsampling step, every other pixel is sampled, reducing the image’s size by half. After performing two rounds of downsampling, the image has significantly fewer pixels, resulting in a lower resolution. This process demonstrates how reducing resolution causes a loss of fine details, resulting in more prominent pixelation.

Upsampling
In the upsampling process, empty pixels are inserted between existing pixels to increase the image size back to its original resolution. Although upsampling restores the size, it does not bring back the details lost during downsampling. The result is a blurry and pixelated image, as the inserted pixels don’t carry meaningful information, leaving the image degraded compared to the original.

Comparison of Results
The downsampled images appear pixelated and lose sharpness due to the loss of resolution. While the upsampling restores the size, the blurring effect becomes more apparent due to the interpolated empty pixels. Once high-frequency details are lost in downsampling, they cannot be accurately recovered through simple upsampling.
Failure Cases
• Without appropriate padding during upsampling, edge artifacts may appear.
• Repeated downsampling and upsampling results in the loss of fine details, especially in areas with high-frequency or sharp edges.
