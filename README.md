build image
			git clone git@github.com:magimat/rpi-samba.git
			cd rpi-samba/
			docker build --no-cache -t magimat/rpi-samba .
			docker push magimat/rpi-samba

		docker run --name rpi-samba -d --restart always -v $PWD:/data/share -p 445:445 -p 139:139 -p 137:137/udp -p 138:138/udp magimat/rpi-samba
