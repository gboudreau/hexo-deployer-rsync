# hexo-deployer-rsync

[![NPM version](https://badge.fury.io/js/hexo-deployer-rsync.svg)](http://badge.fury.io/js/hexo-deployer-rsync)

Rsync deployer plugin for [Hexo].

## Installation

``` bash
$ npm install hexo-deployer-rsync --save
```

## Options

You can configure this plugin in `_config.yml`.

``` yaml
deploy:
  type: rsync
  host: <host>
  user: <user> # Default is user running the deploy command
  root: <root>
  port: [port] # Default is 22
  delete: [true|false] # Default is true
  args: <rsync args>
  verbose: [true|false] # Default is true
  ignore_errors: [true|false] # Default is false
```

- **host**: Address of remote host  
- **user**: Username  
- **root**: Root directory of remote host   
- **port**: Port
- **delete**: Delete old files on remote host
- **args**: Rsync arguments
- **verbose**: Display verbose messages
- **ignore_errors**: Ignore errors

Note: if you define the user and port needed to connect in your `~/.ssh/config` file, you do not need to specify them in here. You can also use an alias as the `host`, if you specify the hostname to connect to in `~/.ssh/config`.  
Example `~/.ssh/config`:

    Host my_web_server
      Hostname dm8723.my-host.com
      User potato
      Port 2222

## License

MIT

[Hexo]: http://hexo.io/
