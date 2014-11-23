１、將cantonesetry.txt轉成為cantonesetry.db (可以唔做，已經做咗，唔方心可以自己整多次)

**注意：未必所有系統都係/usr/share開頭㗎**
> ibus-table-createdb -n  /usr/share/ibus-table/tables/cantonesetry.db -s cantonesetry.txt

２、如果唔轉，直接copy db都得，放/usr/share/ibus-table/tables/ 下。
> cp cantonesetry.db  /usr/share/ibus-table/tables/.

3、裝添加CantoneTry輸入法。Fedora在輸入法嘅Chinese(Hong Kong)下。

4、如果自己修改碼表，用呢個命令刷新ibus
>ibus-daemon -drx

5、對於100個後選字限製導致第一次打某字時無法列出，解決方案係修改/usr/share/ibus-table/engine/tabsqlitedb.py
將
>maximum_number_of_candidates = 200
改成
>maximum_number_of_candidates = 100
只要輸入果一次，就會將字排到前面，下次輸入就好方便。
