FROM python:3.8.5 

WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE ${MLFLOW_PORT}
# change to list 
CMD mlflow server --app-name basic-auth \
  --backend-store-uri ${BACKEND_URI} \
  --artifacts-destination  ${ARTIFACT_ROOT} \
  --host 0.0.0.0
