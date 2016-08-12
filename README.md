# download-progress-bar

This is a [download-progress](https://github.com/AYapejian/download-progress) fork with improvements and modifications

What improvements? Apparently the origin of this module is incomplete, for example, there is no option module configurations so far.

Now, to set the module simply pass a json as second attribute

```javascript
var DownloadProgress = require('download-progress-bar');
var urls = [
    {
        url: 'https://s3.amazonaws.com/node-webkit/v0.7.5/node-webkit-v0.7.5-win-ia32.zip',
        dest: 'node-webkit-v0.7.5-win-ia32.zip'
    }, {
        url: 'https://s3.amazonaws.com/node-webkit/v0.7.5/node-webkit-v0.7.5-linux-ia32.tar.gz',
        dest: 'node-webkit-v0.7.5-linux-ia32.tar.gz'
    }, {
        url: 'https://s3.amazonaws.com/node-webkit/v0.7.5/node-webkit-v0.7.5-osx-ia32.zip',
        dest: 'node-webkit-v0.7.5-osx-ia32.zip'
    }
];

var options = {
	layout: '[:bar] :percent :etas', // https://github.com/visionmedia/node-progress#tokens
	displayMessage: fase,
	complete: // https://github.com/visionmedia/node-progress#options
	incomplete: // https://github.com/visionmedia/node-progress#options
	width: // https://github.com/visionmedia/node-progress#options
	total: // https://github.com/visionmedia/node-progress#options
}

var download = DownloadProgress(urls, options);
```
