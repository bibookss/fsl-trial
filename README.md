## Installation
Install mkcert 
```
brew install mkcert 
mkcert -install  
```

Create certificate for localhost to allow https for the video streaming in mobile browsers
```
cd src
mkcert localhost
```

## Usage
Run the server with the certificates
```
uvicorn server:app --host 0.0.0.0 --port 8000 --ssl-keyfile localhost-key.pem --ssl-certfile localhost.pem                
```