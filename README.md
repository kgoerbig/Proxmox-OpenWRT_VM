Both scripts are designed to be executed via Proxmox terminal. Two scripts are available to build a Proxmox OpenWRT VM, one for the Official release, and the other for snapshot.

1. Edit directory storage details in the script to match your own setup (i.e. /mnt/1TB ), and define the variables at the top:

# Define variables
VM_ID=101
VM_NAME="OpenWRT-Prox-Snap"
VM_MEMORY=256
VM_CPU=4
VM_DISK_SIZE="500M"
VM_NET="model=virtio,bridge=vmbr0,macaddr=BC:24:11:F8:BB:28"
VM_NET_a="model=virtio,bridge=vmbr1,macaddr=BC:24:11:35:C1:A8"
STORAGE_NAME="local-lvm"
VM_IP="192.168.1.1"
PROXMOX_NODE="PVE"


3. Download the file to /usr/local/bin or /usr/bin

4. Make it writable. chmod +x <filename>

5. Run the script
