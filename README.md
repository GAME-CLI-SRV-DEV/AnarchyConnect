# AnarchyConnect
a [CForms](https://github.com/kejonaMC/CrossplatForms) or [ViaProxy](https://github.com/viaversion/viaproxy) Powered Geyser-ViaProxy Service Connection Manager For TRUE ANARCHIST
(USED FOR CONNECTING TO CRACKED ANARCHY SERVER)

# Using With Geyser-ViaProxy
ViaProxy plugin version of AnarchyConnect relys on ViaProxy and GeyserMC, if Geyser-ViaProxy is not installed, then you can't use it.

1. Download AnarchyConnect-3.3.3-G2.4.0-SNAPSHOT.jar
2. Put it in ViaProxy Folder
3. if you join 127.0.0.1.nip.io:25567 then you will be greeted with this form.
 ![image](https://github.com/user-attachments/assets/614c4b35-b17f-4441-a4cf-dcb3aa4e0bd8)

4. register your account(the [minecraftauth](https://github.com/raphimc/minecraftauth) will handle it)
5. now you can join any server. Reminder: join only anarchy servers. if you join big java servers, their anticheat may ban you.

WARNING! The Server May ban your ip or username! Please Be Careful!

# Use on your server
Copy this.
```
  connect:
    type: custom_form
    title: AnarchyConnect
    components:
      - type: label
        text: "Make Sure You are hosting ViaProxy Servers, Wildcard Domain Handler is Public on ViaProxy, and forward-hostname is true on geyser Before You &bRegister&r On This Panel."

      - type: input
        text: Address
        placeholder: address
        parsers:
          - type: block-placeholders

      - type: input
        text: Port
        placeholder: port
        default-text: 19132
        parsers:
          - type: block-placeholders

      - type: dropdown
        text: "Release 1.7-1.21.1"
        default-option: 0
        options:
          - "1.21.1"
          - "1.20.6"
          - "1.20.4"
          - "1.20.2"
          - "1.20.1"
          - "1.19.4"
          - "1.19.3"
          - "1.19.2"
          - "1.18.2"
          - "1.18.1"
          - "1.17.1"
          - "1.17"
          - "1.16.5"
          - "1.16.3"
          - "1.16.2"
          - "1.16"
          - "1.15.2"
          - "1.15.1"
          - "1.15"
          - "1.14.4"
          - "1.14.3"
          - "1.14.2"
          - "1.14.1"
          - "1.14"
          - "1.13.1"
          - "1.13"
          - "1.12.2"
          - "1.12.1"
          - "1.12"
          - "1.11.2"
          - "1.11"
          - "1.10.2"
          - "1.9.4"
          - "1.9.2"
          - "1.9.1"
          - "1.9"
          - "1.8.9"
          - "1.7.10"
          - "1.7.2"

      - type: dropdown
        text: "VSP(Viaproxy Service Provider)"
        default-option: 0
        options:
          - "raphimc.net"
          - "localho.st"
  
      - type: input
        text: Viaproxy Service Port
        placeholder: ViaProxy Service Port
        default-text: 25568
        parsers:
          - type: block-placeholders

    actions:
      - message: "Sending you to %result_1%_%result_2%_%result_3%.viaproxy.%result_4%:%result_5%"
      - type: transfer_packet
        address: "%result_1%_%result_2%_%result_3%.viaproxy.%result_4%"
        port: "%result_5%"
```

# Public AnarchyConnect
To use Public AnarchyConnect, you have to join Approximaster Anarchy 2004. This Anarchy server attached anarchyconnect to Recovery Compass.

To Use Public AnarchyConnect On Other Server, You Must Be Able to install Crossplatforms in the server.

1. to join your server for testing, use localhost option.
2. to join the registeration test server of AnarchyConnect, use 2406-5900-102c-49d-70b9-1348-7da2-125e.sslip.io(IPv6)
3. to use old ViaProxyConnect to Connect, use RaphiMC.net(Shutted Down Permanently before 1.20.3/4)

# To Use:
AnarchyConnect Supports 1.7-1.21.1 and Based on ViaProxy Public Wildcard Domain(address_port_version.viaproxy.hostname) Generator.

1. address: No Defaults. you have to fill the address.
2. port: default is 19132(BE), Change it to 25565 if JE.
3. Version: select the Version. 1.21.1 is default
4. viaproxy address: select localho.st unless your server is registered to your server.
5. viaproxy port: default is 25568(ViaProxy_JE), Change it if require.
6. Click Submit Button. you will be connecting to address_port_version.viaproxy.hostname:25568/19132.

# Conversion:
address: myserver.com
port: 25565
Version: 1.21.1
VSP: localho.st
VSPPort: 19132 -> myserver.com_25565_1.21.1.viaproxy.localho.st:19132.

the action translates your 5 input data to the %result_1%_%result_2%_%result_3%.viaproxy.%result_4%:%result_5% and sends you there.
# Register your VSP
your server must be registered to use in Public without localho.st.

To Register, Your ViaProxy Server Must Run ViaProxy(With Geyser-ViaProxy) and Use ViaProxy Public Wildcard Domain(address_port_version.viaproxy.hostname). forward-hostname should be true on geyser. otherwise, you cannot register.
