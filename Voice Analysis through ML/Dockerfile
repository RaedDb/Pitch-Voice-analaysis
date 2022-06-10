FROM python:3.8

# Create the working directory
RUN set -ex && mkdir /classifier
WORKDIR /classifier

# Install Python dependencies
#RUN apt-get install -y ffmpeg
COPY requirements.txt ./requirements.txt
RUN pip install -r requirements.txt

# Copy the relevant directories
COPY templates/ ./templates
COPY static/ ./static
COPY . ./

# Run the web server
EXPOSE 8000
ENV PYTHONPATH /classifier
CMD python /classifier/app.py
#CMD [ "python" "./classifier/app.py" ]
