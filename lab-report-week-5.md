# Lab Report Week 5
### By Pierre Ellie

For this week's lab report I chose to explore the grep command's options. As we know, grep by default searches files and prints out if they contain the given sequence of characters. In the print out, if you look through a directory like technical, it will print the path of the file as well as the entire line that the sequence is on, we can change some of these settings to find some different results. 

## -c

The -c command option on grep provides a result where it gives the amount of lines in the file that contain the character sequence. 
``` 
 grep  -c  "base pair" technical/plos/journal.*.txt
technical/plos/journal.pbio.0020001.txt:0
technical/plos/journal.pbio.0020010.txt:0
technical/plos/journal.pbio.0020012.txt:0
technical/plos/journal.pbio.0020013.txt:0
technical/plos/journal.pbio.0020019.txt:0
technical/plos/journal.pbio.0020028.txt:0
technical/plos/journal.pbio.0020035.txt:0
technical/plos/journal.pbio.0020040.txt:0
technical/plos/journal.pbio.0020042.txt:0
technical/plos/journal.pbio.0020043.txt:0
technical/plos/journal.pbio.0020046.txt:0
technical/plos/journal.pbio.0020047.txt:0
technical/plos/journal.pbio.0020052.txt:0
technical/plos/journal.pbio.0020053.txt:0
technical/plos/journal.pbio.0020054.txt:0
technical/plos/journal.pbio.0020063.txt:0
technical/plos/journal.pbio.0020064.txt:0
technical/plos/journal.pbio.0020067.txt:0
technical/plos/journal.pbio.0020068.txt:0
technical/plos/journal.pbio.0020071.txt:0
technical/plos/journal.pbio.0020073.txt:0
technical/plos/journal.pbio.0020100.txt:0
technical/plos/journal.pbio.0020101.txt:0
technical/plos/journal.pbio.0020105.txt:0
technical/plos/journal.pbio.0020112.txt:0
technical/plos/journal.pbio.0020113.txt:0
technical/plos/journal.pbio.0020116.txt:0
technical/plos/journal.pbio.0020121.txt:0
technical/plos/journal.pbio.0020125.txt:0
technical/plos/journal.pbio.0020127.txt:0
technical/plos/journal.pbio.0020133.txt:0
technical/plos/journal.pbio.0020140.txt:0
technical/plos/journal.pbio.0020145.txt:0
technical/plos/journal.pbio.0020146.txt:0
technical/plos/journal.pbio.0020147.txt:0
technical/plos/journal.pbio.0020148.txt:0
technical/plos/journal.pbio.0020150.txt:0
technical/plos/journal.pbio.0020156.txt:0
technical/plos/journal.pbio.0020161.txt:0
technical/plos/journal.pbio.0020164.txt:0
technical/plos/journal.pbio.0020169.txt:0
technical/plos/journal.pbio.0020172.txt:0
technical/plos/journal.pbio.0020183.txt:0
technical/plos/journal.pbio.0020187.txt:0
technical/plos/journal.pbio.0020190.txt:2
technical/plos/journal.pbio.0020206.txt:0
technical/plos/journal.pbio.0020213.txt:0
technical/plos/journal.pbio.0020214.txt:0
technical/plos/journal.pbio.0020215.txt:0
technical/plos/journal.pbio.0020216.txt:0
technical/plos/journal.pbio.0020223.txt:1
technical/plos/journal.pbio.0020224.txt:0
technical/plos/journal.pbio.0020228.txt:0
technical/plos/journal.pbio.0020232.txt:0
technical/plos/journal.pbio.0020241.txt:0
technical/plos/journal.pbio.0020262.txt:0
technical/plos/journal.pbio.0020263.txt:0
technical/plos/journal.pbio.0020267.txt:0
technical/plos/journal.pbio.0020272.txt:0
technical/plos/journal.pbio.0020276.txt:0
technical/plos/journal.pbio.0020297.txt:0
technical/plos/journal.pbio.0020302.txt:0
technical/plos/journal.pbio.0020306.txt:0
technical/plos/journal.pbio.0020307.txt:0
technical/plos/journal.pbio.0020310.txt:0
technical/plos/journal.pbio.0020311.txt:0
technical/plos/journal.pbio.0020337.txt:0
technical/plos/journal.pbio.0020346.txt:0
technical/plos/journal.pbio.0020347.txt:0
technical/plos/journal.pbio.0020348.txt:0
technical/plos/journal.pbio.0020350.txt:0
technical/plos/journal.pbio.0020353.txt:0
technical/plos/journal.pbio.0020354.txt:0
technical/plos/journal.pbio.0020394.txt:0
technical/plos/journal.pbio.0020400.txt:0
technical/plos/journal.pbio.0020401.txt:0
technical/plos/journal.pbio.0020404.txt:0
technical/plos/journal.pbio.0020406.txt:0
technical/plos/journal.pbio.0020419.txt:0
technical/plos/journal.pbio.0020420.txt:0
technical/plos/journal.pbio.0020430.txt:0
technical/plos/journal.pbio.0020431.txt:0
technical/plos/journal.pbio.0020439.txt:0
technical/plos/journal.pbio.0020440.txt:0
technical/plos/journal.pbio.0030021.txt:0
technical/plos/journal.pbio.0030024.txt:0
technical/plos/journal.pbio.0030032.txt:0
technical/plos/journal.pbio.0030050.txt:0
technical/plos/journal.pbio.0030051.txt:0
technical/plos/journal.pbio.0030056.txt:0
technical/plos/journal.pbio.0030062.txt:0
technical/plos/journal.pbio.0030065.txt:0
technical/plos/journal.pbio.0030076.txt:0
technical/plos/journal.pbio.0030094.txt:0
technical/plos/journal.pbio.0030097.txt:0
technical/plos/journal.pbio.0030102.txt:0
technical/plos/journal.pbio.0030105.txt:0
technical/plos/journal.pbio.0030127.txt:0
technical/plos/journal.pbio.0030129.txt:0
technical/plos/journal.pbio.0030131.txt:0
technical/plos/journal.pbio.0030136.txt:0
technical/plos/journal.pbio.0030137.txt:0
```
In this example I used -c with the command that looked for the sequence "base pair". It provided the files as well as how many lines contained the sequence. There were a lot of 0's but some 1's and 2's. I used it on a more specific directory because with thousands of files there would be thousands of lines of output with just 0. 

```
 grep -c "base pair" technical/biomed/gb-2001-2-7-research0025.txt
3

```
This is what the output looks like when you run the command on just one file alone, as you can see the file path is not listed since it was used for the command. It prints out the number of lines containing the term base pair, which is 3. You can get a good idea of how much something gets spoken about in a file.

```
 grep  -c  "the" technical/plos/journal.*.txt
technical/plos/journal.pbio.0020001.txt:147
technical/plos/journal.pbio.0020010.txt:46
technical/plos/journal.pbio.0020012.txt:123
technical/plos/journal.pbio.0020013.txt:83
technical/plos/journal.pbio.0020019.txt:85
technical/plos/journal.pbio.0020028.txt:119
technical/plos/journal.pbio.0020035.txt:116
technical/plos/journal.pbio.0020040.txt:52
technical/plos/journal.pbio.0020042.txt:79
technical/plos/journal.pbio.0020043.txt:155
technical/plos/journal.pbio.0020046.txt:103
technical/plos/journal.pbio.0020047.txt:39
technical/plos/journal.pbio.0020052.txt:92
technical/plos/journal.pbio.0020053.txt:137
technical/plos/journal.pbio.0020054.txt:131
technical/plos/journal.pbio.0020063.txt:42
technical/plos/journal.pbio.0020064.txt:117
technical/plos/journal.pbio.0020067.txt:83
technical/plos/journal.pbio.0020068.txt:98
technical/plos/journal.pbio.0020071.txt:45
technical/plos/journal.pbio.0020073.txt:67
technical/plos/journal.pbio.0020100.txt:59
technical/plos/journal.pbio.0020101.txt:80
technical/plos/journal.pbio.0020105.txt:50
technical/plos/journal.pbio.0020112.txt:57
technical/plos/journal.pbio.0020113.txt:142
technical/plos/journal.pbio.0020116.txt:94
technical/plos/journal.pbio.0020121.txt:113
technical/plos/journal.pbio.0020125.txt:77
technical/plos/journal.pbio.0020127.txt:96
technical/plos/journal.pbio.0020133.txt:73
technical/plos/journal.pbio.0020140.txt:90
technical/plos/journal.pbio.0020145.txt:118
technical/plos/journal.pbio.0020146.txt:146
technical/plos/journal.pbio.0020147.txt:62
technical/plos/journal.pbio.0020148.txt:127
technical/plos/journal.pbio.0020150.txt:116
technical/plos/journal.pbio.0020156.txt:71
technical/plos/journal.pbio.0020161.txt:168
technical/plos/journal.pbio.0020164.txt:123
technical/plos/journal.pbio.0020169.txt:112
technical/plos/journal.pbio.0020172.txt:75
technical/plos/journal.pbio.0020183.txt:86
technical/plos/journal.pbio.0020187.txt:89
technical/plos/journal.pbio.0020190.txt:109
technical/plos/journal.pbio.0020206.txt:117
technical/plos/journal.pbio.0020213.txt:136
technical/plos/journal.pbio.0020214.txt:103
technical/plos/journal.pbio.0020215.txt:66
technical/plos/journal.pbio.0020216.txt:88
technical/plos/journal.pbio.0020223.txt:72
technical/plos/journal.pbio.0020224.txt:76
technical/plos/journal.pbio.0020228.txt:99
technical/plos/journal.pbio.0020232.txt:87
technical/plos/journal.pbio.0020241.txt:95
technical/plos/journal.pbio.0020262.txt:60
technical/plos/journal.pbio.0020263.txt:57
technical/plos/journal.pbio.0020267.txt:145
technical/plos/journal.pbio.0020272.txt:61
technical/plos/journal.pbio.0020276.txt:82
technical/plos/journal.pbio.0020297.txt:79
technical/plos/journal.pbio.0020302.txt:108
technical/plos/journal.pbio.0020306.txt:100
technical/plos/journal.pbio.0020307.txt:76
technical/plos/journal.pbio.0020310.txt:99
technical/plos/journal.pbio.0020311.txt:96
technical/plos/journal.pbio.0020337.txt:99
technical/plos/journal.pbio.0020346.txt:72
technical/plos/journal.pbio.0020347.txt:151
technical/plos/journal.pbio.0020348.txt:92
technical/plos/journal.pbio.0020350.txt:134
technical/plos/journal.pbio.0020353.txt:39
technical/plos/journal.pbio.0020354.txt:77
technical/plos/journal.pbio.0020394.txt:135
technical/plos/journal.pbio.0020400.txt:113
technical/plos/journal.pbio.0020401.txt:98
technical/plos/journal.pbio.0020404.txt:113
technical/plos/journal.pbio.0020406.txt:163
technical/plos/journal.pbio.0020419.txt:106
technical/plos/journal.pbio.0020420.txt:92
technical/plos/journal.pbio.0020430.txt:48
technical/plos/journal.pbio.0020431.txt:74
technical/plos/journal.pbio.0020439.txt:208
technical/plos/journal.pbio.0020440.txt:155
technical/plos/journal.pbio.0030021.txt:74
technical/plos/journal.pbio.0030024.txt:92
technical/plos/journal.pbio.0030032.txt:74
technical/plos/journal.pbio.0030050.txt:100
technical/plos/journal.pbio.0030051.txt:82
technical/plos/journal.pbio.0030056.txt:102
technical/plos/journal.pbio.0030062.txt:109
technical/plos/journal.pbio.0030065.txt:93
technical/plos/journal.pbio.0030076.txt:89
technical/plos/journal.pbio.0030094.txt:85
technical/plos/journal.pbio.0030097.txt:99
technical/plos/journal.pbio.0030102.txt:113
technical/plos/journal.pbio.0030105.txt:55
technical/plos/journal.pbio.0030127.txt:131
technical/plos/journal.pbio.0030129.txt:49
technical/plos/journal.pbio.0030131.txt:83
technical/plos/journal.pbio.0030136.txt:88
technical/plos/journal.pbio.0030137.txt:149

```
In this case, I used a different term to search, a more common one, "the". As you can see there are a lot larger and more varying results for a more simple and common term. This can help get not only a  good idea of how long the file may be but also how commonly they use certain phrases. 

## -n
The -n command option for grep provides a line number for the found match in the file. 

```
❯ grep -n "base pair" technical/biomed/gb-2001-2-7-research0025.txt
13:        the 3.2 billion base pair (bp) human genome is
311:          obtain a median of 0.017 entries per base pair for known
312:          genes and 0.005 entries per base pair for anonymous
```
In this example I used -n on one file to find each line where the term "base pair" is found. This is obviously helpful to be able to quickly look into the the file to know where something may be spoken about, in this case, around lines 310-315.


```
grep -n "al Qaeda" technical/911report/chapter-13.*.txt
technical/911report/chapter-13.1.txt:64:                Before 9/11, the CIA was plainly the lead agency confronting al Qaeda. The FBI
technical/911report/chapter-13.3.txt:38:                http://observer.guardian.co.uk/worldview/story/0,11581,845725,00.html). The al Qaeda
technical/911report/chapter-13.3.txt:76:            25. A wealth of information on al Qaeda's evolution and history has been obtained
technical/911report/chapter-13.3.txt:84:                particularly useful insight into the evolution of al Qaeda-written by an early Bin
technical/911report/chapter-13.3.txt:157:                al Qaeda's military camps:"Perhaps later I will tell you about the Qa'ida and Bin
technical/911report/chapter-13.3.txt:167:                al Qaeda's role in Somalia until 1996. Intelligence report, Bin Ladin's Activities
technical/911report/chapter-13.3.txt:204:            54. Ibid.; Intelligence report, al Qaeda and Iraq, Aug. 1, 1997.
technical/911report/chapter-13.3.txt:235:                crisis in al Qaeda at this time, see trial testimony of L'Houssaine Kherchtou,
technical/911report/chapter-13.3.txt:268:                former al Qaeda associate, Mar. 19, 2001, p. 26. On the
technical/911report/chapter-13.3.txt:314:                Iraq and al Qaeda regarding chemical weapons and explosives training, the most
technical/911report/chapter-13.3.txt:315:                detailed information alleging such ties came from an al Qaeda operative who recanted
technical/911report/chapter-13.3.txt:316:                much of his original information. Intelligence report, interrogation of al Qaeda
technical/911report/chapter-13.3.txt:318:                any such ties existed between al Qaeda and Iraq. Intelligence reports,
technical/911report/chapter-13.3.txt:333:            79. The number of actual al Qaeda members seems to have been relatively small during
technical/911report/chapter-13.3.txt:338:                al Qaeda members can only be speculative. On al Qaeda's training and indoctrination,
technical/911report/chapter-13.3.txt:342:            80. By 1996, al Qaeda apparently had established cooperative relationships with at
technical/911report/chapter-13.3.txt:397:                with Bin Ladin and al Qaeda, he was arrested immediately after the embassy bombings
technical/911report/chapter-13.3.txt:460:            8. These prosecutions also had the unintended consequence of alerting some al Qaeda
technical/911report/chapter-13.3.txt:493:                attack was determined to be al Qaeda-related, responsibility shifted to the New York
technical/911report/chapter-13.3.txt:655:                authorized surveillance of a suspected al Qaeda operative, Dec. 24, 1999; NSA email,
technical/911report/chapter-13.3.txt:1051:                army (Nov. 26, 1996; Apr. 18, 1997); on the structure of al Qaeda and leadership
technical/911report/chapter-13.3.txt:1093:                U.S. government still did not know of any al Qaeda attacks on U.S. citizens. Samuel
technical/911report/chapter-13.3.txt:1114:                she noted, though Sudan did eventually expel Bin Ladin, his al Qaeda network
technical/911report/chapter-13.3.txt:1403:            91. See Intelligence report, relations between al Qaeda and the Taliban, Feb. 20,
technical/911report/chapter-13.3.txt:1436:                Berger, Sept. 17, 1998. For an overview of the CIA's efforts to disrupt al Qaeda,
technical/911report/chapter-13.3.txt:1460:            110. NSC email, Clarke to Berger, Nov. 4, 1998. Evidence on Iraqi ties to al Qaeda is
technical/911report/chapter-13.3.txt:1673:                of al Qaeda had been imprisoned over the past year. CIA talking points, C/CTC
technical/911report/chapter-13.3.txt:1676:                32 terrorists to justice since July 1998, more than half of whom were al Qaeda. CIA
technical/911report/chapter-13.4.txt:5:                1980s, KSM apparently did not begin working with al Qaeda until after the 1998 East
technical/911report/chapter-13.4.txt:35:                that Sheikh Abdallah was not a member, financier, or supporter of al Qaeda, he
technical/911report/chapter-13.4.txt:97:                member of al Qaeda and that Yousef never met Bin Ladin. Intelligence report,
technical/911report/chapter-13.4.txt:116:                2004. Even after he began working with Bin Ladin and al Qaeda, KSM concealed from
technical/911report/chapter-13.4.txt:133:                interrogation of KSM, Feb. 19, 2004. On KSM's assistance to al Qaeda, see
technical/911report/chapter-13.4.txt:137:                subsequent bombing of the USS Cole yielded a recruiting bonanza for al Qaeda, as
technical/911report/chapter-13.4.txt:143:                would take charge of producing the propaganda video al Qaeda issued following the
technical/911report/chapter-13.4.txt:163:                12, 2003. On Hambali's relationship with Atef and receipt of al Qaeda funds, see
technical/911report/chapter-13.4.txt:172:                al Qaeda biological weapons program until after JI's December 2000 church bombings
technical/911report/chapter-13.4.txt:189:                Hambali and Sufaat, in each of these instances the al Qaeda guests were lodged at
technical/911report/chapter-13.4.txt:195:                explains his relationship with al Qaeda as follows: he received his marching orders
technical/911report/chapter-13.4.txt:196:                from JI, but al Qaeda would lead any joint operation involving members of both
technical/911report/chapter-13.4.txt:203:                involving himself in al Qaeda's broader terrorist program. Indeed, KSM describes
technical/911report/chapter-13.4.txt:204:                Hambali as an al Qaeda member working in Malaysia. Intelligence report,
technical/911report/chapter-13.4.txt:205:                interrogation of KSM, Aug.18,2003. Nashiri observes that al Qaeda's standard
technical/911report/chapter-13.4.txt:208:                interrogation of Nashiri, Jan. 14, 2003. Yet al Qaeda's deference to Hambali's turf
technical/911report/chapter-13.4.txt:234:                operation; rather, whenever Bin Ladin wanted to meet, he would have an al Qaeda
technical/911report/chapter-13.4.txt:238:                be one of al Qaeda's most committed terrorists and, according to one of his
technical/911report/chapter-13.4.txt:243:                also enjoyed a reputation as a productive recruiter for al Qaeda. See Intelligence
technical/911report/chapter-13.4.txt:283:                Zubaydah, who worked closely with the al Qaeda leadership, has stated that KSM
technical/911report/chapter-13.4.txt:296:            38. For KSM's joining al Qaeda, see Intelligence report, interrogation of KSM, Nov.
technical/911report/chapter-13.4.txt:310:                post-9/11 interview with Al Jazeera reporter Yosri Fouda-that an al Qaeda
technical/911report/chapter-13.4.txt:331:                travel to Bosnia, see Intelligence report, interrogation of Saudi al Qaeda member,
technical/911report/chapter-13.4.txt:334:                interrogations of Saudi al Qaeda member, Oct. 2, 2001; Oct. 18, 2001.
technical/911report/chapter-13.4.txt:397:                interrogation of KSM, Aug.18,2003. However, two of Mihdhar's al Qaeda colleagues who
technical/911report/chapter-13.4.txt:748:                counterfeiting and seal removal. Intelligence report, interrogation of al Qaeda
technical/911report/chapter-13.4.txt:787:                not a primary source of al Qaeda funding, although some funds raised in the United
technical/911report/chapter-13.4.txt:788:                States may have made their way to al Qaeda or its affiliated groups. Frank G. and
technical/911report/chapter-13.4.txt:793:                Report,"Feb. 27, 2002; CIA analytic report, spectrum of al Qaeda donors, CTC
technical/911report/chapter-13.4.txt:806:                reinvigorated fund-raising efforts. By 9/11, al Qaeda was returning the favor,
technical/911report/chapter-13.4.txt:839:                Financiers, CTC 2002- 30138H, Jan. 3, 2003. Moreover, because al Qaeda initially was
technical/911report/chapter-13.4.txt:844:            127. For al Qaeda spending, see Frank G. and Mary S. briefing (July 15, 2003). The
technical/911report/chapter-13.4.txt:848:                there is evidence that al Qaeda experienced funding shortfalls as part of the
technical/911report/chapter-13.4.txt:851:                CHAPTER 5 499 ist acts were interrupted as a result. For al Qaeda expenditures, see,
technical/911report/chapter-13.4.txt:883:                institutional investor with no conceivable ties to al Qaeda purchased 95 percent of
technical/911report/chapter-13.4.txt:926:                Spanish al Qaeda cell, led by Imad Barkat Yarkas and al Qaeda European financier
technical/911report/chapter-13.4.txt:963:                Afghanistan controlled by Abu Zubaydah. While the camps were not al Qaeda
technical/911report/chapter-13.4.txt:966:                al Qaeda. See Intelligence report, interrogation of Abu Zubaydah, July 10, 2002.
technical/911report/chapter-13.4.txt:992:                2004). In the margin next to Clarke's suggestion to attack al Qaeda facilities in
technical/911report/chapter-13.4.txt:1147:                other al Qaeda operatives flew to Bangkok to meet Khallad to pass him money. See
technical/911report/chapter-13.4.txt:1302:                station made some effort to gather intelligence on al Qaeda financing, but it proved
technical/911report/chapter-13.4.txt:1326:                al Qaeda financial issues in the three years prior to the 9/11 attacks. Frank G. and
technical/911report/chapter-13.4.txt:1353:                regulatory initiatives would have significantly harmed al Qaeda, which generally
technical/911report/chapter-13.4.txt:1429:                and raids to capture and destroy al Qaeda leaders and targets. DOD briefing
technical/911report/chapter-13.4.txt:1527:                investigation not to rush to judgment that al Qaeda was responsible. Barbara Bodine
technical/911report/chapter-13.4.txt:1541:                photograph, see FBI electronic communication,"Source reporting on al Qaeda," Jan.
technical/911report/chapter-13.4.txt:1668:            172. NSC memo, Clarke to Rice, al Qaeda review, Jan. 25, 2001 (italics and
technical/911report/chapter-13.4.txt:1678:            173. NSC memo, Clarke to Rice, al Qaeda review, Jan. 25, 2001.
technical/911report/chapter-13.4.txt:1680:                than al Qaeda before 9/11. Condoleezza Rice testimony, Apr. 8, 2004; White House
technical/911report/chapter-13.4.txt:1682:                a principals meeting on al Qaeda because it knew that al Qaeda was a major threat.
technical/911report/chapter-13.4.txt:1691:            177. NSC memo, Clarke to Rice, al Qaeda review, Jan. 25, 2001.
technical/911report/chapter-13.4.txt:1697:                reception at Tarnak Farms for one of Bin Ladin's sons, the al Qaeda leader had read
technical/911report/chapter-13.4.txt:1707:                wrote Rice and Hadley that a new al Qaeda video claimed responsibility for the Cole.
technical/911report/chapter-13.4.txt:1710:                authorities during the threat spike told their captors that their al Qaeda training
technical/911report/chapter-13.4.txt:1747:                already talked with Rice and Hadley about Bin Ladin and al Qaeda, the Taliban, and
technical/911report/chapter-13.4.txt:1750:                possible impact of Taliban actions against al Qaeda and on the likely regional
technical/911report/chapter-13.4.txt:1765:                Clarke's concern about an al Qaeda presence in the United States, see NSC briefing
technical/911report/chapter-13.4.txt:1767:                undated, which noted that al Qaeda had "sleeper cells" in more than 40 countries,
technical/911report/chapter-13.4.txt:1770:                2000), attached to NSC memo, Clarke to Rice, Jan. 25, 2001, discussing al Qaeda's
technical/911report/chapter-13.4.txt:1813:                concerning al Qaeda, Feb. 12, 2001.
technical/911report/chapter-13.4.txt:1816:                to Rice, al Qaeda review, Jan. 25, 2001.
technical/911report/chapter-13.4.txt:1869:                of mass destruction that the al Qaeda network might acquire or make.
technical/911report/chapter-13.4.txt:2008:                were pursuing another al Qaeda mission on the West Coast, while certainly
technical/911report/chapter-13.4.txt:2015:                late 1999 or early 2000 KSM sent an al Qaeda operative named Issa al Britani to
technical/911report/chapter-13.4.txt:2056:                al Qaeda member whose role in the 9/11 plot and the Cole attack we discussed in
technical/911report/chapter-13.4.txt:2175:                that intelligence investigators associate with possible adherence to al Qaeda. It is
technical/911report/chapter-13.4.txt:2362:                recovered during searches at an al Qaeda site in Pakistan in May 2002. The document
technical/911report/chapter-13.4.txt:2579:                Muhammad Bayazid, an al Qaeda arms procurer and trainer; Wadi al Hage, an operative
technical/911report/chapter-13.4.txt:2581:                ties to al Qaeda. CIA and FBI joint analytic report, "Arizona: Long Term Nexus for
technical/911report/chapter-13.4.txt:2593:            60. For al Qaeda activity in Arizona, see Ken Williams interview (Jan. 7, 2004). On
technical/911report/chapter-13.4.txt:2594:                al Qaeda directing individuals in the Phoenix area to enroll in flight training
technical/911report/chapter-13.4.txt:2778:            75. The apartment was already occupied by two other individuals. The al Qaeda
technical/911report/chapter-13.5.txt:31:            6. Zuhair al Thubaiti: He has reportedly admitted membership in al Qaeda, stating
technical/911report/chapter-13.5.txt:34:                because the al Qaeda leadership considered him too high-strung and lacking the
technical/911report/chapter-13.5.txt:53:                Afghanistan but denies hearing of al Qaeda before returning from Afghanistan or
technical/911report/chapter-13.5.txt:70:                obtained Pakistani visas in Sharjah, UAE, and traveled to Islamabad, where al Qaeda
technical/911report/chapter-13.5.txt:86:                religion." The al Qaeda leader accepted both applicants. In October 2000, Abu Basir
technical/911report/chapter-13.5.txt:121:                Binalshibh. While both Binalshibh and Khallad confirm Jdey's status as an al Qaeda
technical/911report/chapter-13.5.txt:354:                Spanish al Qaeda cell were involved in the July meeting and were connected to the
technical/911report/chapter-13.5.txt:359:                Center. The Spanish indictment alleges that an al Qaeda courier was in Ghalyoun's
technical/911report/chapter-13.5.txt:361:                tape to al Qaeda leaders in Afghanistan. Second, the Spanish government contends
technical/911report/chapter-13.5.txt:426:                addition to Moussaoui, the two al Qaeda operatives identified by KSM as candidates
technical/911report/chapter-13.5.txt:532:                had cemented its alliance with al Qaeda and Zawahiri had become Bin Ladin's deputy.
technical/911report/chapter-13.5.txt:592:                to Bin Ladin, al Qaeda, the Taliban, and key countries such as Afghanistan,
technical/911report/chapter-13.5.txt:606:            3. The CIA produced to the Commission all SEIB articles relating to al Qaeda, Bin
technical/911report/chapter-13.5.txt:664:            16. See NSC email, Clarke to Rice and Hadley, Possibility of an al Qaeda Attack, June
technical/911report/chapter-13.5.txt:669:            17. See NSC email, Clarke to Rice and Hadley, Possibility of an al Qaeda Attack, June
technical/911report/chapter-13.5.txt:678:                intelligence services to detain specific al Qaeda members and to generally harass al
technical/911report/chapter-13.5.txt:714:            34. CIA cable, "Threat of Impending al Qaeda Attack to Continue Indefinitely,"Aug. 3,
technical/911report/chapter-13.5.txt:777:            44. NSC memo, Clarke to Rice, al Qaeda review, Jan. 25, 2001 (attaching NSC memo,
technical/911report/chapter-13.5.txt:945:                Freeh, FISA surveillance of a suspected al Qaeda operative, Dec. 24, 1999; NSA
technical/911report/chapter-13.5.txt:2255:                don't believe anybody said this is likely al Qaeda. I don't think so." White House
technical/911report/chapter-13.5.txt:2536:                the paper that went beyond al Qaeda, see NSC memo, Deputies Draft Paper (attached to
technical/911report/chapter-13.5.txt:2608:                Press, 2004), p. 32. According to Clarke, he responded that "al Qaeda did this."
technical/911report/chapter-13.5.txt:2612:                for linkages between al Qaeda and Iraq and never found any real linkages. Ibid.
technical/911report/chapter-13.5.txt:2628:                Front Office because it did not find a tie between Iraq and al Qaeda; Rice and
technical/911report/chapter-13.5.txt:2655:                review contacts between Iraq and al Qaeda in chapter 2. We have found no credible
technical/911report/chapter-13.5.txt:2665:                initial offensive, perhaps deliberately selecting a non-al Qaeda target like Iraq.
technical/911report/chapter-13.5.txt:2681:                declaration that al Qaeda had been behind the October 2000 attack. Clarke said he
technical/911report/chapter-13.5.txt:2700:                of proposed follow-on strikes on al Qaeda targets in Afghanistan.
technical/911report/chapter-13.5.txt:2706:                (nearly two-thirds of the known leaders of al Qaeda had been killed or captured).
technical/911report/chapter-13.5.txt:2795:            29. For President Bush's statement of al Qaeda's responsibility for the Cole attack,
technical/911report/chapter-13.5.txt:2964:                manner that has subsequently been associated with al Qaeda. Based on our review of
technical/911report/chapter-13.5.txt:3133:                would offer an integrated depiction of groups like al Qaeda or Hezbollah worldwide,

```
In this case I used the term "al Qaeda" to search through chapter 13 of the 911report to find every line in which al Qaeda is brought up, and since I looked up with the *, it provided some of the line as well in it's results. 

```
grep -n "Bush" technical/911report/*.txt
technical/911report/chapter-1.txt:6:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
technical/911report/chapter-1.txt:564:    In Sarasota, Florida, the presidential motorcade was arriving at the Emma E. Booker Elementary School, where President Bush was to read to a class and talk about education. White House Chief of Staff Andrew Card told us he was standing with the President outside the classroom when Senior Advisor to the President Karl Rove first informed them that a small, twin-engine plane had crashed into the World Trade Center. The President's reaction was that the incident must have been caused by pilot error.
technical/911report/chapter-10.txt:14:                Bush reluctantly acceded to this advice and, at about 10:10, Air Force One changed
technical/911report/chapter-10.txt:36:            Air Force One arrived at Offutt at 2:50 P.M. At about 3:15, President Bush met with
technical/911report/chapter-10.txt:39:            Rice said President Bush began the meeting with the words, "We're at war," and that Director of Central Intelligence George Tenet said
technical/911report/chapter-10.txt:56:                still-smoldering Pentagon. At 8:30 that evening, President Bush addressed the nation
technical/911report/chapter-10.txt:63:            Following his speech, President Bush met again with his National Security Council
technical/911report/chapter-10.txt:84:                Determining federal assistance. On September 13, President Bush promised to
technical/911report/chapter-10.txt:110:                Council system. Vice President Cheney reviewed the proposal with President Bush and
technical/911report/chapter-10.txt:111:                other advisers. President Bush announced the new post and its first occupant-
technical/911report/chapter-10.txt:217:                domestic department heads broke up, President Bush chaired a smaller meeting of top
technical/911report/chapter-10.txt:237:            President Bush chaired two more meetings of the NSC on September 12. In the first
technical/911report/chapter-10.txt:286:                President Bush led a discussion of an appropriate ultimatum to the Taliban. He also
technical/911report/chapter-10.txt:292:            President Bush also tasked the State Department, which on the following day delivered
technical/911report/chapter-10.txt:314:            President Bush recalled that he quickly realized that the administration would have
technical/911report/chapter-10.txt:325:                15-16, as President Bush convened his war council at Camp David.
technical/911report/chapter-10.txt:333:                military's Special Operations units. President Bush later praised this proposal,
technical/911report/chapter-10.txt:340:                possible significant use of ground forces- and that is where President Bush
technical/911report/chapter-10.txt:343:            After hearing from his senior advisers, President Bush discussed with Rice the
technical/911report/chapter-10.txt:345:                prepared a paper that President Bush then considered with principals on Monday
technical/911report/chapter-10.txt:350:                President Bush charged Ashcroft, Mueller, and Tenet to develop a plan for homeland
technical/911report/chapter-10.txt:351:                defense. President Bush directed Secretary of State Powell to deliver an ultimatum
technical/911report/chapter-10.txt:357:            In addition, Bush and his advisers discussed new legal authorities for covert action
technical/911report/chapter-10.txt:359:                Bin Ladin. Shortly thereafter, President Bush authorized broad new authorities for
technical/911report/chapter-10.txt:362:            President Bush instructed Rumsfeld and Shelton to develop further the Camp David
technical/911report/chapter-10.txt:398:            President Bush had wondered immediately after the attack whether Saddam Hussein's
technical/911report/chapter-10.txt:407:            Clarke has written that on the evening of September 12, President Bush told him and
technical/911report/chapter-10.txt:410:                incorrect, President Bush acknowledged that he might well have spoken to Clarke at
technical/911report/chapter-10.txt:457:                deal with the Iraq problem." Powell said that President Bush did not give
technical/911report/chapter-10.txt:459:                worry about Iraq in the following week, Powell said, President Bush saw Afghanistan
technical/911report/chapter-10.txt:462:            President Bush told Bob Woodward that the decision not to invade Iraq was made at the
technical/911report/chapter-10.txt:466:            Rice said that when President Bush called her on Sunday, September 16, he said the
technical/911report/chapter-10.txt:474:            President Bush ordered the Defense Department to be ready to deal with Iraq if
technical/911report/chapter-10.txt:508:            On September 20, President Bush met with British Prime Minister Tony Blair, and the
technical/911report/chapter-10.txt:515:                military responses in Iraq during the summer before 9/11-a request President Bush
technical/911report/chapter-10.txt:523:                enforce Iraqi no-fly zones. Franks said that President Bush again turned down the
technical/911report/chapter-10.txt:527:                Thursday, September 20, President Bush addressed the nation before a joint session
technical/911report/chapter-10.txt:540:            President Bush argued that the new war went beyond Bin Ladin." Our war on terror
technical/911report/chapter-10.txt:548:            President Bush approved military plans to attack Afghanistan in meetings with Central
technical/911report/chapter-11.txt:44:                President George H.W. Bush dealt with the first of these in 1990 and 1991 when he
technical/911report/chapter-11.txt:154:                George Bush and their top advisers told us they got the picture-they understood Bin
technical/911report/chapter-11.txt:381:                for Operations James Pavitt gave an intelligence briefing to President-elect Bush,
technical/911report/chapter-11.txt:386:            Bush asked whether killing Bin Ladin would end the problem. Pavitt said he and the
technical/911report/chapter-11.txt:427:            Officials in both the Clinton and Bush administrations regarded a full U.S. invasion
technical/911report/chapter-11.txt:443:                already discussed. Since we believe that both President Clinton and President Bush
technical/911report/chapter-11.txt:466:            After 9/11, President Bush announced that al Qaeda was responsible for the attack on
technical/911report/chapter-11.txt:472:            Earlier chapters describe in detail the actions decided on by the Clinton and Bush
technical/911report/chapter-11.txt:479:                debate on counterterrorism in the Bush administration before 9/11 had to do with
technical/911report/chapter-11.txt:483:                for action offered to both President Clinton and President Bush.
technical/911report/chapter-11.txt:527:                sanctuary. The Bush administration adopted this approach, although its emerging new
technical/911report/chapter-11.txt:553:            Other agencies deferred to the FBI. In the August 6 PDB reporting to President Bush
technical/911report/chapter-12.txt:817:            In May 2003, the Bush administration announced the Proliferation Security Initiative
technical/911report/chapter-13.2.txt:969:                White House transcript, President Bush interview with Bob Schieffer of CBS News,
technical/911report/chapter-13.2.txt:1038:                President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.2.txt:1040:                President Bush at Emma E. Booker Elementary School," Sept. 11, 2001 (remaining in
technical/911report/chapter-13.2.txt:1044:                Bush and Vice President Cheney meeting (Apr. 29, 2004) (call to Pataki); White House
technical/911report/chapter-13.2.txt:1052:                speech, see President Bush and Vice President Cheney meeting (Apr. 29, 2004); Ari
technical/911report/chapter-13.2.txt:1064:                the Vice President's recollection, see President Bush and Vice President Cheney
technical/911report/chapter-13.2.txt:1088:                2001, p. 4; President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.2.txt:1102:            212. On communications problems, see, e.g., President Bush and Vice President Cheney
technical/911report/chapter-13.2.txt:1105:            213. On the Vice President's call, see President Bush and Vice President Cheney
technical/911report/chapter-13.2.txt:1117:                Bush and Vice President Cheney meeting, Apr. 29, 2004 (Vice President viewed
technical/911report/chapter-13.2.txt:1121:                combat air patrol, see President Bush and Vice President Cheney meeting (Apr. 29,
technical/911report/chapter-13.2.txt:1122:                2004); White House transcript, President Bush interview with Bob Woodward and Dan
technical/911report/chapter-13.2.txt:1124:            214. President Bush and Vice President Cheney meeting (Apr. 29, 2004); see also White
technical/911report/chapter-13.2.txt:1149:                President Bush and Vice President Cheney meeting (Apr. 29, 2004). For the second
technical/911report/chapter-13.2.txt:1208:            237. President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.3.txt:48:            17. President Bush, remarks at roundtable with Arab- and Muslim-American leaders,
technical/911report/chapter-13.4.txt:1563:                such briefing item we can find summarized the evidence for the new Bush
technical/911report/chapter-13.4.txt:1622:            158. President Bush and Vice President Cheney meeting (Apr. 29, 2004); Condoleezza
technical/911report/chapter-13.4.txt:1628:                to kill Bin Ladin. Tenet told us he recalled the meeting with Bush but not what he
technical/911report/chapter-13.4.txt:1631:                come back to either President Clinton or PresNOTES TO CHAPTER 6 509 ident Bush and
technical/911report/chapter-13.4.txt:1633:                Blair House CIA briefing is recounted in some detail in Bob Woodward, Bush at War
technical/911report/chapter-13.4.txt:1636:            160. President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.4.txt:1637:            161. NSC briefing materials, "CT Briefing for Bush-Cheney Transition Team,
technical/911report/chapter-13.4.txt:1646:            164. Public references by candidate and then President Bush about terrorism before
technical/911report/chapter-13.4.txt:1648:                WMD as a reason to mount a missile defense. See, e.g., President Bush remarks,
technical/911report/chapter-13.4.txt:1650:            165. Rice and Zelikow had been colleagues on the NSC staff during the first Bush
technical/911report/chapter-13.4.txt:1654:                Commission, Zelikow has recused himself from our work on the Clinton-Bush transition
technical/911report/chapter-13.4.txt:1665:            170. President Bush and Vice President Cheney meeting (Apr. 29, 2004); GeorgeTenet
technical/911report/chapter-13.4.txt:1667:            171. President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.4.txt:1679:            174. The Bush administration held 32 Principals Committee meetings on subjects other
technical/911report/chapter-13.4.txt:1714:            181. President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.4.txt:1723:            185. Condoleezza Rice meeting (Feb. 7, 2004). Rice remembered President Bush using
technical/911report/chapter-13.4.txt:1728:                Bush to have given that direction in May, and Clarke said:"No, it was March." Fox
technical/911report/chapter-13.4.txt:1729:                News transcript,"Clarke Praises Bush Team in '02,"Mar. 24, 2004 (online at
technical/911report/chapter-13.4.txt:1731:            186. Barton Gellman, "A Strategy's Cautious Evolution: Before Sept. 11, the Bush
technical/911report/chapter-13.4.txt:1733:            187. President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.4.txt:1766:                materials, TNT to Rice, counterterrorism briefing for Bush/Cheney transition team,
technical/911report/chapter-13.4.txt:1849:            218. See White House letter, President Bush to Musharraf, Aug. 4, 2001. For Rocca's
technical/911report/chapter-13.4.txt:1872:            227. President Bush and Vice President Cheney meeting (Apr. 29, 2004).
technical/911report/chapter-13.5.txt:589:                Clinton administration, up to 25 people received the PDB. In the Bush
technical/911report/chapter-13.5.txt:632:                Response Activities," undated, pp. 1-2 (provided to the Commission by President Bush
technical/911report/chapter-13.5.txt:682:            21. For the Cheney call see President Bush and Vice President Cheney meeting (Apr.
technical/911report/chapter-13.5.txt:684:                Alert, July 2, 2001. For the G-8 summit see Associated Press Online, "Bush Faced
technical/911report/chapter-13.5.txt:718:            36. President Bush and Vice President Cheney meeting (Apr. 29, 2004). For Rice's
technical/911report/chapter-13.5.txt:2217:                that Vice President Cheney informed President Bush in a phone conversation shortly
technical/911report/chapter-13.5.txt:2242:                Marinzel, Oct. 3, 2001; President Bush and Vice President Cheney meeting (Apr. 29,
technical/911report/chapter-13.5.txt:2351:                President Bush named Vice President Cheney to head a task force on problems of
technical/911report/chapter-13.5.txt:2447:            27. Andrew Card meeting (Mar. 31, 2004); President Bush and Vice President Cheney
technical/911report/chapter-13.5.txt:2528:                council." White House transcript, President Bush interview with Bob Woodward and Dan
technical/911report/chapter-13.5.txt:2530:            34. On Secretary Rumsfeld's remarks, see White House transcript, President Bush
technical/911report/chapter-13.5.txt:2542:                September 13, 2001. In addition to the usual members of President Bush's war
technical/911report/chapter-13.5.txt:2557:                Afghanistan," Sept. 14, 2001 (tasked by President Bush). The paper was sent to the
technical/911report/chapter-13.5.txt:2567:                transcript, President Bush interview with Bob Woodward and Dan Balz, Dec. 20, 2001.
technical/911report/chapter-13.5.txt:2570:            42. White House transcript, President Bush interview with Bob Woodward and Dan Balz,
technical/911report/chapter-13.5.txt:2580:            47. White House transcript, President Bush interview with Bob Woodward and Dan Balz,
technical/911report/chapter-13.5.txt:2589:                White House transcript, President Bush interview with Bob Woodward and Dan Balz,
technical/911report/chapter-13.5.txt:2605:            59. President Bush and Vice President Cheney meeting (Apr. 29, 2004). On Iran, see
technical/911report/chapter-13.5.txt:2613:            61. President Bush told us that Clarke had mischaracterized this exchange. On the
technical/911report/chapter-13.5.txt:2620:                /2004/03/19/60minutes/printable607356.shtml), President Bush doubted that anyone
technical/911report/chapter-13.5.txt:2621:                would have found his manner intimidating. President Bush and Vice President Cheney
technical/911report/chapter-13.5.txt:2634:                Wolfowitz's position on Iraq, see Bob Woodward, Bush at War (Simon &
technical/911report/chapter-13.5.txt:2635:                Schuster, 2002), pp. 83-84. Rice told us that the Bush at War account of the Camp
technical/911report/chapter-13.5.txt:2648:            69. White House transcript, President Bush interview with Bob Woodward and Dan Balz,
technical/911report/chapter-13.5.txt:2673:            78. NSC memo, memorandum of conversation from meeting of President Bush with Prime
technical/911report/chapter-13.5.txt:2676:            80. White House transcript, President Bush's Address to a Joint Session of Congress
technical/911report/chapter-13.5.txt:2684:            82. White House transcript, President Bush's Address to a Joint Session of Congress
technical/911report/chapter-13.5.txt:2685:                and the American People, Sept. 20, 2001. President Bush told the Washington Post
technical/911report/chapter-13.5.txt:2688:                transcript, President Bush interview with Bob Woodward and Dan Balz, Dec. 20, 2001.
technical/911report/chapter-13.5.txt:2689:            83. White House transcript, President Bush's Address to a Joint Session of Congress
technical/911report/chapter-13.5.txt:2795:            29. For President Bush's statement of al Qaeda's responsibility for the Cole attack,
technical/911report/chapter-13.5.txt:2892:            14. Some have criticized the Bush administration for neglecting Afghanistan because
technical/911report/chapter-13.5.txt:3078:            1. The Bush administration clarified the respective missions of the different
technical/911report/chapter-2.txt:278:                President Bush observed." Islam is a faith that brings comfort to a billion people
technical/911report/chapter-3.txt:191:                Meanwhile, a task force headed by Vice President George H.W. Bush had endorsed a
technical/911report/chapter-3.txt:931:                George Bush and after terrorist attacks at airports in Rome and Athens, the DCI
technical/911report/chapter-3.txt:1117:                Desert One and the withdrawal from Beirut. The first President Bush had authorized
technical/911report/chapter-3.txt:1166:                administration. George H.W. Bush was scheduled to visit Kuwait to be honored for his
technical/911report/chapter-3.txt:1169:                President Clinton not only ordered precautions to protect Bush but asked about
technical/911report/chapter-3.txt:1239:                to be Presidential Decision Directives; for President George W. Bush, National
technical/911report/chapter-3.txt:1250:                bombing and, a few weeks after that, the Iraqi plot against former President Bush.
technical/911report/chapter-3.txt:1252:                the Bush administration the staffer who dealt with crime, narcotics, and terrorism
technical/911report/chapter-3.txt:1259:                the plot to kill President Bush, President Clinton stated:"From the first days of
technical/911report/chapter-3.txt:1354:                Bush chose not to seek a declaration of war on Bin Ladin after he had declared and
technical/911report/chapter-6.txt:1081:                Nor was the memo discussed during the transition with incoming top Bush
technical/911report/chapter-6.txt:1109:                Gore or his Republican opponent, Texas Governor George W. Bush, would become
technical/911report/chapter-6.txt:1117:            The principal figures on Bush's White House staff would be National Security Advisor
technical/911report/chapter-6.txt:1119:                George H.W. Bush; Rice's deputy, Stephen Hadley, who had been an assistant secretary
technical/911report/chapter-6.txt:1120:                of defense under the first Bush; and Chief of Staff Andrew Card, who had served that
technical/911report/chapter-6.txt:1122:                secretary of state, Bush chose General Colin Powell, who had been national security
technical/911report/chapter-6.txt:1126:                of defense. Bush decided fairly soon to keep Tenet as Director of Central
technical/911report/chapter-6.txt:1128:                of the FBI until his voluntary retirement in the summer of 2001. Bush and his
technical/911report/chapter-6.txt:1131:                led a team to Bush's ranch in Crawford, Texas, and gave him a wide-ranging,
technical/911report/chapter-6.txt:1137:                1995. Bonk told Bush that Americans would die from terrorism during the next four
technical/911report/chapter-6.txt:1141:                pass intelligence to Bush and some of his key advisers.
technical/911report/chapter-6.txt:1144:                President-elect Bush at Blair House during the transition. President Bush told us he
technical/911report/chapter-6.txt:1146:                Ladin would have an effect but would not end the threat. President Bush told us
technical/911report/chapter-6.txt:1149:            In December, Bush met with Clinton for a two-hour, one-on-one discussion of national
technical/911report/chapter-6.txt:1150:                security and foreign policy challenges. Clinton recalled saying to Bush, "I think
technical/911report/chapter-6.txt:1155:            Bush told the Commission that he felt sure President Clinton had mentioned terrorism,
technical/911report/chapter-6.txt:1156:                but did not remember much being said about al Qaeda. Bush recalled that Clinton had
technical/911report/chapter-6.txt:1169:                says that he told her the Bush administration would spend more time on terrorism in
technical/911report/chapter-6.txt:1185:            Generally aware that terrorism had changed since the first Bush administration, they
technical/911report/chapter-6.txt:1194:            In the NSC during the first Bush administration, many tough issues were addressed at
technical/911report/chapter-6.txt:1229:            The procedures of the Bush administration were to be at once more formal and less
technical/911report/chapter-6.txt:1233:                the practice of face-to-face briefings from the DCI. President Bush and Tenet met in
technical/911report/chapter-6.txt:1246:            Within the first few days after Bush's inauguration, Clarke approached Rice in an
technical/911report/chapter-6.txt:1272:                the election, candidate Bush had said to CNN, "I hope that we can gather enough
technical/911report/chapter-6.txt:1275:                not responded militarily, what was the Bush administration to do?
technical/911report/chapter-6.txt:1328:                defense. I want to play offense. I want to take the fight to the terrorists." President Bush explained to us that he had become
technical/911report/chapter-6.txt:1338:                missions-went before the group that, in the Bush NSC, would do most of the policy
technical/911report/chapter-6.txt:1377:            The Bush administration in its first months faced many problems other than terrorism.
technical/911report/chapter-6.txt:1395:            In May, President Bush announced that Vice President Cheney would himself lead an
technical/911report/chapter-6.txt:1527:            The Bush administration immediately encountered the dilemmas that arose from the
technical/911report/chapter-6.txt:1529:                with Pakistan. In February 2001, President Bush wrote General Musharraf on a number
technical/911report/chapter-6.txt:1554:            On August 4, President Bush wrote President Musharraf to request his support in
technical/911report/chapter-6.txt:1567:            The Bush administration did not develop new diplomatic initiatives on al Qaeda with
technical/911report/chapter-6.txt:1617:            With this directive still awaiting President Bush's signature, Secretary Rumsfeld did
technical/911report/chapter-6.txt:1620:            President Bush told us that before 9/11, he had not seen good options for special
technical/911report/chapter-6.txt:1625:            President Bush told us that before 9/11 there was an appetite in the government for
technical/911report/chapter-6.txt:1633:            During the transition, Bush had chosen John Ashcroft, a former senator from Missouri,
technical/911report/chapter-6.txt:1812:                would insist its other priorities were more important. Invoking President Bush's own
technical/911report/chapter-6.txt:1838:            Rice told us that she had, at some point, told President Bush that she and his other
technical/911report/chapter-8.txt:24:            He in turn met daily with President Bush, who was briefed by the CIA through what is
technical/911report/chapter-8.txt:96:            Reports similar to many of these were made available to President Bush in morning
technical/911report/chapter-8.txt:194:                airport during the G-8 summit, which President Bush attended.
technical/911report/chapter-8.txt:280:            During the spring and summer of 2001, President Bush had on several occasions asked
technical/911report/chapter-8.txt:292:                historical in nature. President Bush said the article told him that al Qaeda was
technical/911report/chapter-8.txt:309:                President George W. Bush on August 6, 2001.37 Redacted material is indicated by
technical/911report/chapter-8.txt:361:                in the United States. DCI Tenet visited President Bush in Crawford, Texas, on August
technical/911report/chapter-8.txt:377:                the summer. In addition to his daily meetings with President Bush, and weekly

```
Similarly to the last example, in this one I look up the term Bush but in all of the 911 reports, to find each line where the term Bush shows up. This is helps with finding topics and can make finding for citations easy as well. 



## -l

The -l (l as in Lazer) option makes the output only print out the file name once when the instance is found regardless of amount found in that file. 
```
	grep -l "illegal" technical/government/*/*.txt
technical/government/About_LSC/commission_report.txt
technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
technical/government/Gen_Account_Office/May1998_ai98068.txt
technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
technical/government/Gen_Account_Office/Testimony_cg00010t.txt
technical/government/Gen_Account_Office/ai9868.txt
technical/government/Gen_Account_Office/d01121g.txt
technical/government/Gen_Account_Office/d03232sp.txt
technical/government/Media/Bridging_legal_aid_gap.txt
technical/government/Media/Butler_Co_attorneys.txt
technical/government/Media/Entities_Merge.txt
technical/government/Media/FY_04_Budget_Outlook.txt
technical/government/Media/Few_who_need.txt
technical/government/Media/Terrorist_Attack.txt
technical/government/Media/The_Columbian.txt
technical/government/Media/Too_Crucial_to_Take_Cut.txt
technical/government/Media/less_legal_aid.txt
```
This example of -l shows which  files in the entire government folder contains the words illegal. This option can work really well in combination with another command or even command option to search for files without producing large amounts of output like a regular grep might. 

```
grep -l "the" technical/911report/*.txt
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt

```
This example helps show how -l can help reduce how much output there can be from a general term. The term "the" is extremely common, but with -l we can reduce every found instance to just one file print. 

```
❯ grep -l "illegal" technical/government/Media/less_legal_aid.txt
technical/government/Media/less_legal_aid.txt
```
I was also curious about what would happen if I used -l on a file and this was the results. It provides just the path, which could help if you are trying to go from relative to absolute, but seeing that there are other commands for that it doesn't seem to have much use. 