FROM openjdk:11-jre-slim
COPY --from=python:3-slim / /
COPY target/load-prediction-service-0.0.1-SNAPSHOT.jar /home/load-prediction-service-0.0.1-SNAPSHOT.jar
COPY Load_Prediction_Model.pkl /
COPY LoadPrediction_predict.py /
COPY LoadPrediction_update.py /
COPY requirements.txt /
RUN pip install --no-cache-dir -r /requirements.txt
CMD ["java","-jar","/home/load-prediction-service-0.0.1-SNAPSHOT.jar"]
