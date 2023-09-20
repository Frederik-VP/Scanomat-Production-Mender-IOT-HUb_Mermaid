
1. Machine power gets switched on
2. After boot, connects to hardcoded SSID of Scanomat 
3. Should probably go into some kind of factory mode
3. Handshakes with Mender 
4. Mender creates instance of machine in IOT HUB (integration)
5. Factory SW tool programs serial, model, recipee and setup
6. Data gets synced with IOT HUB / Device Twin
7. Machine leaves factory mode, before ready to ship (resets counters etc)


```mermaid
sequenceDiagram
    Note left of client: Machine power get switched on
    Note left of client: After boot, connects to hardcoded SSID/Wifi of
    Note left of client: Goes into Factory mode Scanomat
    
    client ->> Mender : Handshakes with Mender 

    Mender ->> IOT HUB: Creates instance of machine in IOT HUB
    
    Note left of client:.
    Note left of client:.
    
    Factory Tool ->> client: Factory SW tool programs serial, model, recipee and setup
    
    Note left of client: After upload machine changes state

    client ->> IOT HUB: Data gets synced with IOT HUB / Device Twin

    Note left of client: Machine leaves factory mode, before ready to ship (resets counters etc)    

    
```






