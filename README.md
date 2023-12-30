# efs-mount

## Following are the commands to mount EFS (Elastic File System on Ubuntu)

#### Install Essential Utilities

```sh
sudo apt-get update
sudo apt-get -y install git binutils
git clone https://github.com/aws/efs-utils
cd efs-utils/
./build-deb.sh
sudo apt-get -y install ./build/amazon-efs-utils*deb
cd ..
```

#### Create any directory (efs in our case) and mount

```sh
sudo mkdir efs
sudo mount -t efs EFS_FILE_SYSTEM_ID efs/
```
> **Note** : EFS_FILE_SYSTEM_ID looks something like fs-05f0e931af63cf504
