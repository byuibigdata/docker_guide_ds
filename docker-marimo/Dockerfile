FROM ghcr.io/marimo-team/marimo:latest-sql
EXPOSE 8080
WORKDIR /app
USER root
COPY . .
# Install any additional dependencies here
RUN pip3 install -r requirements.txt
RUN chown -R 1000:1000 /app
user 1000
CMD ["marimo", "edit", "--no-token", "-p", "8080", "--host", "0.0.0.0"]