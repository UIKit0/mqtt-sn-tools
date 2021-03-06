Command line tools written in C for the MQTT-SN (MQTT for Sensor Networks) protocol.

Supported Features
------------------

- QoS 0 and -1
- Keep alive pings
- Publishing retained messages
- Publishing empty messages
- Subscribing to named topic
- Clean / unclean sessions
- Manual and automatic client ID generation
- Displaying topic name with wildcard subscriptions
- Pre-defined topic IDs and short topic names


Limitations
-----------

- Packets must be 255 or less bytes long
- No Last Will and Testament
- No QoS 1 or 2
- No Automatic gateway discovery


Building
--------

Just run 'make' on a POSIX system.


Publishing
----------

    Usage: mqtt-sn-pub [opts] -t <topic> -m <message>

      -d             Enable debug messages.
      -h <host>      MQTT-SN host to connect to. Defaults to '127.0.0.1'.
      -i <clientid>  ID to use for this client. Defaults to 'mqtt-sn-tools-' with process id.
      -m <message>   Message payload to send.
      -n             Send a null (zero length) message.
      -p <port>      Network port to connect to. Defaults to 1883.
      -q <qos>       Quality of Service value (0 or -1). Defaults to 0.
      -r             Message should be retained.
      -t <topic>     MQTT topic name to publish to.
      -T <topicid>   Pre-defined MQTT-SN topic ID to publish to.


Subscribing
-----------

    Usage: mqtt-sn-sub [opts] -t <topic>

      -1             exit after receiving a single message.
      -c             disable 'clean session' (store subscription and pending messages when client disconnects).
      -d             Enable debug messages.
      -h <host>      MQTT-SN host to connect to. Defaults to '127.0.0.1'.
      -i <clientid>  ID to use for this client. Defaults to 'mqtt-sn-tools-' with process id.
      -k <keepalive> keep alive in seconds for this client. Defaults to 10.
      -p <port>      Network port to connect to. Defaults to 1883.
      -t <topic>     MQTT topic name to subscribe to.
      -T <topicid>   Pre-defined MQTT-SN topic ID to publish to.
      -v             Print messages verbosely, showing the topic name.


License
-------

MQTT-SN Tools is licensed under the [BSD 2-Clause License].



[BSD 2-Clause License]: http://opensource.org/licenses/BSD-2-Clause
