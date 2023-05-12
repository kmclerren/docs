# KVM

* Example bridge config
    <network>
     <name>br1</name>
     <forward mode='bridge'/>
     <bridge name='br1'/>
    </network>

* Define a new network
    virsh net-dumpxml default > br1.xml
    vi br1.xml (edit to specification)
    virsh net-define br1.xml
    virsh net-start br1
    virsh net-autostart br1


* Attach additional interfaces example
    virsh shutdown <domain>
    virsh attach-interface --domain <domain> --type bridge --source br1 --model virtio --config
    virsh start <domain>

* Disable VNC after install
