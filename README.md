#CasaValldoreix

## Download Home Assistant

1. Image should be aarch64 & qcow2 format
2. Unzip the Image

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

###

