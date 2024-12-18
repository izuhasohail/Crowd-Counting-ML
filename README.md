# Deep Learning-Based Crowd Analysis System for Social Distance Monitoring

By: Zuha Sohail

## Project Overview

Crowd Counting is an advanced computer vision technique that automatically determines the number of objects in an image. This project focuses on developing a robust crowd counting system specifically for monitoring physical distancing in indoor spaces.

## Real-World Impact & Applications

The applications of crowd counting span across multiple industries:

### Healthcare & Research

- Track the spread of infectious diseases through cell/pathogen counting
- Monitor growth rates in biological samples
- Optimize dosage calculations based on cell counts

### Public Safety & Security

- Monitor crowd density in public spaces
- Enforce capacity limits in restricted areas
- Early detection of unusual crowd formations that may indicate incidents

### Event Management

- Accurate attendance tracking for venues
- Real-time crowd flow analysis
- Capacity management for safety compliance

### Business Analytics

- Customer traffic pattern analysis
- Optimize advertising placement based on foot traffic
- Peak hour identification for resource allocation

## The Challenge: Beyond Manual Counting

Manual counting becomes impractical and error-prone when dealing with:

- Dense crowds with overlapping subjects
- Large-scale scenes
- Real-time monitoring requirements

![](/images/density_ex2.jpg)

<div align="center">Source: nutraceuticalbusinessreview.com</div>

![](/images/density_ex.jpg)

<div align="center">Source: digest.bps.org.uk by Christian Jarrett</div>

## Innovative Solution Framework

I developed an automated counting system using Convolutional Neural Networks (CNN) that:

- Takes CCTV footage as input
- Processes frames in real-time
- Outputs accurate pedestrian counts
- Generates density maps for visualization

## Training Data Foundation

The project utilizes the [Mall Dataset](http://personal.ie.cuhk.edu.hk/~ccloy/downloads_mall_dataset.html) which includes:

- 2000 surveillance images (480x640 pixels, RGB)
- Ground truth pedestrian counts
- Consistent camera angle and positioning
- Varying crowd densities

## System Development Journey

### Initial Prototype

The initial implementation featured:

- Three convolutional blocks with ReLU activation
- Batch normalization for training stability
- Average pooling for dimension reduction
- Dropout layers for overfitting prevention
- Global max pooling
- Mean Squared Error loss function
- Adam optimizer

Performance metrics showed MAE of ~1 for training and ~5 for testing.

### Enhanced Architecture

I improved the model through several key innovations:

1. **Density Map Integration**

   - Replaced simple count labels with spatial density maps
   - Implemented adaptive Gaussian kerneling
   - Enhanced head detection accuracy

2. **Loss Function Enhancement**

   - Combined Structural Similarity Index (SSIM)
   - Implemented Local Pattern Consistency loss
   - Weighted Euclidean loss integration

3. **Architecture Optimization**
   - VGG16-based feature extraction
   - Multi-scale filter implementation
   - Feature enhancement layer
   - Transposed convolution for upsampling

## Performance Analysis

The improved model achieved:

- MAE of 0.51 on random crop testing
- MAE of 2.28 on full-size images
- Accurate density map generation
- Robust crowd distribution visualization

## Final Outcomes & Impact

This project demonstrates the effectiveness of deep learning in crowd counting applications. The developed system provides:

- Accurate pedestrian counting
- Spatial density information
- Real-time monitoring capability
- Practical applications for physical distancing enforcement

## Academic Sources

Cao, X., Wang, Z., Zhao, Y., & Su, F. (2018). Scale aggregation network for accurate and efficient crowd counting. Computer Vision – ECCV 2018, 757-773. https://doi.org/10.1007/978-3-030-01228-1_45

Chen, K., Gong, S., Xiang, T., & Loy, C. C. (2013). Cumulative attribute space for age and crowd density estimation. 2013 IEEE Conference on Computer Vision and Pattern Recognition. https://doi.org/10.1109/cvpr.2013.319

Chen, K., Loy, C. C., Gong, S., & Xiang, T. (2012). Feature mining for localised crowd counting. Procedings of the British Machine Vision Conference 2012. https://doi.org/10.5244/c.26.21

Crowd counting. (n.d.). Kaggle: Your Machine Learning and Data Science Community. https://www.kaggle.com/fmena14/crowd-counting

Li, Y., Zhang, X., & Chen, D. (2018). CSRNet: Dilated Convolutional neural networks for understanding the highly congested scenes. 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition. https://doi.org/10.1109/cvpr.2018.00120

Loy, C. C., Chen, K., Gong, S., & Xiang, T. (2013). Crowd counting and profiling: Methodology and evaluation. Modeling, Simulation and Visual Analysis of Crowds, 347-382. https://doi.org/10.1007/978-1-4614-8483-7_14

Loy, C. C., Gong, S., & Xiang, T. (2013). From semi-supervised to transfer counting of crowds. 2013 IEEE International Conference on Computer Vision. https://doi.org/10.1109/iccv.2013.270

Mall dataset - Crowd counting dataset. (n.d.). https://personal.ie.cuhk.edu.hk/~ccloy/downloads_mall_dataset.html

Tian, Y., Lei, Y., Zhang, J., & Wang, J. Z. (2020). PaDNet: Pan-density crowd counting. IEEE Transactions on Image Processing, 29, 2714-2727. https://doi.org/10.1109/tip.2019.2952083

Yosinski, J., Clune, J., Bengio, Y., & Lipson, H. (2014). How transferable are features in deep neural networks? Advances in Neural Information Processing Systems 27.

Zhang, Y., Zhou, D., Chen, S., Gao, S., & Ma, Y. (2016). Single-image crowd counting via multi-column Convolutional neural network. 2016 IEEE Conference on Computer Vision and Pattern Recognition (CVPR). https://doi.org/10.1109/cvpr.2016.70
