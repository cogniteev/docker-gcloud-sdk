## Docker Google Cloud SDK Dockerfile

This repository contains **Dockerfile** of [Google Cloud SDK](https://cloud.google.com/sdk/) for [Docker](https://www.docker.com/) [automated build](https://registry.hub.docker.com/u/cogniteev/gcloud-sdk/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).

### Base Docker Image

* [ubuntu:14.04](https://registry.hub.docker.com/_/ubuntu/)

### Installation

1. Install [Docker](https://www.docker.com/)

2. Download [automated build](https://registry.hub.docker.com/u/cogniteev/gcloud-sdk/): `docker pull cogniteev/gcloud-sdk`

### Usage

This image allows to easily create sub-images containing your private [service account keys](https://cloud.google.com/compute/docs/authentication#using)

To do so, create sub-images that add your .json or .p12 keys in `/root/project-keys/` directory. The files must be named after the project. For instance:

* `/root/project-keys/my-project.json`
* `/root/project-keys/my-other-project.p12`

For *p12* keys files, you have to also provide the *account* (service account email) to use in the `/root/project-keys/<project>.account` file. For instance:

* `/root/project-keys/my-project.p12`
* `/root/project-keys/my-project.account`
