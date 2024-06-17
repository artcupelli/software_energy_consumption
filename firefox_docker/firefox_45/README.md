## FIREFOX 45.0

- Versão 45.0
- Ano 2016

```sh
sudo docker build -t firefox-45.0 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-45.0 firefox-45.0
```
