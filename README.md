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
