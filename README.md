# antivirus

##About
Antivirus software

##Description
ClamAV daemon as a Docker image. 
`freshclam` in being running in the background for updating the virus database. 
`clamd` is listening on exposed port `3310`.

##Usage

    docker run -d -p 3310:3310 docker-antivirus
    
or linked (recommended)

    docker run -d --name av docker-antivirus
    docker run -d --link av:antivirus application-with-antivirusscan

