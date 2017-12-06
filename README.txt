DomoticMQTTEcosystem

A suite for getting a mqtt system in home.
- DomoticBoards is the software for sensors or actuators.
- MQTTNetworkSW is the software to execute on a local host.


Endpoint list 2017/08/09

- remoteboard protocol
    retained data:
        {
            "stato": "ON"/"OFF"
            "ts": 32143243324
        }
    command:
        {
            "cmd": "ON"/"OFF"/"SW"/"TON"/"TOFF"
            "payload": 5
        }

- actuator
    no retained data: (missing sensor)
    command:
        publish something to:
            topic.../apri
            topic.../trigger

- sensor + actuator | 
    retained data on topic topic../stato {aperto|chiuso} state
    command:
        publish something to:
            topic.../apri
            topic.../chiudi
            topic.../trigger

