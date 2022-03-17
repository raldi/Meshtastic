---
id: serial-module
title: Serial Module Settings
sidebar_label: Serial Module
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

:::warning
GPIO access is fundamentally dangerous because invalid options can physically damage or destroy your hardware. Ensure that you fully understand the schematic for your particular device before trying this as we do not offer a warranty. Use at your own risk.
:::

:::note
This module requires attaching a peripheral accessory to your device. It will not work without one.
:::

:::note
This module has not been implemented yet. Even if you enable the serial module, nothing will happen.  
:::


## Overview

This is a simple interface to send messages over the mesh network by sending strings over a serial port. 

:::tip
Once module settings are changed, a **reset** is required for them to take effect.
:::

:::tip
Connect the TX pin to the other device's RX pin, and vice versa. Connect their grounds to each other (not necessary if they're both plugged into the same USB power source.)
:::

## Settings

|        Setting        |  Acceptable Values  | Default |
| :-------------------: | :-----------------: | :-----: |
| serial_module_enabled |   `true`, `false`   | `false` |
|  serial_module_echo   |   `true`, `false`   | `false` |
|  serial_module_mode   |      `integer`      |   `0`   |
|   serial_module_rxd   |  `integer` (GPIO)   |   `0`   |
| serial_module_timeout | `integer` (seconds) |   `0`   |
|   serial_module_txd   |  `integer` (GPIO)   |   `0`   |

### serial_module_enabled

Enables the module.

<Tabs
groupId="settings"
defaultValue="cli"
values={[
{label: 'CLI', value: 'cli'},
{label: 'Android', value: 'android'},
{label: 'iOS', value: 'iOS'},
{label: 'Web', value: 'web'},
]}>
<TabItem value="cli">

```bash title="Enable module"
meshtastic --set serial_module_enabled true
```

```bash title="Disable module"
meshtastic --set serial_module_enabled false
```

  </TabItem>
  <TabItem value="android">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="iOS">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="web">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
</Tabs>

### serial_module_echo

If set, any packets you send will be echoed back to your device.

<Tabs
groupId="settings"
defaultValue="cli"
values={[
{label: 'CLI', value: 'cli'},
{label: 'Android', value: 'android'},
{label: 'iOS', value: 'iOS'},
{label: 'Web', value: 'web'},
]}>
<TabItem value="cli">

```bash title="Enable serial_module_echo"
meshtastic --set serial_module_echo true
```

```bash title="Disable serial_module_echo"
meshtastic --set serial_module_echo false
```

  </TabItem>
  <TabItem value="android">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="iOS">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="web">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
</Tabs>

### serial_module_mode

<!--- TODO --->

<Tabs
groupId="settings"
defaultValue="cli"
values={[
{label: 'CLI', value: 'cli'},
{label: 'Android', value: 'android'},
{label: 'iOS', value: 'iOS'},
{label: 'Web', value: 'web'},
]}>
<TabItem value="cli">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="android">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="iOS">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="web">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
</Tabs>

### serial_module_rxd

Set the GPIO pin to the RXD pin you have set up.

:::caution
To prevent damaging your device, double check your device's schematics before attaching to the GPIO pins and setting this value.
:::

<Tabs
groupId="settings"
defaultValue="cli"
values={[
{label: 'CLI', value: 'cli'},
{label: 'Android', value: 'android'},
{label: 'iOS', value: 'iOS'},
{label: 'Web', value: 'web'},
]}>
<TabItem value="cli">

:::note
Replace `GPIO` in the below command with the GPIO number your circuit is attached to.
:::

```bash title="Set RXD to GPIO pin number"
meshtastic --set serial_module_rxd GPIO
```

  </TabItem>
  <TabItem value="android">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="iOS">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="web">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
</Tabs>

### serial_module_timeout

The amount of time to wait before we consider your packet as "done".

<Tabs
groupId="settings"
defaultValue="cli"
values={[
{label: 'CLI', value: 'cli'},
{label: 'Android', value: 'android'},
{label: 'iOS', value: 'iOS'},
{label: 'Web', value: 'web'},
]}>
<TabItem value="cli">

```bash title="Set serial_module_timeout to 15 seconds"
meshtastic --set serial_module_timeout 15
```

  </TabItem>
  <TabItem value="android">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="iOS">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="web">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
</Tabs>

### serial_module_txd

Set the GPIO pin to the TXD pin you have set up.

:::caution
To prevent damaging your device, double check your device's schematics before attaching to the GPIO pins and setting this value.
:::

<Tabs
groupId="settings"
defaultValue="cli"
values={[
{label: 'CLI', value: 'cli'},
{label: 'Android', value: 'android'},
{label: 'iOS', value: 'iOS'},
{label: 'Web', value: 'web'},
]}>
<TabItem value="cli">

:::note
Replace `GPIO` in the below command with the GPIO number your circuit is attached to.
:::

```bash title="Set TXD to GPIO pin number"
meshtastic --set serial_module_txd GPIO
```

  </TabItem>
  <TabItem value="android">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="iOS">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
  <TabItem value="web">

:::info
Configuring this setting is not yet available for the selected platform. If this is incorrect please update the documentation for this page.
:::

  </TabItem>
</Tabs>
