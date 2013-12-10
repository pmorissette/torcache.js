torcache.js
===========

A node.js wrapper for torcache.net

##Examples
For example, if you want to download the Ubuntu 13.04 64 bit torrent file and for some strange reason you happen to have
the info hash, then you can do the following:

````javascript
var torcache = require('torcache');

torcache('e50331a0a8499d95ef8ebd546113cd021275c877', 'ubuntu-server-13.04-64.torrent', function(err) {
  if (err) {
    console.log(err);
  } else {
    console.log('great success!');
  }
});
````

Now most people don't really have the info hash handy, so in that case I recommend using another library
for the torrent finding part of the job. The http://github.com/pmorissette/torget library builds on top of
torcache and provides a better interface for downloading torrent files.

###torcache(hash, path, callback)
* `hash` a torrent info hash string
* `filename` the path/filename the torrent file should be saved to
* `callback` only one argument returned (err) - will be null if all went well
