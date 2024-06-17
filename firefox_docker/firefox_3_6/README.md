## FIREFOX 3.6

- Versão 3.6
- Ano 2010

```sh
sudo docker build -t firefox-3.6 .
```

```sh
sudo docker run -it --rm     --env DISPLAY=$DISPLAY     --env XAUTHORITY=$XAUTHORITY     --volume /tmp/.X11-unix:/tmp/.X11-unix     --volume $XAUTHORITY:$XAUTHORITY    --network host  --name firefox-3.6 firefox-3.6
```
