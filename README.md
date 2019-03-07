# darkflow-on-docker

Run darkflow in an iPython notebook from the comfort of a docker container!

Example command line code to get up and running (linux):

```bash
docker build . -t yolo -f iPython_darkflow_dockerfile && \
docker run -v $(pwd)/../out:/out -v $(pwd)/../data:/data -v $(pwd)/../src:/src/userCode -p 8888:8888 yolo
```

All code written to the the ../src directory on the loacal machine will be available to the iPython notebook via the /src/userCode dir. Likewise any code written on the docker image to the userCode folder will be saved to the users /src file.

You can also pass in data though ../data, and output though ../out.
