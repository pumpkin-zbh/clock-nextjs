# Timer

### Make the LED blink 1 time per second periodically through a timer.

```python

# import Pin、Timer module
from machine import Pin, Timer

TITLE = "Timer"

async def on_boot(screen, config):
    led = machine.Pin(2, machine.Pin.OUT)
    Counter = 0
    Fun_Num = 0
    
    # Define a callback function to control the blinking of the LED light
    def fun(timer):
        nonlocal Counter
        # Control the LED light on and off according to the parity of the Counter
        Counter += 1
        # Print the value of Counter
        print(Counter)
        led.value(Counter % 2)

    tim = machine.Timer(0) # create timer
    # Initialize the timer, the period is 1000 milliseconds, the mode is periodic, and the callback function is set to fun
    tim.init(period=1000, mode=machine.Timer.PERIODIC, callback=fun)


async def on_refresh(screen, config):
    # Once active, called by system every 200ms
    pass

async def on_selected(screen, config):
    # User just pressed the button for 1 second
    pass

async def on_leave(screen, config):
    # User triggered to leave this plugin page, all function should be deactivated
    pass

async def on_enter(screen, config):
    # User triggered to enter this plugin page, all function should be activated
    pass

```