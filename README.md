## CSRnet Web Application prototype

This is a web application that pulls images from public webcams in Nanyang Technological University, and analyzes the crowd density in the images using dialted convolutional neural network.

## Install
```
bash build.sh
```

## Run
Run "python backend.py" 

This application will download images from the webcams, store them in /images folder and compute them using the CSR-network. The computed density maps are stored in /density_maps as png-files. The counts are stored in the log.json in /log folder.
The appliaction will repeat this process every 10 seconds.

Run "python app.py" 

This is a server application, running on localhost:5000 by default. When accessed, it returns the index html. 

Access "localhost:5000/fastfood" to get JSON struct {"Image": path, "Count" : int}

Other places:
"localhost:5000/foodcourt"
"localhost:5000/onestop_sac"
"localhost:5000/library"
