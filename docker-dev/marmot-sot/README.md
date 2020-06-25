# Typical command to build a docker image from dockerfile

docker build -t deepo/pth:cu101 --network=host -f ./Dockerfile.pytorch151-py36-cu102-cudnn7-marmot-sot ./

