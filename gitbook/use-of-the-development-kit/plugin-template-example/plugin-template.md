# Template of Plugin

### Each plugin can be modified according to the current template and uploaded to Vobot Clock Tiny

```python
TITLE = "Template of Plugin"

async def on_boot(screen, config):
    # called right after system boot
    print('on init')

async def on_refresh(screen, config):
    # Once active, called by system every 200ms
    print('on refresh')


async def on_selected(screen, config):
    # User just pressed the button for 1 second
    print('on selected')


async def on_leave(screen, config):
    # User triggered to leave this plugin page, all function should be deactivated
    print('on leave')


async def on_enter(screen, config):
    # User triggered to enter this plugin page, all function should be activated
    print('on enter')

```