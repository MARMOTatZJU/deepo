# Typical command to build a docker image from dockerfile

Build & install

```bash
docker build -t deepo/pth:cu102 --network=host -f ./Dockerfile.pytorch151-py36-cu102-cudnn7-marmot-sot ./
docker run -itd --name deepo-pth-dev --network host --ipc host --gpus all -v /home/$USER:/home/$USER deepo/pth:cu102
docker exec -it deepo-pth-dev bash
```

Stop & delete

```bash
docker stop deepo-pth-dev && docker rm $_
docker rmi deepo/pth:cu102
```

P.S.
- tmux bind key in container: Ctrl-x (avoid conflict with host)
- tmux-resurrect
  - save session state: Ctrl-bind Ctrl-s
  - load session state: Ctrl-bind Ctrl-r
