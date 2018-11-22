# 1. INSTRUCTION to Docker Server
# 2. Argument to the instruction

# Use an existing docker image as base
FROM alpine

# Download and install a dependency
# apk is a built-in alpine command
RUN apk add --update gcc
RUN apk add --update redis

# Tell the image what to do when it starts
# as a container
# CMD specifies what image should do if it gets started up as a container
CMD ["redis-server"]

# So when we "run img_hash" it runs "redis-server"