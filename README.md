Debian sources.list dotfiles
======

Working Debian 6 (Squeeze) - Debian 12 (Bookworm) sources.list dotfiles to replace the sources.list in your /etc/apt folder on your Debian server.

## Usage:
Navigate to the `/etc/apt` folder.Backup your current `sources.list` file.
```bash
cd /etc/apt
```

</br>

Backup your current `sources.list` file first.
```bash
mv sources.list sources.list_old
```

</br>

Retrieve the new `sources.list` file based on your Debian server version.

**For Debian 6 (Squeeze)**
> [!IMPORTANT]
> Please update manually.
> 
> Reason is, OpenSSL 0.9.8 supports only TLS 1.0 and lower protocol versions (i.e. SSL 3.0), so there is no way to connect with a TLS 1.0 client to github.com, which itself does not longer support the TLS 1.0 protocol.

</br>

**For Debian 7 (Wheezy)**
```bash
wget https://raw.githubusercontent.com/tkne/debian-sources/main/sources.list.debian7 -O /etc/apt/sources.list
```

</br>

**For Debian 8 (Jessie)**
```bash
wget https://raw.githubusercontent.com/tkne/debian-sources/main/sources.list.debian8 -O /etc/apt/sources.list
```

</br>

**For Debian 9 (Stretch)**
```bash
wget https://raw.githubusercontent.com/tkne/debian-sources/main/sources.list.debian9 -O /etc/apt/sources.list
```

</br>

**For Debian 10 (Buster)**
```bash
wget https://raw.githubusercontent.com/tkne/debian-sources/main/sources.list.debian10 -O /etc/apt/sources.list
```

</br>

**For Debian 11 (Bullseye)**
```bash
wget https://raw.githubusercontent.com/tkne/debian-sources/main/sources.list.debian11 -O /etc/apt/sources.list
```

</br>

**For Debian 12 (Bookworm)**
```bash
wget https://raw.githubusercontent.com/tkne/debian-sources/main/sources.list.debian12 -O /etc/apt/sources.list
```

</br>

Update from the new list:
```bash
apt update
```
or
```bash
apt-get update
```

</br>

Upgrade from the new list:
```bash
apt upgrade
```
or
```bash
apt-get upgrade
```

</br>

You can also edit and/or update your existing `sources.list` file manually if you prefer to do it that way.