# Use the official Jupyter base notebook image
FROM jupyter/base-notebook:latest

# Set the working directory in the container
WORKDIR /home/jovyan

# Expose the Jupyter Lab port
EXPOSE 8888

# Copy the requirements.txt file into the container
COPY requirements.txt /home/jovyan/

# Install Jupyter Lab and dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Run Jupyter Lab with no token
RUN echo "c.NotebookApp.token = ''" >> /etc/jupyter/jupyter_notebook_config.py

# Run Jupyter Lab
CMD ["start.sh", "jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--NotebookApp.allow_root=True"]