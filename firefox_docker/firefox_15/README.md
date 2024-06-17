## FIREFOX 15.0

- Versão 15.0
- Ano 2012

```sh
sudo docker build -t firefox-15.0 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-15.0 firefox-15.0
```
