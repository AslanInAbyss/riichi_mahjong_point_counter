輸入為一組字串(其中"m,p,s,z" 為 "萬,筒,索,字"、"1z-7z" 為 "東南西北白發中"、0為赤，如"0m" 為"赤5萬")<br>
規則如下:<br>
1.自摸 & 栄和:<br>
point_count('112233456789m1s1s') #自摸<br>
point_count('112233456789m1s+1s') #栄和<br>
2.寶牌「指示物」:<br>
point_count('112233456789m1s1s+d12s') #Dora: 1s 2s<br>
3.場風自風:<br>
1234=東南西北<br>
default: 場風東自風南<br>
point_count('112233456789m1s1s+21') #場風南自風東<br>
point_count('112233456789m1s1s+24') #場風南自風北<br>
4.額外訊息:<br>
Meaning:<br>
t天和/地和<br>
r立直<br>
i一発<br>
w雙立直<br>
h海底摸月/河底撈魚<br>
k槍槓/嶺上開花<br>
22場風南自風南<br>
point_count('1s+1s+123m55z666z7777z+d12s+trihk22')<br><br>
輸出為:[是否成功和牌、役、幾倍役滿、翻數、符數、分數、文字描述]<br><br>
注:無法解析本場
