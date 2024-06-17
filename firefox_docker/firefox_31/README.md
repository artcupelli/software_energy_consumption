## FIREFOX 31.0

- Versão 31.0
- Ano 2014

```sh
sudo docker build -t firefox-31.0 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-31.0 firefox-31.0
```
