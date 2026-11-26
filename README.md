# Radio channel activity 

GOal: to simulate the the analsis of a walkie-talkie (push-to-talk) channel.
It works thougth one input, `ui[0]`, == to a busy channel. 

The chip measures three things:

- Duration: how long the current or last transmission lasted.
- Count: how many transmissions there have been.
- Occupancy: what percentage of the last 100 s the channel was busy.

If a transmission reaches 60 s, the decimal point starts blinking. 
That's mean a alarm, that indicates it's probably a continuous carrier. 

## Commands
- Mode `ui[2:1]`:  what to show (00 duration, 01 count, 10 occupancy). 
- Digits `ui[4:3]`: 00 units, 01 tens, 10 hundreds, 11 thousands. 


## Personal Notes (wires)

- Violet, synchronizer: clean the input and detect when a tx starts
- Orange, time base
- Cyan, duration: counts while the channel is busy
- Yellow, count: +1 every time a tx starts
- Green, occupancy: counts on a busy channel 
- Red, alarm: on when a tx reaches 60s
- Blue, display


KAFL
last edition: 25nov26
