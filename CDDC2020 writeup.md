# CDDC 2020

CTF Hosted by dsta.gov.sg/CDDC

## Overview

```
Challenge	                              	    Warp Gate       Flag
[Misc-1] Welcome to CDDC 2020                 WARP GATE 5     CDDC20{g1mM3_M0aRRr_pOiN75}
[Misc-2] ARGH                                 WARP GATE 5     CDDC20{c0mManD_l1n3_ArguM3n75sSs}
[Misc-3] Add to Your Reading List             WARP GATE 5     CDDC20{KNOW_UR_RIGHTS}
[OSINT-1] Better Alternative Than TV          WARP GATE 5     CDDC20{S+@rt_O$!nT}
[OSINT-2] Fun with File Extensions            WARP GATE 5     CDDC20{EVIL_CORP_CH@RT}
[OSINT-3] Transparency is the Best Policy     WARP GATE 5     CDDC20{CERT_TR4SP4RENCY}
[RE (Windows)-1] Decompile Me                 WARP GATE 5     CDDC20{NiCe-2-MeeT-py2exe~:D}
[RE (Windows)-2] Dissect Me                   WARP GATE 5     CDDC20{UR-di$$ector}
[RE (Windows)-3] Cheat Me                     WARP GATE 5     CDDC20{T1ck-T0ck_T1ck-T0ck}
[Pwn (Linux)-1] nc                            WARP GATE 5     CDDC20{NiceToMeetYou@PwnWorld}
[Pwn (Linux)-2] (2^31)-1                      WARP GATE 5     CDDC20{oO0OoO0o0OoO0Oo}
[Pwn (Linux)-3] Find Singapore Bug            WARP GATE 5     CDDC20{AAAABBBB-Oh~YouLeakedIt-CCCCDDDD}
[Forensics-1] Can't See A Thing               WARP GATE 5     CDDC20{pho70gr4phy_i5_aw3sOmE}
[Forensics-2] Shell History                   WARP GATE 5     CDDC20{Sh4LL_we_Sh3LL?}
[Forensics-3] Top Secret                      WARP GATE 5     CDDC20{Lorem-Ipsum-Foo-Bar}
[Web-1] No Time                               WARP GATE 5     CDDC20{N0_71m3_nO_tiMe_oMG}
[Web-2] VulnLogin                             WARP GATE 5     CDDC20{administrator_password12345678}
[Web-3] Keep Me Posted                        WARP GATE 5     CDDC20{YEs5SS_1_4m_aUTh0r1z3DDdD}
[Crypto-1] My Best Friend, Julius!            WARP GATE 5     
[Crypto-2] Cryptic Message                    WARP GATE 5     
[Crypto-3] Iffy Glyphs                        WARP GATE 5     
[Network-1] Baby Shark                        WARP GATE 5     
[Network-2] Mama Shark                        WARP GATE 5     
Very Serious Challenge!                       WARP GATE 5     

[OSINT-1] Funky Transfer Pact                 WARP GATE 4     
[OSINT-2] Follow the Breadcrumbs              WARP GATE 4     
Visual Noise                                  WARP GATE 4     
ilovedes                                      WARP GATE 4     
Recycling Bin                                 WARP GATE 4     
Something's Going On                          WARP GATE 4     
What Time Is It? [1]                          WARP GATE 4     
Ma GIFs                                       WARP GATE 4     
Great Sphinx of Unduplicitous Corp            WARP GATE 4     
Greater Sphinx of Unduplicitous Corp          WARP GATE 4     
Between 0&1                                   WARP GATE 4     
How QueeR...                                  WARP GATE 4     
Suspicious Service                            WARP GATE 4     
Secret Code                                   WARP GATE 4     

[OSINT-1] There's A T In Every Flag           WARP GATE 3     
[OSINT-2] Travel Ban                          WARP GATE 3     
[OSINT-3] Who Needs A Password Manager        WARP GATE 3     
My Favourite Music                            WARP GATE 3     
Clickity Clack                                WARP GATE 3     
```


## [Misc-1] Welcome to CDDC 2020

**Challenge**
Free points for all! See you on Slack! ;)

**Solution**
As mentioned in the challenge description, ‘see you on slack’ when we navigated about the slack channel, we found the flag under the ‘details’ section.

**Flag**

```
CDDC20{g1mM3_M0aRRr_pOiN75}
```

## [Misc-2] ARGH

**Challenge**
I found a binary, together with this long string that looks like some password. I wonder what is it for...

Key: GZ2gXZ3bD2qqNyNxXb5LJ8HfHQtTL5VHA

Attached Files: myprog

**Solution**
The file header is first checked, of which we quickly find out that it is an .ELF (Linux executable). The program is initially run to see that there were insufficient arguments. Since there is a key, we pass in the key together with the program and we get the flag for the challenge!

**Flag**

```
CDDC20{c0mManD_l1n3_ArguM3n75sSs}
```

## [Misc-3] Add to Your Reading List

**Challenge**
As part of our resistance fighters' training program, we need to arm ourselves with academic knowledge. By the graces of my kind senior, he passed me some recommended reading materials.

One pdf seems to be annotated, while the other isn't. I wonder what is the difference between the two.. Can you spot it?

Attached Files: Reading_Material.zip

**Solution**
We used the tool: https://www.diffchecker.com/diff and uploaded both PDFs in the online tool.

The flag can be eyeballed from the differences spotted in the pdf.

**Flag**

```
CDDC20{KNOW_UR_RIGHTS}
```

## [OSINT-1] Better Alternative Than TV

**Challenge**
Looks like we found a clue to the mastermind behind the brainwashing liquid.

The company's name is UnduplicitousCorp, sounds kinda fishy. Let's conduct some basic reconnaisance and see if there's any videos about the company on social media.

**Solution**
Simplest OSINT challenge that gave us the flag right away when we searched for the company name. Youtube also was relevant to TV, which gave us the confirmation that we had the correct flag.

**Flag**

```
CDDC20{S+@rt_O$!nT}
```

## [OSINT-2] Fun with File Extensions

**Challenge**
Now that we have their company website, it will be helpful for us to know how the company layout is like.

Note: This challenge does not require brute-forcing. There is no need to do so.

**Solution**
Opening up the pdf, we see this chart. Just by eyeballing it, we knew that the flag was beneath the chart in the middle. However, at the bottom right of the document, there was an interesting message:
‘I wonder how to get an editable version of this’

Initially, since this seemed like a powerpoint document, we changed it to .pptx and opened it with microsoft powerpoint, but we could not drag out the individual elements. So we decided to use microsoft word to edit it.

The pdf file was converted to word document with an online tool before shifting the elements around a bit, which uncovered the flag.

**Flag**

```
CDDC20{EVIL_CORP_CH@RT}
```

## [OSINT-3] Transparency is the Best Policy

**Challenge**
The website looks state-of-the-art. As expected of a evil mega conglomerate.

Okay, they're using HTTPS certificate, very secure. Is there any way we can discover what other domains they are hosting?

Note: This challenge does not require brute-forcing. There is no need to do so.

**Solution**
We got stuck here for a very long time and apparently did not know we were supposed to look up for all subdomains for this challenge. I personally went to look at all the site certificates but nothing. That was when we went to slack to look for hints, and realised it was literally related to transparency.

https://transparencyreport.google.com/https/certificates?hl=en&cert_search_auth=&cert_search_cert=&cert_search=include_subdomains:true;domain:unduplicitouscorp.tech&lu=cert_search


**Flag**

```
CDDC20{CERT_TR4SP4RENCY}
```

## [RE (Windows)-1] Decompile Me

**Challenge**
Hello py2exe, nice to meet you!

Attached Files: DecompileMe.zip

**Solution**
Reading up on python decompilation, I stumbled upon this really useful article which included the tool link as below: https://blog.f-secure.com/how-to-decompile-any-python-binary/
Tool: https://github.com/countercept/python-exe-unpacker

**Flag**

```
CDDC20{NiCe-2-MeeT-py2exe~:D}
```

## [RE (Windows)-2] Dissect Me

**Challenge**
LET THE GAMES BEGIN!

Attached Files: DissectMe.exe

**Solution**
Extract files with 7zip and look under BITMAP. The flag is in FLAG.bmp

**Flag**

```
CDDC20{UR-di$$ector}
```

## [RE (Windows)-3] Cheat Me

**Challenge**
Be patient :) Then you can get what you want.

Attached Files: CheatMe.exe

**Solution**
Cheat Engine. Select the running Cheatme.exe program and change scan type to “Exact value” and value to “All” since we do not know the data type. Enter the number in the minutes place. First scan is then performed. When the minute value changes, key in the 2nd number which is 54 then click “Next scan”. A single address should appear. Change the value to “0” and repeat for the hours. When time is up, viola! Flag appears.

**Flag**

```
CDDC20{T1ck-T0ck_T1ck-T0ck}
```

## [Pwn (Linux)-1] nc

**Challenge**
Hello PwnWorld!

nc.chall.cddc20.nshc.sg 10000

**Solution**
The challenge name gave away that this was a netcat challenge. So we just interacted with the given IP and port and voila!

**Flag**

```
CDDC20{NiceToMeetYou@PwnWorld}
```

## [Pwn (Linux)-2] (2^31)-1

**Challenge**
I like zer0.

zer0.chall.cddc20.nshc.sg 20002

**Solution**
We know max is: (2^32)-1 = 4294967296 - 1
Using netcat and putting the maximum limit, we get the flag!

**Flag**

```
CDDC20{oO0OoO0o0OoO0Oo}
```

## [Pwn (Linux)-3] Find Singapore Bug

**Challenge**
Let's FSB!

fsb.chall.cddc2020.nshc.sg 30303

**Solution**
Format String Bug. We had to leak the stack from the program. After getting the dump, we changed the hex to ascii, changed the endianness and got the flag!

**Flag**

```
CDDC20{AAAABBBB-Oh~YouLeakedIt-CCCCDDDD}
```

## [Forensics-1] Can't See A Thing

**Challenge**
What kind of lousy photographer takes terrible pictures like these?

Attached Files: img.jpg

**Solution**
exif tool

**Flag**

```
CDDC20{pho70gr4phy_i5_aw3sOmE}
```

## [Forensics-2] Shell History

**Challenge**
What happened to my server? Please help me to investigate.

Username: root / Password: toor

Attached Files: Shell History.ova

**Solution**
We decided to list the files with ls, but nothing. So we decided to use (ls -al) to list all files and found out that there was a directory called  .ash_history. That seemed like it, so we cat the entire bash history out and we can find that the flag is under the echo command.

**Flag**

```
CDDC20{Sh4LL_we_Sh3LL?}
```

## [Forensics-3] Top Secret

**Challenge**
Where is the secret?

Attached Files: TopSecret

**Solution**
Reference writeup: https://poqw.tistory.com/14
FTK imager was used. Convert the file to .AD1 extension before adding logical evidence drive and extracting the files.

**Flag**

```
CDDC20{Lorem-Ipsum-Foo-Bar}
```

## [Web-1] No Time

**Challenge**
Our project manager couldn't handle the stress from the upcoming deadlines and resigned hastily. Sigh. Now that we are taking over his projects, I wonder if he has left any instructions for us...

http://notime.chall.cddc20.nshc.sg:1337/

**Solution**
Inspect element

**Flag**

```
CDDC20{N0_71m3_nO_tiMe_oMG}
```

## [Web-2] VulnLogin

**Challenge**
This is not how you log someone in!

http://vulnlogin.chall.cddc2020.nshc.sg:8090/

Note: Flag format is CDDC20{username_password}

**Solution**
Inspect element gave us the MD5 hashes of the login credentials, which we used Crackstation to crack the hashes.

**Flag**

```
CDDC20{administrator_password12345678}
```

## [Web-3] Keep Me Posted

**Challenge**
Some weird page. Looks fishy. Please help.

**Solution**
Burp Suite + POST Request in Base64 encoding of 'Yes'. The flag was immediately returned.

**Flag**

```
CDDC20{YEs5SS_1_4m_aUTh0r1z3DDdD}
```

## [Crypto-1] My Best Friend, Julius!

**Challenge**


**Solution**


**Flag**

```

```

## [Crypto-2] Cryptic Message

**Challenge**


**Solution**


**Flag**

```

```

## [Crypto-3] Iffy Glyphs

**Challenge**


**Solution**


**Flag**

```

```

## [Network-1] Baby Shark

**Challenge**


**Solution**


**Flag**

```

```

## [Network-2] Mama Shark

**Challenge**


**Solution**


**Flag**

```

```

## Very Serious Challenge!

**Challenge**


**Solution**


**Flag**

```

```

## WARP GATE 4

## [OSINT-1] Funky Transfer Pact

**Challenge**


**Solution**


**Flag**

```

```
