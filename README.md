Maintain healthy battery by avoiding charging devices to 100% all the time.  Using commonly available wifi outlets with Tasmota firmware, this node-red flow monitors the current consumption and turns outlet off when current falls below some threshold.  At intervals, turns outlet back on to reassess battery charge.
<img src="https://github.com/tsaitsai/tasmota_battery_tender/blob/main/img/img_example_tasmota.jpg">

As the charge on Li-ion batteries approach 100%, the charge current steadily decreases.  Charge current can be a good proxy for battery charge.
<img src="https://github.com/tsaitsai/tasmota_battery_tender/blob/main/img/Charge_current_behavior.jpg">

Requires a [Tasmota-fied wifi outlet with current sensing feature](https://cloudfree.shop/product/sonoff-s31-flashed-with-tasmota/). 

<img src="https://github.com/tsaitsai/tasmota_battery_tender/blob/main/img/flow_img.jpg">
