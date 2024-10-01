Thiết lập dự án:
	backend:
		Code bằng netcore#6
		Build
		Run:
	frontend:
		Code bang react
		Build
		run
Note 2:
Cài đặt Gitlab runner:		
# apt update -y
# curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh" | sudo bash
# apt install gitlab-runner

Note 3: File bash script cài đặt Docker:
	sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
	echo "deb [signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
	sudo apt update -y
	sudo apt install docker-ce -y
	sudo systemctl start docker
	sudo systemctl enable docker
	sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
	sudo chmod +x /usr/local/bin/docker-compose
	docker -v
	docker-compose -v
Note 4: 
	Cai dat netcore#6
	# apt update -y && apt upgrade -y
	# apt install -y wget apt-transport-https software-properties-common
	# wget -q https://packages.microsoft.com/config/ubuntu/22.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
	# dpkg -i packages-microsoft-prod.deb
	# apt update -y && apt install -y dotnet-sdk-6.0

Note 5:
	Cài đặt NodeJS version 18:
	# curl -sL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh
	# bash nodesource_setup.sh
	# apt install nodejs
	
Note 6: 
	Cai dat jfrog
	# docker run --name artifactory-jfrog --restart unless-stopped -v /tools/jfrog/data/:/var/opt/jfrog/artifactory -d -p 8081:8081 -p 8082:8082 releases-docker.jfrog.io/jfrog/artifactory-oss:7.77.5
	
Note 7: