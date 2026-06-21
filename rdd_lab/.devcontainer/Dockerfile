FROM mcr.microsoft.com/devcontainers/python:3.10

# Install Java (Required for Spark)
RUN apt-get update && apt-get install -y default-jdk procps && rm -rf /var/lib/apt/lists/*

# Install PySpark and Jupyter dependencies
RUN pip install --no-cache-dir pyspark jupyterlab notebook

# Set Environment Variables
ENV JAVA_HOME=/usr/lib/jvm/default-java
ENV SPARK_HOME=/usr/local/lib/python3.10/site-packages/pyspark
ENV PATH=$PATH:$SPARK_HOME/bin