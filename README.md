# Nibe myUplink add-on for Home Assistant

Nibe myUplink add-on for Home Assistant

### How to build

Bash:

```bash
cd addon
current_dir=$(pwd)

docker run --rm -ti --name hassio-builder --privileged \
  -v $current_dir/addon:/data \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  homeassistant/amd64-builder -t /data --all --test \
  -i nibe-myuplink-{arch} -d local
```

PowerShell:

```powershell
cd addon
$current_dir=(pwd).Path

docker run --rm -ti --name hassio-builder --privileged `
  -v "$($current_dir):/data" `
  -v /var/run/docker.sock:/var/run/docker.sock:ro `
  homeassistant/amd64-builder -t /data --all --test `
  -i "nibe-myuplink-{arch}" -d local
```

Bash / Linux:

```bash
docker run --rm -v /tmp/my_test_data:/data local/nibe-myuplink-amd64:1
```

PowerShell / Windows

```powershell
docker run --rm -v c:\temp\my_test_data:/data local/nibe-myuplink-amd64:1
```
