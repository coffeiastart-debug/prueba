# prueba
11BNU25EA0MxNaLMzwGOF8_
5Lcw9d6gaP4bA24i8rKbfSYn0aBymJ
s7Ktw4b1PtBvuNSRHI53ResrSzNL9


mkdir -p certs
openssl req -x509 -newkey rsa:2048 -sha256 -nodes -days 30 \
  -keyout certs/privkey.pem \
  -out certs/fullchain.pem \
  -subj "/CN=localhost/O=SICOTAG Development" \
  -addext "subjectAltName=DNS:localhost,IP:127.0.0.1" \
  -addext "basicConstraints=critical,CA:FALSE" \
  -addext "keyUsage=critical,digitalSignature,keyEncipherment" \
  -addext "extendedKeyUsage=serverAuth"

Luis Alberto Ramírez
11:07
si quieres que dure un año:
openssl req -x509 -newkey rsa:2048 -sha256 -nodes -days 365 \
  -keyout certs/privkey.pem \
  -out certs/fullchain.pem \
  -subj "/CN=localhost/O=SICOTAG Development" \
  -addext "subjectAltName=DNS:localhost,IP:127.0.0.1" \
  -addext "basicConstraints=critical,CA:FALSE" \
  -addext "keyUsage=critical,digitalSignature,keyEncipherment" \
  -addext "extendedKeyUsage=serverAuth"
o infinito
openssl req -x509 -newkey rsa:2048 -sha256 -nodes -days 9999 \
  -keyout certs/privkey.pem \
  -out certs/fullchain.pem \
  -subj "/CN=localhost/O=SICOTAG Development" \
  -addext "subjectAltName=DNS:localhost,IP:127.0.0.1" \
  -addext "basicConstraints=critical,CA:FALSE" \
  -addext "keyUsage=critical,digitalSignature,keyEncipherment" \
  -addext "extendedKeyUsage=serverAuth"
