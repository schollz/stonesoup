# stonesoup
A little norns softcut fx engine for anyone to contribute and for any script to share


## save your ears from feedback

its very important to have your softcut script do this:

```lua
audio.level_eng_cut(0)
```

## testing

for testing purposes, to reset and recompile and reconnect jacks:

```
~/norns/stop.sh; sleep 1; ~/norns/start.sh; sleep 9; jack_disconnect crone:output_5 SuperCollider:in_1; jack_disconnect crone:output_6 SuperCollider:in_2; jack_connect softcut:output_1 SuperCollider:in_1; jack_connect softcut:output_2 SuperCollider:in_2
```

turn on all effects from maiden:

```
engine.bpm(clock.get_tempo())
engine.vinyl(1)
engine.phaser(1)
engine.delay(1)
engine.strobe(1)
```
