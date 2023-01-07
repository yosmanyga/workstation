# Stop

systemctl stop docker

# Config

touch /etc/docker/daemon.json
nano /etc/docker/daemon.json
{
 "data-root": "/mnt/volume_nyc1_01/docker"
}

# Move data

rsync -a /var/lib/docker/ /mnt/volume_nyc1_01/docker/
chown -R root:root /mnt/volume_nyc1_01/docker/
chmod -R 755 /mnt/volume_nyc1_01/docker/

# Start

systemctl daemon-reload
systemctl restart docker

# Verify

docker info | grep "Docker Root Dir"
