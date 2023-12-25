#CasaValldoreix

## Download Home Assistant

1. Image should be aarch64 & qcow2 format (haos_generic-aarch64-VERSION.qcow2)
2. Extract the Image

## Create the Virtual Machine

1. Download UTM
2. Create new Machine
3. Name it Home Assistant
4. Choose "Virtualize"
5. Check "open settings"
6. In Network, choose "Bridge (advanced)"
7. Specifty en0 if ethernet 
9. Delete de the default drive
10. Create a new drive VirtIO, import the Home Assistant image (qcow2)
11. Go to the disk create, resize it to minimum 32
12. Start the machine

## Advanced mode
1. In User Profile, enable 'Advanced Mode'

## Install Add-ons
In Parameters > Add-on, install
1. File Editor
2. Terminal & SSH

## Install HACS
Link to instructions : https://hacs.xyz/docs/setup/download/
1. Go to Terminal & SSH add-on
2. Open termin
3. Execute 'wget -O - https://get.hacs.xyz | bash -'
4. Restart

## Install & Configure Huawey Solar
1. In HACS, search for Huwaey Solar
2. Install
3. Restart HA
4. Go to Devices & Services
5. Add Huawey Solar
6. Select Network
7. IP : 192.168.1.61
8. Port : 502
9. Slave ID
10. Submit

## Install & Configure Tesla
1. Go to HACS
2. Search for Tesla
3. Dowland
4. Restart
5. Go to Devices & Services
6. Install Tesla
7. Specify Login & Token
8. Submit
Note : get token from https://chromewebstore.google.com/detail/access-token-generator-fo/


# Install Live Energy Flow
1. Install Power Flow Card Plus (https://github.com/flixlix/power-flow-card-plus) via HACS
2. Configuration YAML (also available through the UI)
3. Create the Flow Card 
```       - type: custom:power-flow-card-plus
            entities:
              grid:
                entity: sensor.power_meter_active_power
                invert_state: true
                color_value: true
              solar:
                entity: sensor.inverter_active_power
                display_zero_state: true
                color_icon: false
                color_value: false
              home: {}
              individual1:
                entity: sensor.charger_power
            clickable_entities: true
            display_zero_lines:
              mode: show
              transparency: 50
              grey_color:
                - 189
                - 189
                - 189
            use_new_flow_rate_model: true
            w_decimals: 0
            kw_decimals: 1
            min_flow_rate: 0.75
            max_flow_rate: 6
            max_expected_power: 2000
            min_expected_power: 0.01
            watt_threshold: 1000
            transparency_zero_lines: 0
```

# Add Reolink Camera
1. Add simply a Reolink Camera using IP, 'admin' as user and "SHR**29*" as pwd
2. IP Portail : 192.168.1.143

3. 
     
