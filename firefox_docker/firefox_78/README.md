## FIREFOX 69.0

- Versão 69.0
- Ano 2020

```sh
sudo docker build -t firefox-69.0 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-69.0 firefox-69.0
```
