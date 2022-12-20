# Betterlockscreen with quotes
add a random one liner quote to your lock screen every time you use [betterlockscreen](https://github.com/betterlockscreen/betterlockscreen) in linux
## Requirements
- install [betterlockscreen](https://github.com/betterlockscreen/betterlockscreen)
- install [sxhkd](https://github.com/baskerville/sxhkd)
- text file containing quotes or you can use this one [Quotes.txt](https://github.com/karimhussein1/quotes-on-betterlockscreen/blob/main/Quotes.txt) 

#### just copy this block of code in your shell and it will automate the the process
```
# first clone this repository with
git clone https://github.com/karimhussein1/add-quotes-to-your-lock-screen.git
cd add-quotes-to-your-lock-screen
# updating sxhkd, you can change this keybinding!
echo "super + l 
  betterlockscreen -l --text \"\$(awk 'NF<=25 \{print \$o\}' $(pwd)/Quotes.txt | shuf -n 1)\"" >> ~/.config/sxhkd/sxhkdrc
# then restart sxhkd
pkill -USR1 -x sxhkd
```

quotes resources
- https://www.region10.org/
- [quotes.txt](https://github.com/erossignon/qod4outlook/blob/master/quotes.txt)
- [quotes.txt](https://gist.github.com/robatron/a66acc0eed3835119817)
- [quotes.txt](https://github.com/ik5/pyquotes/blob/master/quotes.txt)
