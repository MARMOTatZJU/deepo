# Typical command to build a docker image from dockerfile

Build & install

```bash
docker build -t deepo/pth:mac --network=host -f ./Dockerfile.u18.python3.6 ./
docker run -itd --name deepo-pth-dev --network host --ipc host --gpus all -v /home/$USER:/home/$USER deepo/pth:mac
docker exec -it deepo-pth-dev bash
```

Stop & delete

```bash
docker stop deepo-pth-dev && docker rm $_
docker rmi deepo/pth:mac
```

P.S.
- tmux bind key in container: Ctrl-x (avoid conflict with host)
- tmux-resurrect
  - save session state: Ctrl-bind Ctrl-s
  - load session state: Ctrl-bind Ctrl-r
