# List disk usage
df -h

# Disk Usage Analyzer (gdu)
docker run --rm --init --interactive --tty --privileged \
--volume /:/mnt/root \
ghcr.io/dundee/gdu /mnt/root