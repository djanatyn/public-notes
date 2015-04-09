= generating ssh keys

ssh keys are composed of two parts: a public key, and a private key. other people use your public key to encrypt things they want to send to you, and you use your private key to decrypt them. this shared secret system works well, and provides more security than a stored password.

zubkoland.org provides ssh access to new accounts using ssh keys. this means you'll need to generate a key of your own to log in!

== from linux
the easiest way to do this is from a linux box you already have access to, using the ssh-keygen command. it's included in the openssh package and is easy to invoke:

----
$ ssh-keygen -t rsa
----

when you run the above line, you'll be prompted for a few values in an interactive script. most of these values you can leave as the default, but a few are worth noting. in particular, the script will prompt you for a passphrase. if you choose to enter a value at that point, you'll need to enter it every time you connect - it's quite normal to leave the passphrase blank.

once you've finished creating your key, submit your *public* key (by default, it should be in ~/.ssh/id_rsa.pub) to whoever is helping you with an account.

== from windows
on windows, you'll most likely be logging in with http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html[PuTTY], which includes it's own keygen utility. instructions for how to use it are available http://www.rackspace.com/knowledge_center/article/generating-rsa-keys-with-ssh-puttygen[here].

i recommend generating an SSH-2 RSA key with no passphrase (you can ignore the warning) and 2048-bit encryption. give the person helping you set up your account your *public* key when you're finished generating it.

after they're done with the configuration, you should be able to log in free of problems! if you experience trouble, make sure you're using the identity you provided to connect to zubkoland.org, and never be afraid to ask for help!
