# 'Could not get lock /var/lib/dpkg/lock-frontend' error in Linux

## 1. Kill all apt-get process

```
sudo killall apt apt-get
```

## 2. Delete directories

```
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock*
```

## 3. Finish

```
sudo dpkg --configure -a
sudo apt update
```
