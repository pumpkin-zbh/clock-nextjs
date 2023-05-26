# Hello World

### Through MicorPython programming, various display functions of LCD are realized, including printing characters, drawing points, lines, rectangles, circles, displaying pictures, etc.

```python
import logging
import modules.common.color as color
from modules.service.time_service import TimeService
import uasyncio

TITLE = "Hello World"
initialized = None
lasttime = 0
counter = 0

#################################################


async def on_refresh(screen, config):
    global initialized, counter, lasttime

    if not initialized:
        initialized = True
        screen.fill(color.ORANGE) # clear screen

    now = TimeService().get_epoch()
    if now % 1 == 0 and now != lasttime:
        logging.debug("@%d", now)
        lasttime = now
        counter += 1
        screen.print_str("Hello Vobot!", 5, 80, color.WHITE, backColor=color.ORANGE, fontId=3)
        screen.print_str(str(counter), 5, 120, color.WHITE, backColor=color.ORANGE, fontId=3)

        # await uasyncio.sleep(2)
        # screen.picture(0, 0, "/data/picture/xx/xx.jpg")
        # await uasyncio.sleep(2)
        # screen.draw_pixel(x, y, color)
        # await uasyncio.sleep(2)
        # screen.draw_circle(x, y, r, color, border=1, fill_color=None)
        # await uasyncio.sleep(2)
        # screen.draw_rect(x, y, width, height, color, border, fillcolor)
        # screen.draw_line(sex0, y0, x1, y1, color)


async def on_selected(scr, config):
    pass


async def on_leave(screen, config):
    global initialized
    initialized = False


async def on_enter(screen, config):
    pass


async def on_boot(screen, config):
    pass

```