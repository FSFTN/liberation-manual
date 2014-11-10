# Physical Security

Physical security is a no-brainer. Make sure your equipment is not lost or stolen by using locks and vaults and being careful and alert. Make sure your equipment isn't damaged or destroyed by handling it with care. In any case, to protect against the loss of data, intentional or accidental, make regular backups. This simply cannot be stressed enough. _BACKUP YOUR FUCKING DATA_. I recommend several layers of backup like copies of data on (encrypted if data is sensitive) thumb drives in
different places. Beware of kensington style cable locks for laptops, because it's not too difficult to open them using pen-caps and toilet paper roll. I had my laptop stuck to a window because I forgot the password to the combination lock. I managed to break it open in 20seconds flat. I was quite suprised. It could have been substandard, but even for good quality locks, instructions are all over youtube on how to open them. Go figure!

# Encryption (In-Situ)

Encrypting data on disk is quite straight forward if you use a Linux distro or any of the BSD ones. Use a disk encryption software like eCryptfs or dm-crypt. You probably shoudln't trust Trucrypt because the code hasn't been audited well and the anonymous developers of the project decided to shut the project down in rather mysterious and slightly creepy ways. 

## Using eCryptfs to encrypt a directory

    $ mkdir testdir
    # mount -t ecryptfs testdir testdir
    Passphrase: correcthorsebatterystaple
    Cipher: aes
    Key byte: 32
    Plaintext passtrough: no
    Filename encryption: yes

This will encrypt and mount the directory testdir over itself with the passphrase correcthorsebatterystaple (not a really secure passphrase,btw). The encryption algorithm chosen heer is AES with at 32byte key. You can also choose whether or not to encrypt the filenames also. Once this is done, you can continue putting files in the directory. When you are done, simply unmount the 


## Using crytsetup to encrypt a flash drive

    # cryptsetup luksFormat /dev/sdx
    # cryptsetup luksOpen /dev/sdb1 crypto
    # mkfs.ext4 /dev/mapper/crypto 
    # mount -t ext4 /dev/mapper/crypto /mnt
    $ yadayada
    # umount /mnt
    # cryptsetup luksClose crypto

- dm-crypt (cryptsetup)
- GPG PGP encryption

# Encryption (in transit)

- LibOTR (Pidgin, etc.) on your system
- LibOTR (Cryptocat, etc.) on your browser
- LibOTR (Chatsecure, TextSecure.) on your phone
- SILC
- GPG encryption for email

# Encryption in the browser

- HTTPS (Use HTTPS everywhere)
- Do not allow arbitrary scripts to run (NoScript)
- Don't get caught in the bubble (Scroogle, ixquick, startpage)
- Use a Secure browser (Firefox, Chromium, etc.)
- Go incognito (unreliable)
- Use TOR 
- Use Tails

# Securing services

- Use OTP for as many services as you can (Google authenticator)
- Use PAM on Linux (OTR, pamusb, etc.)
- Use secure passwords
- Use a password manager and generator (apg)

# Securing servers 

- Use HSTS
- Use good passwords
- Use PFS 
- Use LDAP like / Kerberos
- Use SSH Keys (Disable passwords)
- Role based access control / privilege management
- Use DKIM / SPF for email verifications

# Securing devices 

- Flash them with open firmware
- DD-WRT, etc. 
- Beware of Set-Top-Boxes they send detailed logs
- Encrypt usb flash drives with cryptsetup
- Hide your laptop camera with a tape

# Securing phones

- Use encryption
- Use notecipher
- Use chatsecure, textsecure
- Use Redphone for voice calls
- Use surespot for text
- Avoid snakeoil like Telegram
- Use Orbot for TOR network connectivity
- Use Obscuracam (be responsible)
