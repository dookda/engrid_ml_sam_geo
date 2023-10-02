FROM osgeo/gdal
WORKDIR /app

RUN apt update && apt-get install -y python3 
RUN apt update && apt-get install python3-pip -y
RUN apt update && apt-get install -y gdal-bin python3-gdal

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# COPY resnet50-19c8e357.pth /root/.cache/torch/hub/checkpoints/
# CMD ["python", "app.py"]
