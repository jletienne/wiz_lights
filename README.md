# wiz_lights
Controlling Smart Lights from a Bash Shell

## Reference (Credits - also archived in this repo)
[https://seanmcnally.net](https://seanmcnally.net/wiz-config.html)

Directions - Just fill the XX part out! 1 192.168.1.XX 38899


Get Status Bettom Light
```
echo -n "{\"method\":\"getPilot\",\"params\":{}}" | nc -u -w 1 192.168.1.XX 38899
```

Set Bottom Light to Scene 23 Vibes!

```
echo -n "{\"id\":1,\"method\":\"setPilot\",\"params\":{\"sceneId\":23,\"speed\":20,\"dimming\":45}}" | nc -u -w 1 192.168.1.XX 38899
```

Turn Off Bottom Light

```
echo -n "{\"id\":1,\"method\":\"setState\",\"params\":{\"state\":false}}" | nc -u -w 1 192.168.1.XX 38899  
{"method":"setState","id":1,"env":"pro","result":{"success":true}}
```
