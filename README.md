# Tutorial-Minima

### Daftar Minima
https://incentive.minima.global/account/register?inviteCode=NPE3GKBA

![image](https://user-images.githubusercontent.com/91402307/195984986-9b37768d-9b41-4930-9e40-02e3b150e1f4.png)

### Setelah daftar pilih Linux VPS/Raspberry Pi

![image](https://user-images.githubusercontent.com/91402307/195985029-70ef9743-3771-407e-bfa3-8b698b86206b.png)
 

### Update dan Install Curl
```
sudo apt-get update
sudo apt install curl 
```

### Install Minima
```
wget -O minima_setup.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_setup.sh && chmod +x minima_setup.sh && sudo ./minima_setup.sh -p 9001 
```
Disini membutuhkan waktu kurang lebih 30 menit, kalau sudah CTRL+C aja buat ke next step.

### Pilih ID Incentive dan Copy

![image](https://user-images.githubusercontent.com/91402307/195985231-cafe092f-962a-4993-bd59-1e7c014d669e.png)


### Mengatur ID Incentive xxx diganti dengan ID Incentive mu
```
curl 127.0.0.1:9005/incentivecash%20uid:xxx-xxx-xxx-xxx-xxx
```

### Cek Status Versi 
```
curl 127.0.0.1:9005/status
```

### Cek Reward
```
curl 127.0.0.1:9005/incentivecash | jq
```
Setiap Hari akan mendapatkan 1Coin Minima

### Check log
```
journalctl -u minima_9001 -f
```

### Updrage Node
```
sudo systemctl stop minima_9001
```
```
sudo rm -rf /home/minima/.minima*
```
```
sudo systemctl start minima_9001
```
Masukkan kembali ID Incentive 
```
curl 127.0.0.1:9005/incentivecash%20uid:xxx-xxx-xxx-xxx-xxx
```

### Delete Node
```
wget -O minima_remove.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_remove.sh && chmod +x minima_remove.sh && sudo ./minima_remove.sh -p 9001 -x
```
```
sudo rm -rf /home/minima
```
```
sudo userdel minima
```
