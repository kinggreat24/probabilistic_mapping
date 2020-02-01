This is the implementation of our paper: "Probabilistic Dense Reconstruction from a Moving Camera" in IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2018. Our implementation runs on Linux and is fully integrated with ROS (developed in version of indigo). Eigen, OpenCV 3+, and CUDA are required.

The high resolution video of our submitted paper is: https://1drv.ms/v/s!ApzRxvwAxXqQmlW9ZOrp9hdA7ude (720p is recommmanded)

To complie this code, you should modify the arch code (i.e. --generate-code arch=compute_XX,code=sm_XX) in the CMakeList.txt such that it adapts to your GPU.

This code is not well ready for the public, some hints for use are as follows:
The input of my code is curImg(current image), cur_R (rotation), cur_t (translation) and fx, fy, cx, cy (camera intrinsics) in the ‘evaluate.cc’ file.
You can modify some lines between 240 and 260 of the  ‘evaluate.cc’ file. 
motion_stereo_mapping.init_reference() and motion_stereo_mapping.update()  calculate the cur depth image;
motion_stereo_mapping.outFusion() outputs the fused depth image.



The source code is released under GPLv3 license. If you use our code, please cite our paper:

[1] Yonggen Ling, Kaixuan Wang and Shaojie Shen, "Probabilistic Dense Reconstruction from a Moving Camera" in IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2018.

For more questions, please contact ylingaa at connect dot ust dot hk .
