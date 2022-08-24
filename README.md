# Netcat
 A simple netcat tool to aid with getting a shell on compromised machines
 

usage: netcat.py [-h] [-c] [-e EXECUTE] [-l] [-p PORT] [-t TARGET] [-u UPLOAD]

Netcat tool for remote shell

options:
  -h, --help            show this help message and exit
  -c, --command         command shell
  -e EXECUTE, --execute EXECUTE
                        execute specified command
  -l, --listen          listen
  -p PORT, --port PORT  specified port
  -t TARGET, --target TARGET
                        specified IP
  -u UPLOAD, --upload UPLOAD
                        upload file

Example:
        netcat.py -t 192.168.0.12 -p 9999 -l -c # interactive command shell
        netcat.py -t 192.168.0.12 -p 9999 -l -u=mytest.txt # upload to file
        netcat.py -t 192.168.0.12 -p 9999 -l -e="cat /etc/passwd" # execute command
        echo 'ABC' | ./netcat.py -t 192.168.0.12 -p 135 # echo text to server port 135
        netcat.py -t 192.168.0.12 -p 9999 # connect to server
