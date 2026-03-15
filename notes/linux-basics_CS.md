# explanation of concepts / notes

## HOST 
- fyzický stroj
- tvůj Windows + Hyper-V
- vlastní CPU, RAM, disky

## GUEST
- virtuální server
- běží uvnitř hosta
- myslí si, že je samostatný počítač

## Hypervisor 
- software, který:
  * rozděluje CPU
  * rozděluje RAM
  * vytváří virtuální síť
  * izoluje VM od sebe
- typy:
  * Hyper-V => běží přímo na HW
  * VirtualBox, VMware -> běží na OS

## Výhody virtualizace
- izolace workloadů (Workload = běžící systém nebo aplikace -> např. web server, databáze, AD server…)
- rychlé provisioning (vytvoření a připravení serveru k použití)
- snapshoty
- disaster recovery
- efektivní využití HW
- škálovatelnost

## root 
- správce
- UID 0 -> absolutní kontrola nad systémem.
- může:
  * mazat jádro
  * měnit síť
  * měnit uživatele
  * vypnout bezpečnostní mechanizmy
- proč pod ním nepracovat:
  * auditovatelnost (víš, kdo co provedl)
  * princip least privilege
  * bezpečnost

## SWAP
- odkládací prostor na disku, který simuluje RAM
- když dojde RAM, systém přesune méně používaná data do swapu
- zachrání systém před pádem, ale zpomalí výkon
- proč existuje: 
  * ochrana proti OOM (Out Of Memory)
  * stabilita serveru
  * některé služby ho vyžadují
  * zjištění swap: free -h

## Kernel
- jádro systému
- spravuje CPU scheduling
- spravuje paměť (RAM)
- komunikuje s hardwarem přes drivery
- spravuje procesy
- spravuje souborové systémy
- spravuje síť
- zjištění verze kernelu: uname -r

## Filesystem
- způsob, jakým jsou data organizována na disku
- nap%r: ext4 (nejčastěji v Linuxu), xfs (často u Fedory), btrds, ntfs (Windows)
- určuje jak se ukládají soubory, jak fungují práva, jak se řeší žurnálování
- zjistíme příkazem: df -T, nebo lsblk -f

## Rozsah IP 
- používá se pro určení, která zařízení jsou ve stejné síti, kam se posílá traffic
- zjistíme příkazem: ip a

