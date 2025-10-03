# Killing misbehaving processes
In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write your flag. You need to kill this process.**flag**:pwn.college{MlRS5A1MOEOT0_bkNBWhXv2hsZ4.0FNzMDOxwCOzAzNzEzW}




```bash
hacker@processes~killing-misbehaving-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.0   1056   640 ?        Ss   13:13   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/do
root           7  0.1  0.0 231708  2560 ?        S    13:13   0:00 /run/dojo/bin/sleep 6h
root         137  0.0  0.0   4132  1280 ?        S    13:13   0:00 /bin/bash /challenge/.init
root         138  0.0  0.0   4132  1280 ?        S    13:13   0:00 /bin/bash /challenge/.init
root         139  0.0  0.0   5204  3520 ?        S    13:13   0:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140  0.0  0.0   2744  1600 ?        S    13:13   0:00 sleep 6h
root         141  0.0  0.0   2744  1280 ?        S    13:13   0:00 sleep 6h
hacker       142  0.2  0.0  13516  9280 ?        Ss   13:13   0:00 /usr/bin/python /challenge/decoy
hacker       153  0.1  0.0  36972 21760 ?        Sl   13:13   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --i
hacker       157  0.0  0.0 231972  4160 pts/0    Ss   13:13   0:00 /run/dojo/bin/bash --login
hacker       167  0.0  0.0 233600  3840 pts/0    R+   13:13   0:00 ps aux
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ kill 139
bash: kill: (139) - No such process
hacker@processes~killing-misbehaving-processes:~$ kill 139
bash: kill: (139) - No such process
hacker@processes~killing-misbehaving-processes:~$ /challenge/run | cat /tmp/flag_fifo
pwn.college{ZExHaycnNR0m7WyFeAl3BKcRSYxQdmBD0Bh2gbG.tNS6sHg}
pwn.college{.qyAORMabASvCNra1gpod98y8dNsTAvXzzRhzZnW3wWpneA}
pwn.college{A6U8lne-UAU2JfYw71zx4APO1NroKw9TF7Is9gYpHT2h-MC}
pwn.college{w3RKq8CYd5zahPOEmrFJvJFjNe7bBHTdfxo8BSmFbPqFdKZ}
pwn.college{CLBlByoe.9FSCzCKGL7vV6ryPGFuIK8iTi9c8z8K754wqou}
pwn.college{YrEvGAckJv4QgDfWRTLVM5MxDZY0MwqIegy0ulR97WpRcB3}
pwn.college{fOICLwOPmm85ImR.gEKou3pKEY6d.TDmxdcKIcU3GOr1YtD}
pwn.college{G3mPJRSPkK1sMIfqUTQak5RoSh.PI3yXu0Y0bRJf4YxV.Ln}
pwn.college{j7iLnolWjM1bD9TvJOjCMr0m4HWDYs9Bz72u62mKhVK.aNv}
pwn.college{KiEFHPttmJwQD5GlHaLHue0Y1JEztiv9Z0DS9wF..NB.KnW}
pwn.college{ZHrWHIj1QOhPBORUuarphIJPKC5bx3LgKXkKmQedrBYCitF}
pwn.college{Lb.7RfrPyDP4CGBfya-eRttooUXZS.1asFBaRXN06IflB3N}
pwn.college{x1A6B9c5r32qNq65Tdq7uk3r8p.ww1i4YdhPFBDX9YBMeQE}
pwn.college{XUY07y4jQEQ3LhenruPHxwure45MbSkhLoVObqvgtf8wT9J}
pwn.college{0qHYzcGjQGJpSdpP7EuXgT2PJQo-aChMNgsyT9sTH5jxyHS}
pwn.college{x52opubkY0XWra29IToz72d1WVuWTJMF2w4--1dbo8poXSJ}
pwn.college{OHHKCXwT.R6aVYetEw1PgKie5dJgtwBdqTg7VsV5ofxauhv}
pwn.college{FyG5RMCJxeliUz8NqULwh9EHGPGv1.xZjBtfJThxyzv4uDL}
pwn.college{kjvYOKYENWfl8b9TLCyzHUvyB38wjYO9drEJ09x3NkZOn1a}
pwn.college{PNv4aKWDbCJ2NWZRhzarFjHE15lRxK5GMUZ-CT6OKdjOAQG}
pwn.college{Qi2oHrt1W6qCK5BgPqGOI-7WOswQOTyxLZCn.FpD.7HA9lv}
pwn.college{JjKuGcVQcO2Zf1gzEPA4ywKDRBm6ze4reD.tDLgH9FWAXzX}
pwn.college{auBt-Ls2GR3zeAi54wdY1TzQxUmBAhPsXhBVIH4SqeoGjsr}
pwn.college{m7RLIxyymo0UGimAOmXYvgpm45NTyFlWGf2lly6fTMhPYiR}
pwn.college{cUbw1Pf14b2kQNsSutF7647R467Ay6tRVTSOcaxpMMnhkQm}
pwn.college{H.3EZMhi2W7rBdMkE4HefDzKAIkE4KAskaIYJnc.9-zGVKB}
pwn.college{l84BzwDR.WUZzt-IjfdH8A3IjjXFLGfSEAbQJKvjQlaR55o}
pwn.college{1fu2rje0HNs6v1HkKuoZIwYdH3ezp7NZtOhlf6qlbTipwO6}
pwn.college{JJElzxgAtD.S5vINwRB36zFbL1KC7g35ozukzjtekpSdTdI}
pwn.college{Drde46wl7E2UCsvkgyDXdzefgtajHuqITCmQRMR0evqeyD0}
pwn.college{nSPmR0dsmaxQeGLeBMmGZw0pKTbhbHYLwyYM0QBPMWzPDrl}
pwn.college{ePeVu2sNDFMONx-jtN7uiRBbk4bjEXxB06SfhXyrvIvKwOx}
pwn.college{7qk4BXewtVr2hS0iBYF4xNlr1COnl2SVg.gVu4Q0vUnnjPH}
pwn.college{4PdJbLhnYuz3oHLAOLk2uF4xtK.4iWTT0Tm3mTonfviepLC}
pwn.college{rH.PaaSbPHMWPduZQPvlSvTkIg4bMLQulrOHuL2N2Z6n2oN}
pwn.college{CTi8lkNgh33oeHzQHI6kJwuSr5P9rhAAF9GzhQK0otIuZVs}
pwn.college{7KyhCiJCiwKo5bDcvfZRV67jLJojoa.ythGn9mr89uD.zXZ}
pwn.college{Ozg47jCYS0l6HsFL2hyTy7goSrLU9xsFAr-25ye84c-voD1}
pwn.college{aPo6tuBC55ZZ3eF-z5Y7pjvkUCAP9i3eo1i-C.JUGIENcY8}
pwn.college{b9BxzFe2VwRfPWXpCnP9AZfSgU0v7SpWEJ4c5b0W1ghJ72q}
pwn.college{5jcvpPwApHR2us-YWacca24oSA7UBV5QFzPFqymrwQyYnYW}
pwn.college{atP.jj.azWaraXSTl7r3QbX0b5nC1dqr.Ym2-LUFJvK8aIF}
pwn.college{afXKDk-eGdZ-g8g5skRd43p8PXkPA-U0G3QV-F.951vVSbA}
pwn.college{PnB0xZtUECdfP.9GESsglTwJsqKX8HxmEk23.V2Izfkn6dQ}
pwn.college{WrsVt0oTKsCFbWlQMx9FrIIW6geDdZn92mdL-k7nX19syzV}
pwn.college{ntXK0Nk1D-27.F.HRytzyoG7LDn.xx-aXAXfR7cpBC9NACf}
pwn.college{teTvH3IokW29VlUotZZgftZf9OpfFj1kq-QJ637nMblqJtM}
pwn.college{4p-l6yds9ZvXuvZAspDH8ejvjbNqS3WlvPG54Qd0bCVQAEa}
pwn.college{JGKuhAbj68wOH8qnZldhMMQfdovG8Qh0l5GCL-RKCbBpYVf}
pwn.college{mscpQMqU9v9fQNlT55u6uGpD5d4b8QAiVue6TeqimehJRfA}
pwn.college{PS6oQTS.d-uyLy3mJygrk66de4cuvUBd6HUKZGdLaTLVbHX}
pwn.college{zsnl3acpNsioQ.Qqrgz8-vHYN8Y3bAbMZMkBKKR3rp8zD2h}
pwn.college{pp1z647FF-UnAhLyMh0KCCqO17Z-5ROnyK3NdoHBdleOumw}
pwn.college{oLewVMYFmcnoQCQl1SD0bWL.VdE3hkaHXikJyJ08P2bP49b}
pwn.college{MVuu6xjZHdiI5X5XbB7uFG8dssW2xnn1ZghGoUgSJZzlqMh}
pwn.college{AopUii-RwhXqA59f47I8Qb2F1rSnFnCZtMmDWIyU2H1lvHS}
pwn.college{QeRiBZv-dFxVU.cHNGKOgZG8U4HP0-GSyU3OGF1UdJtuxLz}
pwn.college{o9sk4ZyHH5ajJbBEGQbkzuwgC7wM1xLslBEt5txMasHS2WL}
pwn.college{oOZxMZtEsMkNWSsMW1jLGrcwfg2n6yjFV3xAx94yePDXBqM}
pwn.college{Q6.e5.ih8iagx4iXpsWX3lL21qPaqAGOnax8UOCQgua7yGa}
pwn.college{8Fgi1K6WvOX3ALf4AV..6NKGbY-9PWBjnlqGNJKsh23Tr0l}
pwn.college{-WXyfa4W1fNBdYKRWu-wKRy-YaLh47umPH6Dj4Bvak1MEI9}
pwn.college{T0.zi54rXqkqwEgj0yqCt284biwcvti7Jz6bkESdPJBn6cp}
pwn.college{Z1MnbNesVd3kvCOBLx-IEPpd4SMlyfmbjqAmhl8T5H6UTnb}
pwn.college{8q1jca6TlkWyLXtbiVJnKF0izT-YdRJCHNA.KcqklbF9vwJ}
pwn.college{kmRwOQHpLHUyUSEdKKvNbaZoU7hp0guEaPDzILAxEPfRsbF}
pwn.college{a.cqjI70GXuDcak19G1Isx7bD02avRye40Ws8WZJh1P9.l8}
pwn.college{BGlpA.1bOWo9psOR3etkKvRv2xVWpHknPac2WlIctMSTZWn}
pwn.college{PC1U2LXTg5LAcztaxPhfDHB8MX153lVd8KDIPqh-CmE32k3}
pwn.college{-ihxbUpP-JXjZY.fMd5pwzhpqapCEwdGHH6lVMCsM3ZlOX9}
pwn.college{QEXnrBOPqmKohwYyJDfnZPwjBMLnj1.8tgBHVfbpWb0PKIw}
pwn.college{K4NCRZjk6qGeNRjH6tTI7GXrffU8hMJtxISYkMlXKvP05SI}
pwn.college{0NHChlAZ6rJNOvgCChvng3oufSHG1U9LTDxSFUCi9Uqi8b4}
pwn.college{BsGDTtFnJapIW12sYfXp2FlaJwjngaliAHxtBCvrT1JM6w-}
pwn.college{lKofy..pH44ls-50mXTVkOpye3RPNs7ZohOQQ-09HFklMlh}
pwn.college{vq6bSnS9mTJ.1nabkU4EBmiw07hfjnBY6wTSL7WRpmg82P7}
pwn.college{ECHBKdH--iYmFyO8FdcErwL3lKIU65Aq7F.C7NOt17SYnIl}
pwn.college{BWT.lNv57dWIGXxojnBz8NhRAM5iSV1Kmki-UiOPPsyXAqA}
pwn.college{B7DikxGr64xz070g-foq9r9GDl0heylFfARFm7xyxsw04aL}
pwn.college{kGARGTV7qYr6mGimRCuAbfMu0Wf2A5sQVIoBaYSDx4CceRz}
pwn.college{YNRtnP9MjINsNXA8gLEiG3110UF1fRsZQW2sGXugF447.rp}
pwn.college{mH6UgPGlSGBpUCnRWc1YKRn3kdZ5tUJvQRrDl-bRTgXplDE}
pwn.college{J1nzEFYOiUiwzC8O9nukBYTbSDuA0EC6xXhpS5BcTHn5Ie1}
pwn.college{OtzY42jfJzK9f.CFYCLIQhtVX-0wcTAr8bs0pZACuXCZbV6}
pwn.college{VNxab6j3FGpsktOaQ0SOTzTc8ZiurFaW63rmlUmpv1.4rax}
pwn.college{Til37dikamQEEw9IVJZQvgqauSe54qPmIUa-DeUNZ6w-i4j}
pwn.college{gQKmqu8Hfcv7AF.oisPkMbXFkpXykvzZpirsNVd05T.-LgH}
pwn.college{YS7UlgowvNU7P2oKlSl8pLNgEqSZBGmRSDBG6eVA8NfslN4}
pwn.college{YoueLnQIY3sklpXbGIlcuNenEHffSfi.IvDsYj4F2HvliQS}
pwn.college{UMei8uS2oHEw3DkJSenpqgaHwotBqym2nlQ0q1xtfCkgXBL}
pwn.college{BRJsPwYuPk2cZQNUABVF4Sis0l39jeezH8751h4zIuX8NhY}
pwn.college{7Ps3qudAxAovXPbeT0OjCTU13.0aYMJBW0zCM2Upa7C7ylx}
pwn.college{uoMOHA.vxg1naa-X3Cj7qSLHzcibmu9YQQudYjT9DpE8sBx}
pwn.college{Z6fadOLWFOXw2Niy3y6C.M5-9LOjO-soolWMcirE525yayT}
pwn.college{HJELPtDmIL1h9zCBExMlfSp6NkdFHPxmbRvtjUYRosM8fC7}
pwn.college{jpM95kK9Q3PAQ7E65q7a4jsMJeYHURRFhUJn9z-A8RVBsnN}
pwn.college{yRIeINY-gj4F1T1lCglyaBZFva54gDnGy7y9ubtfuac-KDP}
pwn.college{7Ud95dy15CqT5n4vieCNPMNSgVfTRK9aRHKRozRL0Qa4SDs}
pwn.college{qa1Xe8b3eAQqNYlcDTM3NQSr8G1oj2gliozPE9bNylFJx2y}
pwn.college{wkAbnCr3XTT1lewtVdl-z8Ogj-Zz.56vp7X0ElSq06OD.b2}
pwn.college{LXwMWZpaxVgI75JZSUCeWPO2heBmHx8NoaAJt.WbpKRdjwR}
pwn.college{72xamOrlty7yttW3kgoZYP8Dv8W2QHiTBOtjm06oABwirkx}
pwn.college{RwlBow-r3rPdUKj-XTWz3C0Tr-m46jufrAo2k2gJS6rxV-b}
pwn.college{-6v41DgxRh9haXYYFGqPuX6HskRYnQPuK7qjB8iuPpka9YR}
pwn.college{BVCqSHDHHjPdFzjxkLiu39daFMVcv6MQMdVktiGMTHUbHSf}
pwn.college{DRiuwyxZBYf11OgB1E-VIMgTLDk-6nK2wSau0NwJi-pyZ6T}
pwn.college{jIxwbIBaQ0jgdO-BPhWnYe1DmW3V6jvQbpPSdd7lhCKw4tY}
pwn.college{E2R-UhFAME4L2zTzWirAtBXzvp6aiqtvCvtWrzyoL8bsBWa}
pwn.college{NQhYCcuClzFe3ugFgZhCHJNFT1k486FjjK2o4pKWlpIHAp9}
pwn.college{8NHWSeE-PqL4SZXBOkkrvu6XEoUzqbT7eH8EbPQCifkubq2}
pwn.college{.ydHrA2iD1UpShmDjDTXbSdoz1GNALTsdykFabtmw.p5JJG}
pwn.college{879gOAvp5QaR8.tgK5CwbehpjHSEIk35lwMLXU.xqJ7APEb}
pwn.college{3aSpl9.cY1UGiyWTiukprVMcAkBhh3iltYcRrPpth5MZipw}
pwn.college{O8DjIQhiF-YvQVFq-qcl.YbVpiMnZ6TWSvg2LqgcLWo.U8k}
pwn.college{tBBmEy3ISYbS5OAz2RvsvIRGAq5yidbdblDqwPDW5q5Cwoh}
pwn.college{o-eQG2dE8W06PQFp6NpfBSAaAsv7xzxazBs5R-DuJAC0oEG}
pwn.college{xhXU-N6FIL5U1kSZWFGnT23mlqiBx2auINeDIW7bW3p0Od3}
pwn.college{yoeiYFTKx51M28TgxmTsjDwXm6dX6bR4zeIBL4prLgKY2CK}
pwn.college{ZgmbJNPpkDeV8lKnqTCEcJpATqSmU95RGN8RAxZ.t7yL7Pa}
pwn.college{6wQQfhr2If3gPp6Oyd4vsc0SGQb3Whr2qDJzSutj-zpQt8G}
pwn.college{2uI.VFsZSWiieQWUfUetsTNFFIRug5MD2v8SIsXPqgWrHFq}
pwn.college{7wlaQ2bJg8UZY4Y4YJoFbygwLexgld1He1sFNrH9-NbFkf8}
pwn.college{gRbzCrHDE4h6n3KYsS4ik7iXa1MXNUPy9C9BCQGMX84tG16}
pwn.college{TXk7prVzwZb4kCqLM5pnHOqQRCBb8aLplTJjp7KEqHrf5dW}
pwn.college{p.ELdjYjD7fJQ4uTLVeekCYpkBU1uB2bfAXwXAMgVCQV2JF}
pwn.college{3gDbVHliQfBr7sjJEJxFzZ4D5-zmfOD.umK2tk705oAXOVL}
pwn.college{qR-5jjg7f3l5bpbRuYX7ZZsd3ImnxRMg4xdH90P51CNDazK}
pwn.college{ReIRF1rhyDJY1sIz7HAaNcAxz3QZ8Ip8u3UONfp2.WSy1Y5}
pwn.college{AdJDoJcFgVl4z5yTBJtB47WdV.W7mfXedCeRF-0URjxEnsH}
pwn.college{K1B-gkauRZib.wDF20snvJlF0l7XDz.bW8YGdMEwxXXqNmI}
pwn.college{Skn.tWcVNZgCSzx.p2h7sKIMg8v.F-1iU8G83s5UpgEbSy1}
pwn.college{HWju2ihLV-dUUTN7yaV6.qLBEVCNknJfrRUO-ZWABzdeEiG}
pwn.college{kco-SAhA688..88AMQwfsAoWlyEV6CHWok.qZRNgDh7tyKJ}
pwn.college{3WGv2APROi-WV1jaMk2-FQ8Q63C3kM1v5Sig5gIjdudgt5X}
pwn.college{MlRS5A1MOEOT0_bkNBWhXv2hsZ4.0FNzMDOxwCOzAzNzEzW}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{MlRS5A1MOEOT0_bkNBWhXv2hsZ4.0FNzMDOxwCOzAzNzEzW}
^C
hacker@processes~killing-misbehaving-processes:~$ 

```
i had a little trouble where i thought the process got stuck but it didnt so its fine
## What I learned
killing misbehaving processes
A few decoy flags show up due to FIFO buffer but at the end we get reqd flag

## References 
.