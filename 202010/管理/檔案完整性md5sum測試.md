# md5sum
```
https://en.wikipedia.org/wiki/Md5sum
https://zh.wikipedia.org/wiki/Md5sum

md5sum是一種電腦程式，用於計算與校驗RFC 1321所描述的128位元MD5雜湊值，
此處MD5雜湊值（或校驗和）作一個檔案的數字指紋使用。

md5sum is a computer program that calculates and verifies 128-bit MD5 hashes, as described in RFC 1321. 
The MD5 hash functions as a compact digital fingerprint of a file.

As with all such hashing algorithms, there is theoretically an unlimited number of files that will have any given MD5 hash. 
However, it is very unlikely that any two non-identical files in the real world will have the same MD5 hash, 
unless they have been specifically created to have the same hash.[2]

The underlying MD5 algorithm is no longer deemed secure. 
Thus, while md5sum is well-suited for identifying known files in situations that are not security related, 
it should not be relied on if there is a chance that files have been purposefully and maliciously tampered. 
In the latter case, the use of a newer hashing tool such as sha256sum is recommended.

md5sum is used to verify the integrity of files, as virtually any change to a file will cause its MD5 hash to change. 
Most commonly, md5sum is used to verify that a file has not changed as a result of a faulty file transfer, 
a disk error or non-malicious meddling. 
The md5sum program is included in most Unix-like operating systems or compatibility layers such as Cygwin.

The original C code was written by Ulrich Drepper and extracted from a 2001 release of glibc
```

```
有關md5sum的敘述下列何者為是?
(A)128位元MD5雜湊值
(B)
(C)
(D)
```
#
```
md5sum --help
Usage: md5sum [OPTION]... [FILE]...
Print or check MD5 (128-bit) checksums.

With no FILE, or when FILE is -, read standard input.

  -b, --binary         read in binary mode
  -c, --check          read MD5 sums from the FILEs and check them
      --tag            create a BSD-style checksum
  -t, --text           read in text mode (default)
  -z, --zero           end each output line with NUL, not newline,
                       and disable file name escaping

The following five options are useful only when verifying checksums:
      --ignore-missing  don't fail or report status for missing files
      --quiet          don't print OK for each successfully verified file
      --status         don't output anything, status code shows success
      --strict         exit non-zero for improperly formatted checksum lines
  -w, --warn           warn about improperly formatted checksum lines

      --help     display this help and exit
      --version  output version information and exit

The sums are computed as described in RFC 1321.  When checking, the input
should be a former output of this program.  The default mode is to print a
line with checksum, a space, a character indicating input mode ('*' for binary,
' ' for text or where binary is insignificant), and name for each FILE.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation at: <https://www.gnu.org/software/coreutils/md5sum>
or available locally via: info '(coreutils) md5sum invocation'

```
```
md5sum --version
md5sum (GNU coreutils) 8.30
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by Ulrich Drepper, Scott Miller, and David Madore.


KALI linux 2019 20201022
```

# md5sum簡單測試
```
gedit test.txt

cat test.txt


md5sum test.txt 
f0270e9935270e2d5a04ce5abd64d3bf  test.txt

把小寫改大寫後


md5sum test.txt 
bc9c40435f30f46cace989bdef107e4c  test.txt
```
