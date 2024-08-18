# Автоматическая сборка контейнеров по докер файлу

***Сборка образа:***  
	sudo docker build -f dockerfile . -t automate_project_os/ubuntu:v1

***Запуск тачек:***  
	Меняется адрес порта 2222+1 и ubuntucar+1
		sudo docker run -d --name ubuntucar1 -p 2222:22 automate_project_os/ubuntu:v1
		sudo docker run -d --name ubuntucar2 -p 2223:22 automate_project_os/ubuntu:v1
		
***Получение айпишника по контейнер айди:***  
	sudo docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' 5eb066999bb6


