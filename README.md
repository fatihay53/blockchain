# blockchain
mydexchain


chain adress number: XMD0f13e2b3-a536-11eb-9a3b-02ca075254e8

tracker number: f09017dca53f11eb9a3b02ca075254e8icARvV6zur

9e82dce4aa8611eb9a3b02ca075254e82cw4Hkcg7q



free -m 									Ram Bilgisi Gösterir
top										Cpu Kullanım Gösterir
docker system df 								Herşeyin(Konteyner,Images vb) Bilgisini Gösterir
docker system info								Sistemin Bilgisini Gösterir

docker ps --filter "status=exited"						Çalışmayan Kontainerleri Listeler
docker ps -f "status=exited"							Çalışmayan Kontainerleri Listeler

docker container ls -a								Bütün Konteynerları Listeler(Çalışan-Çalışmayan Hepsi)
docker rm $(docker ps -aqf status=exited)					Çalışmayan Kontainerleri Siler
docker rm $(docker ps --filter status=exited -q)				Çalışmayan Kontainerleri Siler
docker rm -v containername							Seçilen konteyneri ve kapladığı alanı siler

docker start $(docker ps -a -q --filter "status=exited")			Duran Konteynerları Çalıştırır
docker restart $(docker ps -a -q)  						Bütün Konteynerları Yeniden Başlatır
docker container prune								Bütün Durmuş Konteynerları Siler
docker stop $(docker ps -a -q)						Bütün Konteynerları Dudurur

docker container rm $(docker ps -a -q) 			 		Bütün Konteynerları Durdurur(Çalışan-Çalışmayan Hepsi)
docker image prune										KullanılMayan imageleri Siler
docker rmi $(docker images -q)							Bütün İmageleri Siler(Çalışan-Çalışmayan Hepsi)

docker update --restart unless-stopped $(docker ps -q)   			Server Reboot edince otomatik konteyner başlatma kodu
docker update --restart=no $(docker ps -a -q)					Otomatik Restart Kodunu Kapatır
docker update --restart=always $(docker ps -a -q --filter "status=exited")	Exited-Düşen Konteynerlari Otomatik Başlatır	
			
docker volume prune								Remove all volume
docker network prune								Remove all network

docker system prune								- all stopped containers
       										- all networks not used by at least one container
        									- all dangling images
        									- all build cache

docker system prune --volumes							- all stopped containers
       										- all networks not used by at least one container
      										- all volumes not used by at least one container
											- all dangling images
											- all build cache						

docker pull mydexchain/mydexchain            update image



docker run -d -p 2020:2020 -p 2053:3030 -v mydexchain:/var/lib/postgresql/ --privileged --log-driver=none --name mydexchain mydexchain/mydexchain:latest
 


PowerShell Üzerinden MasterTracker Komutu  & işaret %26 olarak yazilacak powershelle
curl http://localhost:2020/setDextracker/f09017dca53f11eb9a3b02ca075254e8icARvV6zur
curl http://localhost:2020/setStartDXCMiner/
curl http://localhost:2020/setStartPRXMiner/
curl http://localhost:2020/setMasterTracker/%20%20%20%20%20havuz1%26Havuz1-home:2053%261



sudo apt-get purge docker-ce docker-ce-cli containerd.io 	Uninstal Docker
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd



/setJoinPool/3c0882c9-bd17-11eb-9a3b-02ca075254e8





ufw status 

ufw disable (Y)



apt update
apt upgrade

apt install docker.io -y
systemctl enable --now docker
systemctl start docker
usermod -aG docker root 


docker update --restart unless-stopped $(docker ps -q) 

docker update --restart always $(docker ps -a -q --filter "status=exited")

(Sunucu kapanıp açıldığında konteynırların son çalışma şekillerine geri dönmesini sağlayan komut)


FIREWALL (GÜVENLİK DUVARI) YAPILANDIRMAK VE AKTİF ETMEK
ufw allow 22 
ufw allow 10000 
ufw allow 2020 
ufw allow 2053 
ufw allow 4000
ufw allow 1001:8000/tcp 
ufw enable 
systemctl restart ufw

hostnamectl set-hostname sunucuadı
hostnamectl set-hostname sunucuadı --pretty
hostnamectl set-hostname sunucuadı --static
hostnamectl set-hostname sunucuadı --transient



docker restart $(docker ps -a -q)
docker inspect -f "{{ .RestartCount }}" cointaner name
docker inspect -f "{{ .State.StartedAt }}"


docker run -d -p 6001:2020 -p 7001:3030 -v mydexchain6001:/var/lib/postgresql/ --privileged --log-driver=none --name 6001 mydexchain/mydexchain:latest

curl http://localhost:6001/setDextracker/f09017dca53f11eb9a3b02ca075254e8icARvV6zur

curl http://localhost:6001/setStartDXCMiner/

curl http://localhost:6001/setStartPRXMiner/

curl http://localhost:6001/setJoinPool/aeaa7d21-c263-11eb-ad54-02ca075254e8










