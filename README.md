- Locally I had to run frontend by writing the npm run dev commmand for frontend and backend each individually
- Command to build docker image: docker build -t alutaskmanagementapp .
- Command to run my tasks project with docker
docker run \
    -p 8080:8080 \
    -v /host/path/to/tasks:/tasks \
    -v /host/path/to/config:/config \
    -e PUID=1000 \
    -e PGID=1000 \
    -e TITLE="ALU Tasks project" \
    -e BASE_PATH="/" \
    -e LOCAL_IMAGES_CLEANUP_INTERVAL=1440 \
    my-docker-image:latest