１、將cantonesetry.txt轉成為cantonesetry.db (可以唔做，已經做咗，唔方心可以自己整多次)

**注意：未必所有系統都係/usr/share開頭㗎**
> ibus-table-createdb -n  /usr/share/ibus-table/tables/cantonesetry.db -s cantonesetry.txt

２、如果唔轉，直接copy db都得，放/usr/share/ibus-table/tables/ 下。
> cp cantonesetry.db  /usr/share/ibus-table/tables/.

3、裝添加CantoneTry輸入法。Fedora在輸入法嘅Chinese(Hong Kong)下。
