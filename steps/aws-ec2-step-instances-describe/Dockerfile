FROM relaysh/core:latest-python
RUN pip --no-cache-dir install boto3
COPY "./step.py" "/step.py"
ENTRYPOINT []
CMD ["python3", "/step.py"]

LABEL "org.opencontainers.image.title"="Describe AWS EC2 instances"
LABEL "org.opencontainers.image.description"="This task describes the EC2 instances in a given account and region."
LABEL "sh.relay.sdk.version"="v1"
