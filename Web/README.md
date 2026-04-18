# Web

The typical software stack for hosting dynamic websites and web applications is LNMP/LAMP stack.

## Nginx

[Nginx](https://nginx.org/) is an HTTP web server, reverse proxy, content cache, load balancer, TCP/UDP proxy server, and mail proxy server. 

Steps to install Nginx:
- Specify Nginx module versions via environment variables, or leave them blank to install the latest versions by default.
- run the `nginx.sh`

```shell []
cd Web

# switch to root first
sudo su

# Nginx version and dependencies versions, modify as needed
export nginx_ver=''
export openssl_ver=''
export pcre2_ver=''
export NDK_ver=''
export Ngx_Lua_ver=''
export Ngx_Stream_Lua_ver=''
export LuaRestyLrucache_ver=''
export LuaRestCore_ver=''

# Nginx website and logs path, e.g.
export nginx_web_path='/usr/local/nginx/html'
export nginx_logs_path='/usr/local/nginx/logs'

# Optional. If you are using the ngx_http_geoip2_module, set values for the following 4 environment variables.
export libmaxminddb_ver=''
export geoipupdate_ver=''
# And maxmind_account_id, maxmind_license_key cannot be empty!
export maxmind_account_id=''
export maxmind_license_key=''

# install Nginx
./scripts/nginx.sh
```

> Last Updated: 2026-04-18
