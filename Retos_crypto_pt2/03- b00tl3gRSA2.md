# Descripcion
In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 18243`.

# Pistas
What is e generally?

# Solucion
```
                                                                                                                                                   
┌──(kali㉿kali)-[~/picoctf/crypto/b00tl3grsa2]
└─$ nc jupiter.challenges.picoctf.org 18243.
c: 34752883854221303547930058314576840122946811539913235959379382488858703350430092929841451930916339617825109601357884751807263997469784082752539832184386533998668457417390989692527964713857854982689251585882551382514332754244441864808222141046922962474131805650441264544756493959942579284976867147719572299314
n: 92066684824399543662688824507017494772422342184229918889224469950506798161889050615638902241650487448644582873794980350998750599932913954859708429136486208152674085833418626716512963709030280173452849547852137405095021981437350959902542470462049298395589023762107766649892420480167679460935442790179283157657
e: 15905198675280400893372642493071884215227516642657600159662472325245860640384940279083016481986768068321009007081599211651553386521208657657836318944768552511651247820093002793065250689014237507801319347723002923216042850065202416102696370215756846049537334893744212734780310713610792871781770547349448219849

──(kali㉿kali)-[~]
└─$ python3 
Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c=34752883854221303547930058314576840122946811539913235959379382488858703350430092929841451930916339617825109601357884751807263997469784082752539832184386533998668457417390989692527964713857854982689251585882551382514332754244441864808222141046922962474131805650441264544756493959942579284976867147719572299314
>>> n=92066684824399543662688824507017494772422342184229918889224469950506798161889050615638902241650487448644582873794980350998750599932913954859708429136486208152674085833418626716512963709030280173452849547852137405095021981437350959902542470462049298395589023762107766649892420480167679460935442790179283157657
>>> 
>>> d=15905198675280400893372642493071884215227516642657600159662472325245860640384940279083016481986768068321009007081599211651553386521208657657836318944768552511651247820093002793065250689014237507801319347723002923216042850065202416102696370215756846049537334893744212734780310713610792871781770547349448219849
>>> e=65537
>>> m=pow(c,d,n)
>>> m
9515972242026648009633184069801661224833089111488890911558763228186483510287788609594085049587469005385186178970318443733515699590947468453922413513671363386114067809533938394727707300516941806750604440919752362426051297779734812692325237334518264622451740702702229400878866335169348818272172966293675166585
>>> from Crypto.Util.number import long_to_bytes
>>> long_to_bytes(m)
b'\r\x8d\x1b\x11\x9d\xfd\xa2\xfc\x1dF\xd5\\\xbd\xc3\xec\x82\xf62\xdc\x92\xa1\x93\xe4\x92Htl\xb6\xb7\x9a^\xff\x05\xb1\x10\xbf\xe8\xf9|\xe8\x18\x08\x84\x08\x8f\xb4\xf6$\x8f_\x831\xcc\xd1w\xcd\x99zl|\x03\xa6I>\x8d\xb9S\x98\xd9\x83L\xee\xb8z\xd2\xdd\xd0\x02\x8aT\xc3/c\x80\x0e\x13!\xeb\x97h\x84G4\xb5I\x17(\xd4x\xba\x9e\xf4\xdai\xeahUY\xec\x10\xf1\xd2>\xc8\xdcW_\x17\x06kn\x9e\xce\x8av\x1f\xcby'
>>> m=pow(c,e,n)
>>> m
180638594769037903267909311328535969949661653466129492033745533
>>> long_to_bytes(m)
b'picoCTF{bad_1d3a5_4783252}'
```

# Bandera
picoCTF{bad_1d3a5_4783252}

# Notas adicionales


# Referencias
https://www.youtube.com/watch?v=fEOYiZ-cpBc&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=42