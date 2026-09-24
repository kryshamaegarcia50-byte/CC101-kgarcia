````markdown
# MinIO Deployment

## Docker Command Used

The MinIO server was deployed using the following Docker command:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
local-minio
````

## Docker Command Explanation

The command runs the MinIO server inside a Docker container.

* `docker run` creates and starts a new container.
* `-d` runs the container in the background.
* `-p 9000:9000` maps port 9000 for the MinIO API.
* `-p 9001:9001` maps port 9001 for the MinIO Web Console.
* `--name minio-server` gives the container the name `minio-server`.
* `-e` sets environment variables for the MinIO container.
* `local-minio` is the Docker image used to run the MinIO server.

## Environment Variables

The `-e` flags were used to configure the administrator credentials of the MinIO server.

```text
MINIO_ROOT_USER=cloudadmin
MINIO_ROOT_PASSWORD=CloudNova2026!
```

`MINIO_ROOT_USER` sets the administrator username, while `MINIO_ROOT_PASSWORD` sets the administrator password.

These credentials were used to log in to the MinIO Web Console.

## Web Console Port

The MinIO Web Console was accessed using **port 9001**.

Port **9000** was used for the MinIO API, while port **9001** was used for the web-based management console.

## Accessing the MinIO Console

After starting the Docker container, port **9001** was accessed through the KillerCoda port interface. The MinIO login page was then opened in a web browser.

The administrator credentials were entered to access the MinIO Web Console.

## Bucket Created

A bucket named **client-photos** was created through the MinIO Web Console.

The bucket was used to store a sample file and demonstrate how objects can be uploaded and managed in MinIO.

## File Upload

After creating the `client-photos` bucket, a sample file was uploaded using the **Upload** button in the MinIO Web Console.

The uploaded file appeared inside the bucket, confirming that the storage server was working properly.

## Deployment Verification

The MinIO container was verified using the following command:

```bash
docker ps
```

The container was running successfully and exposing ports **9000** and **9001**.

## Summary

This deployment demonstrated how MinIO can be used as an object storage server. Docker made it easier to run the MinIO server in a container, while the Web Console provided an easy way to create buckets and upload files.

```
