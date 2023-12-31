# Venice

This GitHub organisation aims at studying how to enable device-to-device communication between smartphones and desktop computers.

Each one of its repositories hosts a communication channel, leveraging a D2D technology such as Bluetooth; you'll also find an example application allowing file exchange between devices using channels of your choice.


### Context

There are lots of device-to-device technologies out there, ready to be used, such as Wi-Fi, NFC, Bluetooth etc;
there are also lots of use-cases that could leverage those technologies, but we feel like something is missing in between.

![A link layer abstraction is missing between D2D tech and opportunistic networks.](https://raw.githubusercontent.com/Venice-D2D/.github/main/profile/img/missing_layer.png)

To solve that problem, we propose the Venice framework, an abstraction layer that allows applications to manipulate communication technologies
through the use of channels.


### Some vocabulary

A [channel](https://github.com/Venice-D2D/venice_core/blob/master/lib/channels/abstractions/channel.dart) is an object that encapsulates a device-to-device physical communication technology (Bluetooth or Wi-Fi, for instance), to
send data from user A to user B.

This framework makes use of two different channel types, bootstrap channels and data channels.
**Bootstrap** channels transmit metadata about communication exchanges and data channels (*e.g.* authentication data required to open a Wi-Fi connection);
**Data** channels do have a greater throughput than bootstrap channels, and are typically intented to carry payload data between nodes.


### Implementation

#### List of communication channels

##### Bootstrap channels

* Bluetooth Low Energy: https://github.com/Venice-D2D/ble_bootstrap_channel
* QR code: https://github.com/Venice-D2D/qr_code_bootstrap_channel

##### Data channels

* Wi-Fi (hotspot): https://github.com/Venice-D2D/wifi_data_channel

#### Demo app

This organization includes a demonstration app that showcases all mentioned channels; it's located here: https://github.com/Venice-D2D/venice_demo_app.

Here is a video showing how channels can be leveraged to exchange data between two phones:

https://github.com/Venice-D2D/.github/assets/11993538/c05c4c3f-7d7f-47c7-bcdf-b14ed4491ef9

