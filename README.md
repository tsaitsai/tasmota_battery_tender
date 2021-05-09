Maintain healthy battery by avoiding charging devices to 100% all the time.  Using commonly available wifi outlets with Tasmota firmware, this node-red flow monitors the current consumption and turns outlet off when current falls below some threshold.  At intervals, turns outlet back on to reassess battery charge.
<img src="https://github.com/tsaitsai/tasmota_battery_tender/blob/main/img/img_example_tasmota.jpg">

As the charge on Li-ion batteries approach 100%, the charge current steadily decreases.  Charge current can be a good proxy for battery charge percentage.  

<img src="https://github.com/tsaitsai/tasmota_battery_tender/blob/main/img/Charge_current_behavior.jpg">

1.  In the node-red flow, pick some current value (amps) that corresponds to your desired charge level.  This is the "current threshold".  
2.  Select some interval (hours) for how often to reassess battery charge state.  The outlet will turn back on at this interval to read charge current.

<img src="https://github.com/tsaitsai/tasmota_battery_tender/blob/main/img/flow_img.jpg">

There's some sensitivity to the AC adapter as well as the device being charged.  Using an AC adapter with a higher current rating (above 1 amp) should generate a bigger differential in charge current between depleted and full battery.


Requires a [Tasmota-fied wifi outlet with current sensing feature](https://cloudfree.shop/product/sonoff-s31-flashed-with-tasmota/). 

Install this moving average node:
https://flows.nodered.org/node/node-red-contrib-moving-average

