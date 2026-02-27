# Documents for ${{values.app_name}}

This is a template app!

For fun, it shows you a random dev excuse + a random cat

# How to access the app?

You can access the app by using either URL:

- `${{values.app_name}}.test.com`
- `${{values.app_name}}-${{values.app_env}}.test.com`

If DNS is not resolving locally, test through ingress with an explicit Host header:

```bash
curl -i -H "Host: ${{values.app_name}}-${{values.app_env}}.test.com" http://127.0.0.1/api/v1/healthz
curl -i -H "Host: ${{values.app_name}}-${{values.app_env}}.test.com" http://127.0.0.1/api/v1/info
```

# Extra info?

This application has two API endpoints:

- `/api/v1/info`
- `/api/v1/healthz`

Here you could expand on what each of these endpoints do.


