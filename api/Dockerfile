FROM python:3.9

# Working dir in the container
WORKDIR /usr/src/app

# Copy dependencies into the working dir
COPY requirements.txt ./

# Install the packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Cope the contents of the local src dir to the working dir
COPY . .

# Start the app
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]