https://github.com/google/restor

~restor is nice and fast but it doesn't support http~ :sadpanda:

It also requires a config before you can use the custom dmg option :sadpanda:

~But you can use Clayton's fork that adds http support https://github.com/clburlison/restor/tree/http_support (a pre-compiled version
is included in this repo)~ Use the "insecure" version that Google releases.

**OR**:

You can use the free SSL cert that github gives us

<!-- cd into this git repo

`python -m SimpleHTTPServer 2015` -->

Set your configs

```bash
sudo defaults write /Library/Preferences/com.google.corp.restor.plist ConfigURL "https://raw.githubusercontent.com/clburlison/restor_local_starter_pack/master/restor.plist"
sudo defaults write /Library/Preferences/com.google.corp.restor.plist CustomImage -bool true
```

Now when you launch Restor.app it will pull the config from GH's CDN and you can use the local
option until you turn blue in the face.
