#build stage
FROM ubuntu as build
RUN apt-get update && apt-get install -y python3
COPY code.py . 

#final stage
FROM python:alpine3.19
COPY --from=build /code.py /code.py
CMD ["python3", "code.py"]
