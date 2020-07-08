FROM ubuntu:latest
RUN echo Updating existing packages, installing and upgrading python and pip.
RUN apt-get update -y
RUN apt-get install -y python3-pip python3-dev build-essential
RUN python3 -m pip install -U pip
RUN echo Copying the Mythical Mysfits Flask service into a service directory.
COPY ./service /MythicalMysfitsService
WORKDIR /MythicalMysfitsService
RUN echo Installing Python packages listed in requirements.txt
RUN pip install -r ./requirements.txt
RUN echo Starting python and starting the Flask service...
ENTRYPOINT ["python3"]
CMD ["mythicalMysfitsService.py"]
