# Caffe


This is rc3-mac-compatible version of caffe. 

## Installation
Follow [the instruction](http://caffe.berkeleyvision.org/install_osx.html)   
Next, Install openblas.
```
$ brew uninstall openblas; brew install --fresh -vd openblas
```
make 'build' directory.
```
$ mkdir build
$ cd build
```
run cmake.
```
#cpu only
$ cmake -DCPU_ONLY=on -DCMAKE_CXX_FLAGS=-I/usr/local/opt/openblas/include ..
#cpu only with matcaffe
$ cmake -DCPU_ONLY=on -DBUILD_matlab=on -DCMAKE_CXX_FLAGS=-I/usr/local/opt/openblas/include ..
```

copy caffe lib files to the /usr/local/lib.
```
$ cp -a lib/. /usr/local/lib
```


-----

## License and Citation of Caffe

Caffe is released under the [BSD 2-Clause license](https://github.com/BVLC/caffe/blob/master/LICENSE).
The BVLC reference models are released for unrestricted use.

Please cite Caffe in your publications if it helps your research:

    @article{jia2014caffe,
      Author = {Jia, Yangqing and Shelhamer, Evan and Donahue, Jeff and Karayev, Sergey and Long, Jonathan and Girshick, Ross and Guadarrama, Sergio and Darrell, Trevor},
      Journal = {arXiv preprint arXiv:1408.5093},
      Title = {Caffe: Convolutional Architecture for Fast Feature Embedding},
      Year = {2014}
    }
