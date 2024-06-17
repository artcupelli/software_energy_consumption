## FIREFOX 3.0

- Versão 3.0
- Ano 2008

```sh
sudo docker build -t firefox-3.0 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-3.0 firefox-3.0
```
