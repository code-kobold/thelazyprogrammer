The Lazy Programmer
===================

## SSH

**Determine your SSH fingerprint**:

    $ ssh-add -l
    4096 SHA256:0123456789abcdefg0123456789abcdef0123456789 ron@example.com (RSA)
    
    $ ssh-add -l -E md5
    4096 MD5:a0:a1:a2:a3:a4:a5:a6:a7:a8:a9:aa:ab:ac:ad:ae:af ron@example.com (RSA)
