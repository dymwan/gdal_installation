# gdal_installation
Illustrate how to install the python interface of GDAL in Ubuntu os.

##  Download source file
you can download the source package via http://download.osgeo.org/gdal/  
-if you download the *.zip file, use `unzip *.zip` to get directory */gdal_x_x_x/
-if you download the *.tar.gz format, use `tar -xzvf *.tar.gz` to get directory */gdal_x_x_x/  


or you can use `wget` to download the file.

## compile what you download
follow the command to enter the gdal package:  
`cd  gdal-x.x.x`  
`./configure --with-python` --> compile the python interface  
`make`  
`make install`  

## Configuration
`vim ~/.bashrc`  
add `export LD_LIBRARY_PATH=$LD_LIBRARY_PATH：/usr/local/lib` to the end  

## build the python package
`cd */gdal-x.x.x/swig/python`  
`sudo python setup.py build`  
`sudo python setup.py install`  


`sudo find / -name gdal.py`
add all path containing gdal.py to `/etc/profile`

LAST, reboot to check the installation

if :  
`>>>import osgeo.gdal`   
without any error, Congratulations! :)

[comment]:<Add some Error fixer>
