# Betterlockscreen with quotes
add a random one liner quote to your lock screen every time you use [betterlockscreen](https://github.com/betterlockscreen/betterlockscreen) in linux
## Requirements
- [betterlockscreen](https://github.com/betterlockscreen/betterlockscreen)
- [sxhkd](https://github.com/baskerville/sxhkd)
- text file containing quotes or you can use this one [Quotes.txt](https://github.com/karimhussein1/quotes-on-betterlockscreen/blob/main/Quotes.txt) 
```
# add this to your sxhkdrc in ~/.config/sxhkd/sxhkdrc
# use this keybinding or any other combination
# replace Quotes.txt with the full path to your Quotes.txt file
super + l
  betterlockscreen -l --text "$(awk 'NF<=25 \{print $o\}' Quotes.txt | shuf -n 1)"
```

  

quotes resources
- https://www.region10.org/
- [quotes.txt](https://github.com/erossignon/qod4outlook/blob/master/quotes.txt)
- [quotes.txt](https://gist.github.com/robatron/a66acc0eed3835119817)
- [quotes.txt](https://github.com/ik5/pyquotes/blob/master/quotes.txt)
