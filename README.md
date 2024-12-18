# Stereo-Vision-Algorithms


## **Description**  

Stereo vision is a fundamental technique in computer vision used to extract depth information from stereo image pairs. The assignment focuses on computing the disparity (horizontal shift) of pixels along the scanlines of two images using:  

1. **Block Matching**  
   - Matching pixels in the left image with corresponding pixels in the right image using a sliding window approach.  
   - Two cost functions were used:  
     - **Sum of Absolute Differences (SAD)**  
     - **Sum of Squared Differences (SSD)**  
   - Disparity maps were generated for window sizes:  
     - \( w = 1 \), \( w = 5 \), and \( w = 9 \).  
   - A total of 6 disparity maps were produced (2 maps per window size).  

2. **Dynamic Programming**  
   - An optimal alignment of scanlines is computed using a dynamic programming approach to minimize the matching cost.  
   - Cost function:  
     \[
     d_{ij} = \frac{(I_l(i) - I_r(j))^2}{\sigma^2}
     \]  
     - Where \( \sigma = 2 \) (measure of pixel noise).  
   - Skipping pixels in either scanline incurs a constant cost \( c_0 = 1 \).  
   - Backtracking was used to extract the optimal alignment and calculate disparity maps.  

---

## **Bonus**  

The alignment of a single scanline is visualized with a graph plotting:  
- **Left Image (Il)** (vertical axis) vs **Right Image (Ir)** (horizontal axis).  
- Three types of lines are drawn to represent the alignment:  
  - **Vertical lines**: Skipping pixels in the left image.  
  - **Horizontal lines**: Skipping pixels in the right image.  
  - **Diagonal lines**: Matching pixels between the two images.  




---

## **Output**  

1. **Disparity Maps**:  
   - 6 disparity maps (SAD and SSD for \( w = 1, 5, 9 \)).  
2. **Dynamic Programming Results**:  
   - Disparity map for scanline alignment.  
3. **Bonus Visualization**:  
   - Graph of alignment for a single scanline, showing matching/skipping behavior.  

---

## **Acknowledgment**  

This assignment was developed as part of the coursework for computer vision studies.  

