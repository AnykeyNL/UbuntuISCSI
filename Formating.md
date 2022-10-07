sudo apt install nvme-cli

nvme format /dev/nvme0n1
(echo g; echo n; echo p; echo 1; echo ""; echo ""; echo w; echo q) | fdisk /dev/nvme0n1
mkfs.ext4 /dev/nvme0n1p1

mkdir /nvme
mount /dev/nvme0n1p1 /nvme

