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

### Install HACS
Link to instructions : https://hacs.xyz/docs/setup/download/
1. Go to Terminal & SSH add-on
2. Open termin
3. Execute 'wget -O - https://get.hacs.xyz | bash -'
4. Restart
