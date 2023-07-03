FROM livingobjects/jre8
RUN mkdir -p /investment/
COPY iam-calculate-server/target/iam-calculate.jar /investment/
WORKDIR /investment/
EXPOSE 8103
CMD ["sh", "-ec", "exec ${JAVA_HOME}"]
