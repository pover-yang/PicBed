### Build gflags

```shell
% cmake \
-DCMAKE_SYSTEM_PROCESSOR=arm64 \
-DCMAKE_OSX_ARCHITECTURES=arm64 \
../gflags

% make
% make test (optional)
% sudo make install
```



### Build glog

```shell
% cmake \
-DCMAKE_SYSTEM_PROCESSOR=arm64 \
-DCMAKE_OSX_ARCHITECTURES=arm64 \
../glog

% make
% make test
% sudo make install
```



### Build OpenCV

```shell
% cmake \
  -DCMAKE_SYSTEM_PROCESSOR=arm64 \
  -DCMAKE_OSX_ARCHITECTURES=arm64 \
  -DWITH_OPENJPEG=OFF \
  -DWITH_IPP=OFF \
  -D CMAKE_BUILD_TYPE=RELEASE \
  -D CMAKE_INSTALL_PREFIX=/usr/local \
  -D OPENCV_EXTRA_MODULES_PATH=~/Downloads/opencv_contrib/modules \
  -D PYTHON3_EXECUTABLE=~/miniforge3/envs/bin/python3 \
  -D BUILD_opencv_python2=OFF \
  -D BUILD_opencv_python3=ON \
  -D INSTALL_PYTHON_EXAMPLES=ON \
  -D INSTALL_C_EXAMPLES=OFF \
  -D OPENCV_ENABLE_NONFREE=ON \
  -D BUILD_EXAMPLES=ON ../opencv

% make -j8
% sudo make install
```

