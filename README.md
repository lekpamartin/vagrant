# vagrant
Tools for easy generate test environment. 

## Configuration

### Proxy
Vagrant is able to use http_proxy, https_proxy, ... environment variable when he need to download box, plugin, ... 

### Plugin 
Vagrant have some plugin to interact with some product.

#### Proxy
If you want to use vagrant with proxy, you need to install this plugin 
```bash
vagrant plugin install vagrant-proxyconf
```
If the plugin is installed, you can define the proxy to use in your vagrantfile 
```bash
if Vagrant.has_plugin?("vagrant-proxyconf")
  config.proxy.http     = "http://IP:PORT/"
  config.proxy.https    = "http://IP:PORT/"
  config.proxy.no_proxy = "localhost,127.0.0.1,.example.com"
end
```
If you don't wan't to edit the vagrantfile, you can use environment variable 
```bash
VAGRANT_HTTP_PROXY
VAGRANT_HTTPS_PROXY
VAGRANT_FTP_PROXY
VAGRANT_NO_PROXY
```
