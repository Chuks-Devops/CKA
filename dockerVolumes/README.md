# Docker Volumes

## 2 Types of Layers
- Image layer (Readonly Layer) - Changes can not be made on this layer. This layers combine to make up container layer. They are created with the help of storage drivers

- Container Layer (Writable Layer) - This layer is writable. that is one can make changes to this layer. 

## 2 Types of Drivers
- Storage Drivers - This is used to data to container layer. Example (Overlay2, zfs, vfs)

- Volume Driver - This is use to make the data in the layers persistent. Example (aufs, devicemapper).

## To create a volume
```
sudo docker volume create data-volume
```
## Everything in docker resides on 
```
cd /var/lib/docker
``` 

## To mount container volume to docker volume

```
docker run -p 3000:3000 -v data-volume:/app -d