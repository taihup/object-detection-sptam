*En progreso ...* 

En el directorio ros están los nodos de Ros y el modelo que usa para correr definido en rcnn_pose.py 
Mover el contenido del directorio ros al workspace de ros y compilar 

para correr:

    roslaunch sptam dl_zed.launch

En tiempo de ejecución pide por
    ~/.local/lib/python2.7/models/modelpose/VGG16/faster_rcnn_end2end/test.final.prototxt

que está en el directio models_tained:

    models_tained/modelpose/VGG16/faster_rcnn_end2end/test.final.prototxt
    
copiar o moverlos para que funcione.    
    
    
*COMPILACIÓN*

**caffe-fast-rcnn**

*dependencia general Ubuntu 16.01*

    sudo apt-get install libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libhdf5-serial-dev protobuf-compiler
    sudo apt-get install --no-install-recommends libboost-all-dev
    
***Blas***
 
 **ATLAS**:
 
    apt-get install libatlas-base-dev
 
 **OpenBlas**:
 
    apt-get install libopenblas-dev
 
    cp Makefile.config.example Makefile.config (revisar el Makefile.config y setear las variables necesarias) 
    mkdir build
    cd build
    cmake ..
    make -j4 && make pycaffe
    make install

Agregar a las variables de entorno el contenido de install o moverlos/copiarlos a directorios de sistema.
Para copiarlos

    sudo cp install/lib/* /usr/local/lib 
    sudo cp -Rf install/include/ /usr/local/include
    cp install/python/caffe ./local/local/lib/python2.7/site-packages/
    sudo cp install/bin/* /usr/local/bin
    sudo cp -Rf install/share/Caffe /usr/local/share 
    
 
 **py-faster-rcnn**
 
    cd lib
    make
 
 **dependencies **
 
 
 
 
 
 
 
 