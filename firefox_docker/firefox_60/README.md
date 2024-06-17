## FIREFOX 60.0

- Versão 60.0
- Ano 2018

```sh
sudo docker build -t firefox-60.0 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-60.0 firefox-60.0
```
