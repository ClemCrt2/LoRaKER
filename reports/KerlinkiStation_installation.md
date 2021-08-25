# 082021 : Kerlink Gateway iStation 868MHz installation

## My Kerlink Starter Pack

- Gateway LoRaWAN 868MHz
- 6dB antenna KLK02374
- 1 antenna adaptator
- 1 surge protector device
- 1 Ethernet Surge Protector
- 1 PoE Power supply 
- The Instalation guide
- Antenna and gateway mounting system
- No USB-C Cable to debug :(


## First connexion

Connectez-vous en SSH sur la passerelle avec les identifiants suivants :
Login : root
Mot de passe : pdmk-XXXXXX
XXXXX étant les 6 derniers caractères du boardID

with the web interface

Login : spn
Password : spnpwd


## Chirpstack configuration

In the file /etc/lorafwd/lorafwd.toml

[gwmp]
node = #YourChirpstackNode
service.uplink = 1700
service.downlink = 1700

In Chirpstack-application-server

Add the EUI wrote on the back of the gateway in the Gateway ID field

