To generate a new certificate:

`openssl req -new -x509 -newkey rsa:2048 -sha256 -nodes -keyout localhost.key -days 3560 -out localhost.crt -config certificate.cnf`

Register certifictae with windows powershell:

`Import-Certificate -FilePath 'c:\dev\ssl_certs\localhost.crt' -CertStoreLocation Cert:\LocalMachine\Root`

Angular

`ng serve -o --prod --ssl --ssl-cert c:/dev/ssl_certs/localhost.crt --ssl-key c:/dev/ssl_certs/localhost.key`