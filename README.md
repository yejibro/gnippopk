# A few yejiscripts for downloading pics

Honestly I no longer remember what most of these were for

`getKoreanka <url>` returns list of images of supplied celebrity or pages with higher
resolution photos, I don't remember, `getImages` looks similar

`justGet` - I don't have a clue

`koreankid` - if you want to download more pics than those first 9 rows in the gallery
displayed by default you may want to use this script, it scans your clipboard and if
there's an url to the supported website which wasn't used previously downloads the photo
to the appropriate directory (if it even works). Made for OS X, so you probably would
need to change pbpaste command to something your distro uses

`getKpo*ingByKoreanka <url>` - this is the script I've been frequently using, it
downloads pics in folders and it's really convenient.

## Cron

You can make script for automating stuff a bit, something like this:

```
rev=$(echo gnippopk | rev)
cd ~/k
my_girls="Rose Winter Leeseo Gaeul5 IU Karina2 Hayoung2 Xiaoting Kazuha Danielle"
for i in $my_girls; do
	./getKpo*gByKoreanka "https://${rev}.com/goog/kpics/gender-all/category-any/idol-${i}/group-any/order-new"
done
```

and put it in cron so it'll download new pics for you

