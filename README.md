# reshare-dcb-testing

All the scripts in this repository require a ~/.dcb.sh file which contains defaults for the script.

~/.dcb.sh was chosen to avoid accidental check-ins to source control.

Your ~/.dcb.sh script should set the following properties


    #!/bin/bash
    export KEYCLOAK_BASE="https://reshare-hub-kc.libsdev.k-int.com/realms/reshare-hub"
    export KEYCLOAK_CERT_URL="$KEYCLOAK_BASE/protocol/openid-connect/certs"
    export KEYCLOAK_CLIENT="dcb"
    export KEYCLOAK_SECRET="THE_KEYCLOAK_SECRET_FOR_DCB_CLIENT"
    export DCB_ADMIN_USER=
    export DCB_ADMIN_PASS=
    export DCB_STD_USER=
    export DCB_STD_PASS=


Having set up this file and made it executable the following scripts are available in the ./bin directory

- login - Talks to keycloak and returns a JWT which can be used in subsequent requests. Paste this into jwt.io to decode

