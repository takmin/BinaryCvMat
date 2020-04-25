### Note
I created new version of BinaryCvMat.  Please use the following to save not only cv::Mat but cv::KeyPoint, cv::Size, and cv::Point as binary.

https://github.com/takmin/SaveBinaryOpenCV


BinaryCvMat
===========

Save and Load cv::Mat as a binary file.

It requires OpenCV 2.0 or later.

cv::FileStorage is not so fast to save cv::Mat of large size, because it writes datas as ASCII.
So I write a code to save cv::Mat data as binary. 

Just copy the whole functions in BinaryCvMat.cpp to your code or write header.

Mainly there are 2 functions

SaveMatBinary()
//! Save cv::Mat as binary
/*!
\param[in] filename filaname to save
\param[in] output cvmat to save
*/
bool SaveMatBinary(const std::string& filename, const cv::Mat& output);

//! Load cv::Mat as binary
/*!
\param[in] filename filaname to load
\param[out] output loaded cv::Mat
*/
bool LoadMatBinary(const std::string& filename, cv::Mat& output);
