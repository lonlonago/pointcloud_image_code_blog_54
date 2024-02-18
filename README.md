#  Overview of the principle 

##  1. Space straight line 

 ![avatar]( 92b36424e61e4bce8fadcf0aaffb88ed.png) 

##  2. Least square fitting 

 ![avatar]( 1e110ed91f814e818784ca79171e701f.png) 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524210
  ```  
#  III. Display of results 

 ![avatar]( 6eb7beff241f4cd0969cec2cbd2e009a.png) 

#  IV. Visual reference 

 Given the point equation of a straight line in space, how to draw this line? 



--------------------------------------------------------------------------------

#  Overview of the principle 

   The principle of the least squares method is to determine the best function match for a set of data based on minimizing the sum of squares of errors. The principle of its specific fitting circle is as follows. Assuming that the circle equation is known: Equation (1) can be written as: Rewrite equation (2) into the form of the right equal to 0, and convert the formula: Therefore, the values of the three parameters of the above binary quadratic equation can be determined, so as to calculate the radius of the fitting circle and give the coordinates of the center of the circle. The distance from the point in the sample set to the center of the circle: In order to obtain the most accurate fitting of the actual parameters of the circle, use the distance from the sample point to the center of the circle to square the difference with the radius, and find the value that minimizes the sum of squares, that is, the final solution, so as to determine the parameters of the circle and draw the circle. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574561180
  ```  
#  III. Display of results 

 ![avatar]( 75e90ddefc284059b184ca16f016f8a9.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   The expression of a plane straight line is written as a matrix in the form of: Solving the linear equation system can obtain the coefficients of the straight line. 

#  Code implementation 

##  1. Detailed process implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574511708
  ```  
##  2. Call function implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574511708
  ```  
#  III. Display of results 

 ![avatar]( c49e947ae9b3472c86bf3c82cd5f3fb6.png) 



--------------------------------------------------------------------------------

#  1. Main function 

 The smoothdata function in matlab can realize the mean, median, and Gaussian smoothing of the data. The detailed function description only needs to be entered in the command line window: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574515463
  ```  
 That's it. 

#  2. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574515463
  ```  
#  3. Display of results 

 ![avatar]( 7f0f137da9d14479bac718d6742af2f8.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Median filtering 

#  First, the principle of the algorithm 

##  1. Median filtering 

   The method of median filtering is to treat the current sampling point to be processed, select a template, which is composed of several data points in its vicinity, sort the point cloud data in the template from small to large, and then use the median value of the template to replace the value of the current sampling point. For a three-dimensional point cloud, the template is a sphere (as shown in Figure 1c), and for a sampling point in a three-dimensional point cloud, its neighborhood. All points in the neighborhood, for each channel (xyz axis direction) from large to small: 

   Take the data at the middle value as the surrogate value at the sampling point. From this, the point-to-point mapping of median filtering is obtained: 

 ![avatar]( 20210602184900801.png) 

   In this algorithm, the noise suppression effect is better, the detail information of the point cloud is basically maintained, and the noise reduction effect is also good for impulse noise, but the noise suppression effect is not very good for Gaussian noise.  

##  2. References 

>  [1] Zhu Zhihua, Liu Jin, Hu Xiyuan. Research on three-dimensional point cloud denoising technology of linear traces [J]. Criminal Technology, 2020, 45 (06): 556-561. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543380
  ```  
   Median filtering is performed on the 3D point cloud data. The function filters each channel of the point cloud separately. The output is a filtered point cloud. Each output position attribute value is the median of the neighborhood near the corresponding input position attribute value. The pcmedian function does not zero-process edges. Instead, it operates only on the neighborhood values available. If the input point cloud is an organized point cloud, the pcmedian function uses the N-by-N neighborhood method. If the point cloud is unorganized, the function takes the radial neighborhood method. 

##  3. References 

>  [1] Zhu Zhihua, Liu Jin, Hu Xiyuan. Research on three-dimensional point cloud denoising technology of linear traces [J]. Criminal Technology, 2020, 45 (06): 556-561. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574543380
  ```  
#  III. Display of results 

 ![avatar]( 20210604075550956.png) 

 1. Point cloud before filtering 2. Point cloud after filtering  



--------------------------------------------------------------------------------

#  I. Overview 

##  1. Algorithm overview 

   PCMerge: Merge two 3D point clouds 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519503
  ```  
 Given the input point cloud A and input point cloud B, as well as the voxel downsampled gridstep (used to downsample overlapping regions), the merged result is saved to pcCloudMerge. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519503
  ```  
#  III. Display of results 

 ![avatar]( e1dfb0da3458492294a4a6e34dee3454.png) 

#  IV. Parameter analysis 

##  input parameter 

##  output parameter 

#  V. Reference links 

>  Matlab point cloud toolbox - pcmerge 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Calculation process 

   The transformation matrix of the two-dimensional mirror transformation is: The transformation matrix of the three-dimensional mirror transformation is: Note: The mirror transformation belongs to the reflection transformation, which requires the reflection plane to pass through the origin, while the reflection transformation is not a strict rigid change, so there is deformation. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560288
  ```  
#  III. Display of results 

 ![avatar]( 08dab6be13044ae88ff9a4ab44d7c9d5.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  References 

>  [1] BESL P J, MCKAY N D. A method for registration of 3-Dshapes [J]. IEEE Transactions on Pattern Analysis and Machine Intelligence, 1992, 14 (2): 239-256. [2] Wang Mingjun, Yi Fang, Li Le, Huang Chaojun. Adaptive local neighborhood feature point extraction and matching point cloud registration [J/OL]. Infrared and Laser Engineering: 1-10 [2021-08-30]. http://kns.cnki.net/kcms/detail/12.1261.TN.20210804.1311.004.html. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574553657
  ```  
#  III. Display of results 

 ![avatar]( 2baacb8765b5457595e94cbb0ff8bc5f.png) 

#  IV. Reference link 

 [1]matlab点云工具箱——pcregistericp [2]matlab ICP实现点云精配准 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  References 

>  [1] Yang Chen, and Gerard Medioni. Object Modeling by Registration of Multiple Range Images. International Journal of Image and Vision Computing, 10 (3), pp. 145-155, 1992. [2] Yu Wenli, Zhou Mingquan, Shi Wuyang, Wu Zhongke. Automatic registration method for point clouds based on curvature [J]. Journal of System Simulation, 2015, 27 (10): 2374-2379 + 2386. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574584844
  ```  
#  III. Display of results 

 ![avatar]( 2cd17bfd775442928356dc6016cc988a.png) 

#  IV. Reference link 

 [1]matlab点云工具箱——pcregistericp [2]matlab ICP实现点云精配准 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Overview of the principle 

 See paper: [1] Li Xin, Mo Site, Huang Hua, Yang Shiji. Multi-source point cloud registration method for automatic calculation of overlap [J/OL]. Infrared and Laser Engineering: 1-10 [2021-05-16]. 

##  2. References 

>  [1] Chetverikov D, Svirko D, Stepanov D, et al. The Trimmed Iterative Closest Point Algorithm [C]//International Conference on Pattern Recognition. IEEE, 2002. [2] Li Xin, Moster, Huang Hua, Yang Shiji. Multi-source point cloud registration method for automatic calculation of overlap [J/OL]. Infrared and Laser Engineering: 1-10 [2021-05-16]. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574531241
  ```  
#  III. Display of results 

 ![avatar]( bdb3dd66049d4259b1181f211eb594a7.png) 

#  IV. Reference link 

 [1]matlab点云工具箱——pcregistericp [2]matlab ICP实现点云精配准 



--------------------------------------------------------------------------------

#  I. Overview of algorithms 

   First, the intrinsic shape feature (ISS) feature points are extracted from the point cloud to be registered, then the point cloud is ICP registered based on the ISS feature points, and finally the original point cloud is registered using the transformation matrix. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574545280
  ```  
#  III. Display of results 

 ![avatar]( ab5a4f61d0a14b58a7d379720563273d.png) 

#  Fourth, a warning!!! 

   Copy and paste the code and run it directly. Don't read other content on the blog. If you report an error, you can directly open "Why did I report an error, what kind of garbage code is this"??? detectISSFeatures is a new function in matlab2022a and above, so why do some bosses make mistakes?? Why ask?????  



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

    Given the spherical center and spherical radius of a spherical sphere in space, the coordinates projected onto the spherical surface at any point in space are: In the formula, the distance from the point to the origin is expressed.  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554271
  ```  
#  III. Display of results 

 ![avatar]( f7540f29beb0483c80a7450fc9117445.png) 

#  IV. Relevant links 

 [1] Open3D 点云投影到球面 [2] PCL 点云投影到球面 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   There are three representations of straight line equations: general formula, point-to-point formula, and parametric formula. PCL uniformly adopts the point-to-point formula. The point-to-point equation of a straight line is: Among them, the direction vector, the known point. The coordinates of the projection point from a point outside the line to the line are: In formula (2), it is:  

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574536279
  ```  
#  III. Display of results 

 ![avatar]( 76accee16a3141daacb6c7f5bf812670.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 Just look at the code. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574524890
  ```  
#  III. Display of results 

 ![avatar]( 2904c212e32c45cbb306d8c9af412dfc.png) 



--------------------------------------------------------------------------------

#  I. Overview 

##  1、pointCloud 

   The pointCloud in Matlab is a data type used to handle point clouds, and the main properties contained therein are: 

   To color a cloud, simply modify the Color property. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574563189
  ```  
#  III. Display of results 

 ![avatar]( 571b39d1092b4e6fa7d5430d9e245a45.png) 



--------------------------------------------------------------------------------

#  First, random sampling 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957459242
  ```  
 Returns a downsampled point cloud with random sampling that does not require substitution. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957459242
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( bc98734bfcd944be9f17c586ae813e3b.png) 

##  2. Sampling results 

 ![avatar]( a86c4439df8140ad802dbea6029ecf52.png) 

#  IV. Reference link 

 Matlab point cloud tool - pcdownsample 



--------------------------------------------------------------------------------

#  First, sampling filtering 

##  1. Algorithm overview 

    Given the number of fixed sampling points, downsample the point cloud to the given number of points. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574573736
  ```  
#  III. Display of results 

 ![avatar]( 45d8bfb3fc8f4ae1aeb1d07a071a95f5.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  References 

>  LIU Yi. 3D Reconstruction of Binocular Visual Scene Based on Kinect [D]. University of Electronic Science and Technology of China, 2016. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554415
  ```  
#  III. Display of results 

 ![avatar]( 80bd9e8a7def42d6b051dfe0d7374513.png) 

#  IV. Test data 

 The test data is generated by MATLAB code, which is as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554415
  ```  


--------------------------------------------------------------------------------

#  First, rigid body transformation 

##  1. Algorithm overview 

   Rigid3D: Three-dimensional rigid geometric transformations, supporting positive and inverse transformations. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 Create a default rigid body transformation, i.e. Rotation: [3 × 3 double] Translation: [0 0 0] 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 Creates a rigid transformation matrix based on the specified forward rigid transformation matrix. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 Create a transformation matrix from the rotation matrix and the translation vector. 

##  3. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
##  4. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
##  5. Parameter analysis 

##  6. Inverse transformation matrix 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 That is, finding the inverse matrix of the transformation matrix 

#  Affine transformation 

##  1. Algorithm overview 

   Affine3D: 3D affine geometric transformation, supports positive and inverse transformations. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 Creates an affine3d object with default property settings corresponding to identity transformations. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 An effective affine transformation defined by a nonsingular matrix A. 

##  3. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
##  4. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574580268
  ```  
 ![avatar]( 11717ef6aaf34abea1effc83b245d3db.png) 

##  5. Parameter analysis 

#  III. Reference link 

 Matlab point cloud toolbox - rigid3d matlab point cloud toolbox - affine3d 



--------------------------------------------------------------------------------

#  I. Overview 

##  1. Preface 

   It is well known that the accuracy evaluation criterion of point cloud registration is root mean square error. 

##  2. Data preparation 

 ![avatar]( f98bbe0e83574576ae8dcc75bbadfa97.png) 

   Translate 0.1m along the X direction to obtain the two-phase point cloud in the figure below  

 ![avatar]( f9f41198ee294bc7becde5b903aa6703.png) 

    For these two point clouds, the registration accuracy obtained by oral arithmetic is 0.1m. The following code is verified 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574540789
  ```  
#  III. Display of results 

 ![avatar]( 343c028c7227458fb3443fe78400628b.png) 

  Amazing!!!! 

#  IV. Test data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574540789
  ```  


--------------------------------------------------------------------------------

