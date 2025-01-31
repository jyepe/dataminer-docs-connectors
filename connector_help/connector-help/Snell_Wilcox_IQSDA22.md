---
uid: Connector_help_Snell_Wilcox_IQSDA22
---

# Snell Wilcox IQSDA22

The **Snell Wilcox IQSDA22** connector monitors and configures the IQSDA22 amplifier device.

## About

The connector polls all parameters once after startup. After this, parameter updates depend on event messages generated by the device when a parameter changes. However, it is possible to manually trigger the polling of all parameters with the **Force Poll** button on the General page.

### Version Info

| Range | Description | DCF Integration | Cassandra Compliant |
|----------------------|-----------------|---------------------|-------------------------|
| 1.0.0.x \[SLC Main\] | Initial version | No                  | Yes                     |

### Product Info

| Range | Supported Firmware Version |
|------------------|-----------------------------|
| 1.0.0.x          | V115                        |

## Installation and configuration

### Creation

#### Serial Main Connection

This connector uses a single smart-serial connection and requires the following input during element creation:

SERIAL CONNECTION:

- Interface connection:

  - **IP address/host:** The polling IP of the device.
  - **IP port:** The IP port of the device, by default *2050*.
  - **Bus Address:** The bus of the card on the chassis. The default, *UU.PP*, shows the expected structure of the address, where *UU* is the chassis ID, and the *PP* is the card position, both in hex.

## Usage

### General

This page contains general information about the device, such as the various **versions**, the **Serial Number**, the **Build Number**, and more. It also contains **connection info**, **information display** and **Simulated RollCall response**. The latter allows you to set a custom response that will be handled by the connector as if it were received by the device. The tooltip for this functionality displays more information.

The page also includes the following buttons:

- **Restart**: Restarts the device.
- **Force** **Poll**: Repolls the device.
- **Factory Defaults**: Sets all settings back to the factory default.

### Input

This page allows you to enable various settings related to each different input. You can switch the SDI input rate, mute the output, switch the input name, and specify what should happen on input loss.

### Memories

On this page, you can **select** a memory (1-16) and edit its name, **recall** a previous memory (if available), and also view the **Last User Memory**.

The page includes the following buttons:

- **Save Memory**: Saves the current memory name.
- **Clear Memory**: Clears the current memory.

### RollTrack

This page contains various RollTrack controls, such as the **Address**, **Command**, **Disable all**, **Index**, and **Source**. It also displays the **Status** and the **Sending** status.

### Logging

This page displays **Misc** and **Input 1** information as well as controls to enable/disable the logging of this information.

### Web Interface

This page displays the web interface of the device. Note that the client machine has to be able to access the device, as otherwise it will not be possible to open the web interface.
