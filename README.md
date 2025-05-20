# pythonrunner

A simple Dockerfile to be able to run Python scripts without having Python installed directly. Usable for quick prototyping and running different versions of Python for different projects.

Build the Docker image using:
```
docker build -t <your_image_name> .
```

Run in python project directory:
```
docker run -it --rm -v $PWD:/home/app_user <your_image_name>
```

In the interactive terminal, you can run your python script as
```
python <script> <parameters>
```

If any python dependencies are missing, you can add them in requirements.txt and rebuild the image.

The python version can be configured in the Dockerfile