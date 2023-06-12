# Use the official TensorFlow Serving runtime as the base image
FROM tensorflow/serving

# Set the model name, version, and base path
ENV MODEL_NAME lung_cancer
ENV MODEL_VERSION 1
ENV MODEL_BASE_PATH /models

# Copy the model files into the container
COPY ./my_model /${MODEL_BASE_PATH}/${MODEL_NAME}/${MODEL_VERSION}

# Expose the REST API port
EXPOSE 8501

# Start TensorFlow Serving when the container launches
CMD tensorflow_model_server \
    --port=8501 \
    --rest_api_port=8501 \
    --model_name=${MODEL_NAME} \
    --model_base_path=${MODEL_BASE_PATH}/${MODEL_NAME}