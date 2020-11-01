# 1st-DL-CVMarathon

## Day 001 - introduction to OpenCV & read/show image
* Read image: [cv2.imread( filename[, flags] )](https://docs.opencv.org/4.4.0/d4/da8/group__imgcodecs.html#ga288b8b3da0892bd651fce07b3bbd3a56)
* Show image: [cv2.imshow( winname, mat )](https://docs.opencv.org/4.4.0/d7/dfc/group__highgui.html#ga453d42fe4cb60e5723281a89973ee563), [cv2.waitKey([, delay])](https://docs.opencv.org/4.4.0/d7/dfc/group__highgui.html#ga5628525ad33f52eab17feebcfba38bd7)

## Day 002 - color space conversion (HSV, HSL, Lab)
* Convert color space: [cv2.cvtColor( src, code[, dst[, dstCn]] )](https://docs.opencv.org/4.4.0/d8/d01/group__imgproc__color__conversions.html#ga397ae87e1288a81d2363b61574eb8cab)

## Day 003 - adjust brightness, saturation, contrast
* Histogram equalization: [cv2.equalizeHist( src[, dst] )](https://docs.opencv.org/4.4.0/d6/dc7/group__imgproc__hist.html#ga7e54091f0c937d49bf84152a16f76d6e)
* Scales, calculates absolute values: [cv2.convertScaleAbs( src[, dst[, alpha[, beta]]] )](https://docs.opencv.org/4.4.0/d2/de8/group__core__array.html#ga3460e9c9f37b563ab9dd550c4d8c4e7d)

## Day 004 - image flipping, scaling, translation
* Flip:
    * vertical: image[::-1, :, :]
    * horizontal: image[:, ::-1, :]
* Scaling: [cv2.resize( src, dsize[, dst[, fx[, fy[, interpolation]]]] )](https://docs.opencv.org/4.4.0/da/d54/group__imgproc__transform.html#ga47a974309e9102f5f08231edc7e7529d)
* Translation: [cv2.warpAffine( src, M, dsize[, dst[, flags[, borderMode[, borderValue]]]] )](https://docs.opencv.org/4.4.0/da/d54/group__imgproc__transform.html#ga0203d9ee5fcd28d40dbc4a1ea4451983)
    * adjust M13, M23

## Day 005 - drawing functions
* [cv2.rectangle( img, pt1, pt2, color[, thickness[, lineType[, shift]]] )](https://docs.opencv.org/4.4.0/d6/d6e/group__imgproc__draw.html#ga07d2f74cadcf8e305e810ce8eed13bc9)
* [cv2.line( img, pt1, pt2, color[, thickness[, lineType[, shift]]] )](https://docs.opencv.org/4.4.0/d6/d6e/group__imgproc__draw.html#ga7078a9fae8c7e7d13d24dac2520ae4a2)
* [cv2.putText( img, text, org, fontFace, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]] )](https://docs.opencv.org/4.4.0/d6/d6e/group__imgproc__draw.html#ga5126f47f883d730f633d74f07456c576)
* Tutorial: [Drawing Functions in OpenCV](https://docs.opencv.org/4.4.0/dc/da5/tutorial_py_drawing_functions.html)

## Day 006 - affine transformation basics
* Get rotation & scale matrix: [cv2.getRotationMatrix2D( center, angle, scale )](https://docs.opencv.org/4.4.0/da/d54/group__imgproc__transform.html#gafbbc470ce83812914a70abfb604f4326)
* Translation matrix: adjust M13, M23 manually
* Shearing is not discussed here
* Or, get affine transformation matrix by matching 3 points: [cv2.getAffineTransform( src, dst )](https://docs.opencv.org/4.4.0/da/d54/group__imgproc__transform.html#ga8f6d378f9f8eebb5cb55cd3ae295a999)
* Apply affine transformarion: [cv2.warpAffine( src, M, dsize[, dst[, flags[, borderMode[, borderValue]]]] )](https://docs.opencv.org/4.4.0/da/d54/group__imgproc__transform.html#ga0203d9ee5fcd28d40dbc4a1ea4451983)
