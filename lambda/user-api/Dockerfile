FROM public.ecr.aws/lambda/python:3.11

# Install Python dependencies
RUN pip install --no-cache-dir \
    psycopg2-binary \
    boto3

# Copy application code
COPY lambda_function.py ${LAMBDA_TASK_ROOT}/
COPY schema.sql ${LAMBDA_TASK_ROOT}/

# Set the handler
CMD ["lambda_function.handler"]