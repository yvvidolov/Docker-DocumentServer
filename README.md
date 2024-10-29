## Description
Changed Docker-OnlyOffice to use https://github.com/btactic-oo/unlimited-onlyoffice-package-builder debian package instead of OnlyOffice provided one.  
This makes an OnlyOffice docker image with mobile editing and without concurrent user limit.  

## Usage
> modify `your_username` in commands and `docker-compose.yml`  

### Build Image
- Build: `docker build -t your_username/onlyoffice-unrestricted:latest .`

### Push to docker hub (for remote use)
- Login using your credentials: `docker login`
- Upload the built image: `docker push your_username/onlyoffice-unrestricted:latest`

### Use with docker compose
- Without docker hub: 
  - in `docker-compose.yml` uncomment `#build:` and `#  context: .`, comment `image: your_username/onlyoffice-unrestricted`
  - `docker compose up -d --build`
- With docker hub:
  - `docker compose up -d`
