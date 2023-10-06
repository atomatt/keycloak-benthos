Start it all up.

Open http://localhost:8080/ and sign in using admin/admin.

Reduce the realm's "Access Token Lifespan" to 15s.

Create a "bar" client. Disable "Standard flow". Disable "Direct access grants".

Add a "api" role to the "bar" client.

Create a "foo" client. Enable "Client authentication". Disable "Standard flow". Enable "Serice account roles". Copy-paste the client secret to the `foo` service's `KEYCLOAK_CLIENT_SECRET` env var.

Assign the "bar" client's "api" role to the "foo" client's "Service account roles".
