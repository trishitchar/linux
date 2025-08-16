# git && github
```bash
git config --global user.name "trishitchar"
git config --global user.email "trishitchar@gmail.com"
git config --global --list
```
```bash
ssh-keygen -t ed25519 -C "trishitchar@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
ssh -T git@github.com
```

# Out of Memory issue (OOM) - earlyoom
```bash
sudo apt install earlyoom
sudo systemctl enable --now earlyoom
sudo nano /etc/default/earlyoom
```
- EARLYOOM_ARGS="-r 3600" ----> EARLYOOM_ARGS="-m 20 -s 20 -r 60"
```bash
sudo systemctl restart earlyoom
systemctl status earlyoom
journalctl -u earlyoom -f
```

Tools:
1. CopyQ
2. FlameShot
