# `timrogers/ruby-with-openjdk-8-jre`

This repository contains a `Dockerfile` which builds a Docker image based on CircleCI's `cimg/ruby` image, but with OpenJDK 8 installed.

This is particularly useful if you want to use the `cimg/ruby` image in CircleCI, but you need Java and you don't want to have to wait for it to install every run.

This image is pushed to Docker Hub as `timrogers/ruby-with-openjdk-8-jre`. The tags on the pushed images correspond to Ruby versions - so, for example, `timrogers/ruby-with-openjdk-8-jre:3.0.2` contains Ruby 3.0.2.

## Pushing an image with a new Ruby version

1. Update the `Dockerfile` to refer to the new version of the base image, `cimg/ruby`. For example, if you wanted to use Ruby 4.5.6, you'd want to refer to `cimg/ruby:4.5.6`.
2. Build the image by running `docker build -t timrogers/ruby-with-openjdk-8-jre:3.0.2 .`, replacing `3.0.2` with the Ruby version from step 1
3. Push the image to Docker Hub by running `docker push timrogers/ruby-with-openjdk-8-jre:3.0.2`, replacing `3.0.2` with the Ruby version from step 1
