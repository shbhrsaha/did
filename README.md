
# did

did is a few bash aliases to log what you worked on.

```
> d submitted diff for login feature
> d designed server API with Ahmed
> d debugging logout race condition
> d no progress on debugging, should ask Kyle tomorrow
> did
Tue 2018-07-17 12:31:22 submitted diff for login feature
Tue 2018-07-17 12:57:18 designed server API with Ahmed
Tue 2018-07-17 13:32:34 debugging logout race condition
Tue 2018-07-17 13:58:19 no progress on debugging, should ask Kyle tomorrow
```

To use it yourself, add the following lines to your `.bashrc` or `.bash_profile`. Change `DID_FILEPATH` to whatever file you want.

```
export DID_FILEPATH=~/Dropbox/did.txt;
alias d='echo $(date "+%a %Y-%m-%d %H:%M:%S") "$@" >> $DID_FILEPATH';
alias did='less +F $DID_FILEPATH';
```

Tested on OS X.
