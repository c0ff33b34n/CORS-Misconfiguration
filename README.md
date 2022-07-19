# Exploiting Misconfigured CORS (Cross Origin Resource Sharing)

Testing: curl http://testing-url.tld/endpoint -H "Origin: http://evil.com" -H

Cases:

+ Poorly implemented, Best case for Attack:

    Access-Control-Allow-Origin: https://attacker.com

    Access-Control-Allow-Credentials: true

+ Poorly implemented, Exploitable:

    Access-Control-Allow-Origin: null

    Access-Control-Allow-Credentials: true

+ Bad implementation but not exploitable:

    Access-Control-Allow-Origin: *

    Access-Control-Allow-Credentials: true

    or just

    Access-Control-Allow-Origin: *
    
  Put vulnerable endpoint in CORS_PoC.html and check the response.
  
